---
id: IND-16
code: I16
used_by: [Propagation, Product-Impact, Inside-out Monitor]
steps: [2, 3, 4]
depends_on: [industry/ind_00_index.md, examples/ex_NW_02_ty_le_sinh_giam.md]
load_when: Tin về tỷ lệ sinh, chính sách giáo dục, học phí, chương trình phổ thông, quy định trường tư và trung tâm, chính sách thị thực du học của nước ngoài, tỷ giá, dịch bệnh (đóng cửa trường), AI trong giáo dục
version: v3.1
updated: 2026-11-03
---

# I16 – Giáo dục

> Kiến thức nền định tính, không chứa số liệu. Mức phơi nhiễm của Techcombank theo ngành cần truy vấn nội bộ.

## 1. Cấu trúc ngành ở Việt Nam
- **Các mảng:**
  - **công lập** chiếm phần lớn;
  - **tư thục và quốc tế** (mầm non, phổ thông, đại học) tăng ở đô thị;
  - **trung tâm** ngoại ngữ, luyện thi, kỹ năng;
  - **du học** (Mỹ, Úc, Canada, Anh, Nhật, Hàn và các nước khác);
  - **giáo dục số**.
- **Người tham gia:**
  - DN lớn hệ thống trường tư, đại học tư;
  - SME trung tâm, công ty tư vấn du học, công nghệ giáo dục;
  - HKD nhóm trẻ, mầm non tư nhỏ, lớp học thêm, trung tâm nhỏ;
  - KHCN là phụ huynh (chi tiêu giáo dục rất ưu tiên), giáo viên, học sinh và sinh viên du học.
- **Đặc thù:**
  - phụ huynh coi giáo dục là khoản chi cuối cùng bị cắt;
  - học phí thu theo kỳ nên tạo dòng tiền vào theo mùa;
  - du học tạo dòng chuyển tiền ra nước ngoài, nhạy với tỷ giá và chính sách thị thực;
  - mầm non tư nhỏ nhạy với số trẻ sinh ra theo địa bàn.
- **Mùa vụ:** tựu trường, đóng học phí đầu kỳ, mùa nộp hồ sơ du học.

## 2. Biến số nhạy cảm
| Biến số | Chiều | Độ trễ | Ghi chú |
|---|---|---|---|
| Tỷ lệ sinh, số trẻ theo địa bàn | Giảm → mầm non trước, rồi phổ thông vài năm sau | Rất dài | Tin `GT`, xem `ex_NW_02_ty_le_sinh_giam.md` |
| Thu nhập phụ huynh | Giảm → chuyển từ trường quốc tế sang tư thục rẻ hơn, giảm học thêm | Một năm học | |
| Chính sách thị thực, giới hạn du học sinh ở nước ngoài | Siết → giảm du học, chuyển nước | Một đến hai mùa tuyển | |
| USD và ngoại tệ mạnh | Chi phí du học tăng | Ngay | |
| Quy định học thêm, trường tư, liên kết quốc tế | Siết → trung tâm, lớp học thêm giảm | Theo hiệu lực | |
| Dịch bệnh | Đóng cửa trường, học online; trường tư nhỏ thiếu dòng tiền | Ngay | |
| AI, giáo dục số | Thay đổi mô hình trung tâm truyền thống | Dài | Tin `GT` |
| Đô thị hóa, di cư | Trường ở khu đô thị mới thiếu chỗ; vùng xuất cư thừa chỗ | Dài | |

## 3. Tác động theo đối tượng
### KHCN – cá nhân
- **Thách thức:**
  - phụ huynh vay để đóng học phí, du học khi thu nhập giảm;
  - chi phí du học tăng khi ngoại tệ mạnh;
  - giáo viên trường tư nhỏ mất việc khi trường đóng.
- **Cơ hội:**
  - nhu cầu chuyển tiền du học, tài khoản ngoại tệ, thẻ cho du học sinh;
  - tích lũy giáo dục, bảo hiểm cho con;
  - phụ huynh có thu nhập cao là khách hàng ưu tiên.

### KHCN – hộ kinh doanh
- **Thách thức:** nhóm trẻ, mầm non tư nhỏ thiếu trẻ ở vùng tỷ lệ sinh giảm; lớp học thêm chịu quy định.
- **Cơ hội:** khu đô thị mới thiếu trường; nhận học phí qua QR.

### SME
- **Thách thức:** trung tâm có chi phí thuê mặt bằng cố định, nhạy với quy định và cạnh tranh online; tư vấn du học phụ thuộc chính sách nước ngoài.
- **Cơ hội:** giáo dục số, kỹ năng nghề, đào tạo cho DN; chuyển tiền du học.

### DN lớn
- **Thách thức:** trường tư vay để xây cơ sở, nhạy với số học sinh tuyển được; cạnh tranh.
- **Cơ hội:** trung lưu tăng, nhu cầu chất lượng cao; trường ở khu đô thị mới; thu học phí tập trung.

## 4. Sản phẩm ngân hàng liên quan
| Đối tượng | Phía rủi ro | Phía cơ hội |
|---|---|---|
| KHCN | Vay tiêu dùng `CN-LN-06`, thẻ `CN-CARD-01` để đóng học phí | Chuyển tiền quốc tế `CN-PAY-01`, tài khoản ngoại tệ `CN-ACC-02` (`O3`), tích lũy `CN-DEP-02`, bảo hiểm tích lũy `CN-INS-02` (`O2` `O4`) |
| HKD | ShopCredit `HKD-LN-02` của mầm non tư nhỏ | QR thu học phí `HKD-REV-02`, tài khoản HKD (`O3`) |
| SME | Hybrid `SME-LN-01` của trung tâm | Chuyển tiền đi nước ngoài `SME-PAY-07`, thu học phí (`O3`) |
| DN lớn | Vay đầu tư cơ sở `CIB-LN-02` | Thu hộ học phí `CIB-COL-01`, chi lương `CIB-PAY-06`, tiền gửi theo mùa học phí `CIB-DEP-01` (`O3` `O2`) |
| Cấp ngân hàng | Chuyển tiền du học đi: nhu cầu ngoại tệ (`NH-MR-01`); tuân thủ mục đích chuyển tiền (`NH-CO-01`) | – |

## 5. Tín hiệu theo dõi
- Giá trị chuyển tiền du học theo mùa; số tài khoản ngoại tệ mới.
- `S02` doanh thu QR thu học phí của HKD, SME giáo dục theo địa bàn.
- `S04` thẻ, thấu chi phụ huynh tăng mùa tựu trường.
- `S01` chi lương giáo viên trường tư giảm người.
- Cần truy vấn: dư nợ giáo dục theo loại hình; số khách chuyển tiền du học.

## 6. Liên kết ngành
- **Song song:** `I01` (khu đô thị mới, đất xây trường), `I17` (giáo dục số).
- **Theo dân số:** `I15` (cùng chịu tác động già hóa), `I08` (sữa trẻ em).
- **Theo thu nhập:** việc làm ở mọi ngành.

## 7. Điểm đảo chiều và lưu ý
- Tin tỷ lệ sinh là `GT`: không cảnh báo khẩn, không ước lượng số trường bị ảnh hưởng.
- Chi tiêu giáo dục bị cắt sau cùng; khi phụ huynh bắt đầu cắt học phí, đó là tín hiệu thu nhập đã yếu rõ.
- Chính sách thị thực nước ngoài có thể đổi nhanh; chỉ nêu khi tin nêu.
