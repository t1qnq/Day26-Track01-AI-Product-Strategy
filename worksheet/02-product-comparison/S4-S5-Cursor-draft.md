# Draft Slide Deck (Phần Cursor) - S4 và S5 (8 mục con)

Dưới đây là nội dung dự thảo cho các slide S4 và S5 (bao gồm 8 mục con mở rộng) dành riêng cho sản phẩm **Cursor**. Bạn có thể đưa vào slide deck, phần của GitHub Copilot sẽ do đồng đội của bạn điền thêm vào bảng so sánh.

---

## Slide S4 — Business Signal (Tín hiệu kinh doanh)

*   **Sản phẩm:** Cursor
*   **Pricing Strategy:** Freemium (Miễn phí có giới hạn) & Premium.
    *   **Bản Free:** Giới hạn lượt dùng các model thông minh nhất (Claude 3.5 Sonnet / GPT-4o) kèm theo slow requests.
    *   **Bản Pro:** **$20/tháng** (Chuẩn giá ngành AI B2C). Cung cấp 500 fast premium requests.
*   **Cost-Capability-Speed:** Trả $20/tháng để đổi lấy tốc độ gõ code nhanh gấp 2-3 lần (Speed) và khả năng xử lý context toàn dự án (Capability) mà con người không thể tự nhớ hết.
*   *Ảnh tham chiếu:* `product-A-5-pricing.png`

---

## Slide S5 — Product Judgment (Đánh giá chuyên sâu 8 chiều)

### S5.1 Verdict (Phán quyết)
*   **Cursor:** **Strong (Mạnh mẽ)**. Đây là công cụ AI-native đột phá nhất cho lập trình viên hiện tại, tạo ra trải nghiệm "Flow state" mượt mà nhờ tích hợp sâu vào workflow.

### S5.2 User base + Tăng trưởng (Định lượng)
*   **Cursor:** Tăng trưởng bùng nổ trong năm 2024 thông qua truyền miệng (Word of mouth). Định giá công ty vọt lên mức 2 tỷ USD vào giữa năm 2024. *(Số liệu user/MAU chính xác không có nguồn công khai chính thức)*.

### S5.3 Doanh thu / Pricing power
*   **Pricing power của Cursor rất mạnh.** Lập trình viên sẵn sàng trả $20/tháng (thậm chí tự bỏ tiền túi cá nhân chứ không đợi công ty cấp) vì giá trị mang lại trực tiếp đo đếm được bằng thời gian tiết kiệm. Doanh thu ước tính đạt hàng chục triệu USD ARR chỉ trong thời gian rất ngắn.

### S5.4 Moat phân tích (Hào phòng thủ)
*   **Switching Cost (Chi phí chuyển đổi) - RẤT MẠNH:** Cursor fork trực tiếp từ VS Code. Người dùng có thể import toàn bộ extension, theme, phím tắt từ VS Code sang Cursor chỉ bằng 1 cú click. Chuyển đổi không ma sát.
*   **Distribution (Kênh phân phối) - YẾU:** Không có sẵn kênh phân phối B2B lớn như Microsoft (công ty mẹ của GitHub Copilot). Cursor hoàn toàn dựa vào Product-Led Growth (PLG).
*   **Dễ bị copy không?** Giao diện Chat có thể bị copy (như Copilot Chat), nhưng tính năng cốt lõi như Composer (tự sửa nhiều file cùng lúc) và Cursor Tab (Dự đoán dòng tiếp theo) đòi hỏi hạ tầng custom model routing rất khó bắt chước.

### S5.5 Data flywheel + Feedback loop
*   **Hành động feed model:** Mỗi khi user nhấn `Tab` để accept code, hoặc gõ tiếp để sửa code mà Cursor vừa sinh ra (reject).
*   **Loop có compounding không?** Có. Dữ liệu ngầm này (implicit feedback) giúp Cursor tinh chỉnh các mô hình dự đoán (shadow models) ngày càng mượt hơn.
*   **Thu thập feedback:** Hệ thống tự động đo lường tỷ lệ chấp nhận code (Acceptance Rate) cực kỳ sát sao.

### S5.6 Niche Down + AI Feature Map
*   **Niche của Cursor rất rõ ràng:** "Lập trình viên muốn AI hiểu toàn bộ codebase của họ thay vì chỉ một file hiện tại".
*   **User Value:** Tiết kiệm thời gian đọc hiểu code cũ.
*   **Business Value:** Giữ chân user ở lại IDE càng lâu càng tốt, biến IDE thành điểm truy cập AI duy nhất.

### S5.7 Spark → Loop → System
*   **Giai đoạn hiện tại:** Cursor đang ở mức **Loop** (người dùng tương tác qua lại liên tục với AI qua `Cmd+K` và `Composer`).
*   **Dự báo 12 tháng tới:** Chuyển sang mức **System** (Background Agents). Người dùng chỉ cần gõ yêu cầu lớn (VD: "Đổi toàn bộ UI sang Dark Mode"), AI sẽ chạy ngầm dưới background, tự mở file, tự sửa lỗi, tự chạy test và chỉ báo cáo khi hoàn thành.

### S5.8 Liên hệ Lab 1 case (Stack Overflow)
*   Cursor chính là "Kẻ hủy diệt" (Lực lượng số 2 - Startup xây AI chuyên biệt) đã tạo ra Big Squeeze bóp nghẹt mô hình B2C của Stack Overflow.
*   **Bài học từ Lab 1 áp dụng vào đây:** Kỳ vọng của người dùng đã vĩnh viễn chuyển sang Shift #1 (Do the work for me) và Shift #7 (Tool sees context). Sản phẩm nào bắt được 2 Shift này (như Cursor) sẽ thắng, sản phẩm nào bắt người dùng phải copy-paste (như Stack Overflow) sẽ sụp đổ.

---
