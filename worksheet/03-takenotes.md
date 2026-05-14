---
artifact: 03-takenotes — Quan sát cá nhân sau phần chia sẻ nhóm khác
bai-tap: 3 — Quan sát + rút ra bài học (cá nhân)
phase: Sau phần shareout của các nhóm
time: 15 phút (xem deck slide 4 để biết khung giờ chính xác)
input: Phần thuyết trình của ít nhất 2 nhóm khác trên lớp
nop-cuoi: Có — file cuối Lab 3 (cá nhân)
---

# 03 — Take notes: quan sát + bài học cá nhân

Đây là phần cá nhân. Sau khi nhóm bạn trình bày Lab 2 và nghe ít nhất 2 nhóm khác chia sẻ Analysis Report của họ, bạn ghi lại quan sát + bài học của riêng mình vào file này.

Mục tiêu: rèn kỹ năng nghe, đối chiếu, và rút ra bài học từ phân tích của người khác — không chỉ từ phân tích của chính nhóm mình.

Quy tắc khi viết:

- Trích dẫn cụ thể tên sản phẩm + nhóm đã quan sát (không nói chung chung).
- Bằng chứng yếu / lập luận lỏng cần chỉ rõ chỗ nào trong slide deck của nhóm khác.
- Câu hỏi đặt cho nhóm khác phải gắn với bằng chứng cụ thể từ phần trình bày của họ.

---

## Thông tin

- **Mã học viên**: 2A202600285 — Quách Ngọc Quang
- **Ngày**: 2026-05-14
- **Nhóm Lab 2 của tôi**: Cursor vs GitHub Copilot (Ngành Lập trình) — làm phần S1-S3

---

## Phần 1 — Thành viên đã quan sát (≥ 2 thành viên khác)

| # | Mã học viên / Tên | Case BigTech | Sản phẩm họ phân tích |
|---|---|---|---|
| 1 | 2A202600369 Hồ Thị Tố Nhi | Adobe bị AI disruption | Midjourney / Stable Diffusion |
| 2 | 2A202600392 — Nguyễn Đông Hưng | Fiverr bị AI disruption | ChatGPT / GitHub Copilot / Cursor |

---

## Phần 2 — Điều thấy hay từ thành viên khác

**Quan sát 1** (từ 2A202600369 - Hồ Thị Tố Nhi ,Adobe case):

- **Cụ thể họ đưa ra**: Phân tích chi tiết về việc Adobe Creative revenue growth plummet từ +23% YoY (FY2021) xuống +10% YoY (FY2022-2024), kèm theo market cap collapse -63.7% từ $320B (Nov 2021) xuống $99.5B (May 2026). Có bằng chứng cụ thể về 4 fits bị vỡ: PMF, MMF, PCM, PCF.
- **Vì sao tôi thấy hay**: Cách phân tích "switching cost moat bị AI phá vỡ" rất thuyết phục — khi prompts thay thế pixel-level editing, hours users spent mastering Photoshop không còn lock them in. Có so sánh đối chiếu với Canva (phản ứng nhanh hơn với AI APIs + freemium model).

**Quan sát 2** (từ 2A202600392 - Nguyễn Đông Hưng, Fiverr case):

- **Cụ thể họ đưa ra**: Timeline chi tiết từ ChatGPT ra mắt (30/11/2022) đến Fiverr cuts 30% staff (09/2025), với 16 sources đã kiểm chứng. Có bảng số liệu so sánh trước/sau: active buyers giảm từ 4.217M → 2.907M, marketplace revenue giảm 13.6% YoY Q1 2026.
- **Vì sao tôi thấy hay**: Phân tích "4 Fit Collapse" rất cụ thể — không chỉ nói "AI ảnh hưởng" mà chỉ rõ Product Market Fit, Model Market Fit, Product Channel Fit, Channel Model Fit nào bị phá vỡ. Có phần so sánh với Upwork (phản ứng tốt hơn với Uma AI từ 04/2024, FY2024 record revenue $769.3M).

---

## Phần 3 — Điểm yếu / chỗ chưa thuyết phục (Thành viên chấm Thành viên)

**Điểm yếu 1** (từ 2A202600369 - Hồ Thị Tố Nhi, Adobe case):

- **Cụ thể**: Phần phân tích Data Flywheel chỉ mô tả "có một phần compounding effect" nhưng chưa phân tích sâu tại sao Adobe's flywheel yếu hơn so với Midjourney/ChatGPT. Không có so sánh định lượng về velocity của feedback loop.
- **Bằng chứng gì còn thiếu**: So sánh cụ thể về loại dữ liệu mà mỗi platform thu thập — Adobe thu thập creative workflow data (project files, edits) trong khi Midjourney thu thập prompt-response pairs — loại nào valuable hơn cho model improvement? Không có số liệu về user retention rate hoặc engagement metrics sau khi dùng Firefly.
- **Tôi sẽ đề xuất họ làm thêm**: Vẽ diagram data flow cho cả 2 platforms để thấy rõ hơn sự khác biệt trong feedback loop. Thêm bảng so sánh định lượng: dữ liệu thu thập, frequency, và value cho model training.

**Điểm yếu 2** (từ 2A202600392 - Nguyễn Đông Hưng, Fiverr case):

- **Cụ thể**: Phần S5.4 Moat Strategy có ghi "Brand — Mạnh" nhưng không có bằng chứng định lượng về brand strength (NPS, brand recall survey, hoặc share of search).
- **Bằng chứng gì còn thiếu**: Link URL cụ thể đến survey/third-party brand ranking, và nên có thêm source thứ 2 để corroborate claim "Fiverr là brand quen thuộc của freelance gigs". Không có so sánh brand strength với Upwork.
- **Tôi sẽ đề xuất họ làm thêm**: Thêm trích dẫn full URL từ Interbrand/BrandZ brand ranking, hoặc ít nhất ghi rõ source từ Google Trends share of search comparison Fiverr vs Upwork.

---

## Phần 4 — Câu hỏi đặt cho thành viên khác

- **Cho 2A202600369 - Hồ Thị Tố Nhi (Adobe case)**: Nếu Adobe ra Firefly sớm hơn 8 tháng (ngay khi Midjourney public beta ra mắt), liệu họ có giữ được Creative growth momentum không? Hay việc bundling vào subscription flat-rate là mistake không thể sửa?

- **Cho 2A202600392 - Nguyễn Đông Hưng (Fiverr case)**: Trong phần 6 so sánh Fiverr vs Upwork, bạn nói Upwork phản ứng tốt hơn vì ra Uma AI từ 04/2024 — nhưng Upwork's core business (enterprise freelance) khác Fiverr's core (micro-gigs). Liệu đây có phải fair comparison không? Fiverr nên so sánh với đối thủ nào thì hợp lý hơn?

---

## Phần 5 — Điều tôi (Quách Ngọc Quang) rút ra cho bản thân

**Bài học 1**:

- **Tôi sẽ làm khác lần sau**: Khi phân tích case study disruption, không chỉ nhìn total revenue mà phải tách marketplace revenue vs services revenue — như Fiverr case cho thấy total revenue có thể tăng nhưng marketplace lõi đang chết dần.
- **Lý do**: Số liệu tổng có thể đánh lừa — cần drilling down vào từng business line để thấy real picture.

**Bài học 2**:

- **Tôi sẽ làm khác lần sau**: Khi làm moat analysis, không chỉ liệt kê 5 loại moat mà phải ranking từng moat theo strength (Strong/Medium/Weak) và chỉ ra moat nào đang bị tấn công trực tiếp bởi AI. Có bằng chứng định lượng (survey, ranking, trend data).
- **Lý do**: Mô hình 5 moat types là useful framework nhưng cần quantifiable assessment mới có actionable insights.

**Bài học 3**:

- **Tôi sẽ làm khác lần sau**: Luôn có phần so sánh với "đối thủ phản ứng tốt hơn" (như Upwork vs Fiverr, Canva vs Adobe) để show contrast — điều này làm bài phân tích có chiều sâu hơn là chỉ mô tả 1 chiều.
- **Lý do**: So sánh đối chiếu giúp làm rõ hơn tại sao 1 company phản ứng tốt hơn company khác — bài học kinh nghiệm cho sản phẩm mình đang phân tích.

---

## Checklist trước khi nộp

- [x] Phần 1 ghi rõ ≥ 2 thành viên đã quan sát (mã học viên + case + sản phẩm).
- [x] Phần 2 có ≥ 2 quan sát hay, gắn với thành viên cụ thể.
- [x] Phần 3 có ≥ 2 điểm yếu / câu hỏi chưa được trả lời.
- [x] Phần 4 có ≥ 2 câu hỏi cụ thể cho thành viên khác.
- [x] Phần 5 có ≥ 2 bài học rút ra, kèm lý do và cách áp dụng lần sau.

---