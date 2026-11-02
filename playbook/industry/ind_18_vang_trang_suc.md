---
id: IND-18
code: I18
used_by: [Propagation, Product-Impact, Inside-out Monitor]
steps: [2, 3, 4]
depends_on: [industry/ind_00_index.md, bank/ngan_hang.md]
load_when: Tin về giá vàng thế giới và trong nước, chênh lệch giá vàng, chính sách quản lý vàng miếng, nhập khẩu vàng, xung đột địa chính trị, lạm phát, USD, ngày Vía Thần Tài, mùa cưới, quy định chống rửa tiền
version: v3.1
updated: 2026-11-03
---

# I18 – Vàng bạc và trang sức

> Kiến thức nền định tính, không chứa số liệu. Mức phơi nhiễm của Techcombank theo ngành cần truy vấn nội bộ.

## 1. Cấu trúc ngành ở Việt Nam
- **Các mảng:**
  - **vàng miếng** (sản xuất và nhập khẩu do Nhà nước quản lý chặt, chính sách đang được điều chỉnh);
  - **vàng nhẫn, vàng trang sức** (nhiều DN và tiệm vàng);
  - **bạc**, **đá quý**.
- **Người tham gia:**
  - DN lớn kinh doanh vàng bạc đá quý có hệ thống cửa hàng;
  - SME xưởng chế tác, cửa hàng;
  - HKD **tiệm vàng** ở mọi địa phương (vừa bán lẻ, vừa thu mua, nhiều giao dịch tiền mặt);
  - KHCN là người giữ vàng – một kênh tích trữ truyền thống của hộ gia đình, đặc biệt ở nông thôn.
- **Đặc thù:**
  - giá trong nước có thể chênh so với thế giới do quản lý nguồn cung;
  - tâm lý đám đông mạnh (xếp hàng mua khi giá tăng nóng);
  - vàng là đối thủ trực tiếp của tiền gửi ngân hàng;
  - giao dịch tiền mặt lớn là điểm nhạy về chống rửa tiền.
- **Mùa vụ:** ngày Vía Thần Tài, mùa cưới cuối năm, trước Tết.

## 2. Biến số nhạy cảm
| Biến số | Chiều | Độ trễ | Ghi chú |
|---|---|---|---|
| Giá vàng thế giới | Tăng → người giữ vàng lợi; người mua đổ xô (Greed); trang sức sức mua giảm | Ngay | Xem `news/nw_01_truc_tiep.md` mục 2.1 |
| Xung đột địa chính trị, lạm phát | Tăng → cầu vàng trú ẩn | Ngay | |
| Chênh lệch giá trong nước và thế giới | Rộng → áp lực buôn lậu, chính sách can thiệp | Nhanh | |
| Chính sách quản lý vàng miếng, nhập khẩu | Nới → nguồn cung tăng, chênh lệch thu hẹp | Theo quyết định | Không suy đoán chính sách nếu tin không nêu |
| USD, lãi suất | USD mạnh, lãi suất cao thường kìm giá vàng | Vài tuần | Không phải luôn đúng |
| Lãi suất tiền gửi trong nước | Thấp → tiền chuyển sang vàng | Vài tuần | Chạm `NH-LQ-01` |
| Quy định chống rửa tiền, hóa đơn bán vàng | Siết → tiệm vàng chịu chi phí tuân thủ | Theo hiệu lực | |

## 3. Tác động theo đối tượng
### KHCN – cá nhân
- **Thách thức:**
  - người mua ở đỉnh, nhất là bằng tiền vay hoặc tất toán tiết kiệm, chịu lỗ khi giá quay đầu;
  - lừa đảo đầu tư vàng online, sàn vàng không phép;
  - mua vàng không hóa đơn khó bán lại.
- **Cơ hội:** người giữ vàng chốt lời có tiền gửi lại ngân hàng, đầu tư, mua nhà (`O2` `O4`).

### KHCN – hộ kinh doanh
- **Thách thức:**
  - tiệm vàng cần vốn lớn cho hàng tồn khi giá tăng;
  - rủi ro cướp, vàng giả;
  - chi phí tuân thủ hóa đơn, chống rửa tiền;
  - doanh thu trang sức giảm khi giá quá cao.
- **Cơ hội:** doanh thu mua bán tăng mạnh mùa sốt giá; nhận thanh toán số thay tiền mặt.

### SME
- **Thách thức:** xưởng chế tác chịu giá nguyên liệu biến động; tồn kho trang sức bán chậm.
- **Cơ hội:** trang sức thiết kế, giá trị gia tăng; xuất khẩu trang sức.

### DN lớn
- **Thách thức:** chịu chính sách quản lý; tồn kho lớn khi giá giảm nhanh.
- **Cơ hội:** nguồn cung vàng miếng mở rộng nếu chính sách nới; mở rộng chuỗi; thu hộ, thanh toán tiền mặt lớn.

## 4. Sản phẩm ngân hàng liên quan
| Đối tượng | Phía rủi ro | Phía cơ hội |
|---|---|---|
| KHCN | Tất toán `CN-DEP-01` để mua vàng (`G02`), vay tiêu dùng `CN-LN-06` mua vàng (`G01`), rút qua CDM `CN-PAY-02`; `FR` sàn vàng không phép (`G07`) | Tiền gửi từ khách chốt lời (`O2`), đầu tư, bảo hiểm (`O4`) |
| HKD | ShopCredit `HKD-LN-02` của tiệm vàng; tiền mặt lớn | CDM `HKD-SVC-01`, QR, SoftPOS (`O3`), tiền gửi HKD (`O2`) |
| SME | Hybrid `SME-LN-01` của xưởng chế tác | Thanh toán, thu hộ (`O3`) |
| DN lớn | Vốn lưu động `CIB-LN-01`, hàng tồn làm TSBĐ (`CL`), nhập khẩu vàng `CIB-TF-01` | Thu hộ tiền mặt `CIB-COL-01`, chi lương (`O3` `O2`) |
| Cấp ngân hàng | Huy động giảm (`NH-LQ-01`), tiền mặt (`NH-LQ-02`), tỷ giá (`NH-MR-01`), giao dịch tiền mặt lớn (`NH-CO-01`) | – |

## 5. Tín hiệu theo dõi
- `G02` tất toán tiết kiệm sau đó rút tiền mặt hoặc chuyển cho tiệm vàng.
- `S07` rút tiền mặt CDM tăng cùng lúc giá vàng tăng.
- `G01` tiền vay tiêu dùng chuyển cho bên bán vàng.
- `S16` doanh thu tiệm vàng chảy về tài khoản cá nhân.
- `X01` tài khoản nhận tiền nhiều nguồn ghi nội dung đầu tư vàng.
- Cần truy vấn: dòng tiền chuyển đến tài khoản tiệm vàng, DN vàng theo tuần.

## 6. Liên kết ngành
- **Song song:** `I07` (nông hộ giữ vàng sau vụ), `I10` (khách du lịch mua trang sức).
- **Cấp ngân hàng:** `bank/ngan_hang.md` (huy động, tỷ giá).
- **Đối thủ của dòng tiền:** chứng khoán, BĐS (`I01`) trong pha Greed.

## 7. Điểm đảo chiều và lưu ý
- Pha xếp hàng mua vàng là Greed điển hình; điểm đảo chiều là khi giá quay đầu hoặc chênh lệch thu hẹp đột ngột do chính sách.
- Khi giá vàng giảm mạnh, có thể có dòng tiền quay lại tiền gửi (cơ hội), nhưng người mua ở đỉnh bằng tiền vay gặp khó.
- Không đưa ra dự báo giá vàng; không khuyến nghị mua bán vàng.
