---
id: IND-14
code: I14
used_by: [Propagation, Product-Impact, Inside-out Monitor]
steps: [2, 3, 4]
depends_on: [industry/ind_00_index.md]
load_when: Tin về lệ phí trước bạ, thuế nhập khẩu ô tô, xe điện, chính sách hạn chế xe xăng, lãi suất vay mua xe, giá xăng, tiêu dùng nội địa, ưu đãi của hãng xe, giá xe cũ
version: v3.1
updated: 2026-11-03
---

# I14 – Ô tô, xe máy, xe điện, đại lý và sửa chữa

> Kiến thức nền định tính, không chứa số liệu. Mức phơi nhiễm của Techcombank theo ngành cần truy vấn nội bộ.

## 1. Cấu trúc ngành ở Việt Nam
- **Ô tô:**
  - lắp ráp trong nước và xe nhập khẩu (nhiều từ ASEAN và Trung Quốc);
  - xe điện tăng nhanh, có hãng trong nước;
  - ô tô vẫn là tài sản có giá trị lớn với hộ gia đình.
- **Xe máy:** thị trường lớn, gần bão hòa ở đô thị; chính sách hạn chế xe xăng ở nội đô có thể thúc đẩy chuyển sang xe máy điện.
- **Người tham gia:**
  - DN lớn hãng lắp ráp, nhà nhập khẩu, hệ thống đại lý lớn;
  - SME đại lý, showroom xe cũ, garage;
  - HKD tiệm sửa xe, cửa hàng xe máy, phụ tùng, rửa xe;
  - KHCN người vay mua xe (cá nhân và tài xế công nghệ, taxi).
- **Đặc thù:**
  - đại lý cần vốn lưu động lớn để nhập xe, thường qua tài trợ chuỗi do hãng giới thiệu (`L03`);
  - xe là TSBĐ mất giá nhanh;
  - nhu cầu nhạy với lãi suất, lệ phí, chính sách hãng.

## 2. Biến số nhạy cảm
| Biến số | Chiều | Độ trễ | Ghi chú |
|---|---|---|---|
| Lệ phí trước bạ, thuế | Giảm → doanh số tăng mạnh trong thời gian áp dụng | Ngay | Kéo cầu tương lai về hiện tại |
| Lãi suất vay mua xe | Tăng → cầu giảm, áp lực trả nợ | Vài tháng | |
| Chính sách xe điện, hạn chế xe xăng | Thúc đẩy xe điện; xe xăng cũ mất giá; garage truyền thống thiệt | Theo lộ trình | Hai chiều |
| Cuộc đua giảm giá giữa các hãng | Giá xe mới giảm → xe cũ, TSBĐ mất giá | Nhanh | `CL` |
| Giá xăng | Tăng → tài xế công nghệ, taxi bị ép thu nhập; cầu xe điện tăng | Nhanh | |
| Xe nhập giá rẻ | Tăng → cạnh tranh với xe lắp ráp, đại lý tồn kho | Vài tháng | |
| Tiêu dùng nội địa | Yếu → hoãn mua xe | Vài tháng | |
| USD mạnh | Xe nhập, linh kiện đắt hơn | Vài tháng | |

## 3. Tác động theo đối tượng
### KHCN – cá nhân
- **Thách thức:**
  - người vay mua xe chạy dịch vụ chịu rủi ro thu nhập (giá xăng, cạnh tranh, phí nền tảng);
  - xe mất giá nhanh khi hãng giảm giá;
  - người mua xe ở cao điểm ưu đãi có thể vay vượt khả năng.
- **Cơ hội:** ưu đãi lệ phí và lãi suất kéo nhu cầu vay mua xe; chuyển sang xe điện (vay, bảo hiểm).

### KHCN – hộ kinh doanh
- **Thách thức:** garage, tiệm sửa xe xăng giảm việc khi xe điện tăng; cửa hàng xe máy phụ thuộc thu nhập công nhân, nông hộ.
- **Cơ hội:** dịch vụ sửa xe điện, lắp sạc; mùa cao điểm cuối năm.

### SME
- **Thách thức:** đại lý tồn kho khi doanh số giảm hoặc hãng giảm giá; showroom xe cũ chịu xe mất giá.
- **Cơ hội:** mùa ưu đãi, doanh số tăng cần vốn nhập xe; mở đại lý xe điện.

### DN lớn
- **Thách thức:** cạnh tranh xe nhập; chi phí linh kiện nhập; chuyển đổi dây chuyền sang xe điện.
- **Cơ hội:** chính sách ưu đãi sản xuất trong nước; xe điện; đội xe cho DN vận tải, dịch vụ.

## 4. Sản phẩm ngân hàng liên quan
| Đối tượng | Phía rủi ro | Phía cơ hội |
|---|---|---|
| KHCN | Vay mua ô tô `CN-LN-04` (`CR` `CL`) | Vay mua xe mới (`O1`), bảo hiểm ô tô `CN-INS-03` (`O4`) |
| HKD | ShopCash `HKD-LN-01` của garage, cửa hàng xe máy | Vốn mở dịch vụ xe điện (`O1`), SoftPOS (`O3`) |
| SME | Hybrid `SME-LN-01` của đại lý nhỏ, showroom xe cũ | Vốn nhập xe mùa cao điểm (`O1`), thu hộ, thanh toán (`O3`) |
| DN lớn | Tài trợ chuỗi kinh doanh ô tô `CIB-SCF-01`, L/C nhập xe, linh kiện `CIB-TF-01` | Tài trợ đại lý, vay mua ô tô DN `CIB-LN-02`, phái sinh tỷ giá (`O1` `O3`) |
| Cấp ngân hàng | Giá trị TSBĐ là xe giảm theo cuộc đua giá (`CL`) | – |

## 5. Tín hiệu theo dõi
- `S11` đại lý cùng một hãng chậm trả tài trợ chuỗi đồng loạt.
- `S05` người vay mua xe chuyển sang trả tối thiểu thẻ; DPD vay mua xe theo nhóm tài xế dịch vụ.
- Số hồ sơ vay mua xe trước khi hết ưu đãi lệ phí (chiều cơ hội, cẩn trọng `G05`).
- `F03` bán gấp xe để trả nợ.
- Cần truy vấn: dư nợ vay mua ô tô theo loại xe (xăng, điện); dư nợ tài trợ đại lý theo hãng.

## 6. Liên kết ngành
- **Thượng nguồn:** `I02` (thép), `I13` (nhựa), `I04` (điện tử ô tô), nhập khẩu qua `I11`.
- **Song song:** `I12` (xăng, hạ tầng sạc).
- **Khách hàng:** `I11` vận tải, `I10` (xe du lịch).
- **Theo thu nhập:** `I07` (nông hộ mua xe khi được mùa).

## 7. Điểm đảo chiều và lưu ý
- Ưu đãi lệ phí có thời hạn: doanh số tăng mạnh rồi giảm sau khi hết hạn.
- Xe điện là cơ hội cho bên này và thách thức cho bên kia (garage xe xăng, xe cũ).
- Không suy ra giá xe, chính sách của hãng cụ thể nếu tin không nêu.
