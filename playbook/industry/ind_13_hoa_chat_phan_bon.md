---
id: IND-13
code: I13
used_by: [Propagation, Product-Impact, Inside-out Monitor]
steps: [2, 3, 4]
depends_on: [industry/ind_00_index.md]
load_when: Tin về giá urê, DAP, kali, giá khí, than, hạt nhựa, hóa chất cơ bản; thuế VAT phân bón; xuất khẩu phân bón của Trung Quốc; CBAM; mùa vụ nông nghiệp; giá dầu
version: v3.1
updated: 2026-11-03
---

# I13 – Hóa chất, phân bón, nhựa và bao bì

> Kiến thức nền định tính, không chứa số liệu. Mức phơi nhiễm của Techcombank theo ngành cần truy vấn nội bộ.

## 1. Cấu trúc ngành ở Việt Nam
- **Phân bón:**
  - urê sản xuất trong nước từ khí và than, đủ dùng và có xuất khẩu;
  - DAP, lân sản xuất một phần trong nước;
  - kali chủ yếu nhập khẩu;
  - NPK pha trộn có rất nhiều nhà sản xuất.
- **Hóa chất:** hóa chất cơ bản (xút, axit, phốt pho vàng) và hóa chất chuyên dùng; nhiều nguyên liệu nhập khẩu.
- **Nhựa, bao bì:**
  - hạt nhựa phần lớn nhập khẩu (giá theo dầu);
  - sản phẩm nhựa gồm bao bì, ống, nhựa gia dụng, linh kiện;
  - có xuất khẩu bao bì, túi nhựa.
- **Người tham gia:**
  - DN lớn sản xuất phân bón, hóa chất, nhựa;
  - SME xưởng nhựa, in bao bì, nhà phân phối vật tư;
  - HKD đại lý phân bón, thuốc bảo vệ thực vật ở nông thôn (bán chịu theo vụ);
  - KHCN nông hộ là người mua cuối.
- **Đặc thù:**
  - phân bón theo mùa vụ, giá theo thế giới;
  - đại lý phân bón là kênh tín dụng không chính thức cho nông hộ;
  - nhựa nhạy với giá dầu và quy định môi trường.

## 2. Biến số nhạy cảm
| Biến số | Chiều | Độ trễ | Ghi chú |
|---|---|---|---|
| Giá khí, than | Tăng → chi phí sản xuất urê | Nhanh | Giá bán urê theo thế giới nên biên có thể giữ |
| Giá phân bón thế giới; chính sách xuất khẩu của nước lớn | Tăng → nhà sản xuất trong nước lợi; nông hộ thiệt | Vài tuần | Đại lý trữ hàng lợi trên tồn kho |
| Thuế VAT với phân bón | Thay đổi → giá bán, khấu trừ đầu vào của nhà sản xuất | Theo hiệu lực | |
| Giá dầu, hạt nhựa | Tăng → chi phí ngành nhựa | Vài tuần | Ngành nhựa khó chuyển giá ngay |
| USD mạnh | Nhập hạt nhựa, kali, hóa chất đắt hơn | Ngay | |
| Mùa vụ lúa, cà phê, cây ăn trái | Cao điểm → cầu phân bón tăng | Theo mùa | Xem `I07` |
| CBAM của EU | Phân bón xuất sang EU chịu chi phí phát thải | Theo lộ trình | |
| Quy định nhựa dùng một lần, trách nhiệm tái chế | Siết → chi phí; cơ hội cho bao bì thay thế | Dài | Tin `GT` |
| Sự cố hóa chất, cháy nổ | Dừng sản xuất, trách nhiệm pháp lý | Ngay | |

## 3. Tác động theo đối tượng
### KHCN – cá nhân
- **Thách thức:** nông hộ chịu giá phân bón tăng, lợi nhuận vụ giảm; công nhân xưởng nhựa giảm ca khi đơn bao bì xuất khẩu giảm.
- **Cơ hội:** giá phân bón giảm làm chi phí nông hộ giảm, thu nhập vụ tăng.

### KHCN – hộ kinh doanh
- **Thách thức:**
  - đại lý phân bón bán chịu cho nông hộ, bị nợ đọng khi mất mùa hoặc giá nông sản giảm;
  - trữ hàng ở giá cao rồi giá giảm thì lỗ.
- **Cơ hội:** đầu vụ cần vốn nhập hàng; doanh thu tăng khi giá nông sản tốt.

### SME
- **Thách thức:** xưởng nhựa bị ép biên khi hạt nhựa tăng; phụ thuộc đơn bao bì của DN FMCG, xuất khẩu.
- **Cơ hội:** bao bì thân thiện môi trường; thay thế hàng nhập; tài trợ nhập nguyên liệu.

### DN lớn
- **Thách thức:** chi phí khí, than; cạnh tranh hàng nhập; chi phí môi trường.
- **Cơ hội:** giá phân bón thế giới tăng, xuất khẩu; đầu tư hóa chất chuyên dùng, phân bón công nghệ cao.

## 4. Sản phẩm ngân hàng liên quan
| Đối tượng | Phía rủi ro | Phía cơ hội |
|---|---|---|
| KHCN | Vay tiêu dùng `CN-LN-06` của nông hộ | Tiền gửi sau vụ (`O2`) |
| HKD | ShopCash `HKD-LN-01`, ShopCredit `HKD-LN-02` của đại lý vật tư | Vốn nhập hàng đầu vụ (`O1`), QR, CDM (`O3`) |
| SME | Hybrid `SME-LN-01`, ngoại tệ `SME-PAY-04` | Vốn nhập hạt nhựa (`O1`), thanh toán quốc tế `SME-PAY-07` (`O3`) |
| DN lớn | L/C nhập nguyên liệu `CIB-TF-01`, FX `CIB-FX-01`, vay dự án `CIB-LN-02` | Tài trợ xuất khẩu `CIB-TF-02`, tài trợ chuỗi đại lý `CIB-TF-03`, phái sinh `CIB-CM-02` (`O1` `O3`) |
| Cấp ngân hàng | Rủi ro môi trường, sự cố của khách (`RP`) | – |

## 5. Tín hiệu theo dõi
- `S04` ShopCash đại lý vật tư nông nghiệp tăng giữa vụ; `S02` doanh thu QR đại lý theo tỉnh.
- `G05` đại lý xin tăng hạn mức để trữ hàng khi giá tăng.
- `S10` hóa đơn điện của nhà máy hóa chất, nhựa.
- Nhu cầu L/C nhập hạt nhựa, kali theo quý.
- Cần truy vấn: dư nợ đại lý vật tư nông nghiệp theo tỉnh; dư nợ ngành nhựa.

## 6. Liên kết ngành
- **Thượng nguồn:** `I12` (khí, than, dầu).
- **Hạ nguồn:** `I07` (nông hộ), `I08` (bao bì thực phẩm), `I09` (bao bì bán lẻ), `I03` (xơ sợi tổng hợp), `I02` (ống nhựa, sơn).

## 7. Điểm đảo chiều và lưu ý
- Giá phân bón cao làm nhà sản xuất lợi nhưng nông hộ thiệt – cùng một tin, hai nhóm khách.
- Đại lý trữ hàng chờ giá là ô B (tham lam); giá phân bón đảo chiều nhanh khi nước xuất khẩu lớn mở lại.
- Sự cố hóa chất: không suy đoán nguyên nhân hay trách nhiệm nếu tin không nêu.
