---
id: IND-15
code: I15
used_by: [Propagation, Product-Impact, Inside-out Monitor]
steps: [2, 3, 4]
depends_on: [industry/ind_00_index.md]
load_when: Tin về dịch bệnh, bảo hiểm y tế, đấu thầu thuốc, giá dịch vụ y tế, quy định nhà thuốc, già hóa dân số, thuốc giả, tỷ giá (thuốc nhập), y tế tư nhân, du lịch chữa bệnh
version: v3.1
updated: 2026-11-03
---

# I15 – Y tế và dược phẩm

> Kiến thức nền định tính, không chứa số liệu. Mức phơi nhiễm của Techcombank theo ngành cần truy vấn nội bộ.

## 1. Cấu trúc ngành ở Việt Nam
- **Dịch vụ y tế:**
  - bệnh viện công là chủ đạo;
  - bệnh viện tư, phòng khám tư, nha khoa, thẩm mỹ, xét nghiệm tăng nhanh ở đô thị.
- **Dược phẩm:**
  - DN sản xuất trong nước (chủ yếu thuốc generic), DN FDI;
  - nhiều thuốc chuyên khoa và nguyên liệu dược nhập khẩu;
  - kênh **bệnh viện** (qua đấu thầu) và kênh **nhà thuốc** (chuỗi nhà thuốc và nhà thuốc lẻ).
- **Thiết bị y tế:** chủ yếu nhập khẩu, phân phối qua DN thương mại.
- **Người tham gia:**
  - DN lớn chuỗi bệnh viện tư, nhà sản xuất dược, chuỗi nhà thuốc;
  - SME phân phối dược, thiết bị, phòng khám;
  - HKD nhà thuốc lẻ, phòng khám tư nhỏ, nha khoa;
  - KHCN y bác sĩ, dược sĩ (thu nhập ổn định) và người bệnh.
- **Đặc thù:**
  - nhu cầu ít nhạy chu kỳ;
  - đấu thầu thuốc và thanh toán BHYT có thể chậm, gây áp lực vốn cho nhà cung cấp;
  - già hóa dân số là động lực dài hạn.

## 2. Biến số nhạy cảm
| Biến số | Chiều | Độ trễ | Ghi chú |
|---|---|---|---|
| Dịch bệnh | Tăng cầu thuốc, xét nghiệm, thiết bị; bệnh viện quá tải | Ngay | Dịch kéo dài: dịch vụ không khẩn cấp giảm |
| Chính sách đấu thầu, thanh toán BHYT | Chậm → nhà cung cấp kẹt vốn | Vài tháng | `L12` |
| Giá dịch vụ y tế, tự chủ bệnh viện | Điều chỉnh → doanh thu bệnh viện thay đổi | Theo quyết định | |
| Quy định nhà thuốc, kê đơn, hóa đơn | Siết → nhà thuốc lẻ chịu chi phí tuân thủ | Theo hiệu lực | Chuỗi nhà thuốc có lợi thế |
| USD mạnh | Thuốc nhập, nguyên liệu, thiết bị đắt hơn | Vài tháng | |
| Già hóa, bệnh mãn tính tăng | Cầu dài hạn tăng | Dài | Tin `GT` |
| Thu nhập tăng, tầng lớp trung lưu | Cầu y tế tư, bảo hiểm sức khỏe tăng | Dài | |
| Vụ việc thuốc giả, sai phạm đấu thầu | Mất niềm tin, điều tra | Nhanh | Có thể chạm `CO` `RP` cho đối tác |

## 3. Tác động theo đối tượng
### KHCN – cá nhân
- **Thách thức:** chi phí y tế lớn đột xuất làm cạn tiết kiệm, phải vay tiêu dùng, tất toán sớm; người bệnh mãn tính chịu giá thuốc nhập tăng.
- **Cơ hội:**
  - nhu cầu bảo hiểm sức khỏe tăng sau dịch hoặc tin y tế;
  - y bác sĩ là khách thu nhập ổn định (vay mua nhà, đầu tư);
  - mở phòng khám riêng.

### KHCN – hộ kinh doanh
- **Thách thức:** nhà thuốc lẻ cạnh tranh với chuỗi, chi phí tuân thủ; tồn kho thuốc sau mùa dịch.
- **Cơ hội:** mùa dịch làm doanh thu tăng; số hóa thanh toán, quản lý bán hàng.

### SME
- **Thách thức:** nhà phân phối thuốc, thiết bị bị bệnh viện chậm thanh toán; cần bảo lãnh dự thầu.
- **Cơ hội:** trúng thầu; phòng khám chuyên khoa, nha khoa mở rộng (vay đầu tư thiết bị).

### DN lớn
- **Thách thức:** đấu thầu giá thấp; chi phí nguyên liệu nhập; tuân thủ quy chuẩn sản xuất.
- **Cơ hội:** chuỗi bệnh viện tư mở rộng, chuỗi nhà thuốc; sản xuất trong nước thay thế nhập khẩu; già hóa dân số.

## 4. Sản phẩm ngân hàng liên quan
| Đối tượng | Phía rủi ro | Phía cơ hội |
|---|---|---|
| KHCN | Vay tiêu dùng `CN-LN-06`, tất toán sớm `CN-DEP-01` (`S06`) do chi phí y tế | Bảo hiểm sức khỏe `CN-INS-01` (`O4`), vay mua nhà cho y bác sĩ (`O1`), tài khoản lương (`O2`) |
| HKD | ShopCash `HKD-LN-01` của nhà thuốc lẻ | QR, SoftPOS `HKD-REV-03`, vốn nhập thuốc (`O3` `O1`) |
| SME | Hybrid `SME-LN-01` kẹt vốn do chậm thanh toán | Bảo lãnh mua sắm công `SME-GTE-01` (`O3`), vay thiết bị (`O1`) |
| DN lớn | L/C nhập nguyên liệu, thiết bị `CIB-TF-01`, FX `CIB-FX-01` | Vay đầu tư bệnh viện `CIB-LN-02`, chi lương `CIB-PAY-06`, thu hộ viện phí `CIB-COL-01` (`O1` `O2` `O3`) |
| Cấp ngân hàng | `RP` khi bán bảo hiểm sức khỏe không phù hợp nhu cầu | – |

## 5. Tín hiệu theo dõi
- `S06` tất toán sớm, vay cầm cố tiền gửi tăng trong mùa dịch.
- `S09` hủy bảo hiểm sớm, hoặc ngược lại: số hợp đồng bảo hiểm sức khỏe mới tăng.
- `S02` doanh thu QR của nhà thuốc theo địa bàn (chỉ báo sớm dịch bệnh cục bộ).
- Thời gian thu tiền từ bệnh viện của nhà phân phối.
- Cần truy vấn: dư nợ ngành y tế, dược theo kênh (bệnh viện, nhà thuốc).

## 6. Liên kết ngành
- **Thượng nguồn:** nhập khẩu nguyên liệu qua `I11`, `I13` (hóa chất).
- **Song song:** `I17` (y tế số), `I10` (du lịch chữa bệnh, thẩm mỹ).
- **Ngành bị tác động ngược khi có dịch:** `I10`, `I16`, `I09` cửa hàng.

## 7. Điểm đảo chiều và lưu ý
- Doanh thu tăng mạnh mùa dịch không phải xu hướng; nhà thuốc, phân phối mở rộng ở đỉnh dịch dễ tồn kho.
- Bảo hiểm sức khỏe là cơ hội `O4`, nhưng phải đúng nhu cầu (`guardrails.md`, `RP`).
- Không nêu tên cơ sở y tế; không suy đoán sai phạm.
