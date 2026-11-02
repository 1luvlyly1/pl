---
id: IND-08
code: I08
used_by: [Propagation, Product-Impact, Inside-out Monitor]
steps: [2, 3, 4]
depends_on: [industry/ind_00_index.md]
load_when: Tin về dịch tả lợn châu Phi, cúm gia cầm, giá lợn hơi, giá ngô, đậu tương, lúa mì, đường, sữa; tiêu dùng nội địa; thuế tiêu thụ đặc biệt đồ uống; an toàn thực phẩm; tỷ lệ sinh
version: v3.1
updated: 2026-11-03
---

# I08 – Chăn nuôi, thực phẩm, đồ uống và hàng tiêu dùng nhanh

> Kiến thức nền định tính, không chứa số liệu. Mức phơi nhiễm của Techcombank theo ngành cần truy vấn nội bộ.

## 1. Cấu trúc ngành ở Việt Nam
- **Chăn nuôi:** chuỗi từ thức ăn chăn nuôi → con giống → trang trại → giết mổ, chế biến → chợ, siêu thị.
  - Thức ăn chăn nuôi phụ thuộc lớn vào ngô, đậu tương, lúa mì nhập khẩu.
  - Chăn nuôi nông hộ nhỏ lẻ đang giảm; trang trại quy mô lớn và mô hình liên kết tăng.
- **Thực phẩm, đồ uống, FMCG:**
  - DN lớn (sữa, bia, nước giải khát, mì gói, dầu ăn, bánh kẹo, gia vị);
  - phân phối qua nhà phân phối, đại lý (SME, HKD) và tạp hóa;
  - một số DN lớn có chương trình tài trợ nhà phân phối với ngân hàng (`L03`).
- **Người tham gia:**
  - DN lớn sản xuất và phân phối;
  - SME nhà phân phối khu vực, cơ sở chế biến;
  - HKD đại lý cấp 2, tạp hóa, lò mổ, sạp chợ;
  - KHCN trang trại hộ gia đình, công nhân, người tiêu dùng.
- **Đặc thù:**
  - nhu cầu thiết yếu nên ít nhạy với chu kỳ;
  - nhóm đồ uống có cồn, nước ngọt nhạy với chính sách thuế và quy định;
  - dịch bệnh vật nuôi tạo cú sốc cung đột ngột.

## 2. Biến số nhạy cảm
| Biến số | Chiều | Độ trễ | Ghi chú |
|---|---|---|---|
| Giá ngô, đậu tương, lúa mì thế giới; USD | Tăng → chi phí thức ăn, ép biên trang trại | Vài tuần | |
| Dịch tả lợn châu Phi, cúm gia cầm | Bùng phát → nông hộ mất đàn; giá thịt tăng sau đó | Ngay rồi đảo | Trang trại an toàn sinh học có lợi |
| Giá lợn hơi | Tăng → trang trại lợi, F&B dùng thịt thiệt | Nhanh | Chu kỳ tái đàn |
| Tiêu dùng nội địa, thu nhập | Yếu → người tiêu dùng chuyển sang hàng rẻ | Một đến hai quý | |
| Thuế tiêu thụ đặc biệt, quy định nồng độ cồn | Tăng → sản lượng đồ uống giảm, nhà hàng thiệt | Theo hiệu lực | Chạm `I10` ăn uống |
| Giá đường, sữa bột, dầu thực vật | Tăng → chi phí sản xuất | Vài tuần | |
| Sự cố an toàn thực phẩm | Mất niềm tin thương hiệu, thu hồi sản phẩm | Ngay | Có thể kèm `RP` cho đối tác |
| Tỷ lệ sinh giảm, già hóa | Sữa trẻ em giảm cầu, dinh dưỡng người già tăng | Dài | Tin `GT` |

## 3. Tác động theo đối tượng
### KHCN – cá nhân
- **Thách thức:**
  - nông hộ chăn nuôi mất đàn do dịch, không có bảo hiểm;
  - giá thực phẩm tăng làm chi tiêu co lại.
- **Cơ hội:** giá lợn hơi tăng kéo theo thu nhập trang trại hộ tăng; tái đàn cần vốn.

### KHCN – hộ kinh doanh
- **Thách thức:**
  - đại lý thức ăn bán chịu cho trại nhỏ bị nợ đọng khi có dịch;
  - sạp thịt, lò mổ mất nguồn hàng;
  - tạp hóa chịu cạnh tranh từ chuỗi bán lẻ.
- **Cơ hội:** đại lý FMCG trong chuỗi DN lớn có doanh thu ổn định; mùa Tết là cao điểm nhập hàng.

### SME
- **Thách thức:** nhà phân phối phụ thuộc chính sách công nợ của hãng; tồn kho cận hạn.
- **Cơ hội:** tài trợ nhà phân phối theo chương trình của DN lớn; chế biến thực phẩm tiện lợi.

### DN lớn
- **Thách thức:**
  - chi phí nguyên liệu nhập, tỷ giá;
  - thuế tiêu thụ đặc biệt;
  - sự cố thương hiệu.
- **Cơ hội:**
  - giá nguyên liệu giảm;
  - mở rộng sang chăn nuôi khép kín;
  - thị trường người cao tuổi;
  - xuất khẩu thịt, thực phẩm chế biến.

## 4. Sản phẩm ngân hàng liên quan
| Đối tượng | Phía rủi ro | Phía cơ hội |
|---|---|---|
| KHCN | Vay tiêu dùng `CN-LN-06` của hộ chăn nuôi | Tiền gửi (`O2`), bảo hiểm (`O4`) |
| HKD | ShopCash `HKD-LN-01` của đại lý thức ăn, sạp thịt | Vốn nhập hàng mùa Tết (`O1`), QR, Soundbox `HKD-REV-01` (`O3`) |
| SME | Hybrid `SME-LN-01`, MerchantOne `SME-PKG-02` | Vốn lưu động nhà phân phối (`O1`), thanh toán (`O3`) |
| DN lớn | L/C nhập ngô, đậu tương `CIB-TF-01`, FX `CIB-FX-01` | Tài trợ nhà phân phối `CIB-SCF-01`, phái sinh tỷ giá `CIB-CM-02`, thu hộ `CIB-COL-01`, chi lương (`O1` `O3` `O2`) |
| Cấp ngân hàng | Tập trung tài trợ chuỗi theo một anchor | – |

## 5. Tín hiệu theo dõi
- `S11` nhà phân phối cùng một DN lớn chậm trả đồng loạt.
- `S02` doanh thu QR của sạp thịt, tạp hóa theo địa bàn.
- `S04` ShopCash đại lý thức ăn tăng khi có dịch.
- Nhu cầu L/C nhập nguyên liệu thức ăn chăn nuôi theo mùa.
- Cần truy vấn: dư nợ theo chuỗi anchor FMCG, số nhà phân phối trong chương trình tài trợ.

## 6. Liên kết ngành
- **Thượng nguồn:** `I07` (ngô, gạo, cà phê làm nguyên liệu), nhập khẩu ngũ cốc qua `I11`, `I13` (bao bì).
- **Hạ nguồn:** `I09` bán lẻ, `I10` ăn uống.
- **Song song:** `I06` (thức ăn thủy sản dùng chung nguyên liệu).

## 7. Điểm đảo chiều và lưu ý
- Sau dịch, giá thịt tăng kéo tái đàn ồ ạt → vài quý sau giá giảm.
- Hàng thiết yếu là nơi trú ẩn khi tiêu dùng yếu, nhưng biên vẫn bị ép.
- Không nêu tên thương hiệu; với sự cố an toàn thực phẩm chỉ mô tả tác động lên chuỗi.
