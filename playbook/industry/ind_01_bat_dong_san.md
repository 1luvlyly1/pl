---
id: IND-01
code: I01
used_by: [Propagation, Product-Impact, Inside-out Monitor]
steps: [2, 3, 4]
depends_on: [industry/ind_00_index.md]
load_when: Tin về lãi suất, tín dụng BĐS, luật đất đai, bảng giá đất, pháp lý dự án, trái phiếu chủ đầu tư, FDI vào KCN, hạ tầng, du lịch nghỉ dưỡng
version: v3.1
updated: 2026-11-03
---

# I01 – Bất động sản (nhà ở, khu công nghiệp, nghỉ dưỡng)

> Kiến thức nền định tính, không chứa số liệu. Mức phơi nhiễm của Techcombank theo ngành cần truy vấn nội bộ.

## 1. Cấu trúc ngành ở Việt Nam
- **Ba mảng chính, chu kỳ khác nhau:**
  - **nhà ở** (căn hộ, nhà phố, đất nền): nhạy với lãi suất và pháp lý;
  - **khu công nghiệp**: nhạy với FDI;
  - **nghỉ dưỡng** (condotel, biệt thự biển): nhạy với khách du lịch và với tâm lý đầu tư.
- **Người tham gia:**
  - DN lớn là chủ đầu tư, thường huy động vốn qua vay dự án, trái phiếu và tiền đặt cọc của người mua;
  - SME là sàn môi giới, nhà thầu phụ, thiết kế, quản lý tòa nhà;
  - HKD là môi giới tự do, cho thuê nhà trọ, cửa hàng nội thất;
  - KHCN là người mua để ở, nhà đầu tư cá nhân, người cho thuê.
- **Vùng:**
  - nhà ở tập trung ở hai đô thị lớn và vùng ven;
  - KCN ở các tỉnh phía Bắc và Đông Nam Bộ;
  - nghỉ dưỡng ở các tỉnh ven biển miền Trung và các đảo.
- **Đặc thù:**
  - BĐS là **tài sản bảo đảm phổ biến nhất** của toàn hệ thống ngân hàng, nên biến động giá BĐS lan sang mọi phân khúc qua `CL`;
  - tâm lý đầu cơ mạnh, dễ có pha Greed (sốt đất) và pha Fear (đóng băng thanh khoản).
- **Chu kỳ:** dài, phụ thuộc pháp lý dự án; độ trễ từ chính sách đến giao dịch thường nhiều tháng.

## 2. Biến số nhạy cảm
| Biến số | Chiều | Độ trễ | Ghi chú |
|---|---|---|---|
| Lãi suất cho vay mua nhà | Tăng → cầu giảm, áp lực trả nợ người đã vay | Vài tháng | Kỳ hết ưu đãi lãi suất là điểm nóng |
| Room tín dụng, siết tín dụng BĐS | Siết → chủ đầu tư thiếu vốn, người mua khó vay | Nhanh | Tín dụng nới dễ kéo Greed |
| Luật đất đai, bảng giá đất, thủ tục pháp lý | Tháo gỡ → dự án mở bán lại; tăng bảng giá → chi phí tiền sử dụng đất tăng | Nhiều tháng | Ảnh hưởng giá vốn và giá bán |
| Đáo hạn trái phiếu chủ đầu tư | Áp lực trả nợ, giãn nợ, bán tài sản | Theo lịch đáo hạn | Chạm nhà đầu tư cá nhân qua `L05` |
| FDI, dịch chuyển chuỗi cung ứng | Tăng → cầu thuê đất KCN, nhà xưởng, nhà ở công nhân | Trung hạn | Thuế quan với hàng xuất khẩu có thể làm FDI chậm lại |
| Đầu tư công vào hạ tầng | Tăng → giá đất ven tuyến tăng, kéo đầu cơ | Kỳ vọng đi trước | Dễ thành Greed theo tin đồn quy hoạch |
| Khách du lịch | Tăng → công suất BĐS nghỉ dưỡng | Theo mùa | Xem `I10` |
| Giá vật liệu xây dựng | Tăng → chi phí xây dựng, chậm tiến độ | Vài tháng | Xem `I02` |
| Thiên tai, ngập lụt | Giảm giá trị TSBĐ vùng rủi ro | Ngay đến dài hạn | Khí hậu là tin `GT` |

## 3. Tác động theo đối tượng
### KHCN – cá nhân
- **Thách thức:**
  - người vay mua nhà gặp áp lực khi lãi suất tăng hoặc hết ưu đãi;
  - người mua nhà dự án chịu rủi ro chậm bàn giao, chậm cấp giấy chứng nhận;
  - nhà đầu tư dùng đòn bẩy chịu lỗ khi thanh khoản đóng băng;
  - người mua trái phiếu chủ đầu tư bị chậm trả.
- **Cơ hội:**
  - lãi suất giảm và pháp lý thông thoáng làm nhu cầu vay mua nhà để ở tăng;
  - người có tiền nhàn rỗi mua được giá tốt ở pha Fear;
  - nhu cầu vay sửa chữa, xây nhà.

### KHCN – hộ kinh doanh
- **Thách thức:** môi giới tự do mất thu nhập khi thị trường trầm lắng; chủ nhà trọ quanh KCN mất khách khi công nhân giảm.
- **Cơ hội:** sốt giao dịch làm doanh thu môi giới, nội thất, sửa chữa tăng; KCN mở rộng kéo nhu cầu nhà trọ, ăn uống quanh khu.

### SME
- **Thách thức:** sàn môi giới, nhà thầu phụ bị chủ đầu tư chậm thanh toán; dòng tiền đứt khi dự án dừng.
- **Cơ hội:** dự án tái khởi động cần nhà thầu, bảo lãnh thực hiện hợp đồng, vốn lưu động.

### DN lớn
- **Thách thức:**
  - chủ đầu tư phụ thuộc vốn vay và trái phiếu dễ gặp áp lực thanh khoản;
  - pháp lý chậm làm vốn bị chôn;
  - giá đất tăng làm chi phí tiền sử dụng đất tăng.
- **Cơ hội:**
  - tháo gỡ pháp lý mở bán được;
  - chủ KCN hưởng lợi từ FDI;
  - nhu cầu nhà ở xã hội, nhà ở công nhân theo chính sách.

## 4. Sản phẩm ngân hàng liên quan
| Đối tượng | Phía rủi ro | Phía cơ hội |
|---|---|---|
| KHCN | Vay mua nhà `CN-LN-01` `CN-LN-02` `CN-LN-03`, xây sửa `CN-LN-08`; iBond chủ đầu tư `CN-INV-01` | Vay mua nhà mới (`O1`), bảo hiểm nhà `CN-INS-03` (`O4`) |
| HKD | Vay thế chấp kinh doanh `HKD-LN-02` dùng BĐS làm TSBĐ | Tài khoản, thanh toán cho môi giới, nội thất (`O3`) |
| SME | Vốn lưu động `SME-LN-01`, bảo lãnh `SME-GTE-01`; TK giữ hộ BĐS `SME-ACC-04` | Bảo lãnh, vốn lưu động khi dự án khởi động (`O1` `O3`) |
| DN lớn | Vay dự án `CIB-LN-02`, trái phiếu `CIB-INV-01`, TK giữ hộ BĐS `CIB-ACC-04`, bảo lãnh `CIB-TF-04` | Thu xếp vốn dự án, tài khoản giữ hộ, chi lương (`O1` `O3`) |
| Cấp ngân hàng | `CL` toàn danh mục, tập trung tín dụng, `RP` với iBond | – |

## 5. Tín hiệu theo dõi
- `G04` hồ sơ vay mua BĐS thứ hai, thứ ba cùng khu vực; định giá TSBĐ vượt giá giao dịch.
- `G01` tiền vay tiêu dùng chuyển sang đặt cọc BĐS.
- `F03` bán gấp TSBĐ để trả nợ; `S06` tất toán tiết kiệm của chủ đầu tư.
- `S08` bán lại iBond của tổ chức phát hành BĐS; `S12` chủ DN rút tiền cá nhân bơm cho DN.
- `S11` nhà thầu cùng một chủ đầu tư chậm trả đồng loạt.
- Cần truy vấn: dư nợ BĐS theo khu vực, tỷ lệ TSBĐ là BĐS theo phân khúc.

## 6. Liên kết ngành
- **Thượng nguồn:** `I02` xây dựng và vật liệu.
- **Hạ nguồn:** `I05` nội thất nội địa, `I09` bán lẻ đồ gia dụng.
- **Song song:** `I10` (nghỉ dưỡng), `I04` (KCN theo FDI).
- **Toàn hệ thống:** giá BĐS chạm mọi khoản vay có TSBĐ là BĐS.

## 7. Điểm đảo chiều và lưu ý
- Pha Greed (sốt đất theo tin quy hoạch, hạ tầng) đảo nhanh khi tín dụng siết hoặc tin đồn không thành.
- Pha Fear kéo dài khi pháp lý tắc; tháo gỡ pháp lý là điểm đảo chiều phổ biến.
- Không đánh đồng ba mảng: KCN có thể tốt khi nhà ở trầm lắng.
- Với dự án cụ thể, không suy đoán tình trạng pháp lý nếu tin không nêu.
