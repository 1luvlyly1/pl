---
id: BANK-LEVEL
used_by: [Propagation, Product-Impact, Inside-out Monitor, Critic]
steps: [1, 2, 3, 4]
depends_on: [core/01_risk_codes.md, core/03_linkage_graph.md]
load_when: Sự kiện chạm thẳng vào hoạt động của ngân hàng (thanh khoản, tỷ giá, hệ thống, lỗ hổng CVE, gian lận, tuân thủ, danh tiếng, nhà đầu tư), hoặc rủi ro từ khách hàng cộng dồn lên cấp ngân hàng (kênh L10)
version: v3.0
updated: 2026-11-02
---

# Cấp ngân hàng

> **Không phải phân khúc khách hàng.** Đây là nơi ghi các tác động chạm thẳng vào hoạt động của chính ngân hàng. Nhiều tin outside-in (lỗ hổng CVE, làn sóng gian lận, cú sốc tỷ giá, giá vàng tăng) chạm ngân hàng trước khi chạm khách hàng, hoặc chạm cùng lúc.
>
> Mã `NH-` là **nhóm năng lực, hệ thống hoặc chỉ tiêu** của ngân hàng, không phải sản phẩm bán cho khách. Mã `IR-` (nhà đầu tư, xếp hạng) giữ nguyên từ bản trước.

## (a) Sáu kênh tác động trực tiếp
| Kênh | Chạm vào gì | Loại tin thường gặp |
|---|---|---|
| Thanh khoản & huy động | Tiền gửi, CASA, tiền mặt | Giá vàng/chứng khoán tăng nóng, tin đồn, lãi suất đối thủ |
| Thị trường | Trạng thái ngoại tệ, lãi suất, danh mục đầu tư của ngân hàng | Chiến tranh, giá dầu, quyết định lãi suất của Fed, tỷ giá |
| Hệ thống & công nghệ | Ngân hàng số, core banking, thẻ, POS, đối tác công nghệ | Lỗ hổng CVE, ransomware, sự cố nhà cung cấp, sự cố hạ tầng |
| Gian lận & tuân thủ | Tài khoản bị lợi dụng, rửa tiền, trừng phạt | Làn sóng lừa đảo, thủ đoạn mới ở nước khác, danh sách trừng phạt mới |
| Danh tiếng & nhà đầu tư | Niềm tin công chúng, giá cổ phiếu, xếp hạng | Sự cố lớn, khiếu nại tập thể, tin xấu toàn ngành |
| Vận hành mạng lưới | Chi nhánh, nhân sự, tiền mặt | Thiên tai, dịch bệnh, mất điện diện rộng |

## (b) Bảng độ nhạy cấp ngân hàng
| Mã | Năng lực / hệ thống | Rủi ro chính | Nhạy với | Chiều tác động khi sự kiện xấu |
|---|---|---|---|---|
| `NH-LQ-01` | Huy động và CASA toàn hàng | `LQ` | Kênh đầu tư khác hấp dẫn hơn (vàng, chứng khoán), tin đồn | Tiền gửi chảy ra, chi phí vốn tăng |
| `NH-LQ-02` | Tiền mặt tại chi nhánh, CDM | `LQ` `OR` | Hoảng loạn, thiên tai, cơn sốt mua vàng bằng tiền mặt | Thiếu tiền mặt cục bộ |
| `NH-MR-01` | Trạng thái ngoại tệ, tỷ giá | `MR` | Chiến tranh, giá dầu, USD mạnh lên, nhập khẩu vàng | Áp lực mua ngoại tệ, lỗ trạng thái |
| `NH-MR-02` | Danh mục trái phiếu và đầu tư của ngân hàng | `MR` | Lãi suất trong nước và quốc tế | Giá trị danh mục giảm |
| `NH-OR-01` | Ngân hàng số, core banking | `OR` `FR` | Lỗ hổng CVE, tấn công, sự cố hạ tầng | Gián đoạn mọi phân khúc cùng lúc |
| `NH-OR-02` | Hệ thống thẻ, POS/SoftPOS, cổng thanh toán, kết nối liên ngân hàng | `OR` `FR` | Lỗ hổng trong thiết bị/phần mềm thanh toán, gian lận thẻ | Gian lận giao dịch, tra soát tăng |
| `NH-OR-03` | Đối tác công nghệ và phần mềm liên kết (phần mềm bán hàng, kế toán, đối tác bảo hiểm, chữ ký số) | `OR` `FR` | Sự cố hoặc lỗ hổng ở bên thứ ba | Rò rỉ dữ liệu, gián đoạn tính năng liên kết |
| `NH-OR-04` | Mạng lưới chi nhánh, nhân sự | `OR` | Thiên tai, dịch bệnh | Gián đoạn phục vụ tại quầy |
| `NH-FR-01` | Tài khoản bị lợi dụng (thuê, mượn, mua bán tài khoản) | `FR` `CO` | Làn sóng lừa đảo, thủ đoạn mới | Ngân hàng thành mắt xích chuyển tiền lừa đảo |
| `NH-CO-01` | Phòng chống rửa tiền, trừng phạt, báo cáo giao dịch đáng ngờ | `CO` | Trừng phạt quốc tế mới, xung đột, gian lận xuyên biên giới | Giao dịch bị chặn, rủi ro bị phạt |
| `NH-CO-02` | Bảo vệ dữ liệu cá nhân | `CO` `RP` | Rò rỉ dữ liệu ở ngân hàng hoặc đối tác | Phạt, mất niềm tin |
| `NH-RP-01` | Danh tiếng, niềm tin công chúng | `RP` | Sự cố, khiếu nại, tin xấu toàn ngành | Khách rút tiền, ngừng dùng dịch vụ |
| `IR-EQ-01` | Cổ phiếu TCB | `MR` `RP` | Kết quả kinh doanh, tin danh tiếng, dòng vốn ngoại | Giá giảm, khó tăng vốn |
| `IR-RT-01` | Xếp hạng tín nhiệm | `MR` `LQ` | Chất lượng tài sản, rủi ro tập trung | Hạ hạng → chi phí vốn quốc tế tăng |
| `IR-DIS-01` | Công bố thông tin | `CO` `RP` | Chậm hoặc sai công bố | Phạt, mất niềm tin |
| `IR-ECO-01` | Hệ sinh thái (chứng khoán, quản lý quỹ, bảo hiểm) | `RP` `MR` | Sự cố tại công ty con, đối tác | Lan danh tiếng về ngân hàng mẹ (`L11`) |

## (c) Cơ hội ở cấp ngân hàng (ít, không ép)
| Khi nào | Cơ hội | Điều kiện |
|---|---|---|
| Tiền gửi tìm nơi an toàn khi tổ chức khác gặp sự cố | `O2` `O6` qua `NH-LQ-01` | Đón khách chính đáng, không khai thác tin đồn (`guardrails.md` mục 13) |
| Khách bán vàng hoặc chứng khoán chốt lời | `O2` | Có kênh tiếp nhận tiền về (tiết kiệm, Sinh lời tự động) |
| Biến động tỷ giá, lãi suất làm khách cần phòng ngừa | `O3` | Gắn nhu cầu phòng ngừa thực, xem `segments/seg_03_DN_lon.md` |
| Đối thủ gặp sự cố hệ thống | Không coi là cơ hội để quảng bá. Chỉ dùng làm bài học kiểm tra lỗ hổng tương tự ở mình | – |

## (d) Tín hiệu nội bộ ở cấp ngân hàng
- Thanh khoản: `S07` rút tiền mặt, `F01` chuyển tiền gửi đi, `F02` chuyển kỳ hạn ngắn, `G02` tất toán để mua tài sản nóng.
- Hệ thống và gian lận: `S13` đăng nhập lạ, `S14` khiếu nại theo chủ đề, và các tín hiệu `X01`–`X08` trong `news/nw_03_gian_lan_an_ninh.md`.
- Thị trường: `S15` vị thế phái sinh của khách, nhu cầu mua ngoại tệ của doanh nghiệp nhập khẩu tăng.

## (e) Liên hệ với các phân khúc
- **Cấp ngân hàng → mọi phân khúc** (kênh `L09`): sự cố hệ thống hoặc thay đổi chính sách chạm cùng lúc KHCN, SME, DN lớn (mẫu P3).
- **Phân khúc → cấp ngân hàng** (kênh `L10`): rủi ro của khách hàng cộng dồn thành vấn đề thanh khoản, chất lượng tài sản, danh tiếng.
- **Đối tác công nghệ → ngân hàng và khách hàng** (kênh `L13`): lỗ hổng ở bên thứ ba đi vào qua tính năng liên kết.
- **Thủ đoạn ở nước khác → Việt Nam** (kênh `L14`): thủ đoạn gian lận lan qua biên giới khi dùng cùng loại kênh thanh toán.
