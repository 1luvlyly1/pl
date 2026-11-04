---
id: SEG-DNL
used_by: [Propagation, Product-Impact, Inside-out Monitor]
steps: [2, 3, 4]
depends_on: [core/01_risk_codes.md, core/03_linkage_graph.md]
load_when: Sự kiện chạm DN lớn, ngành, thương mại quốc tế, BĐS, trái phiếu, hoặc lan qua L03, L04, L05, L08
version: v3.0
updated: 2026-11-02
---

# Phân khúc: Doanh nghiệp lớn (CIB)

> Gồm doanh nghiệp lớn và định chế tài chính. Mã phân khúc trong dòng nhãn và mã sản phẩm vẫn dùng `CIB`.

> Cấu trúc: (a) Chân dung → (b) Động lực rủi ro → (c) Bảng độ nhạy sản phẩm → (d) Tín hiệu sớm nội bộ → (e) Lan ra phân khúc khác → (f) Danh mục sản phẩm & URL nguồn


## (a) Chân dung
- DN quy mô lớn, tập đoàn, FDI, định chế tài chính.
- Dư nợ tập trung lớn; dùng sản phẩm phức tạp (tài trợ thương mại, FX, phái sinh, trái phiếu); là **anchor** trong chuỗi cung ứng và là **CĐT BĐS / tổ chức phát hành trái phiếu** (cạnh `L04`, `L05`).

## (b) Động lực rủi ro chính
1. **Ngành** (BĐS, thép, dệt may, gỗ, thủy sản, hàng không, ô tô, tiêu dùng nhanh…)
2. **Thương mại quốc tế** – thuế quan, trừng phạt, đứt gãy vận tải (cạnh `L08`)
3. **Tỷ giá & lãi suất** – nợ ngoại tệ, vị thế phái sinh
4. **Pháp lý doanh nghiệp & lãnh đạo** – thanh tra, khởi tố, tranh chấp
5. **Thị trường vốn** – đáo hạn trái phiếu, khả năng huy động mới
6. **Rủi ro tập trung theo nhóm khách hàng liên quan**
7. **ESG** – quy định phát thải, CBAM, tín dụng xanh

## (c) Bảng độ nhạy sản phẩm CIB
**Quản trị hàng ngày**
| Mã | Sản phẩm | Rủi ro chính | Nhạy với sự kiện | Chiều tác động khi sự kiện xấu |
|---|---|---|---|---|
| `CIB-PKG-01` | BusinessOne Connect / Plus / Premium | `BR` | **P3:** hoạt động DN giảm | **P3:** hạ gói |
| `CIB-DIG-01` | Techcombank Business; F@st EBank (đang chuyển đổi sang Techcombank Business); Chữ ký số | `OR` `FR` | **P1:** sự cố, giai đoạn chuyển đổi nền tảng, chiếm đoạt chữ ký số | **P1:** gián đoạn thanh toán quy mô lớn; chuyển tiền trái phép (`X03` `X04`) |
| `CIB-ACC-01` | Tài khoản thanh toán | `LQ` `CO` | **P1:** tin đồn ngân hàng; BEC<br>**P2:** dòng tiền giảm, AML | **P1:** số dư lớn rút đột ngột (`NH-LQ-01`)<br>**P2:** số dư giảm, giao dịch cần rà soát |
| `CIB-ACC-02` | Tài khoản vốn | `CO` `MR` | **P2:** quy định FDI, ngoại hối<br>**P3 (+):** FDI tăng, dịch chuyển chuỗi cung ứng | **P2:** dòng vốn dừng<br>**(+):** dòng vốn mới (`O6`) |
| `CIB-ACC-03` | Tài khoản giữ hộ thương mại | `RP` `CO` | **P2:** tranh chấp M&A, mua bán | **P2:** tranh chấp giải ngân giữ hộ |
| `CIB-ACC-04` | Tài khoản giữ hộ bất động sản | `RP` `CO` `CR` | **P1:** dự án dừng, chủ đầu tư vỡ nợ<br>**P2:** pháp lý dự án, tiến độ (cạnh `L04`) | **P1:** phong tỏa, tranh chấp với người mua nhà<br>**P2:** chậm giải ngân |
| `CIB-PAY-01` | Thanh toán hàng hóa dịch vụ trong nước | `FR` `OR` | **P1:** BEC, sự cố | **P1:** chuyển nhầm/lừa đảo, thanh toán chậm (`X04`) |
| `CIB-PAY-02` | Chuyển tiền đi nước ngoài | `CO` `MR` | **P1:** trừng phạt<br>**P2:** AML, tỷ giá | **P1:** giao dịch bị giữ, rà soát (`NH-CO-01`)<br>**P2:** chi phí tăng |
| `CIB-PAY-03` | Nộp ngân sách nhà nước | `CO` | **P2:** thuế, hải quan | **P2:** nộp chậm = dấu hiệu thiếu tiền (`S10`) |
| `CIB-PAY-04` | Thẻ dành cho DN | `CR` `FR` | **P1:** gian lận thẻ<br>**P2:** dòng tiền DN giảm | **P1:** giao dịch trái phép<br>**P2:** dư nợ thẻ chậm trả |
| `CIB-PAY-05` | Thanh toán hóa đơn | `OR` | **P2:** sản lượng giảm do mất đơn, thuế quan | **P2:** hóa đơn điện/cảng giảm = sản xuất/xuất khẩu giảm (`S10`) |
| `CIB-PAY-06` | Thanh toán lương | `BR` | **P1:** cắt giảm nhân sự, đóng nhà máy<br>**P2:** mất đơn hàng, thuế quan<br>**P3 (+):** mở nhà máy mới | **P1:** cắt giảm nhân sự lan tới hàng nghìn KHCN (cạnh `L02`, `S01`)<br>**P2:** quỹ lương giảm<br>**(+):** tài khoản lương mới (`O2`) |
| `CIB-COL-01` | Thu hộ: TK định danh, POS, QR, Payment Gateway, tiền mặt tại quầy, tại địa điểm KH, qua quầy đối tác | `OR` `FR` `BR` | **P1:** sự cố cổng thanh toán<br>**P2:** doanh thu bán lẻ giảm | **P1:** gián đoạn thu hộ<br>**P2:** thu hộ giảm = doanh thu DN giảm |
| `CIB-LIQ-01` | Báo cáo tổng hợp dòng tiền | – | Công cụ quan sát | Nguồn tín hiệu sớm |
| `CIB-DEP-01` | CCTG Bảo Lộc; Tiền gửi xanh | `LQ` `MR` | **P1:** tin đồn ngân hàng<br>**P2:** lãi suất, nhu cầu vốn, đáo hạn trái phiếu của DN | **P1:** rút tiền gửi lớn ảnh hưởng thanh khoản ngân hàng (`NH-LQ-01`)<br>**P2:** tất toán sớm |

**Vay**
| Mã | Sản phẩm | Rủi ro chính | Nhạy với sự kiện | Chiều tác động khi sự kiện xấu |
|---|---|---|---|---|
| `CIB-LN-01` | Vay vốn lưu động: theo món, theo hạn mức, theo ngành, thấu chi | `CR` `CL` | **P2:** doanh thu, vòng quay hàng tồn giảm; thuế quan, giá hàng hóa, cước vận tải (xem file ngành)<br>**P3:** TSBĐ hàng tồn giảm giá | **P2:** DPD, xin cơ cấu<br>**P3:** LTV xấu đi |
| `CIB-LN-02` | Vay trung dài hạn: theo món, theo dự án, theo ngành, mua ô tô DN | `CR` `CL` `MR` | **P1:** dự án bị dừng, thu hồi<br>**P2:** lãi suất, tiến độ, pháp lý dự án | **P1:** dòng tiền trả nợ mất<br>**P2:** dự án chậm → dòng tiền trả nợ chậm |
| `CIB-SCF-01` | Tài trợ chuỗi cung ứng: kinh doanh ô tô; đại lý bán vé hàng không; vận chuyển hàng hóa hàng không; nhà phân phối Masan | `CR` | **P1:** anchor gặp sự cố: vỡ nợ, đình chỉ, bị điều tra<br>**P2:** nhu cầu cuối giảm: giá nhiên liệu bay, doanh số ô tô, tiêu dùng FMCG | **P1:** toàn bộ spoke bị ảnh hưởng đồng thời (cạnh `L03`, `S11`)<br>**P2:** spoke chậm trả dần |

**Thương mại (Trade)**
| Mã | Sản phẩm | Rủi ro chính | Nhạy với sự kiện | Chiều tác động khi sự kiện xấu |
|---|---|---|---|---|
| `CIB-TF-01` | Nhập khẩu: L/C nhập khẩu, nhờ thu | `CR` `MR` `CO` | **P1:** trừng phạt<br>**P2:** tỷ giá, giá hàng hóa tăng | **P1:** giao dịch bị dừng<br>**P2:** ngân hàng phải thanh toán thay khi DN thiếu tiền |
| `CIB-TF-02` | Xuất khẩu: L/C xuất khẩu, nhờ thu, tài trợ thương mại | `CR` `CO` | **P1:** trừng phạt nước người mua<br>**P2:** thuế quan, phòng vệ thương mại, cước vận tải; chứng từ bất hợp lệ | **P1:** không thu được tiền<br>**P2:** hủy đơn, chậm thu tiền (`X06`) |
| `CIB-TF-03` | Nội địa: L/C nội địa, tài trợ thương mại, tài trợ chuỗi cung ứng | `CR` `FR` | **P1:** gian lận chứng từ, hóa đơn khống<br>**P2:** chuỗi cung ứng đứt gãy | **P1:** tài trợ trên giao dịch không có thật (`X06`)<br>**P2:** chậm thanh toán trong chuỗi |
| `CIB-TF-04` | Bảo lãnh; L/C UPAS | `CR` `CO` | **P1:** chủ đầu tư vỡ nợ, bảo lãnh bị gọi hàng loạt<br>**P2:** vi phạm hợp đồng, tranh chấp | **P1:** ngân hàng phải trả thay<br>**P2:** bị gọi bảo lãnh |

**Nguồn vốn (Treasury & Markets)**
| Mã | Sản phẩm | Rủi ro chính | Nhạy với sự kiện | Chiều tác động khi sự kiện xấu |
|---|---|---|---|---|
| `CIB-FX-01` | Giao dịch ngoại tệ: giao ngay, kỳ hạn, hoán đổi | `MR` `CR` (đối tác) | **P1:** cú sốc tỷ giá đột ngột<br>**P2:** biến động tỷ giá | **P1:** lỗ vị thế lớn của khách → rủi ro đối tác (`S15`)<br>**P2:** lỗ vị thế, yêu cầu ký quỹ |
| `CIB-CM-01` | Phái sinh lãi suất | `MR` `CR` | **P2:** thay đổi lãi suất | **P2:** giá trị thị trường âm lớn với khách (`S15`) |
| `CIB-CM-02` | Phái sinh tỷ giá | `MR` `CR` | **P1:** cú sốc tỷ giá<br>**P2:** tỷ giá biến động | **P1:** giá trị thị trường âm lớn, rủi ro đối tác (`S15`)<br>**P2:** vị thế vượt nhu cầu phòng ngừa (`G06`) |
| `CIB-CM-03` | Sản phẩm cấu trúc | `MR` `RP` | **P1:** khách lỗ lớn, khiếu nại<br>**P2:** biến động thị trường | **P1:** tranh chấp về tính phù hợp sản phẩm (`RP`)<br>**P2:** giá trị sản phẩm giảm |
| `CIB-INV-01` | Trái phiếu doanh nghiệp (phát hành/thu xếp) | `CR` `RP` `CO` | **P1:** đáo hạn không trả được, vỡ nợ<br>**P2:** quy định phát hành | **P1:** lan sang nhà đầu tư cá nhân qua iBond (cạnh `L05`)<br>**P2:** khó phát hành, thu xếp |
| `CIB-INS-01` | Bảo hiểm phi nhân thọ cho DN | `INS` | **P1:** cháy nổ, thiên tai<br>**P2:** gián đoạn kinh doanh | **P1:** claim lớn<br>**P2:** claim gián đoạn |

## (d) Tín hiệu sớm nội bộ – CIB
- Báo cáo tổng hợp dòng tiền: dòng vào giảm, dòng ra tăng; tiền thu hộ giảm
- Sử dụng hạn mức vốn lưu động tăng liên tục; đề nghị gia hạn/cơ cấu
- L/C nhập khẩu tăng nhưng thanh toán chậm; chứng từ xuất khẩu bất hợp lệ tăng
- Vị thế FX/phái sinh của khách có giá trị thị trường âm lớn
- Lô lương giảm quy mô (cạnh `L02`)
- Spoke SCF cùng một anchor đồng loạt chậm trả
- Bán ra tài sản bảo đảm, chuyển nhượng cổ phần lớn của lãnh đạo

## (e) Lan ra phân khúc khác
- **→ KHCN** qua `L02` (nhân viên quy mô lớn), `L01` (lãnh đạo/cổ đông Private), `L04` (người mua nhà), `L05` (trái chủ iBond, NĐT iFund)
- **→ SME/HKD** qua `L03` (nhà phân phối, đại lý, nhà cung cấp)
- **→ Cấp ngân hàng** qua `L10` (rủi ro tập trung lớn ảnh hưởng trực tiếp chất lượng tài sản, xếp hạng và nhà đầu tư của ngân hàng – `bank/ngan_hang.md`)


## (f) Danh mục sản phẩm & URL nguồn (chốt 26/10/2026)


- **Quản trị hàng ngày:** Gói BusinessOne (Connect/Plus/Premium) · Techcombank Business · F@st EBank (đang chuyển đổi) · Chữ ký số · TK thanh toán · TK vốn · Giữ hộ thương mại · Giữ hộ BĐS · Thanh toán trong nước · Chuyển tiền nước ngoài · Nộp NSNN · Thẻ DN · Hóa đơn · Lương · Thu hộ (TK định danh, POS, QR, Payment Gateway, tiền mặt tại quầy / tại địa điểm KH / qua đối tác) · Báo cáo tổng hợp dòng tiền · CDM · Tổng đài · CCTG Bảo Lộc · Tiền gửi xanh
- **Vay:** Vốn lưu động (theo món, hạn mức, theo ngành, thấu chi) · Trung dài hạn (theo món, theo dự án, theo ngành, mua ô tô DN) · Tài trợ chuỗi cung ứng (kinh doanh ô tô, đại lý bán vé hàng không, vận chuyển hàng hóa hàng không, nhà phân phối Masan)
- **Thương mại:** L/C nhập khẩu · Nhờ thu NK · L/C xuất khẩu · Nhờ thu XK · Tài trợ thương mại · L/C nội địa · Tài trợ chuỗi cung ứng nội địa · Bảo lãnh · L/C UPAS
- **Nguồn vốn:** FX giao ngay · Kỳ hạn · Hoán đổi · Phái sinh lãi suất · Phái sinh tỷ giá · Sản phẩm cấu trúc · Trái phiếu doanh nghiệp
- **Bảo hiểm:** Bảo hiểm phi nhân thọ cho DN
