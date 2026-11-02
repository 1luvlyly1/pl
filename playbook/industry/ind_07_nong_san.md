---
id: IND-07
code: I07
used_by: [Propagation, Product-Impact, Inside-out Monitor]
steps: [2, 3, 4]
depends_on: [industry/ind_00_index.md, examples/ex_FG_01_ca_phe_o_B.md]
load_when: Tin về giá cà phê, gạo, tiêu, điều, cao su, sầu riêng và trái cây; chính sách xuất khẩu gạo của các nước; quy định chống phá rừng EU; thời tiết, El Niño, hạn mặn; biên mậu Trung Quốc; giá phân bón
version: v3.1
updated: 2026-11-03
---

# I07 – Nông sản (cà phê, gạo, tiêu, điều, cao su, trái cây)

> Kiến thức nền định tính, không chứa số liệu. Mức phơi nhiễm của Techcombank theo ngành cần truy vấn nội bộ.

## 1. Cấu trúc ngành ở Việt Nam
- **Chuỗi giá trị:** nông hộ → thương lái, đại lý thu mua (nhiều là HKD) → DN chế biến, xuất khẩu → người mua nước ngoài.
- **Theo mặt hàng:**
  - cà phê (chủ yếu robusta), tiêu: Tây Nguyên, Đông Nam Bộ;
  - gạo: đồng bằng sông Cửu Long, xuất sang các nước châu Á và châu Phi;
  - điều: chế biến ở Đông Nam Bộ, phụ thuộc điều thô nhập khẩu;
  - cao su: Đông Nam Bộ, Tây Nguyên;
  - trái cây (sầu riêng và các loại khác): Tây Nguyên, đồng bằng sông Cửu Long, xuất mạnh sang Trung Quốc.
- **Người tham gia:**
  - DN lớn xuất khẩu và chế biến sâu (cà phê rang xay, hòa tan);
  - SME thu mua, sơ chế, kho lạnh;
  - HKD đại lý, vựa, cửa hàng vật tư nông nghiệp;
  - KHCN nông hộ – thu nhập theo mùa vụ, thường giữ tiền mặt và vàng.
- **Đặc thù:**
  - giá do thị trường thế giới quyết định;
  - đại lý và DN giữ hàng tồn nên có lợi khi giá tăng nhưng cần nhiều vốn lưu động;
  - DN đã ký hợp đồng bán giá cố định có thể lỗ khi giá tăng vọt;
  - đầu cơ trữ hàng phổ biến ở pha Greed.
- **Mùa vụ:** mỗi mặt hàng có mùa thu hoạch riêng; tiền về sau thu hoạch là cơ hội huy động.

## 2. Biến số nhạy cảm
| Biến số | Chiều | Độ trễ | Ghi chú |
|---|---|---|---|
| Giá thế giới từng mặt hàng | Tăng → nông hộ, người giữ hàng lợi; DN bán giá cố định thiệt | Ngay với hàng tồn, một vụ với nông hộ | Xem `ex_FG_01_ca_phe_o_B.md` |
| Thời tiết ở nước sản xuất khác | Mất mùa ở nước khác → giá tăng | Vài tuần | |
| Thời tiết trong nước: El Niño, hạn mặn, bão | Mất mùa, chi phí tưới | Theo mùa | Ghi rõ vùng |
| Chính sách xuất khẩu gạo của các nước | Nước khác hạn chế xuất → giá gạo Việt Nam tăng | Nhanh | Đảo chiều khi họ mở lại |
| Biên mậu, kiểm dịch Trung Quốc | Siết → ùn xe ở cửa khẩu, trái cây hỏng | Ngay | |
| Quy định chống phá rừng EU | Chi phí truy xuất vườn cà phê, cao su | Theo lộ trình | Nông hộ nhỏ khó đáp ứng |
| Giá phân bón | Tăng → chi phí nông hộ | Vụ sau | Xem `I13` |
| USD mạnh | Doanh thu quy đổi tăng | Ngay | |
| Giá điều thô nhập khẩu | Tăng → ép biên DN chế biến điều | Vài tuần | |

## 3. Tác động theo đối tượng
### KHCN – cá nhân
- **Thách thức:**
  - mất mùa, giá giảm sau khi đầu tư mở rộng vườn;
  - nông hộ vay mở rộng ở giá đỉnh (Greed) chịu lỗ khi giá đảo chiều;
  - nhiều nông hộ bị nhắm bởi lừa đảo khi tiền về sau vụ.
- **Cơ hội:**
  - giá cao kéo theo thu nhập tăng mạnh, tiền gửi, mua nhà, xe, bảo hiểm;
  - chuyển đổi cây trồng giá trị cao.

### KHCN – hộ kinh doanh
- **Thách thức:**
  - đại lý trữ hàng chờ giá chịu lỗ khi giá giảm đột ngột;
  - cửa hàng vật tư bán chịu bị nợ đọng khi mất mùa.
- **Cơ hội:** mùa giá cao cần vốn thu mua lớn; doanh thu dịch vụ, bán lẻ ở vùng trồng tăng theo thu nhập nông hộ (`L06`).

### SME
- **Thách thức:** thu mua bằng vốn vay ngắn hạn; giá biến động nhanh, rủi ro hợp đồng giao sau.
- **Cơ hội:** kho lạnh, sơ chế trái cây đạt chuẩn xuất khẩu; vốn lưu động mùa vụ.

### DN lớn
- **Thách thức:**
  - hợp đồng bán giá cố định khi giá tăng vọt;
  - nông hộ bán cho bên khác (bẻ kèo);
  - chi phí truy xuất nguồn gốc.
- **Cơ hội:**
  - giá cao, USD mạnh;
  - chế biến sâu;
  - liên kết vùng trồng có truy xuất (tài trợ chuỗi).

## 4. Sản phẩm ngân hàng liên quan
| Đối tượng | Phía rủi ro | Phía cơ hội |
|---|---|---|
| KHCN | Vay tiêu dùng `CN-LN-06`, vay mua ô tô `CN-LN-04` ở giá đỉnh; `FR` với tiền về sau vụ | Tiền gửi `CN-DEP-01` `CN-DEP-04` (`O2`), bảo hiểm (`O4`), vay mua nhà (`O1`) |
| HKD | ShopCash `HKD-LN-01`, ShopCredit `HKD-LN-02` của đại lý trữ hàng | Vốn thu mua (`O1`), CDM `HKD-SVC-01`, QR (`O3`), tiền gửi HKD (`O2`) |
| SME | Hybrid `SME-LN-01` | Vốn lưu động, ngoại tệ `SME-PAY-04` (`O1` `O3`) |
| DN lớn | Vốn lưu động `CIB-LN-01`, hàng tồn làm TSBĐ (`CL`) | Tài trợ xuất khẩu `CIB-TF-02`, phái sinh tỷ giá `CIB-CM-02`, tài trợ chuỗi `CIB-TF-03` (`O1` `O3`) |
| Cấp ngân hàng | Rút tiền mặt mùa thu mua (`NH-LQ-02`) | Huy động sau vụ |

## 5. Tín hiệu theo dõi
- `G05` đại lý xin tăng hạn mức theo doanh thu ở giá đỉnh.
- `G01` tiền vay chuyển sang mua đất, mở rộng vườn.
- `S07` rút tiền mặt mùa thu mua theo tỉnh.
- Tiền gửi mới sau thu hoạch theo tỉnh (chiều cơ hội).
- `X02` báo lừa đảo theo vùng trồng sau vụ.
- Cần truy vấn: dư nợ theo mặt hàng và tỉnh; tỷ trọng hàng tồn làm TSBĐ.

## 6. Liên kết ngành
- **Thượng nguồn:** `I13` (phân bón, thuốc bảo vệ thực vật).
- **Song song:** `I11` (vận tải biển, đường bộ ra cửa khẩu).
- **Hạ nguồn:** `I08` (chế biến, đồ uống: cà phê rang xay là bên dùng đầu vào).
- **Theo thu nhập:** `I14` (xe), `I01` (đất vùng trồng), `I18` (vàng của nông hộ).

## 7. Điểm đảo chiều và lưu ý
- Giá đỉnh kéo mở rộng diện tích → vài năm sau dư cung (cây lâu năm có độ trễ dài).
- Nông hộ và đại lý thường là ô B khi giá tăng nóng (tham lam, cơ bản tốt) – nêu cả rủi ro đầu cơ.
- Tin giá của một mặt hàng không chạm đều mọi vùng; chỉ nêu vùng trồng chính của mặt hàng đó.
