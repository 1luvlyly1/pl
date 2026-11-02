---
id: CORE-PROCEDURE
used_by: [Orchestrator, ALL]
steps: [1-6]
depends_on: [00_INDEX.md, fear_greed/fg_01_dual_lens.md]
load_when: Orchestrator luôn nạp; agent con nạp khi cần biết vai trò của mình
version: v3.1
updated: 2026-11-03
---

# Quy trình suy luận 6 bước (bắt buộc)

**Đầu vào:** thông tin một sự kiện **đã được người dùng sàng lọc**. Agent không lọc, không đánh giá sự kiện có đáng xử lý hay không, không tự tìm thêm tin. Agent chỉ suy luận từ nội dung sự kiện và playbook.

**Đầu ra:** một bài văn xuôi theo mẫu `core/05_output_prose.md`, có cả hai lăng kính **Fear (rủi ro)** và **Greed (cơ hội)**, kết thúc bằng 1–3 dòng nhãn `[FG]`.

**Tin outside-in:** ở bước 1, xếp tin vào nhóm `TT` (trực tiếp), `GT` (gián tiếp) hoặc `GL` (gian lận, lừa đảo, an ninh mạng) theo `news/nw_00_router.md`, rồi nạp file của nhóm đó. Nhóm tin quyết định cách đọc ở các bước 2–6.

**Lăng kính ngành:** cũng ở bước 1, liệt kê biến số trong tin và tra `industry/ind_00_index.md` mục 3 để biết ngành nào thiệt, ngành nào lợi; nạp tối đa 3 file ngành. Bước 2 dùng mục 3 và 6 của file ngành (ai trong ngành bị chạm, ngành liên đới), bước 3 dùng mục 4, bước 4 dùng mục 5.

**Bối cảnh (không bắt buộc):** nếu orchestrator truyền kèm chỉ số hành vi, áp dụng `fear_greed/fg_01_dual_lens.md` mục 7.

| Bước | Câu hỏi phải trả lời | Agent phụ trách | File cần dùng |
|---|---|---|---|
| 1 | Tin thuộc nhóm nào (`TT` / `GT` / `GL`)? Sự kiện chạm ai đầu tiên (KHCN, SME, DN lớn, hay cấp ngân hàng)? Mẫu P1 / P2 / P3? **Ai thiệt (Fear), ai lợi (Greed)? Tâm lý khách hàng thế nào, nhánh nào ở ô A, B, C, D?** | Propagation | `news/nw_00_router.md` + file của nhóm tin, `industry/ind_00_index.md` + tối đa 3 file ngành, `core/02_concepts_patterns.md`, `fear_greed/fg_01_dual_lens.md` |
| 2 | Rủi ro lan sang ai và **dòng tiền tăng lan sang ai**, qua kênh nào (`L01`–`L14`), sau bao lâu? Tin `GL`: thay bằng câu hỏi phạm vi áp dụng và bề mặt tấn công. Có vòng phản hồi nào không? | Propagation | `core/03_linkage_graph.md`, file phân khúc phần (e), file ngành mục 3 và 6 |
| 3 | Sản phẩm nào chịu rủi ro, **sản phẩm nào có nhu cầu tăng** (`O1`–`O6`)? Cơ hội có thỏa điều kiện đủ chuẩn không? | Product-Impact | File phân khúc phần (c), `bank/ngan_hang.md` khi chạm cấp ngân hàng, `fear_greed/fg_03_opportunity_map.md`, `core/01_risk_codes.md` |
| 4 | Tín hiệu nội bộ nào xác nhận rủi ro, xác nhận cơ hội, hoặc cho thấy hành vi sợ hãi (`F`) hay tham lam (`G`)? | Inside-out Monitor | `inside_out/signals.md`, `fear_greed/fg_02_behavior_signals.md`; tin `GL` thêm tín hiệu `X01`–`X08` |
| 5 | Nếu ngân hàng phản ứng theo tâm lý sợ (siết) hoặc tham (nới, đẩy bán), có tạo rủi ro mới không? | Inside-out Monitor | `inside_out/bank_response_risks.md`, `fear_greed/fg_01_dual_lens.md` mục 6 |
| 6 | Hai lăng kính có cân bằng không? Mỗi cơ hội có mặt trái và điểm đảo chiều chưa? Rủi ro lớn đã xét cơ hội ngược chu kỳ chưa? Có suy diễn quá đà hay bịa số không? Viết kết luận. | Critic | `guardrails.md`, `core/05_output_prose.md` |

## Câu hỏi kiểm tra nhanh ở bước 1
- Sự kiện làm thay đổi **doanh thu, chi phí hoặc pháp lý của một tổ chức** trước? → P1.
- Sự kiện làm thay đổi **thu nhập, sức khỏe, tài sản hoặc hành vi của con người** trước? → P2.
- Sự kiện tác động **cùng lúc** tới mọi khách hàng qua giá cả vĩ mô, quy định hay hạ tầng ngân hàng? → P3.
- Sự kiện bắt nguồn từ **bên trong ngân hàng** → inside-out; còn lại → outside-in.
- Đối tượng là hộ kinh doanh → luôn xét cả P1 và P2 (nút lai).
- **Sự kiện có lợi cho ai, có hại cho ai?** Liệt kê cả hai, kể cả khi một bên rất nhỏ.
- **Biến số nào trong tin chạm ngành nào?** Tra `industry/ind_00_index.md`; cùng một ngành có thể vừa lợi vừa thiệt tùy vai trò trong chuỗi.
- **Sự kiện có mô tả hành vi đổ xô, sốt, bán tháo, rút tiền, tin đồn không?** Có → tâm lý cực đoan (ô B hoặc C). Không → "tâm lý chưa rõ".

## Mức chắc chắn
Không dùng điểm số. Gắn mỗi nhận định, ở cả hai lăng kính, với một trong ba mức:
- **Có khả năng cao:** nút chạm đầu tiên hoặc hop 1, cơ chế rõ ràng.
- **Có thể:** hop 2, hoặc hop 1 nhưng cơ chế còn phụ thuộc điều kiện.
- **Giả thuyết, cần kiểm chứng:** hop 3 trở lên, hoặc phải dựa vào giả định do sự kiện thiếu chi tiết.

Nếu đã có tín hiệu nội bộ xác nhận, được nâng lên một mức và phải nói rõ tín hiệu nào. Cơ hội chưa thỏa điều kiện đủ chuẩn thì không được ở mức "có khả năng cao".
