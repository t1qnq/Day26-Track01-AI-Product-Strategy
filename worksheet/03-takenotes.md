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

## Phần 1 — Nhóm đã quan sát (≥ 2 nhóm khác)

| # | Tên nhóm / mã 2 học viên | Ngành | 2 sản phẩm họ test |
|---|---|---|---|
| 1 | 2A202600392 (Lab 1 cá nhân) | N/A | Case study: Fiverr bị AI disruption |
| 2 | Nhóm khác (chưa ghi nhận) | — | — |

---

## Phần 2 — Điều thấy hay từ nhóm khác

**Quan sát 1** (từ Lab 1 Fiverr case của đồng đội Nguyễn Đông Hưng):

- **Cụ thể họ đưa ra**: Phân tích timeline chi tiết từ ChatGPT ra mắt (30/11/2022) đến khi Fiverr phải cắt 30% nhân sự (09/2025), với 16 sources đã kiểm chứng. Đặc biệt có bảng số liệu so sánh trước/sau AI shock với active buyers giảm từ 4.217M → 2.907M.
- **Vì sao tôi thấy hay**: Cách vận dụng Lens 1 rất cụ thể — không chỉ nói "AI ảnh hưởng" mà chỉ rõ 3 shifts nào xảy ra (Shift 1: Do the work for me, Shift 5: Expect it now, Shift 4: Pay for output), và mỗi shift đều có bằng chứng số liệu đi kèm. Phần so sánh với Upwork (đối thủ phản ứng tốt hơn) cho thấy góc nhìn đa chiều.

**Quan sát 2** (từ nhóm Lab 2 Cursor vs Copilot của Quách Ngọc Quang & Nguyễn Đông Hưng):

- **Cụ thể họ đưa ra**: Framework S1-S5 mở rộng 8 mục con, đặc biệt phần S5.4 Moat Analysis đánh giá 5 loại moat (data/network/switching cost/brand/distribution) riêng cho từng sản phẩm. S5.7 Spark→Loop→System có dự báo 12 tháng tới rất cụ thể.
- **Vì sao tôi thấy hay**: Phân tích moat rất thực tế — không chỉ liệt kê mà còn chỉ ra moat nào "dễ bị copy" (Cursor's UX moat) vs moat nào "bền vững hơn" (Copilot's distribution moat trên GitHub ecosystem).

---

## Phần 3 — Điểm yếu / chỗ chưa thuyết phục

**Điểm yếu 1** (từ Lab 1 Fiverr case của đồng đội):

- **Cụ thể**: Phần S5.5 Data Flywheel chỉ mô tả "có một phần compounding" nhưng chưa phân tích sâu tại sao Fiverr's flywheel yếu hơn so với ChatGPT's flywheel.
- **Bằng chứng gì còn thiếu**: So sánh cụ thể về loại dữ liệu mà mỗi platform thu thập — Fiverr thu thập transaction data (order, review) trong khi ChatGPT thu thập interaction data (prompt, edit, accept/reject) — loại nào valuable hơn cho model improvement?
- **Tôi sẽ đề xuất họ làm thêm**: Vẽ diagram data flow cho cả 2 platforms để thấy rõ hơn sự khác biệt trong feedback loop.

**Điểm yếu 2** (từ Lab 2 Cursor vs Copilot của nhóm):

- **Cụ thể**: Phần S5.2 User Base có ghi "~720,000 paying users (ước tính)" cho Cursor nhưng nguồn chỉ ghi "Sacra" — không có link trực tiếp.
- **Bằng chứng gì còn thiếu**: Link URL cụ thể đến bài báo Sacra, và nên có thêm nguồn thứ 2 để corroborate con số này.
- **Tôi sẽ đề xuất họ làm thêm**: Thêm trích dẫn full URL trong slide deck credits, hoặc ít nhất ghi rõ ngày xuất bản bài báo Sacra để verify.

---

## Phần 4 — Câu hỏi đặt cho nhóm khác

- **Cho Lab 1 Fiverr case** (đồng đội Hưng): Nếu Fiverr phản ứng sớm hơn 6 tháng (ra AI workspace ngay giữa 2023 thay vì đầu 2025), liệu họ có giữ được marketplace momentum không? Hay cái chết của micro-gigs là không thể tránh?

- **Cho Lab 2 Cursor vs Copilot** (nhóm mình): Trong S5.7 dự báo Cursor sẽ chuyển sang "System" stage với Background Agents — nhưng nếu Microsoft tích hợp tương tự vào Copilot Workspace, Cursor có bị commoditize không? Moat nào của Cursor là thực sự defendable?

---

## Phần 5 — Điều tôi (Quách Ngọc Quang) rút ra cho bản thân

**Bài học 1**:

- **Tôi sẽ làm khác lần sau**: Khi phân tích case study disruption, không chỉ nhìn total revenue mà phải tách marketplace revenue vs services revenue — như Fiverr case cho thấy total revenue có thể tăng nhưng marketplace lõi đang chết dần.
- **Lý do**: Số liệu tổng có thể đánh lừa — cần drilling down vào từng business line để thấy real picture.

**Bài học 2**:

- **Tôi sẽ làm khác lần sau**: Khi làm moat analysis, không chỉ liệt kê 5 loại moat mà phải ranking từng moat theo strength (Strong/Medium/Weak) và chỉ ra moat nào đang bị tấn công trực tiếp bởi AI.
- **Lý do**: Mô hình 5 moat types là useful framework nhưng cần quantifiable assessment mới có actionable insights.

**Bài học 3**:

- **Tôi sẽ làm khác lần sau**: Luôn có phần so sánh với "đối thủ phản ứng tốt hơn" (như Upwork vs Fiverr) để show contrast — điều này làm bài phân tích có chiều sâu hơn là chỉ mô tả 1 chiều.
- **Lý do**: So sánh đối chiếu giúp làm rõ hơn tại sao 1 company phản ứng tốt hơn company khác — bài học kinh nghiệm cho sản phẩm mình đang phân tích.

---

## Checklist trước khi nộp

- [x] Phần 1 ghi rõ ≥ 2 nhóm đã quan sát (mã 2 học viên + ngành + sản phẩm).
- [x] Phần 2 có ≥ 2 quan sát hay, gắn với nhóm cụ thể.
- [x] Phần 3 có ≥ 2 điểm yếu / câu hỏi chưa được trả lời.
- [x] Phần 4 có ≥ 2 câu hỏi cụ thể cho nhóm khác.
- [x] Phần 5 có ≥ 2 bài học rút ra, kèm lý do và cách áp dụng lần sau.

---