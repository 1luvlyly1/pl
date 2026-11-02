---
id: IND-INDEX
used_by: [Orchestrator, Propagation, Product-Impact]
steps: [1, 2, 3]
depends_on: [news/nw_00_router.md, core/03_linkage_graph.md]
load_when: Mọi sự kiện có biến số bên ngoài (giá, tỷ giá, thuế quan, thời tiết, dịch bệnh, chính sách, công nghệ) – tra ngành bị tác động trước khi chọn file ngành
version: v3.1
updated: 2026-11-03
---

# Định tuyến ngành: biến số bên ngoài → ngành nào bị tác động

## 1. Module ngành dùng để làm gì
Tin bên ngoài thường chạm vào **một ngành** trước, rồi ngành truyền tới chủ DN, người lao động, hộ kinh doanh và đối tác trong chuỗi. Module này trả lời ba câu hỏi:
1. Biến số trong tin chạm **ngành nào**, theo chiều lợi hay thiệt?
2. Với từng ngành, **ai** chịu tác động: KHCN cá nhân (người lao động, nông hộ, người tiêu dùng, nhà đầu tư), KHCN hộ kinh doanh, SME, DN lớn?
3. Mỗi nhóm đó gặp **thách thức** gì và có **cơ hội** gì, dẫn tới sản phẩm ngân hàng nào?

Nguyên tắc dùng:
- File ngành là **kiến thức nền định tính**, không phải dữ liệu. Không suy ra số liệu, thị phần hay dư nợ theo ngành; mức phơi nhiễm của Techcombank luôn ghi "cần truy vấn nội bộ".
- Sự kiện được giao vẫn là nguồn duy nhất về diễn biến. File ngành chỉ giải thích **cơ chế** truyền dẫn; không thêm diễn biến mà tin không nêu.
- Một ngành có thể vừa lợi vừa thiệt trong cùng một tin, tùy vai trò trong chuỗi giá trị (xem `news/nw_01_truc_tiep.md` mục 1). Luôn đọc cả hai chiều.
- Mức chắc chắn theo số bước: ngành bị chạm trực tiếp có thể là "có khả năng cao"; ngành liên đới qua mục 6 của file ngành thường chỉ "có thể" hoặc "giả thuyết".

## 2. Danh sách 18 ngành
| Mã | File | Phạm vi | Khách hàng điển hình |
|---|---|---|---|
| `I01` | `ind_01_bat_dong_san.md` | Nhà ở, khu công nghiệp, nghỉ dưỡng, môi giới | DN lớn (chủ đầu tư), SME môi giới, KHCN người mua nhà |
| `I02` | `ind_02_xay_dung_vlxd.md` | Xây dựng, thép, xi măng, vật liệu | DN lớn, SME nhà thầu, HKD cửa hàng VLXD |
| `I03` | `ind_03_det_may_da_giay.md` | Dệt, may, da giày, túi xách | DN lớn/FDI, SME gia công, công nhân |
| `I04` | `ind_04_dien_tu.md` | Điện tử, linh kiện, bán dẫn, công nghiệp hỗ trợ | DN FDI, SME phụ trợ, công nhân KCN |
| `I05` | `ind_05_go_noi_that.md` | Gỗ, đồ gỗ, nội thất xuất khẩu và nội địa | DN lớn, SME, làng nghề HKD |
| `I06` | `ind_06_thuy_san.md` | Tôm, cá tra, hải sản đánh bắt, chế biến | DN lớn chế biến, nông hộ nuôi, ngư dân |
| `I07` | `ind_07_nong_san.md` | Cà phê, gạo, tiêu, điều, cao su, trái cây | Nông hộ, đại lý thu mua HKD, DN xuất khẩu |
| `I08` | `ind_08_chan_nuoi_thuc_pham.md` | Chăn nuôi, thức ăn chăn nuôi, thực phẩm, đồ uống, FMCG | DN lớn, trang trại, nhà phân phối, đại lý |
| `I09` | `ind_09_ban_le_tmdt.md` | Bán lẻ hiện đại, tạp hóa, chợ, thương mại điện tử | HKD, SME, chuỗi bán lẻ, người bán online |
| `I10` | `ind_10_du_lich_hang_khong.md` | Du lịch, lưu trú, ăn uống, hàng không, lữ hành | HKD ăn uống/lưu trú, SME lữ hành, DN lớn |
| `I11` | `ind_11_logistics.md` | Vận tải đường bộ/biển/hàng không, cảng, kho bãi, giao hàng | SME, HKD xe tải, DN lớn cảng/kho |
| `I12` | `ind_12_nang_luong.md` | Dầu khí, xăng dầu, điện, năng lượng tái tạo | DN lớn, cửa hàng xăng dầu, SME lắp đặt điện mặt trời |
| `I13` | `ind_13_hoa_chat_phan_bon.md` | Phân bón, hóa chất, nhựa, bao bì | DN lớn, SME nhựa, đại lý vật tư nông nghiệp |
| `I14` | `ind_14_o_to.md` | Ô tô, xe máy, xe điện, đại lý, sửa chữa | DN lớn lắp ráp, đại lý (SCF), HKD sửa xe, KHCN vay mua xe |
| `I15` | `ind_15_y_te_duoc.md` | Bệnh viện, phòng khám, dược, thiết bị y tế, nhà thuốc | DN lớn, SME phân phối, HKD nhà thuốc, KHCN y bác sĩ |
| `I16` | `ind_16_giao_duc.md` | Trường tư, mầm non, trung tâm, du học, giáo dục số | SME, HKD, KHCN phụ huynh và giáo viên |
| `I17` | `ind_17_cntt.md` | Phần mềm, thuê ngoài, viễn thông, trung tâm dữ liệu | DN lớn, SME công nghệ, KHCN lương cao |
| `I18` | `ind_18_vang_trang_suc.md` | Vàng miếng, vàng nhẫn, trang sức, tiệm vàng | HKD tiệm vàng, DN kinh doanh vàng, KHCN người giữ vàng |

## 3. Ma trận biến số → ngành (khi biến số **tăng**)
Khi biến số **giảm**, đảo chiều hai cột. Ngành in đậm là ngành chịu tác động mạnh hoặc nhanh nhất.

| Biến số | Ngành thường **thiệt** | Ngành thường **lợi** | Ghi chú |
|---|---|---|---|
| Giá dầu | **I10** **I11**, I13, I06 (đánh bắt), I08, I02 | **I12** (khai thác, phân phối trên hàng tồn) | Qua lạm phát chạm thêm tiêu dùng `I09` |
| Giá khí, than, giá điện bán lẻ | **I02** (thép, xi măng), **I13**, I03 (nhuộm), I04 | I12 (bên bán, nếu giá bán được điều chỉnh) | Giá điện bán lẻ do Nhà nước điều chỉnh |
| Giá vàng | I18 (trang sức: sức mua giảm), cấp ngân hàng (huy động) | **I18** (hàng tồn, vàng miếng), KHCN đang giữ vàng | Đọc `I18` cùng `bank/ngan_hang.md` |
| USD mạnh, VND mất giá | Nhập khẩu ròng: **I12** (nhập xăng dầu), I13, I08 (thức ăn chăn nuôi), I14, I15, I16 (du học); DN nợ USD (I10, I12) | Xuất khẩu ròng có đầu vào nội địa: **I06** **I07** I05; I10 (khách quốc tế rẻ hơn) | I03 I04 xuất khẩu nhưng nhập nhiều đầu vào: tác động ròng nhỏ |
| Lãi suất cho vay trong nước | **I01**, **I02**, I14, I09 (trả góp), I12 (tái tạo đòn bẩy cao) | Ít ngành lợi trực tiếp | Lãi suất giảm: đảo chiều, dễ kéo Greed ở `I01` |
| Thuế quan Mỹ, rào cản nhập khẩu | **I03** **I04** **I05** **I06**, I07, I02 (thép), I12 (tấm pin) | I11 ngắn hạn (đẩy hàng trước hạn áp thuế) | Xem thêm điều tra chống lẩn tránh xuất xứ |
| Chống bán phá giá, chống trợ cấp | **I02** (thép), **I06** (tôm, cá tra), I05, I04 (pin mặt trời) | Đối thủ trong nước khi Việt Nam áp thuế lên hàng nhập | Hai chiều: Việt Nam cũng áp lên hàng nhập |
| Quy định xanh EU (chống phá rừng, CBAM) | **I07** (cà phê, cao su), **I05**, I02 (thép, xi măng), I13 (phân bón) | DN đã truy xuất được nguồn gốc | Tác động theo lộ trình, độ trễ dài |
| Thẻ vàng IUU | **I06** (đánh bắt, chế biến hải sản) | Không | Ngư dân và cảng cá là KHCN, HKD |
| Nhu cầu Trung Quốc mạnh | – | **I07** (trái cây, cao su, gạo), I06, **I10** (khách), I13 | TQ yếu và dư cung: hàng TQ giá rẻ chạm **I02** I03 **I09** |
| Giá nông sản thế giới | **I08** (ngô, đậu tương làm thức ăn), F&B dùng nguyên liệu, đại lý thu mua (cần vốn) | **I07** (nông hộ, DN xuất khẩu), I13 (cầu phân bón) | Xem `ex_FG_01_ca_phe_o_B.md` |
| Hạn mặn, El Niño, bão lũ | **I07** **I06** I08, I12 (thủy điện), I10, I11, I01 (vùng ngập) | I02 (sửa chữa sau bão), I13 (vụ sau), I12 (nhiệt điện bù) | Ghi rõ vùng; tác động theo mùa vụ |
| Dịch bệnh ở người | **I10**, I09 (cửa hàng), I16, I03, I11 | **I15**, I09 (TMĐT), I17, I08 (thiết yếu) | Ba pha, xem `news/nw_02_gian_tiep.md` |
| Dịch bệnh vật nuôi, thủy sản | **I08** (chăn nuôi), **I06** (nuôi tôm) | Nguồn đạm thay thế, thuốc thú y | Nông hộ là KHCN |
| Khách quốc tế, nới visa | – | **I10**, I09, I01 (nghỉ dưỡng), I18 | Nhạy với tin chính trị, hàng không |
| Đầu tư công giải ngân | – | **I02**, I01 (giá đất ven hạ tầng), I11 | Thanh toán chậm từ ngân sách: `L12` |
| Chính sách BĐS, pháp lý dự án, bảng giá đất | **I01**, I02, I05 (nội thất nội địa) | I01 khi tháo gỡ pháp lý | Kéo theo TSBĐ `CL` toàn hệ thống |
| FDI, dịch chuyển chuỗi cung ứng | I03 (cạnh tranh lao động) | **I04**, **I01** (KCN), I02, I11, I12 | Lao động KCN là KHCN lương |
| Tiêu dùng nội địa mạnh | – | **I09**, I08, I14, I10, I15, I18 | Tiêu dùng yếu: đảo chiều, HKD chịu trước |
| Thu nhập công nhân giảm, cắt giảm lao động | **I09** (quanh KCN), I01 (nhà trọ), I14 (xe máy) | – | Thường đến sau đơn hàng `I03` `I04` giảm |
| Tỷ lệ sinh giảm, già hóa | **I16** (mầm non), I08 (sữa trẻ em) | **I15**, I08 (dinh dưỡng người già) | Nhóm tin `GT`, không cảnh báo khẩn |
| AI, tự động hóa, số hóa | I17 (thuê ngoài cấp thấp), I09 (cửa hàng truyền thống) | **I17**, I04 (bán dẫn), I12 (điện cho trung tâm dữ liệu) | `GT`, chân trời dài |
| Cước vận tải biển, tuyến hàng hải gián đoạn | **I05** **I03** I07 I06 (hàng lạnh), nhập khẩu nguyên liệu | I11 (hãng tàu, giao nhận: cước cao, nhưng khách giảm) | Đi kèm giá dầu khi do xung đột |
| Giá thép, VLXD | **I02** (nhà thầu giá cố định), I01 | I02 (nhà sản xuất có hàng tồn) | Cùng ngành, khác vai trò |
| Thuế HKD, hóa đơn điện tử, kê khai | **I09** **I10** (ăn uống) I18, I14 (sửa xe) | Chuyển đổi HKD lên DN (`L07`) | Xem `segments/seg_01b_KHCN_ho_kinh_doanh.md` |
| Chính sách xe (lệ phí, xe điện, hạn chế xe xăng) | I14 (xe xăng, sửa chữa) | I14 (xe điện, hạ tầng sạc), I12 | |
| Đấu thầu thuốc, BHYT, giá dịch vụ y tế | I15 (tùy chiều chính sách) | I15 | |

## 4. Tin `GT` và `GL` → ngành
- **`GT`** (dân số, đại dịch, khí hậu, đô thị hóa, AI): dùng ma trận như trên nhưng giữ chân trời dài; chỉ chọn ngành có cơ chế rõ, không kể hết.
- **`GL`** (gian lận, lừa đảo, CVE): ngành là **bề mặt tấn công**, không phải nơi chịu rủi ro tín dụng. Chỉ mô tả ở mức nhận diện:
  - `I09` `I11`: mạo danh giao hàng, cửa hàng online giả, chiếm tài khoản người bán;
  - `I10`: đặt phòng, vé, tour giả; `I01`: dự án không có thật, đặt cọc trái phép;
  - `I18`: tiền mặt lớn, vàng giả, rửa tiền qua vàng; `I17`: lỗ hổng nhà cung cấp phần mềm (`L13`);
  - `I03` `I05` `I06`: email giả người mua nước ngoài đổi tài khoản nhận tiền, chứng từ giả (`X04` `X06`).

## 5. Cách chọn file ngành (trong bước 1–2)
1. Sau khi `news/nw_00_router.md` xếp nhóm tin, liệt kê **biến số** trong tin (giá gì, chính sách gì, ở đâu).
2. Tra mục 3 để có danh sách ngành thiệt và ngành lợi.
3. Nạp **tối đa 3 file ngành**, ưu tiên: ngành chịu tác động mạnh hoặc nhanh nhất; ngành có cả chiều lợi và thiệt; ngành có nhiều khách hàng KHCN hoặc HKD trong chuỗi.
4. Ngành bậc hai (liên đới) không nạp; chỉ nêu tên qua mục 6 của file ngành đã nạp, mức "có thể" hoặc "giả thuyết".
5. Product-Impact dùng mục 4 của file ngành để chọn mã sản phẩm, rồi kiểm lại tên sản phẩm trong file phân khúc.
6. Inside-out Monitor lấy mục 5 của file ngành làm danh sách tín hiệu cần truy vấn.

## 6. Ngành đi vào văn xuôi thế nào
- **Đoạn 2** (bên thiệt, bên lợi đầu tiên): gọi tên ngành và vai trò trong chuỗi, không ghi mã `I`.
- **Đoạn 3, 4** (rủi ro, cơ hội): tách theo đối tượng – người lao động, nông hộ, hộ kinh doanh, SME, DN lớn – lấy từ mục 3 của file ngành.
- **Đoạn 6** (tín hiệu): luôn có câu "cần truy vấn dư nợ, số khách theo ngành".
- Mã `I01`–`I18` chỉ dùng trong ghi chú nội bộ giữa các agent, **không** đưa vào dòng nhãn `[FG]`.

## 7. Khuôn chung mỗi file ngành
1. Cấu trúc ngành ở Việt Nam
2. Biến số nhạy cảm (bảng: biến số, chiều, độ trễ, ghi chú)
3. Tác động theo đối tượng (KHCN cá nhân, KHCN hộ kinh doanh, SME, DN lớn – thách thức và cơ hội)
4. Sản phẩm ngân hàng liên quan
5. Tín hiệu theo dõi
6. Liên kết ngành
7. Điểm đảo chiều và lưu ý

Bảo trì: mỗi file giữ dưới 10 KB, không ghi tên công ty, không ghi số liệu. Khi chính sách thay đổi, cập nhật mục 2 và mục 7 của file ngành, tăng `version`.
