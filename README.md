# Playbook Rủi ro & Cơ hội (Fear & Greed) – Techcombank

Phiên bản **v3.1** · Cập nhật 03/11/2026 · Danh mục sản phẩm chốt 26/10/2026 từ techcombank.com

Bộ tài liệu cho hệ thống multi-agent đọc sự kiện (đã được người dùng sàng lọc) và suy luận rủi ro, cơ hội lan tới từng nhóm khách hàng, sản phẩm và chính ngân hàng.

- **3 phân khúc:** KHCN (gồm nhóm cá nhân và nhóm hộ kinh doanh), SME, doanh nghiệp lớn (mã `CIB`).
- **Cấp ngân hàng:** tác động chạm thẳng vào hoạt động của ngân hàng (thanh khoản, tỷ giá, hệ thống, lỗ hổng CVE, gian lận, tuân thủ, danh tiếng, nhà đầu tư).
- **3 nhóm tin outside-in**, mỗi nhóm một cách suy luận:
  - `TT` – tác động trực tiếp: xung đột làm giá vàng, dầu tăng; giá hàng hóa; tỷ giá; lãi suất; thương mại; chính sách.
  - `GT` – tác động gián tiếp: tỷ lệ sinh, già hóa, đại dịch, khí hậu, đô thị hóa, công nghệ.
  - `GL` – gian lận, lừa đảo, an ninh mạng: thủ đoạn ở nước khác, làn sóng lừa đảo, lỗ hổng CVE, rò rỉ dữ liệu.
- **18 ngành Việt Nam** (mới ở v3.1): từ biến số bên ngoài (giá dầu, vàng, tỷ giá, thuế quan, thời tiết, dịch bệnh, chính sách…) tra ra ngành nào thiệt, ngành nào lợi; mỗi ngành một file mô tả thách thức và cơ hội cho cá nhân, hộ kinh doanh, SME, DN lớn.

## 1. Cấu trúc thư mục và ai dùng

```
(thư mục giải nén)
├── README.md                     ← file này
│
├── playbook/                     ← AGENT ĐỌC. Nạp vào kho tri thức / prompt của hệ thống
│   ├── 00_INDEX.md               ← agent luôn đọc đầu tiên; chỉ dẫn đọc file nào tiếp theo
│   ├── guardrails.md             ← 16 ràng buộc bắt buộc
│   ├── core/                     ← quy trình 6 bước, 14 kênh liên kết, mẫu văn xuôi + dòng nhãn [FG]
│   ├── news/                     ← bộ định tuyến tin và 3 file cho tin TT, GT, GL
│   ├── industry/                 ← MỚI v3.1: ind_00_index (biến số → ngành) + 18 file ngành ind_01…ind_18
│   ├── fear_greed/               ← hai lăng kính rủi ro/cơ hội, ma trận ô A–D, tín hiệu F/G, cơ hội O1–O6
│   ├── segments/                 ← KHCN (2 file: cá nhân, hộ kinh doanh), SME, doanh nghiệp lớn
│   ├── bank/                     ← cấp ngân hàng (thay phân khúc nhà đầu tư)
│   ├── inside_out/               ← tín hiệu nội bộ S01–S16, phản ứng của ngân hàng
│   └── examples/                 ← 10 bài mẫu văn xuôi có dòng nhãn
│
├── index_spec/                   ← ĐỘI DỮ LIỆU / KỸ THUẬT ĐỌC. Agent KHÔNG nạp
│   ├── fg_index_spec.md          ← cách tính chỉ số hành vi, dòng tiền thực, tin tức
│   ├── fg_tag_format.md          ← định dạng dòng nhãn [FG] v3.0, biểu thức kiểm tra, mã Python đọc nhãn
│   └── sample_data.json          ← dữ liệu mẫu đúng cấu trúc dashboard cần
│
└── tham_khao/                    ← NGƯỜI XEM. Mở bằng trình duyệt
    ├── luong_chay_playbook.html          ← luồng chạy (bản v3.0, chưa thể hiện module ngành)
    ├── dashboard_fear_greed_mau.html     ← dashboard chỉ số Fear & Greed (dữ liệu mẫu)
    └── ban_do_co_hoi_outside_in.html     ← minh họa chiều cơ hội (bản v2, vẫn tách hộ kinh doanh riêng)
```

**Vì sao tách `index_spec/` ra ngoài `playbook/`:** agent chỉ cần viết dòng nhãn đúng định dạng (đã có trong `playbook/core/05_output_prose.md`). Công thức tính chỉ số là việc của code; để chung, agent có thể nạp nhầm và tự chấm điểm.

## 2. Triển khai từng bước

### Bước 1 – Đưa playbook vào hệ thống agent
- Chép nguyên thư mục `playbook/`, **giữ nguyên cấu trúc thư mục con**: các file tham chiếu nhau bằng đường dẫn tương đối.
- Không gộp các file; mỗi file giữ quanh 12 KB để agent đọc được.

### Bước 2 – Cấu hình từng agent
Theo `playbook/00_INDEX.md` mục 3. Tóm tắt:

| Agent | Luôn nạp | Nạp thêm khi cần |
|---|---|---|
| Orchestrator | `00_INDEX.md`, `core/04`, `guardrails.md`, `news/nw_00_router.md` | – |
| Propagation | `core/02`, `core/03`, `fear_greed/fg_01`, `news/nw_00_router.md` | **Một** file nhóm tin, file phân khúc, `industry/ind_00_index.md` + **tối đa 3** file ngành, 1 bài mẫu |
| Product-Impact | `core/01`, `fear_greed/fg_03` | Tối đa 3 file phân khúc; `bank/ngan_hang.md` khi chạm cấp ngân hàng; mục 4 file ngành |
| Inside-out Monitor | `inside_out/signals.md`, `fear_greed/fg_02`, `inside_out/bank_response_risks.md` | Phần (d) file phân khúc; tín hiệu `X01`–`X08` với tin `GL`; mục 5 file ngành |
| Critic | `guardrails.md`, `core/05`, `fear_greed/fg_01` | 1 bài mẫu, ghi chú các agent trước |

### Bước 3 – Đầu vào và đầu ra
- **Đầu vào:** nội dung một sự kiện đã sàng lọc. Agent xếp tin vào `TT` / `GT` / `GL` chỉ để chọn cách suy luận, không để loại tin.
- **Đầu ra:** một bài văn xuôi 350–650 từ (7 đoạn, có cả rủi ro và cơ hội), kết thúc bằng 1–3 dòng nhãn, ví dụ:
  ```
  [FG] loai_tin=TT | o=D | tam_ly=chua_ro | huong=rui_ro | phan_khuc=CIB,SME,KHCN,NH | muc=co_kha_nang_cao
  ```

### Bước 4 – Lưu dòng nhãn
- Dùng biểu thức và mã mẫu trong `index_spec/fg_tag_format.md`.
- Dòng sai định dạng: ghi log và bỏ, không đoán sửa.
- `NH` (cấp ngân hàng) không tính vào chỉ số của KHCN, SME, CIB; chỉ tính vào chỉ số toàn hàng.

### Bước 5 – Tính chỉ số (khi đã có dữ liệu)
- Làm theo `index_spec/fg_index_spec.md`: chỉ số hành vi (7 thành phần), dòng tiền thực (4 thành phần), tin tức (từ dòng nhãn).
- Cần ít nhất 12 tháng lịch sử cho hai chỉ số đầu.

### Bước 6 – Đưa chỉ số hành vi vào agent làm bối cảnh (không bắt buộc)
- Orchestrator thêm một dòng kèm sự kiện: `Bối cảnh: chỉ số hành vi KHCN = 78 (Tham lam cực độ)`.
- **Không bao giờ** truyền chỉ số tin tức vào agent.

### Bước 7 – Hiển thị
- Mở `tham_khao/dashboard_fear_greed_mau.html` bằng trình duyệt. Dữ liệu nằm trong khối `<script type="application/json" id="data">` cuối file; thay bằng nội dung `sample_data.json` hoặc output thật.

## 3. Lưu ý
- Mọi ví dụ và số liệu mẫu là **giả định**, không phản ánh dữ liệu hay khách hàng thực.
- File ngành là **kiến thức nền định tính**: không có số liệu, không có tên công ty. Mức phơi nhiễm của Techcombank theo ngành luôn cần truy vấn nội bộ. Khi chính sách thay đổi, cập nhật mục 2 và mục 7 của file ngành.
- Mã ngành `I01`–`I18` chỉ dùng giữa các agent, không đưa vào dòng nhãn `[FG]` (định dạng nhãn không đổi so với v3.0).
- Với tin `GL`, agent chỉ mô tả ở mức nhận diện, không mô tả cách khai thác hay thủ đoạn chi tiết, và không kết luận hệ thống ngân hàng bị ảnh hưởng hay an toàn khi chưa có xác nhận của đội an ninh thông tin.
- Chỉ số Fear & Greed là chỉ số nội bộ để đọc tâm lý khách hàng, **không phải dự báo thị trường**.
- Trang HTML cần mạng để tải font; khi offline vẫn hiển thị đúng tiếng Việt.

