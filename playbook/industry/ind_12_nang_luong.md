---
id: IND-12
code: I12
used_by: [Propagation, Product-Impact, Inside-out Monitor]
steps: [2, 3, 4]
depends_on: [industry/ind_00_index.md]
load_when: Tin về giá dầu, khí, than, điều hành giá xăng dầu, giá điện bán lẻ, quy hoạch điện, năng lượng tái tạo, thiếu điện, hạn hán (thủy điện), xung đột tại vùng dầu mỏ, chuyển đổi xanh, trung tâm dữ liệu
version: v3.1
updated: 2026-11-03
---

# I12 – Năng lượng (dầu khí, xăng dầu, điện, tái tạo)

> Kiến thức nền định tính, không chứa số liệu. Mức phơi nhiễm của Techcombank theo ngành cần truy vấn nội bộ.

## 1. Cấu trúc ngành ở Việt Nam
- **Dầu khí:**
  - thượng nguồn (thăm dò, khai thác), trung nguồn (lọc hóa dầu, khí), hạ nguồn (phân phối xăng dầu);
  - xăng dầu trong nước một phần từ nhà máy lọc dầu, phần còn lại nhập khẩu;
  - giá bán lẻ được điều hành định kỳ theo giá thế giới, có quỹ bình ổn.
- **Điện:**
  - nguồn gồm thủy điện, nhiệt điện than, khí, điện mặt trời, điện gió;
  - truyền tải và bán lẻ do Nhà nước chi phối, giá điện bán lẻ do Nhà nước điều chỉnh;
  - có chủ trương mua bán điện trực tiếp và điện mặt trời mái nhà.
- **Người tham gia:**
  - DN lớn khai thác, lọc dầu, phát điện, phân phối xăng dầu;
  - SME đầu mối phân phối nhỏ, nhà thầu lắp đặt điện mặt trời, dịch vụ kỹ thuật;
  - HKD cửa hàng xăng dầu tư nhân, đại lý gas;
  - KHCN người tiêu dùng nhiên liệu và điện, hộ lắp điện mặt trời mái nhà.
- **Đặc thù:**
  - dự án điện vốn lớn, vay dài hạn, nhạy lãi suất và chính sách giá mua điện;
  - phân phối xăng dầu cần vốn lưu động lớn và chịu rủi ro giá hàng tồn giữa các kỳ điều hành.

## 2. Biến số nhạy cảm
| Biến số | Chiều | Độ trễ | Ghi chú |
|---|---|---|---|
| Giá dầu thế giới | Tăng → thượng nguồn lợi; phân phối lợi trên hàng tồn nhưng cần thêm vốn | Ngay | Giá giảm nhanh: phân phối lỗ hàng tồn |
| Kỳ điều hành giá xăng dầu trong nước | Chậm theo giá thế giới → đầu mối bị kẹp biên | Theo kỳ | Từng có giai đoạn thiếu xăng cục bộ |
| Giá khí, than nhập khẩu | Tăng → chi phí phát điện | Nhanh | Nhà máy chịu nếu giá bán điện không điều chỉnh |
| Giá điện bán lẻ | Tăng → bên bán lợi; ngành dùng nhiều điện thiệt | Theo quyết định | Xem `I02` `I13` |
| Hạn hán, El Niño | Thủy điện giảm → nguy cơ thiếu điện | Theo mùa | Từng có giai đoạn cắt điện ở phía Bắc |
| Chính sách giá mua điện tái tạo, quy hoạch | Không rõ ràng → dự án tái tạo kẹt dòng tiền | Dài | |
| USD mạnh | Nhập xăng dầu, thiết bị, nợ USD thiệt | Ngay | |
| Lãi suất | Tăng → dự án đòn bẩy cao chịu áp lực | Vài tháng | |
| Xu hướng xanh, trung tâm dữ liệu, xe điện | Cầu điện tăng, cơ hội đầu tư nguồn mới | Dài | Tin `GT` |

## 3. Tác động theo đối tượng
### KHCN – cá nhân
- **Thách thức:** giá xăng, điện tăng làm chi phí sinh hoạt tăng, chi tiêu khác co lại (`L06`).
- **Cơ hội:** lắp điện mặt trời mái nhà, xe điện (vay mua, bảo hiểm); lao động kỹ thuật năng lượng có thu nhập tốt.

### KHCN – hộ kinh doanh
- **Thách thức:**
  - cửa hàng xăng dầu tư nhân bị đầu mối hạn chế nguồn hoặc chiết khấu thấp khi giá biến động;
  - giá giảm nhanh thì lỗ hàng tồn.
- **Cơ hội:** doanh thu tăng theo giá; dịch vụ lắp đặt điện mặt trời, sạc xe điện.

### SME
- **Thách thức:** nhà thầu lắp đặt bị chủ dự án chậm thanh toán khi chính sách không rõ; đầu mối nhỏ thiếu vốn khi giá tăng.
- **Cơ hội:** điện mặt trời mái nhà cho nhà xưởng; dịch vụ bảo trì; mua bán điện trực tiếp.

### DN lớn
- **Thách thức:**
  - nhà máy điện chịu giá nhiên liệu, chậm thu tiền điện;
  - dự án tái tạo kẹt giá mua điện;
  - đầu mối xăng dầu chịu kỳ điều hành.
- **Cơ hội:**
  - giá dầu cao làm thượng nguồn lợi;
  - đầu tư nguồn điện mới, lưới, khí hóa lỏng;
  - tài trợ xanh.

## 4. Sản phẩm ngân hàng liên quan
| Đối tượng | Phía rủi ro | Phía cơ hội |
|---|---|---|
| KHCN | Chi tiêu, thẻ `CN-CARD-01` co lại khi giá tăng | Vay lắp điện mặt trời, xe điện (`CN-LN-08` `CN-LN-04`, `O1`), bảo hiểm (`O4`) |
| HKD | ShopCredit `HKD-LN-02` của cửa hàng xăng dầu | Vốn nhập hàng (`O1`), QR, POS (`O3`) |
| SME | Hybrid `SME-LN-01`, bảo lãnh `SME-GTE-01` | Vốn lưu động, bảo lãnh (`O1` `O3`) |
| DN lớn | Vay dự án điện `CIB-LN-02`, L/C nhập xăng dầu `CIB-TF-01`, FX `CIB-FX-01` | Vốn lưu động `CIB-LN-01`, phái sinh tỷ giá, hàng hóa `CIB-CM-02`, tiền gửi xanh, trái phiếu xanh `CIB-INV-01` (`O1` `O3`) |
| Cấp ngân hàng | Nhu cầu USD của nhà nhập khẩu (`NH-MR-01`); lạm phát → lãi suất (`NH-MR-02`) | – |

## 5. Tín hiệu theo dõi
- Nhu cầu mua USD, L/C nhập xăng dầu theo kỳ.
- `S04` hạn mức của đầu mối, cửa hàng xăng dầu.
- `S10` hóa đơn điện của khách sản xuất (dấu hiệu sản lượng).
- `S15` vị thế phái sinh hàng hóa của khách.
- Cần truy vấn: dư nợ dự án điện theo loại nguồn; dư nợ phân phối xăng dầu.

## 6. Liên kết ngành
- **Khách dùng năng lượng làm đầu vào:** `I10` hàng không, `I11` vận tải, `I13` hóa chất, phân bón, nhựa, `I02` thép, xi măng, `I06` tàu cá.
- **Song song:** `I14` xe điện, `I17` trung tâm dữ liệu, `I04` (FDI cần điện ổn định).

## 7. Điểm đảo chiều và lưu ý
- Giá dầu là biến số chạm nhiều ngành nhất; chỉ nạp file của ngành bị tác động mạnh nhất, không kể hết.
- Phân phối xăng dầu lợi khi giá tăng nhưng lỗ khi giá giảm nhanh – đây là điểm đảo chiều thường gặp.
- Không suy đoán quyết định điều hành giá của cơ quan nhà nước.
