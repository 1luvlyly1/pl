---
id: SEG-KHCN-HKD
used_by: [Propagation, Product-Impact, Inside-out Monitor]
steps: [2, 3, 4]
depends_on: [core/01_risk_codes.md, core/03_linkage_graph.md]
load_when: Sự kiện chạm nhóm hộ kinh doanh của KHCN, sức mua địa phương, thuế HKD, hoặc lan qua L03, L06, L07
version: v3.0
updated: 2026-11-02
---

# Phân khúc KHCN – nhóm hộ kinh doanh (HKD)

> Hộ kinh doanh thuộc phân khúc **KHCN**. Tài chính của hộ và của chủ hộ không tách bạch, nên luôn đọc cùng `segments/seg_01a_KHCN_ca_nhan.md`. Mã sản phẩm `HKD-` giữ nguyên.

> Cấu trúc: (a) Chân dung → (b) Động lực rủi ro → (c) Bảng độ nhạy sản phẩm → (d) Tín hiệu sớm nội bộ → (e) Lan ra phân khúc khác → (f) Danh mục sản phẩm & URL nguồn


## (a) Chân dung
- Chủ hộ là cá nhân, thường đồng thời là KHCN (một CIF hoặc hai CIF liên kết).
- Mô hình: tạp hóa, ăn uống, bán lẻ online, dịch vụ nhỏ; doanh thu nhận qua QR, Soundbox, POS, phần mềm bán hàng.
- Đang trong giai đoạn **chuyển đổi thuế** và có lộ trình **chuyển lên doanh nghiệp** (cạnh `L07`).

## (b) Động lực rủi ro chính
1. **Chi tiêu của KHCN tại địa bàn** (cạnh `L06`) – nguồn doanh thu trực tiếp
2. **Chính sách thuế/hóa đơn** cho HKD – thay đổi chi phí tuân thủ, minh bạch doanh thu
3. **Chuỗi cung ứng / nhà phân phối** (cạnh `L03`) – điều khoản công nợ, giá nhập
4. **Sức khỏe & biến cố của chủ hộ** – dừng kinh doanh ngay lập tức
5. **Thiên tai, dịch bệnh, giải tỏa mặt bằng, quy hoạch chợ**
6. **Cạnh tranh từ thương mại điện tử / chuỗi bán lẻ**
7. **Lừa đảo nhắm vào chủ shop** (QR giả, mạo danh cơ quan thuế)

## (c) Bảng độ nhạy sản phẩm HKD
| Mã | Sản phẩm | Rủi ro chính | Nhạy với sự kiện | Chiều tác động khi sự kiện xấu |
|---|---|---|---|---|
| `HKD-ACC-01` | Tài khoản Hộ kinh doanh | `LQ` `CO` `FR` | **P1:** mạo danh cơ quan thuế, ngân hàng nhắm chủ hộ; tài khoản bị dùng làm trung gian<br>**P2:** bỏ thuế khoán, kê khai, hóa đơn điện tử; AML tách bạch dòng tiền<br>**P3:** sàn TMĐT khấu trừ thuế thay<br>**P2 (+):** quy định tách tài khoản HKD; HKD chuyển lên DN (`L07`) | **P1:** mất tiền, phong tỏa tài khoản (`X01`)<br>**P2:** doanh thu chảy về TK cá nhân thay TK HKD (`S16`); doanh thu về TK giảm<br>**P3:** đổi kênh bán hàng<br>**(+):** mở mới TK HKD, chuyển đổi lên DN |
| `HKD-REV-01` | Soundbox | `OR` `BR` | **P1:** sự cố mạng, thiết bị hàng loạt<br>**P2:** sức mua giảm; trả mặt bằng, giới hạn giờ hoạt động, siết vỉa hè<br>**P3:** QR miễn phí của đối thủ | **P1:** không nhận được tiền<br>**P2:** giảm số giao dịch/ngày, số người trả tiền (`S02` `S03`)<br>**P3:** rời bỏ thiết bị |
| `HKD-REV-02` | Liên kết phần mềm bán hàng (QR liên kết) | `OR` `BR` | **P1:** sự cố, lộ dữ liệu ở đối tác phần mềm (`L13`)<br>**P2:** đối tác đổi chính sách; hóa đơn điện tử từ máy tính tiền<br>**P3 (+):** quy định hóa đơn điện tử thúc đẩy số hóa | **P1:** mất dữ liệu doanh thu, gián đoạn nhận tiền<br>**P2:** chuyển sang đối tác khác<br>**(+):** kết nối mới tăng |
| `HKD-REV-03` | Nhận thanh toán thẻ: SoftPOS / SmartPOS / SoundPOS | `OR` `FR` `BR` | **P1:** gian lận thẻ tại điểm bán, lộ dữ liệu thẻ<br>**P2:** khách quốc tế giảm, sức mua giảm<br>**P3 (+):** khách du lịch tăng | **P1:** tra soát, chargeback (`X05`)<br>**P2:** doanh số thẻ giảm<br>**(+):** doanh số thẻ tăng |
| `HKD-LN-01` | Vay tín chấp kinh doanh ShopCash (hạn mức cấp sẵn) | `CR` | **P2:** doanh thu giảm (sức mua, thuế, mặt bằng, giờ hoạt động); dịch bệnh vật nuôi, giá nông sản giảm (với đại lý); biến cố chủ hộ<br>**P3 (+):** mùa Tết, mùa vụ nhập hàng | **P2:** sử dụng hạn mức tăng khi doanh thu giảm = tín hiệu căng thẳng (`S04`); DPD<br>**(+):** nhu cầu vốn mùa vụ, kèm rủi ro xin hạn mức ở giá đỉnh (`G05`) |
| `HKD-LN-02` | Vay thế chấp kinh doanh ShopCredit | `CR` `CL` | **P2:** doanh thu giảm, trả mặt bằng; giá nhà phố, giá thuê mặt bằng giảm; lãi suất tăng | **P2:** DPD; TSBĐ là nhà ở/mặt bằng giảm giá (`CL`) |
| `HKD-LN-03` | Vay trả góp tín chấp cho chủ HKD | `CR` | **P2:** doanh thu giảm; chủ hộ ốm đau, biến cố | **P2:** DPD sớm |
| `HKD-CARD-01` | Thẻ thanh toán Techcombank Visa Seller | `FR` `BR` | **P1:** gian lận thẻ, lộ dữ liệu thẻ<br>**P2:** HKD thu hẹp, giá đầu vào tăng | **P1:** giao dịch trái phép, tra soát<br>**P2:** giảm chi tiêu nhập hàng = HKD thu hẹp |
| `HKD-DEP-01` | Tiền gửi HKD; Sinh lời tự động | `LQ` | **P2:** doanh thu giảm, cần vốn nhập hàng; giá vàng tăng (tiệm vàng giữ tiền mặt)<br>**P3 (+):** tiền về sau mùa vụ, mùa cao điểm | **P2:** số dư nhàn rỗi giảm<br>**(+):** số dư tăng (`O2`) |
| `HKD-INS-01` | BH sức khỏe nhóm; BH toàn diện HKD & DN | `INS` | **P1:** cháy chợ, cháy nổ, bão lũ<br>**P2:** dịch bệnh | **P1:** claim tăng theo địa bàn<br>**P2:** claim sức khỏe tăng |
| `HKD-DIG-01` | Techcombank Mobile (cho HKD) | `OR` `FR` | **P1:** sự cố app; mạo danh, chiếm đoạt tài khoản | **P1:** mất doanh thu trực tiếp trong thời gian gián đoạn; mất tiền (`S13`) |
| `HKD-SVC-01` | Dịch vụ qua CDM | `OR` | **P1:** sự cố máy, thiên tai, mất điện<br>**P2:** mùa cao điểm tiền mặt | **P1:** không nộp được tiền mặt doanh thu<br>**P2:** máy quá tải, cần tiếp quỹ |

## (d) Tín hiệu sớm nội bộ – HKD
- Số giao dịch QR/Soundbox/POS **theo ngày** giảm so với cùng kỳ, theo địa bàn và MCC
- Số lượng người trả tiền khác nhau (unique payers) giảm → mất khách
- Doanh thu chuyển sang TK cá nhân thay vì TK HKD (né thuế hoặc rủi ro AML)
- Hạn mức ShopCash bị rút tối đa, trả chậm
- Chi tiêu thẻ Visa Seller cho nhập hàng giảm
- Ngắt liên kết phần mềm bán hàng

## (e) Lan ra phân khúc khác
- **→ KHCN (cùng chủ hộ)**: hop 0 – rủi ro HKD là rủi ro cá nhân chủ hộ (các khoản vay tiêu dùng, mua nhà, thẻ của chủ hộ).
- **→ DN lớn / nhà phân phối** (cạnh `L03` ngược): HKD giảm nhập hàng, chậm thanh toán công nợ → nhà phân phối SCF.
- **→ SME** (cạnh `L07`): HKD chuyển đổi lên DN mang theo rủi ro tín dụng cũ.


## (f) Danh mục sản phẩm & URL nguồn (chốt 26/10/2026)


- Tài khoản Hộ kinh doanh
- Quản lý doanh thu: Soundbox · Liên kết phần mềm bán hàng · (SoftPOS/SmartPOS/SoundPOS theo chương trình ưu đãi)
- Vay: ShopCash (tín chấp) · ShopCredit (thế chấp) · Vay trả góp tín chấp cho chủ HKD
- Techcombank Mobile · Thẻ thanh toán Techcombank Visa Seller · Tiền gửi (Sinh lời tự động)
- Bảo hiểm: Bảo hiểm sức khỏe nhóm · Bảo hiểm toàn diện
- Dịch vụ khác: CDM · Đặt lịch hẹn
- Lộ trình: Chuyển đổi HKD lên doanh nghiệp
