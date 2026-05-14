# Analysis Report Draft — Cursor vs GitHub Copilot

> File này là bản nội dung để dựng slide/export PDF. Theo yêu cầu hiện tại, chưa tạo `analysis-report.pdf`.

---

## Cover

- **Ngành**: [B] Lập trình
- **Sản phẩm A**: Cursor — https://www.cursor.com
- **Sản phẩm B**: GitHub Copilot — https://github.com/features/copilot
- **Nhiệm vụ chung**: "Viết hàm Python tính khoảng cách Levenshtein giữa 2 chuỗi, có kèm unit test và giải thích chi tiết phần xử lý edge cases."
- **Thành viên**:
  - 2A202600285 — Quách Ngọc Quang
  - 2A202600392 — Nguyễn Đông Hưng

---

## S1 — Product Moment

### Sản phẩm A: Cursor

- **Entry point**: Người dùng mở editor giống VS Code, dùng Chat panel hoặc phím tắt `Ctrl + L`.
- **Khoảnh khắc chính**: Prompt được nhập trực tiếp trong IDE, AI trả lời bằng code + test + giải thích ngay trong luồng làm việc.
- **Bằng chứng ảnh**:
  - `screenshots/01-cursor-entry.png`
  - `screenshots/02-cursor-input.png`

### Sản phẩm B: GitHub Copilot

- **Entry point**: Người dùng dùng Copilot Chat trong VS Code/GitHub, hoặc gợi ý inline trong file code.
- **Khoảnh khắc chính**: Copilot bám vào repository/editor context để đề xuất code, giải thích edge cases và có thể tạo file test.
- **Ảnh cần bổ sung trước khi export PDF**:
  - `screenshots/product-B-1-entry.png`
  - `screenshots/product-B-2-input.png`
  - `screenshots/product-B-3-output.png`

### Nhận định S1

Cursor thắng ở product moment vì AI là trung tâm của editor ngay từ đầu. GitHub Copilot thắng ở độ quen thuộc và distribution vì nằm trong hệ sinh thái GitHub/VS Code mà developer đã dùng sẵn.

---

## S2 — Workflow Evidence

### Trước khi có AI

Developer thường phải:

1. Google hoặc Stack Overflow cách viết Levenshtein distance.
2. Copy/paste code mẫu vào IDE.
3. Tự sửa edge cases như chuỗi rỗng, Unicode, phân biệt hoa/thường.
4. Tự viết unit test.
5. Chạy test và debug.

Ước tính workflow thủ công mất khoảng 10-15 phút với người đã biết Python, lâu hơn với người mới.

### Workflow với Cursor

1. Nhập prompt trực tiếp vào Chat panel trong IDE.
2. Cursor sinh code cho `levenshtein.py` và `test_levenshtein.py`.
3. Người dùng dùng "Apply" để chèn code vào file.
4. Chạy test trong terminal để kiểm chứng.

**Friction areas**:

- Chat output dài, người dùng vẫn phải biết tách file logic/test.
- Vẫn phải chạy test thủ công trong terminal.
- Nếu accept quá nhanh, developer có thể bỏ qua review thuật toán.

**Bằng chứng ảnh**:

- `screenshots/03-cursor-output-test.png`
- `screenshots/04-cursor-output-code.png`

### Workflow với GitHub Copilot

1. Mở VS Code/GitHub repository.
2. Dùng Copilot Chat với cùng prompt.
3. Copilot sinh code/test hoặc hướng dẫn sửa trong file hiện tại.
4. Developer dùng inline suggestions/chat edits để áp dụng.
5. Chạy test và chỉnh nếu có lỗi.

**Friction areas**:

- Copilot mạnh khi có file/repo context; nếu bắt đầu từ blank workspace, output có thể ít "trọn gói" hơn Cursor.
- Một số tính năng agent/chat phụ thuộc plan và IDE setup.
- Dễ bị phân tán vì Copilot nằm trong nhiều bề mặt: VS Code, GitHub web, CLI, pull request, code review.

### Nhận định S2

Cursor tối ưu cho workflow "AI pair programmer trong editor". Copilot tối ưu cho workflow "AI nằm trong hệ sinh thái dev có sẵn". Với task Levenshtein từ đầu, Cursor có lợi thế vì trải nghiệm prompt-to-files mạch lạc hơn.

---

## S3 — Output & Trust

### Cursor

- **Chất lượng output**: Rất cao. Hàm `levenshtein_distance` dùng type hints, xử lý input không hợp lệ và tối ưu bộ nhớ bằng mảng 1D/2 hàng thay vì ma trận 2D đầy đủ.
- **Edge cases**: Chuỗi rỗng, chuỗi giống nhau, phân biệt hoa/thường, Unicode tiếng Việt, input không phải string.
- **Trust signal**: Không có citation, nhưng có unit test để kiểm chứng bằng thực thi code.
- **Rủi ro**: Nếu test do AI tự sinh chưa đủ, output có thể "trông đúng" nhưng thiếu case quan trọng.

### GitHub Copilot

- **Chất lượng output kỳ vọng**: Cao với code phổ biến như Levenshtein, đặc biệt khi trong repo đã có convention test.
- **Edge cases cần kiểm tra**: Chuỗi rỗng, Unicode, chuỗi dài, input `None`, case-sensitive, performance.
- **Trust signal**: Tích hợp sâu với editor/GitHub giúp review diff, chạy test, tạo PR hoặc code review.
- **Rủi ro**: Copilot không cung cấp nguồn cho thuật toán; developer vẫn phải kiểm chứng bằng test.

### 6 tín hiệu đáng tin cần chấm

| Tín hiệu | Cursor | GitHub Copilot |
|---|---|---|
| Code chạy được | Có bằng chứng ảnh output/test | Cần bổ sung screenshot test |
| Edge cases | Có nhiều edge cases | Cần kiểm chứng khi test Copilot |
| Giải thích | Giải thích rõ bằng tiếng Việt | Thường giải thích tốt trong Copilot Chat |
| Citation/source | Không có | Không có |
| Dễ kiểm chứng | Có, qua unit test | Có, qua IDE/GitHub workflow |
| Context awareness | Mạnh trong workspace Cursor | Rất mạnh trong GitHub/VS Code ecosystem |

### Nhận định S3

Với code generation, "trust" không đến từ citation mà đến từ khả năng chạy test, đọc diff và review edge cases. Cursor tạo cảm giác tin nhanh hơn trong demo; Copilot có trust dài hạn tốt hơn khi gắn với repo thật, PR và review workflow.

---

## S4 — Business Signal

### Pricing và giới hạn

| Yếu tố | Cursor | GitHub Copilot |
|---|---|---|
| Free tier | Hobby/free với giới hạn agent/tab completions | Copilot Free có giới hạn |
| Individual paid | Pro $20/tháng | Copilot Pro $10/tháng |
| Higher individual tier | Pro+/Ultra cho agent-heavy users | Copilot Pro+ / premium requests tùy thời điểm |
| Team/business | Teams $40/user/tháng | Business $19/user/tháng; Enterprise $39/user/tháng |
| Nguồn | https://cursor.com/pricing | https://github.com/features/copilot/plans |

### Cost-Capability-Speed

| Tiêu chí | Cursor | GitHub Copilot |
|---|---|---|
| Cost | Đắt hơn cho cá nhân cơ bản ($20/tháng) | Rẻ hơn cho cá nhân cơ bản ($10/tháng) |
| Capability | Rất mạnh ở AI-native coding workflow, agent/edit/apply | Rất mạnh ở ecosystem, repo context, PR/review, enterprise |
| Speed | Nhanh khi bắt đầu task trong Cursor editor | Nhanh nếu team đã ở GitHub/VS Code |

### Business signal từ thị trường

- Cursor được Sacra ước tính đạt khoảng $200M ARR và khoảng 720,000 paying users trong giai đoạn 2024-2025, cho thấy developer sẵn sàng trả tiền cho AI-native IDE.
- Microsoft 2025 Annual Report ghi GitHub Copilot có hơn 20 triệu users và đã tiến hóa thành peer programmer.
- Copilot có distribution moat rất lớn vì gắn với GitHub, VS Code, Microsoft enterprise và developer workflow hiện hữu.

### Nhận định S4

Cursor có pricing power tốt với power users vì product moment rất mạnh. Copilot có business moat tốt hơn nhờ distribution và enterprise bundling. Nếu chỉ xét cá nhân làm bài code nhanh, Cursor đáng tiền hơn; nếu xét tổ chức và repo thật, Copilot có lợi thế kinh doanh lớn hơn.

---

## S5 — Product Judgment

### S5.1 Verdict

| Sản phẩm | Verdict | Lý do |
|---|---|---|
| Cursor | **Strong** | Product moment rõ, workflow AI-native, rất hợp với developer muốn từ prompt sang code/test nhanh. |
| GitHub Copilot | **Strong** | Distribution và ecosystem mạnh, phù hợp team/repo thật hơn là demo đơn lẻ. |

Kết luận ngắn: Cursor thắng ở trải nghiệm sử dụng tức thì; Copilot thắng ở moat và khả năng đi sâu vào workflow tổ chức.

### S5.2 User base + tăng trưởng

| Chỉ số | Cursor | GitHub Copilot |
|---|---|---|
| Users / paying users | Sacra ước tính khoảng 720,000 paying users khi đạt $200M ARR | Microsoft báo cáo hơn 20 triệu users |
| Revenue / ARR | Sacra ước tính khoảng $200M ARR | Sacra từng ước tính Copilot khoảng $400M ARR; Microsoft không tách revenue chính thức |
| Growth signal | Tăng nhanh trong nhóm AI coding tool | Enterprise adoption và GitHub/Microsoft distribution rất mạnh |
| Nguồn | https://sacra.com/research/cursor-at-200m-arr/ | https://www.microsoft.com/investor/reports/ar25/index.html |

Nhận định: Cursor có hypergrowth nhưng dựa trên ước tính bên thứ ba. Copilot có số user chính thức hơn và distribution rộng hơn.

### S5.3 Doanh thu / pricing power

| Yếu tố | Cursor | GitHub Copilot |
|---|---|---|
| Pricing power cá nhân | Cao: Pro $20/tháng, Pro+/Ultra cho heavy users | Tốt: Pro $10/tháng dễ vào, Business/Enterprise cho org |
| Pricing power enterprise | Đang tăng qua Teams/Enterprise | Rất mạnh nhờ GitHub/Microsoft procurement |
| Mức công khai | Pricing công khai; ARR là ước tính | Pricing công khai; user có nguồn Microsoft, revenue không tách rõ |

Nhận định: Cursor kiếm tiền tốt từ developer power users. Copilot có thể mở rộng doanh thu tốt hơn ở enterprise vì được mua theo seat trong tổ chức.

### S5.4 Moat phân tích

| Moat | Cursor | GitHub Copilot |
|---|---|---|
| Data moat | Trung bình: workspace/editor interaction | Cao hơn: GitHub repo, PR, issue, enterprise workflow |
| Network effect | Thấp-trung bình | Cao: GitHub developer ecosystem |
| Switching cost | Trung bình: quen Cursor workflow/rules | Cao hơn với tổ chức dùng GitHub/VS Code |
| Brand | Mạnh trong AI-native coding | Rất mạnh vì GitHub + Microsoft |
| Distribution | Trung bình, phải thuyết phục dev đổi editor | Rất mạnh, nằm trong GitHub/VS Code/enterprise |

Nhận định: Cursor có product moat; Copilot có distribution moat. Product moat có thể bị copy, nhưng distribution moat của Copilot khó bị phá hơn.

### S5.5 Data flywheel + feedback loop

| Câu hỏi | Cursor | GitHub Copilot |
|---|---|---|
| User action feed lại sản phẩm | Prompt, accept/reject edits, repo context, rules | Prompt, completions, PR/code review, repo context, enterprise feedback |
| Loop compounding? | Có một phần: workflow càng cá nhân hóa càng tốt | Có mạnh hơn nhờ GitHub ecosystem rộng |
| Feedback systematic? | Có usage dashboard/rules/hooks; chi tiết training không công khai đầy đủ | Có telemetry/product feedback; enterprise privacy tùy plan |
| Rủi ro | Nếu model nền bị commoditize, Cursor phải giữ UX/agent loop | Nếu AI bị ép vào quá nhiều bề mặt, user có thể thấy intrusive |

Nhận định: Cả hai đều phụ thuộc vào model nền, nên flywheel bền nhất không phải "model thông minh hơn" mà là context + workflow + habit.

### S5.6 Niche Down + AI Feature Map

#### Cursor

- **Niche**: AI-native IDE cho developer muốn code nhanh trong editor.
- **User Value**: Rất cao với cá nhân/power user.
- **User Alignment**: Cao nếu user muốn AI chủ động sửa code; thấp hơn nếu team yêu cầu governance chặt.
- **Business Value**: Cao vì willingness-to-pay $20+ rõ.

#### GitHub Copilot

- **Niche**: AI pair programmer nằm trong GitHub/VS Code/workflow tổ chức.
- **User Value**: Cao với developer trong repo thật.
- **User Alignment**: Cao với team dùng GitHub; có rủi ro nếu feature quá intrusive.
- **Business Value**: Rất cao vì enterprise seat expansion.

### S5.7 Spark → Loop → System

| Giai đoạn | Cursor | GitHub Copilot |
|---|---|---|
| Spark | Cảm giác wow khi chat sinh code/test và apply vào file | Gợi ý inline/chat giúp code nhanh hơn trong tool quen thuộc |
| Loop | Người dùng quay lại vì editor biến thành pair programmer | Người dùng quay lại vì Copilot gắn vào repo, PR, issue, review |
| System | Đang xây system qua rules, MCP, cloud agents, team features | Đã gần system hơn nhờ GitHub/Microsoft ecosystem |

Dự báo 12 tháng: Cursor cần chứng minh không chỉ là "better UX wrapper" mà là coding operating system. Copilot cần tránh cảm giác ép AI vào mọi nơi và phải giữ chất lượng review/code cao.

### S5.8 Liên hệ Lab 1 case Fiverr

Lab 1 cho thấy Fiverr bị AI ép ở các task freelance đơn giản vì buyer chuyển từ "thuê người làm task" sang "AI làm bản nháp ngay". Cursor và Copilot đang ở phía ngược lại: chính chúng là công cụ thay thế micro-task code trên marketplace.

Bài học áp dụng:

1. **Không chỉ output, mà workflow mới quyết định thắng**: Cursor thắng vì ở ngay editor; Copilot thắng vì ở ngay GitHub/VS Code.
2. **Moat phải nằm trong habit/context**: Fiverr mất buyer vì chat interface thay thế search marketplace; Copilot có lợi vì nằm trong repo workflow.
3. **Task đơn giản sẽ bị commoditize**: cả Cursor và Copilot phải đi lên agentic workflow, repo-scale context và team governance, không chỉ autocomplete.

---

## Nguồn tham khảo cho Lab 2

1. Cursor Pricing — https://cursor.com/pricing
2. Cursor usage/pricing docs — https://docs.cursor.com/en/account/usage
3. Sacra, Cursor at $200M ARR — https://sacra.com/research/cursor-at-200m-arr/
4. GitHub Copilot plans — https://github.com/features/copilot/plans
5. GitHub Copilot licenses — https://docs.github.com/en/billing/concepts/product-billing/github-copilot-licenses
6. Microsoft Annual Report 2025 — https://www.microsoft.com/investor/reports/ar25/index.html
7. Lab 1 final case Fiverr — `../01-bigtech-disruption/3-FINAL-case-analysis.md`

---

## Checklist trước khi export PDF

- [x] Có đủ S1-S5 theo template.
- [x] Có S5.1, S5.6, S5.7, S5.8.
- [x] Có phân tích S5.2-S5.5.
- [x] Có nguồn pricing/user/revenue/moat.
- [x] Có ảnh Cursor.
- [ ] Bổ sung ảnh GitHub Copilot thật: entry, input, output.
- [ ] Chuyển nội dung này thành slide deck và export `analysis-report.pdf`.
