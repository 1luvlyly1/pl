---
id: SEG-SME
used_by: [Propagation, Product-Impact, Inside-out Monitor]
steps: [2, 3, 4]
depends_on: [core/01_risk_codes.md, core/03_linkage_graph.md]
load_when: Sự kiện chạm DN vừa và nhỏ, mua sắm công, hoặc lan qua L01, L02, L03, L07, L12
version: v3.0
updated: 2026-11-02
---

# Phân khúc: Doanh nghiệp vừa và nhỏ (SME)

> Cấu trúc: (a) Chân dung → (b) Động lực rủi ro → (c) Bảng độ nhạy sản phẩm → (d) Tín hiệu sớm nội bộ → (e) Lan ra phân khúc khác → (f) Danh mục sản phẩm & URL nguồn


## (a) Chân dung
- Quy mô vừa/nhỏ, quản trị phụ thuộc chủ sở hữu (cạnh `L01` rất mạnh).
- Dùng gói BusinessOne / MerchantOne; vay dựa trên dữ liệu (Misa Lending, Hybrid, B1CP); tham gia mua sắm công.

## (b) Động lực rủi ro chính
1. **Dòng tiền ngắn hạn** – SME ít đệm thanh khoản; chậm thu tiền khách hàng là nguy cơ lớn nhất
2. **Phụ thuộc khách hàng/nhà cung cấp lớn** (cạnh `L03`)
3. **Chủ sở hữu** – biến cố cá nhân của chủ = biến cố DN
4. **Thuế, hóa đơn, kế toán** (dữ liệu từ phần mềm kế toán ảnh hưởng hạn mức vay)
5. **Thanh toán chậm từ ngân sách / chủ đầu tư công** (cạnh `L12`)
6. **Tỷ giá** với SME có nhập khẩu nguyên liệu
7. **Lừa đảo chiếm đoạt tài khoản DN, giả mạo email đối tác (BEC)**

## (c) Bảng độ nhạy sản phẩm SME
**Tài khoản & Gói giải pháp**
| Mã | Sản phẩm | Rủi ro chính | Nhạy với sự kiện | Chiều tác động khi sự kiện xấu |
|---|---|---|---|---|
| `SME-ACC-01` | Tài khoản doanh nghiệp | `LQ` `FR` `CO` | **P1:** email giả đối tác (BEC), chiếm quyền tài khoản<br>**P2:** dòng tiền giảm, bị chậm thanh toán; AML | **P1:** chuyển tiền nhầm cho đối tượng lừa đảo (`X04`)<br>**P2:** số dư giảm; giao dịch bất thường |
| `SME-ACC-02` | Tài khoản vốn | `CO` `MR` | **P2:** quy định đầu tư nước ngoài, ngoại hối; FDI rút<br>**P3 (+):** FDI tăng, dịch chuyển chuỗi cung ứng | **P2:** dòng vốn FDI/góp vốn dừng<br>**(+):** dòng vốn mới |
| `SME-ACC-03` | Tài khoản giữ hộ thương mại | `RP` `CO` | **P2:** tranh chấp hợp đồng mua bán, đối tác vỡ nợ | **P2:** tranh chấp giải ngân giữ hộ |
| `SME-ACC-04` | Tài khoản giữ hộ bất động sản | `RP` `CO` | **P1:** dự án bị dừng, thanh tra<br>**P2:** pháp lý giao dịch BĐS | **P1:** phong tỏa<br>**P2:** tranh chấp |
| `SME-ACC-05` | Tài khoản ký quỹ | `CO` `MR` | **P2:** bảo lãnh bị gọi, giao dịch có điều kiện tranh chấp | **P2:** ký quỹ bị phong tỏa/giải tỏa đột ngột |
| `SME-PKG-01` | BusinessOne Plus / Connect / Premium | `BR` | **P3:** hoạt động DN giảm, cắt giảm chi phí | **P3:** hạ gói, đóng gói |
| `SME-PKG-02` | MerchantOne | `BR` `OR` | **P2:** doanh thu bán lẻ giảm, sức mua yếu (cạnh `L06`)<br>**P3 (+):** mùa mua sắm | **P2:** giảm giao dịch nhận tiền<br>**(+):** giao dịch tăng |
| `SME-REV-01` | SoftPOS; liên kết phần mềm bán hàng | `OR` `FR` | **P1:** gian lận thẻ, sự cố<br>**P2:** sức mua giảm | **P1:** chargeback, gián đoạn<br>**P2:** doanh số giảm |

**Thanh toán**
| Mã | Sản phẩm | Rủi ro chính | Nhạy với sự kiện | Chiều tác động khi sự kiện xấu |
|---|---|---|---|---|
| `SME-PAY-01` | Thanh toán tiền hàng hóa, dịch vụ | `FR` `OR` | **P1:** BEC, đổi tài khoản thụ hưởng; sự cố | **P1:** chuyển nhầm/lừa đảo (`X04`); thanh toán chậm |
| `SME-PAY-02` | Thẻ tín dụng DN (Visa Business Platinum) | `CR` `FR` | **P1:** lộ dữ liệu thẻ<br>**P2:** dòng tiền DN giảm | **P1:** giao dịch gian lận<br>**P2:** dư nợ thẻ tăng, chậm trả |
| `SME-PAY-03` | Thẻ thanh toán DN | `FR` | **P1:** gian lận thẻ, lộ dữ liệu thẻ | **P1:** giao dịch trái phép, tra soát |
| `SME-PAY-04` | Giao dịch ngoại tệ | `MR` `CO` | **P2:** tỷ giá, USD tăng; quy định ngoại hối<br>**P3 (+):** USD tăng với DN xuất khẩu | **P2:** chi phí nhập khẩu tăng<br>**(+):** doanh thu xuất khẩu quy đổi tăng, nhu cầu bán ngoại tệ (`O3`) |
| `SME-PAY-05` | Thanh toán hóa đơn | `OR` | **P1:** sự cố<br>**P3:** đổi nhà cung cấp dịch vụ | **P1:** hóa đơn trễ hạn<br>**P3:** giảm giao dịch |
| `SME-PAY-06` | Thanh toán lương | `CR` (gián tiếp) `BR` | **P1:** DN chậm hoặc giảm lương<br>**P2:** thuế quan, mất đơn, đơn hàng giảm<br>**P3 (+):** tuyển dụng mới | **P1:** trả lương trễ/giảm = DN căng thẳng, lan sang nhân viên (tín hiệu then chốt cạnh `L02`, `S01`)<br>**P2:** quỹ lương giảm dần<br>**(+):** tài khoản lương mới |
| `SME-PAY-07` | Chuyển tiền đi nước ngoài | `CO` `MR` | **P1:** trừng phạt<br>**P2:** AML, tỷ giá | **P1:** giao dịch bị giữ lại<br>**P2:** rà soát, chi phí tăng |
| `SME-PAY-08` | Chuyển tiền nộp ngân sách nhà nước | `CO` | **P2:** thay đổi thuế, hóa đơn<br>**P3:** lịch nộp thuế | **P2:** nộp thuế chậm = dấu hiệu thiếu tiền (`S10`)<br>**P3:** giao dịch dồn kỳ |

**Tiền gửi, Ngân hàng số, Vay, Bảo lãnh, Bảo hiểm**
| Mã | Sản phẩm | Rủi ro chính | Nhạy với sự kiện | Chiều tác động khi sự kiện xấu |
|---|---|---|---|---|
| `SME-DEP-01` | Tiền gửi có kỳ hạn / linh hoạt | `LQ` | **P2:** cần vốn lưu động, đơn hàng giảm<br>**P3:** lãi suất | **P2:** tất toán sớm<br>**P3:** kỳ hạn ngắn lại |
| `SME-DEP-02` | Chứng chỉ tiền gửi Bảo Lộc | `LQ` `MR` | **P1:** tin đồn về ngân hàng<br>**P2:** lãi suất | **P1:** yêu cầu bán lại<br>**P2:** không mua mới |
| `SME-DIG-01` | Techcombank Business; F@st EBank | `OR` `FR` | **P1:** sự cố, chiếm quyền truy cập; giai đoạn chuyển đổi nền tảng | **P1:** không chi lương/thanh toán đúng hạn; chuyển tiền trái phép (`X03`) |
| `SME-LN-01` | Giải pháp tín dụng linh hoạt (Hybrid) | `CR` `CL` | **P2:** doanh thu giảm do thuế quan, giá đầu vào, cước vận tải, sức mua (xem file ngành)<br>**P3:** TSBĐ giảm giá | **P2:** DPD<br>**P3:** LTV xấu đi |
| `SME-LN-02` | Tín dụng kết nối Misa Lending | `CR` `OR` | **P1:** sự cố, lộ dữ liệu ở đối tác dữ liệu (`L13`)<br>**P2:** dữ liệu kế toán bị thao túng | **P1:** gián đoạn xét duyệt<br>**P2:** hạn mức dựa trên dữ liệu sai lệch |
| `SME-LN-03` | Giải pháp tín dụng B1CP | `CR` | **P2:** dòng tiền giảm | **P2:** DPD |
| `SME-GTE-01` | Bảo lãnh mua sắm công | `CR` `CO` | **P1:** điều tra sai phạm đấu thầu<br>**P2:** chậm giải ngân vốn đầu tư công (cạnh `L12`)<br>**P3 (+):** đầu tư công tăng | **P1:** bị yêu cầu thực hiện bảo lãnh<br>**P2:** nhà thầu thiếu vốn, gia hạn bảo lãnh<br>**(+):** nhu cầu bảo lãnh tăng (`O3`) |
| `SME-INS-01` | BH sức khỏe nhóm; BH toàn diện | `INS` | **P1:** cháy nổ, thiên tai<br>**P2:** dịch bệnh | **P1:** claim lớn<br>**P2:** claim sức khỏe tăng |

## (d) Tín hiệu sớm nội bộ – SME
- Lô chi lương **trễ ngày**, **giảm số nhân viên** hoặc **giảm tổng quỹ lương**
- Nộp NSNN trễ; tần suất thanh toán hóa đơn (điện, nước) giảm → sản xuất giảm
- Dòng tiền vào giảm, tập trung từ ít khách hàng hơn
- Sử dụng hạn mức Hybrid/B1CP tối đa liên tục
- Chủ DN rút tiết kiệm cá nhân, tăng thấu chi cá nhân (cạnh `L01`)
- Thay đổi đột ngột người đại diện pháp luật / chủ sở hữu
- Đăng nhập Techcombank Business từ thiết bị/IP lạ, thay đổi người thụ hưởng (BEC)

## (e) Lan ra phân khúc khác
- **→ KHCN** qua `L01` (chủ DN) và `L02` (nhân viên)
- **→ HKD** (là nhà cung cấp hoặc khách hàng của SME)
- **→ DN lớn** (SME là spoke trong chuỗi SCF – cạnh `L03`)


## (f) Danh mục sản phẩm & URL nguồn (chốt 26/10/2026)


- Tài khoản: Tài khoản DN · Tài khoản vốn · Giữ hộ thương mại · Giữ hộ BĐS · Ký quỹ
- Gói giải pháp: BusinessOne Plus · BusinessOne Connect · BusinessOne Premium · MerchantOne
- Quản lý doanh thu: SoftPOS · Liên kết phần mềm bán hàng
- Thanh toán: Hàng hóa dịch vụ · Thẻ tín dụng DN (Visa Business Platinum) · Thẻ thanh toán DN · Giao dịch ngoại tệ · Thanh toán hóa đơn · Thanh toán lương · Chuyển tiền đi nước ngoài · Nộp NSNN
- Tiền gửi: Có kỳ hạn · Linh hoạt · CCTG Bảo Lộc
- Ngân hàng số: Techcombank Business · F@st EBank
- Vay: Tín dụng linh hoạt (Hybrid) · Kết nối Misa Lending · B1CP
- Bảo lãnh: Bảo lãnh mua sắm công
- Bảo hiểm: Sức khỏe nhóm · Toàn diện
- Dịch vụ khác: CDM · Đặt lịch hẹn
