---
id: CORE-OUTPUT-PROSE
used_by: [Critic, Orchestrator]
steps: [6]
depends_on: [core/04_reasoning_procedure.md, guardrails.md, fear_greed/fg_01_dual_lens.md]
load_when: Khi viết kết luận cuối cùng của một lượt suy luận
version: v3.0
updated: 2026-11-02
---

# Mẫu viết kết luận bằng văn xuôi (Fear & Greed)

Kết luận là một bài viết đọc liền mạch, **350–650 từ**. Không dùng bảng, không dùng JSON. Mã (`L..`, `CN-..`, `O..`, `S..`, `F..`, `G..`) chỉ đặt trong ngoặc sau cụm từ tiếng Việt để tra cứu; câu văn vẫn phải đọc hiểu được khi bỏ mã đi.

## Bố cục 7 đoạn

1. **Sự kiện và cách đọc.** Tóm tắt sự kiện được giao; outside-in hay inside-out; mẫu lan truyền; tâm lý khách hàng (bình thường, sợ hãi, tham lam hay chưa rõ); nhánh chính nằm ở ô nào của ma trận.
2. **Ai thiệt, ai lợi đầu tiên.** Nêu cả hai phía và cơ chế cụ thể. Nếu một phía không có, nói rõ là không thấy.
3. **Fear – rủi ro lan đi thế nào.** Theo từng nhánh: từ ai sang ai, qua kênh gì, sau bao lâu, mức chắc chắn. Vòng phản hồi nói ở cuối đoạn.
4. **Greed – dòng tiền tăng lan đi thế nào.** Viết giống đoạn 3 nhưng cho phía hưởng lợi. Với nhánh ở ô B, nói rõ phần nào là nhu cầu thật, phần nào là hành vi đầu cơ.
5. **Sản phẩm ở hai phía.** Sản phẩm chịu rủi ro và loại rủi ro; sản phẩm có nhu cầu tăng, loại cơ hội và điều kiện đủ chuẩn. Đi theo thứ tự phân khúc như đoạn 3–4.
6. **Tín hiệu cần kiểm tra.** Tín hiệu xác nhận rủi ro, tín hiệu xác nhận cơ hội, và tín hiệu cảnh báo cơ hội đã thành nóng (G) hoặc sợ hãi lan rộng (F). Chưa có số liệu thì nói thẳng.
7. **Phản ứng của ngân hàng, điểm đảo chiều và giả định yếu nhất.** Ngân hàng dễ phản ứng sai theo hướng nào (siết quá mạnh hay nới quá nhanh); điều kiện nào làm cơ hội đảo thành rủi ro; giả định yếu nhất của lập luận.

## Quy tắc viết
- Viết như chuyên viên rủi ro báo cáo cho trưởng phòng: rõ, cụ thể, không rào đón, không cổ vũ.
- **Cân bằng:** độ dài đoạn 3 và đoạn 4 tương xứng với tầm quan trọng thật, không cố viết đều. Nếu sự kiện gần như chỉ có một phía, phía kia chỉ cần một câu.
- Mỗi nhận định ở hop 2 trở đi kèm từ chỉ mức chắc chắn (“có thể”, “giả thuyết”).
- Cơ hội viết ở dạng "nhu cầu có thể tăng ở…", không viết thành chỉ thị bán hàng nhắm vào khách cụ thể.
- Chỉ dùng thông tin có trong sự kiện và playbook. Không viết số liệu không có cơ sở. Không nêu tên khách hàng cụ thể.
- Ưu tiên chiều sâu ở 2–3 nhánh quan trọng nhất của mỗi lăng kính.

## Khung câu gợi ý
> [Sự kiện] là sự kiện [outside-in/inside-out], lan theo mẫu [P..]; tâm lý khách hàng [bình thường/sợ hãi/tham lam/chưa rõ], nên nhánh chính nằm ở ô [A/B/C/D]. Bên thiệt đầu tiên là [phân khúc] vì [cơ chế]; bên hưởng lợi đầu tiên là [phân khúc] vì [cơ chế]. Về rủi ro, [nhánh]… Về cơ hội, dòng tiền tăng có khả năng cao lan sang [phân khúc] qua [kênh] ([L..])… Ở phía sản phẩm, rủi ro tập trung ở [sản phẩm] ([mã]); nhu cầu có thể tăng ở [sản phẩm] ([mã], [O..]) nếu [điều kiện đủ chuẩn]… Để xác nhận, cần kiểm tra [tín hiệu]; nếu thấy [tín hiệu G] thì cơ hội đã chuyển sang nóng… Ngân hàng dễ [phản ứng sai]. Cơ hội sẽ đảo thành rủi ro nếu [điều kiện đảo chiều]. Giả định yếu nhất là […].

## Dòng nhãn [FG] (bắt buộc, đặt sau bài văn)
Sau bài văn xuôi, xuống dòng và ghi **1 đến 3 dòng nhãn**, mỗi dòng cho một nhánh chính (không tính vào số từ). Code dùng các dòng này để tính chỉ số tin tức; viết đúng định dạng, không thêm trường khác.

```
[FG] loai_tin=<nhóm tin> | o=<ô> | tam_ly=<tâm lý> | huong=<hướng> | phan_khuc=<phân khúc> | muc=<mức chắc chắn>
```

| Trường | Giá trị hợp lệ |
|---|---|
| `loai_tin` | `TT` (trực tiếp), `GT` (gián tiếp), `GL` (gian lận, lừa đảo, an ninh mạng), `IO` (sự kiện inside-out). Ghi nhóm của **nhánh** đó |
| `o` | `A`, `B`, `C`, `D`; hai ô thì ghi `A,B` |
| `tam_ly` | `so`, `binh_thuong`, `tham`, `chua_ro` |
| `huong` | `rui_ro`, `co_hoi`, `ca_hai` |
| `phan_khuc` | Một hoặc nhiều trong `KHCN` (gồm cả hộ kinh doanh), `SME`, `CIB` (doanh nghiệp lớn), `NH` (cấp ngân hàng), cách nhau bằng dấu phẩy, không dấu cách |
| `muc` | `co_kha_nang_cao`, `co_the`, `gia_thuyet` |

Ví dụ cho sự kiện giá cà phê lập đỉnh (hai nhánh ở hai ô khác nhau):
```
[FG] loai_tin=TT | o=B | tam_ly=tham | huong=co_hoi | phan_khuc=KHCN,CIB | muc=co_kha_nang_cao
[FG] loai_tin=TT | o=D | tam_ly=chua_ro | huong=rui_ro | phan_khuc=KHCN,SME | muc=co_the
```

## Biến thể theo nhóm tin
- **`GT`:** ghi tầm thời gian cho từng nhánh; đề xuất ở dạng theo dõi định kỳ hoặc xem lại khẩu vị, không cảnh báo khẩn (`news/nw_02_gian_tiep.md` mục 5).
- **`GL`:** đoạn 3 viết về bề mặt tấn công thay cho chuỗi lan truyền; đoạn 4 thường là "không thấy cơ hội"; đoạn 6 có danh sách điều cần đội an ninh xác nhận; đoạn 7 nêu khung thời gian hành động (`news/nw_03_gian_lan_an_ninh.md` mục 8).
- **Tin nhiều nhóm:** nhóm phụ viết thành một nhánh ngắn và có dòng nhãn riêng.
