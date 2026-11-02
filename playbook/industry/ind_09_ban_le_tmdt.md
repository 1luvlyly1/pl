---
id: IND-09
code: I09
used_by: [Propagation, Product-Impact, Inside-out Monitor]
steps: [2, 3, 4]
depends_on: [industry/ind_00_index.md, segments/seg_01b_KHCN_ho_kinh_doanh.md]
load_when: Tin về tiêu dùng nội địa, lạm phát, thuế và hóa đơn với hộ kinh doanh, thương mại điện tử, hàng nhập giá rẻ xuyên biên giới, lừa đảo mua sắm online, mùa lễ Tết, thu nhập công nhân
version: v3.1
updated: 2026-11-03
---

# I09 – Bán lẻ và thương mại điện tử

> Kiến thức nền định tính, không chứa số liệu. Mức phơi nhiễm của Techcombank theo ngành cần truy vấn nội bộ.

## 1. Cấu trúc ngành ở Việt Nam
- **Ba kênh:**
  - **truyền thống** (chợ, tạp hóa, cửa hàng nhỏ) vẫn chiếm phần lớn, chủ yếu là HKD;
  - **hiện đại** (chuỗi siêu thị, cửa hàng tiện lợi, điện máy, dược phẩm, thời trang) do DN lớn vận hành;
  - **thương mại điện tử** và bán qua mạng xã hội, livestream, với rất nhiều người bán nhỏ (HKD, cá nhân).
- **Người tham gia:**
  - DN lớn chuỗi bán lẻ;
  - SME cửa hàng, nhà phân phối, người bán online có quy mô;
  - HKD tạp hóa, sạp chợ, người bán online;
  - KHCN là người tiêu dùng (đầu ra của ngành).
- **Thanh toán:** chuyển dịch nhanh sang QR, thẻ, ví; dòng tiền QR của HKD là dữ liệu rất giá trị cho ngân hàng.
- **Đặc thù:**
  - nhạy với thu nhập và niềm tin tiêu dùng;
  - chính sách thuế với HKD (chuyển sang kê khai, hóa đơn điện tử) và với người bán online đang thay đổi;
  - hàng nhập giá rẻ qua sàn xuyên biên giới cạnh tranh với người bán trong nước.
- **Mùa vụ:** Tết, các dịp khuyến mãi lớn cuối năm, mùa tựu trường.

## 2. Biến số nhạy cảm
| Biến số | Chiều | Độ trễ | Ghi chú |
|---|---|---|---|
| Thu nhập, việc làm, niềm tin tiêu dùng | Yếu → doanh thu giảm, HKD chịu trước | Một đến hai tháng | `L06` |
| Lạm phát, giá xăng | Tăng → chi tiêu chuyển sang hàng thiết yếu | Vài tuần | |
| Chính sách thuế, hóa đơn HKD | Siết → chi phí tuân thủ, một số hộ ngừng hoặc chuyển dòng tiền | Theo hiệu lực | Có thể kéo `S16`; cơ hội chuyển lên DN (`L07`) |
| Thuế, quản lý người bán trên sàn | Siết → người bán nhỏ rời sàn hoặc chuyển kênh | Theo hiệu lực | |
| Hàng nhập giá rẻ xuyên biên giới | Tăng → người bán, nhà sản xuất nội địa mất khách | Nhanh | |
| Khách du lịch | Tăng → bán lẻ khu du lịch, trung tâm thương mại | Theo mùa | `I10` |
| Lãi suất, tín dụng tiêu dùng | Thấp → mua trả góp điện máy, điện thoại tăng | Vài tháng | |
| Lừa đảo mua sắm online | Tăng → mất niềm tin, tranh chấp | Nhanh | Tin `GL` |

## 3. Tác động theo đối tượng
### KHCN – cá nhân
- **Thách thức:**
  - người mua online bị lừa đảo, hàng giả;
  - chi tiêu thẻ, trả góp vượt khả năng ở mùa mua sắm;
  - người bán online cá nhân chịu chi phí thuế, phí sàn tăng.
- **Cơ hội:** ưu đãi thẻ, hoàn tiền mùa mua sắm; thu nhập phụ từ bán online.

### KHCN – hộ kinh doanh
- **Thách thức:**
  - doanh thu giảm khi tiêu dùng yếu, mất khách vào chuỗi và sàn;
  - chi phí tuân thủ thuế, hóa đơn;
  - tài khoản người bán bị chiếm đoạt.
- **Cơ hội:**
  - số hóa (QR, phần mềm bán hàng), dòng tiền minh bạch để vay theo doanh thu;
  - chuyển đổi lên DN;
  - mùa Tết cần vốn nhập hàng.

### SME
- **Thách thức:** tồn kho khi tiêu dùng yếu; cạnh tranh giá với hàng nhập; phí sàn tăng.
- **Cơ hội:** mở cửa hàng, kênh online đa sàn; vốn lưu động mùa cao điểm; nhận thanh toán đa kênh.

### DN lớn
- **Thách thức:** cạnh tranh giá, chi phí thuê mặt bằng, biên mỏng.
- **Cơ hội:** chiếm thị phần từ kênh truyền thống; mở rộng chuỗi ở tỉnh; chi lương, thu hộ lớn.

## 4. Sản phẩm ngân hàng liên quan
| Đối tượng | Phía rủi ro | Phía cơ hội |
|---|---|---|
| KHCN | Thẻ tín dụng `CN-CARD-01`, trả góp `CN-LN-06`, MyCash `CN-LN-05`; `FR` mua sắm online | Chi tiêu thẻ (`O3`), ưu đãi OneU `CN-LOY-01` |
| HKD | ShopCash `HKD-LN-01`, doanh thu QR `HKD-REV-01` `HKD-REV-02` giảm | Vay theo dòng tiền (`O1`), Soundbox, SoftPOS `HKD-REV-03`, tài khoản HKD `HKD-ACC-01` (`O3` `O6`) |
| SME | Hybrid `SME-LN-01`, Misa Lending `SME-LN-02` | MerchantOne `SME-PKG-02`, SoftPOS `SME-REV-01` (`O3`), vốn mùa Tết (`O1`) |
| DN lớn | Vốn lưu động `CIB-LN-01` | Thu hộ `CIB-COL-01`, chi lương `CIB-PAY-06`, thẻ DN (`O3` `O2`) |
| Cấp ngân hàng | `BR` phí QR, thẻ giảm; `FR` tài khoản trung gian | – |

## 5. Tín hiệu theo dõi
- `S02` doanh thu QR, POS theo MCC và địa bàn; `S03` số người trả tiền giảm.
- `S16` doanh thu HKD chảy về tài khoản cá nhân sau thay đổi chính sách thuế.
- `S04` `S05` thẻ, thấu chi cá nhân sau mùa mua sắm.
- `X01` tài khoản mới nhận tiền nhiều nguồn rồi chuyển đi; `X02` báo lừa đảo mua sắm.
- Cần truy vấn: số HKD bán lẻ theo MCC, xu hướng doanh thu QR theo quý.

## 6. Liên kết ngành
- **Thượng nguồn:** `I08` (FMCG), `I03` (thời trang), `I04` (điện máy, điện thoại).
- **Song song:** `I11` (giao hàng chặng cuối), `I10` (bán lẻ du lịch), `I17` (nền tảng).
- **Đầu vào thu nhập:** việc làm ở `I03` `I04` (khu công nhân).

## 7. Điểm đảo chiều và lưu ý
- HKD là nơi tác động tiêu dùng hiện ra sớm nhất trong dữ liệu ngân hàng (QR theo ngày).
- Thay đổi thuế có thể làm doanh thu QR giảm mà không phải do tiêu dùng yếu – phân biệt bằng `S16`.
- Không mô tả thủ đoạn lừa đảo chi tiết (`guardrails.md` quy tắc 15).
