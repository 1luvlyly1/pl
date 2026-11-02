---
id: IND-10
code: I10
used_by: [Propagation, Product-Impact, Inside-out Monitor]
steps: [2, 3, 4]
depends_on: [industry/ind_00_index.md]
load_when: Tin về khách quốc tế, chính sách thị thực, đường bay, giá nhiên liệu bay, dịch bệnh, thiên tai ở điểm du lịch, sự kiện quốc tế lớn, xung đột, thu nhập và tiêu dùng nội địa, thuế với nhà hàng
version: v3.1
updated: 2026-11-03
---

# I10 – Du lịch, lưu trú, ăn uống và hàng không

> Kiến thức nền định tính, không chứa số liệu. Mức phơi nhiễm của Techcombank theo ngành cần truy vấn nội bộ.

## 1. Cấu trúc ngành ở Việt Nam
- **Các mảng:**
  - **hàng không** (vài hãng nội địa, nhiều hãng nước ngoài);
  - **lưu trú** (khách sạn, khu nghỉ dưỡng, homestay);
  - **lữ hành**, **ăn uống** (nhà hàng, quán ăn, cà phê);
  - **vui chơi giải trí**, **vận chuyển khách**.
- **Người tham gia:**
  - DN lớn hãng hàng không, tập đoàn nghỉ dưỡng;
  - SME khách sạn, công ty lữ hành, đại lý bán vé (một số trong chương trình tài trợ đại lý vé của ngân hàng);
  - HKD là lực lượng rất đông: quán ăn, cà phê, homestay, cho thuê xe, cửa hàng lưu niệm;
  - KHCN là lao động dịch vụ (thu nhập theo mùa, tiền tip) và khách du lịch.
- **Thị trường khách:**
  - khách quốc tế từ Đông Bắc Á, Đông Nam Á, Ấn Độ, Âu, Mỹ, Úc;
  - khách nội địa mạnh vào hè và dịp lễ.
- **Vùng:** các đô thị lớn, các tỉnh ven biển miền Trung, đảo phía Nam, vùng núi phía Bắc.
- **Đặc thù:**
  - nhạy cực mạnh với dịch bệnh và an ninh;
  - hàng không chịu chi phí nhiên liệu và thuê máy bay bằng USD;
  - nhiều doanh thu HKD là tiền mặt hoặc QR cá nhân.

## 2. Biến số nhạy cảm
| Biến số | Chiều | Độ trễ | Ghi chú |
|---|---|---|---|
| Chính sách thị thực, đường bay mới | Nới → khách quốc tế tăng | Một đến hai mùa | |
| Kinh tế, chính sách ở thị trường nguồn | Yếu → khách giảm | Vài tháng | Nhất là các thị trường khách lớn |
| Giá nhiên liệu bay | Tăng → giá vé tăng, hãng bị ép biên, đại lý vé chịu áp lực | Ngay | `L03` qua tài trợ đại lý vé |
| USD mạnh | Hãng bay chi phí USD tăng; khách quốc tế thấy Việt Nam rẻ hơn | Ngay | Hai chiều |
| Dịch bệnh | Đóng băng ngành | Ngay | Pha phục hồi kéo dài |
| Thiên tai, bão ở điểm đến | Hủy tour, thiệt hại cơ sở | Ngay | Mùa bão miền Trung |
| Xung đột, sự cố an ninh, hàng không | Khách tránh vùng, đổi đường bay | Nhanh | |
| Thu nhập nội địa | Yếu → du lịch, ăn uống giảm | Vài tháng | |
| Thuế, hóa đơn với nhà hàng; quy định nồng độ cồn | Siết → doanh thu nhà hàng giảm | Theo hiệu lực | |

## 3. Tác động theo đối tượng
### KHCN – cá nhân
- **Thách thức:** lao động dịch vụ mất thu nhập khi khách giảm, thường không có hợp đồng dài hạn; khách bị lừa đặt phòng, vé giả.
- **Cơ hội:**
  - mùa cao điểm có thu nhập tốt;
  - khách du lịch dùng thẻ, chuyển tiền quốc tế, bảo hiểm du lịch;
  - lao động có ngoại ngữ được tuyển dụng nhiều.

### KHCN – hộ kinh doanh
- **Thách thức:**
  - homestay, quán ăn vay để mở rộng ở pha bùng nổ, rồi chịu áp lực khi khách giảm;
  - bão, dịch làm mất doanh thu đột ngột;
  - chi phí thuế, hóa đơn.
- **Cơ hội:** khách quốc tế tăng làm doanh thu QR, thẻ tăng; nhận thanh toán thẻ quốc tế.

### SME
- **Thách thức:** khách sạn và lữ hành có chi phí cố định cao; đại lý bán vé chịu cọc và công nợ với hãng.
- **Cơ hội:** đường bay, thị trường khách mới; nâng cấp cơ sở lưu trú; vốn lưu động mùa cao điểm.

### DN lớn
- **Thách thức:**
  - hãng bay chịu giá nhiên liệu, tỷ giá, nợ thuê máy bay;
  - tập đoàn nghỉ dưỡng có vay dự án lớn.
- **Cơ hội:** khách quốc tế phục hồi, đường bay mới; chuyển tiền quốc tế, phòng ngừa tỷ giá và nhiên liệu.

## 4. Sản phẩm ngân hàng liên quan
| Đối tượng | Phía rủi ro | Phía cơ hội |
|---|---|---|
| KHCN | Vay tiêu dùng `CN-LN-06`, thẻ `CN-CARD-01` của lao động dịch vụ | Thẻ, bảo hiểm du lịch TechCare Travel `CN-INS-03`, ngoại tệ `CN-ACC-02` (`O3` `O4`) |
| HKD | ShopCash `HKD-LN-01`, ShopCredit `HKD-LN-02` của homestay, quán ăn | SoftPOS, SmartPOS `HKD-REV-03` nhận thẻ quốc tế, QR (`O3`), tiền gửi HKD (`O2`) |
| SME | Hybrid `SME-LN-01` | Vốn lưu động mùa cao điểm (`O1`), MerchantOne `SME-PKG-02` (`O3`) |
| DN lớn | Tài trợ đại lý bán vé `CIB-SCF-01`, vốn lưu động `CIB-LN-01`, vay dự án nghỉ dưỡng `CIB-LN-02` | Phái sinh tỷ giá, hàng hóa `CIB-CM-02`, chuyển tiền quốc tế `CIB-PAY-02`, thu hộ `CIB-COL-01` (`O3`) |
| Cấp ngân hàng | `BR` phí thẻ quốc tế giảm khi khách giảm | – |

## 5. Tín hiệu theo dõi
- `S02` doanh thu QR, POS theo MCC lưu trú, ăn uống, theo tỉnh du lịch.
- Giao dịch thẻ quốc tế tại điểm bán (chiều cơ hội).
- `S11` đại lý vé cùng một hãng chậm thanh toán.
- `S04` ShopCash của HKD du lịch tăng mùa thấp điểm.
- `X02` báo lừa đảo đặt phòng, vé.
- Cần truy vấn: dư nợ HKD, SME du lịch theo tỉnh; dư nợ tài trợ đại lý vé.

## 6. Liên kết ngành
- **Thượng nguồn:** `I12` (nhiên liệu bay), `I08` (thực phẩm, đồ uống).
- **Song song:** `I01` (BĐS nghỉ dưỡng), `I11` (vận tải hàng không), `I09` (bán lẻ khu du lịch), `I18` (khách mua trang sức).

## 7. Điểm đảo chiều và lưu ý
- Pha bùng nổ khách kéo HKD vay mở homestay, quán ăn → dư cung khi khách chững lại (Greed đảo chiều).
- Một sự cố an ninh, dịch bệnh có thể đảo chiều ngành trong vài ngày; phục hồi chậm hơn nhiều.
- Dầu tăng là thiệt cho hãng bay nhưng không phải lúc nào cũng làm khách giảm ngay.
