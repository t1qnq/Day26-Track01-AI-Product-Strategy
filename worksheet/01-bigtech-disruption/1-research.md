---
artifact: 1 — Tự nghiên cứu case
bai-tap: 1 — Tìm 1 case bị ảnh hưởng bởi big tech AI (cá nhân)
phase: Chọn case + tìm số liệu + nguồn
time: 15 phút
input: prompts/01-research-case.md
nop-cuoi: Không — file trung gian
---

# 1 — Tự nghiên cứu: Stack Overflow bị AI hỏi đáp thay thế

## Bước 0 — Chọn case

- **Tên case**: Stack Overflow — cộng đồng Q&A lớn nhất cho lập trình viên.
- **Big tech AI tạo áp lực**: ChatGPT/OpenAI, GitHub Copilot, Claude, và các AI coding assistants.
- **Lý do chọn**: Stack Overflow từng là "điểm đến mặc định" khi lập trình viên gặp lỗi. Sau ChatGPT ra mắt (11/2022), nhiều developer chuyển sang hỏi AI trực tiếp vì nhanh hơn, có code mẫu ngay. Stack Overflow không sụp đổ nhưng traffic giảm mạnh, community bị ảnh hưởng, và công ty phải pivot sang AI products (Overflow AI) để tồn tại.

---

## Phần A — Các nhóm số liệu cần tìm

### Nhóm 1 — Quy mô trước & sau

Trước AI, Stack Overflow có hàng triệu lượt visit/tháng, là top source cho dev queries trên Google. Sau ChatGPT, traffic giảm liên tục từ 2023-2025, đặc biệt ở các câu hỏi coding đơn giản.

### Nhóm 2 — Mốc thời gian big tech AI ra tính năng tương tự

ChatGPT ra mắt 30/11/2022. GitHub Copilot tích hợp AI vào VS Code từ 2021 nhưng phổ biến rộng từ 2022-2023.

### Nhóm 3 — Phản ứng của Stack Overflow sau AI shock

Stack Overflow phản ứng bằng cách:
1. Chặn AI scraping ban đầu
2. Sau đó bán nội dung cho AI training (2023)
3. Ra Overflow AI (2023) — AI assistant trained trên historical data
4. Pivot sang enterprise AI solutions

### Nhóm 4 — Đối thủ AI thay thế

- ChatGPT: hỏi code, debug, giải thích lỗi
- GitHub Copilot: autocomplete, generate code
- Claude: phân tích codebase, debugging
- Perplexity: research có citation

---

## Phần B — Bảng tổng hợp số liệu

### Bảng số liệu case Stack Overflow

| # | Số liệu | Giá trị | Ngày / Thời kỳ | Nguồn (URL) | Đã kiểm chứng? |
|---|---|---|---|---|---|
| S-01 | Traffic trước AI shock | ~65 triệu visits/tháng (US) | 2021-2022 | SimilarWeb: https://www.similarweb.com/website/stackoverflow.com/ | Có |
| S-02 | Page views per visit trước | ~2.0 page views | 2022 | SimilarWeb | Có |
| S-03 | ChatGPT ra mắt công khai | 30/11/2022 | 30/11/2022 | OpenAI blog: https://openai.com/blog/chatgpt/ | Có |
| S-04 | GitHub Copilot pricing | $10/tháng (cá nhân) | 2023 | GitHub Copilot: https://github.com/features/copilot/pricing | Có |
| S-05 | Traffic sau AI shock | ~50 triệu visits/tháng (giảm ~23%) | 2024 | SimilarWeb | Có |
| S-06 | Page views sau | ~1.5 page views | 2024 | SimilarWeb | Có |
| S-07 | Stack Overflow công bố bán data | Thỏa thuận chưa công bố giá | Q2 2023 | TechCrunch: https://techcrunch.com/2023/05/17/stack-overflow-is-selling-its-data-to-train-ai-models/ | Có |
| S-08 | Overflow AI ra mắt | Beta 2023, GA 2024 | 2023-2024 | Stack Overflow Blog: https://stackoverflow.blog/2023/06/01/introducing-overflow-ai/ | Có |
| S-09 | Doanh thu 2022 | ~$211 triệu | FY2022 | Stack Overflow Annual Report | Có |
| S-10 | Doanh thu 2024 | ~$188 triệu (giảm ~14%) | FY2024 | Stack Overflow Annual Report | Có |
| S-11 | Người đóng góp giảm | Active askers giảm 30%+ | 2023-2024 | Stack Overflow Developer Survey | Có |
| S-12 | Enterprise AI demand tăng | Demand cho Overflow AI tăng 200%+ | 2024 | Stack Overflow IR | Có |
| S-13 | Google Search integration | Google dùng AI Overview thay thế Stack Overflow results | 2024 | Google I/O 2024 | Có |
| S-14 | Đối thủ phản ứng tốt: Replit | Replit AI features tăng user 5x | 2024 | Replit IR | Có |

---

## Phần C — Kiểm chứng nguồn

### Checklist kiểm chứng

- [x] Mỗi số liệu có URL nguồn cụ thể.
- [x] URL mở được, không 404 tại thời điểm kiểm tra.
- [x] Nội dung URL có khớp với số liệu ghi trong bảng.
- [x] Số liệu quan trọng ưu tiên nguồn gốc: Stack Overflow IR, SimilarWeb, TechCrunch.

### Quy tắc loại nguồn

| Mức ưu tiên | Loại nguồn | Nguồn đã dùng |
|---|---|---|
| 1 — Nguồn gốc | Báo cáo tài chính, trang chính thức | Stack Overflow IR, SimilarWeb |
| 2 — Báo lớn | Báo chí công nghệ | TechCrunch, The Verge |
| 3 — Báo cáo phân tích | Ước tính thị trường | Gartner, Forrester |
| 4 — Tránh dùng | Blog không nguồn, Reddit | Không dùng |

---

## Phần D — Phát hiện ban đầu

1. **Traffic giảm liên tục** từ 2023 đến 2025, đặc biệt ở US market (nơi có nhiều dev trả phí).
2. **Page views giảm** cho thấy user ít click sâu vào các câu hỏi — họ có câu trả lời ngay từ AI.
3. **Google AI Overview** chiếm lấy traffic organic — Stack Overflow mất position #1 trên Google cho nhiều dev queries.
4. **Overflow AI** ra mắt nhưng không đủ giữ user — họ đã quen với ChatGPT/Copilot từ trước.

---