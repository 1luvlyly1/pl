---
id: IND-11
code: I11
used_by: [Propagation, Product-Impact, Inside-out Monitor]
steps: [2, 3, 4]
depends_on: [industry/ind_00_index.md]
load_when: Tin về cước container, tuyến hàng hải gián đoạn, xung đột tại eo biển, giá dầu diesel, thuế quan (đẩy hàng trước hạn), sản lượng xuất nhập khẩu, hạ tầng cảng, đường cao tốc, thương mại điện tử, lừa đảo mạo danh giao hàng
version: v3.1
updated: 2026-11-03
---

# I11 – Logistics, vận tải và cảng

> Kiến thức nền định tính, không chứa số liệu. Mức phơi nhiễm của Techcombank theo ngành cần truy vấn nội bộ.

## 1. Cấu trúc ngành ở Việt Nam
- **Các mảng:**
  - **vận tải biển** (phần lớn hàng xuất khẩu do hãng tàu nước ngoài chở);
  - **cảng** (các cụm cảng nước sâu phía Bắc và phía Nam);
  - **vận tải đường bộ**, **kho bãi**, **giao nhận** (forwarder);
  - **vận tải hàng không**, **giao hàng chặng cuối** cho TMĐT;
  - **đường sắt, đường thủy nội địa** (tỷ trọng nhỏ).
- **Người tham gia:**
  - DN lớn khai thác cảng, kho, giao hàng;
  - SME là forwarder, vận tải container, kho lạnh;
  - HKD là chủ xe tải, đầu kéo, xe ba gác, shipper;
  - KHCN là tài xế, shipper (thu nhập theo chuyến, nhiều người vay mua xe).
- **Đặc thù:**
  - doanh thu theo khối lượng hàng xuất nhập khẩu và TMĐT;
  - chi phí nhiên liệu chiếm tỷ trọng cao;
  - forwarder có thể lợi khi cước cao (biên trên cước) nhưng cũng chịu rủi ro thanh toán từ khách;
  - chi phí logistics trong nước còn cao.
- **Vùng:** các hành lang cảng – KCN phía Bắc, Đông Nam Bộ; cửa khẩu biên giới phía Bắc.

## 2. Biến số nhạy cảm
| Biến số | Chiều | Độ trễ | Ghi chú |
|---|---|---|---|
| Cước container quốc tế | Tăng → chủ hàng xuất khẩu thiệt; forwarder, hãng tàu có biên cao hơn | Vài tuần | Hai chiều trong cùng ngành |
| Tuyến hàng hải bị gián đoạn (xung đột, eo biển) | Tàu đi vòng, thời gian dài, cước tăng, thiếu container rỗng | Vài tuần | Xem `ex_NW_01_xung_dot_trung_dong.md` |
| Giá dầu diesel | Tăng → chủ xe tải, HKD vận tải bị ép biên | Ngay | Giá cước nội địa điều chỉnh chậm |
| Khối lượng xuất nhập khẩu | Giảm do thuế quan, đơn hàng → kho, cảng giảm công suất | Một quý | Pha đẩy hàng trước hạn tạo đỉnh tạm thời |
| Đầu tư hạ tầng (cao tốc, cảng) | Tăng → giảm chi phí, mở tuyến mới | Dài | |
| TMĐT | Tăng → giao hàng chặng cuối tăng | Nhanh | `I09` |
| Biên mậu Trung Quốc | Đóng, siết → ùn xe ở cửa khẩu | Ngay | Chạm `I07` |
| Bão lũ | Gián đoạn tuyến, cảng đóng | Ngay | |

## 3. Tác động theo đối tượng
### KHCN – cá nhân
- **Thách thức:**
  - tài xế, shipper vay mua xe chịu áp lực khi giá dầu tăng hoặc ít chuyến;
  - shipper là đối tượng bị mạo danh trong lừa đảo, và người dân bị lừa qua tin nhắn giả đơn vị giao hàng.
- **Cơ hội:** TMĐT tăng kéo theo thu nhập shipper tăng; tuyển dụng tài xế cho tuyến mới.

### KHCN – hộ kinh doanh
- **Thách thức:** chủ xe tải nhỏ có biên mỏng, vay mua xe, giá dầu tăng là thiệt ngay.
- **Cơ hội:** đầu tư công, KCN mới làm tăng nhu cầu chở vật liệu, hàng hóa.

### SME
- **Thách thức:**
  - forwarder ứng cước cho khách, bị chậm thu;
  - vận tải container chịu giá dầu;
  - bị email giả đổi tài khoản thanh toán.
- **Cơ hội:** cước cao làm doanh thu forwarder tăng; kho lạnh cho nông sản, thủy sản; vốn mua xe, đầu kéo mới.

### DN lớn
- **Thách thức:** cảng giảm công suất khi xuất nhập khẩu giảm; đầu tư hạ tầng vay dài hạn, chịu lãi suất.
- **Cơ hội:** FDI và thương mại tăng; trung tâm logistics mới; vay dự án hạ tầng.

## 4. Sản phẩm ngân hàng liên quan
| Đối tượng | Phía rủi ro | Phía cơ hội |
|---|---|---|
| KHCN | Vay mua ô tô `CN-LN-04`, vay tiêu dùng `CN-LN-06` của tài xế, shipper; `FR` mạo danh giao hàng | Thẻ, tài khoản (`O3`), bảo hiểm (`O4`) |
| HKD | ShopCredit `HKD-LN-02` của chủ xe tải | Vốn mua xe, vốn lưu động (`O1`), QR (`O3`) |
| SME | Hybrid `SME-LN-01`, thẻ DN `SME-PAY-02` trả nhiên liệu | Vốn lưu động (`O1`), chuyển tiền quốc tế `SME-PAY-07`, ngoại tệ `SME-PAY-04` (`O3`) |
| DN lớn | Vay dự án `CIB-LN-02`, vốn lưu động `CIB-LN-01` | Tài trợ vận chuyển hàng không `CIB-SCF-01`, bảo lãnh `CIB-TF-04`, thu hộ `CIB-COL-01` (`O1` `O3`) |
| Cấp ngân hàng | `FR` tin nhắn mạo danh giao hàng (`X08`) | – |

## 5. Tín hiệu theo dõi
- `S10` hóa đơn cảng, phí hạ tầng cảng biển của khách xuất nhập khẩu.
- `S04` hạn mức của HKD vận tải tăng khi giá dầu tăng.
- Giá trị chuyển tiền quốc tế trả cước tăng (chiều cơ hội cho forwarder).
- `X04` đổi tài khoản thụ hưởng trước kỳ thanh toán; `X08` tin nhắn mạo danh giao hàng.
- Cần truy vấn: dư nợ vận tải theo loại hình; số khoản vay mua xe tải.

## 6. Liên kết ngành
- **Đầu vào:** `I12` nhiên liệu.
- **Khách hàng của ngành:** `I03` `I04` `I05` `I06` `I07` xuất khẩu, `I09` TMĐT.
- **Song song:** `I02` hạ tầng, `I14` xe tải và đầu kéo.

## 7. Điểm đảo chiều và lưu ý
- Cước cao là cơ hội cho forwarder nhưng thường ngắn; khi cước giảm nhanh, ai ký thuê tàu, container giá cao sẽ lỗ.
- Tin xung đột hàng hải tác động qua ba kênh cùng lúc: cước, thời gian giao hàng, giá dầu – nêu cả ba.
- Với tin `GL` mạo danh giao hàng, chỉ mô tả ở mức nhận diện.
