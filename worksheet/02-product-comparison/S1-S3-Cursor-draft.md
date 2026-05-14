# Draft Slide Deck (Phần Cursor) - S1 đến S3

---

## Slide S1 — Product Moment (Khoảnh khắc sử dụng)

*   **Sản phẩm:** Cursor AI
*   **Ngành:** [B] Lập trình
*   **Nhiệm vụ chung:** "Viết hàm Python tính khoảng cách Levenshtein giữa 2 chuỗi, có kèm unit test và giải thích chi tiết phần xử lý edge cases."
*   **Entry Point (Điểm bắt đầu):** 
    *   Giao diện quen thuộc (fork từ VS Code), giúp lập trình viên không phải thay đổi môi trường.
    *   Người dùng kích hoạt AI thông qua khung Chat ở sidebar bên phải (hoặc phím tắt `Ctrl + L`).
    *   *Ảnh tham chiếu:* `01-cursor-entry.png` và `02-cursor-input.png`.

---

## Slide S2 — Workflow Evidence (Bằng chứng luồng làm việc)

*   **Trước khi có AI:** Lập trình viên phải mở trình duyệt -> Google -> Stack Overflow -> Đọc thread -> Copy code -> Paste vào IDE -> Tự viết thêm Unit Test. (Mất 10-15 phút).
*   **Workflow hiện tại (Với Cursor):**
    *   **Bước 1:** Gõ prompt trực tiếp vào Chat panel trong IDE.
    *   **Bước 2:** AI lập tức phân tích và sinh ra code cho cả file hàm (`levenshtein.py`) và file test (`test_levenshtein.py`).
    *   **Bước 3:** Lập trình viên dùng tính năng "Apply" để chèn code thẳng vào file mà không cần copy/paste thủ công.
*   **Friction Areas (Điểm ma sát):**
    *   Giao diện Chat panel sinh ra đoạn code khá dài, người dùng vẫn phải biết cách tổ chức thư mục (tách file test và file logic).
    *   Phải gõ lệnh chạy test thủ công trong Terminal (`python -m unittest...`) theo hướng dẫn của AI.
    *   *Ảnh tham chiếu:* `03-cursor-output-test.png` và `04-cursor-output-code.png`.

---

## Slide S3 — Output & Trust (Kết quả và Độ tin cậy)

*   **Chất lượng Output (Đánh giá: Rất cao):**
    *   Hàm thuật toán `levenshtein_distance` được tối ưu bộ nhớ (chỉ dùng mảng 1D/2 hàng thay vì ma trận đầy đủ 2D).
    *   Có Type Hinting đầy đủ (`a: str, b: str -> int`).
    *   Bắt lỗi Exception rõ ràng (bắt `TypeError` nếu truyền vào `None` hoặc `bytes`).
*   **Kiểm soát Edge Cases (Tín hiệu đáng tin):**
    *   AI sinh ra đầy đủ bộ Unit Test cho các trường hợp góc: chuỗi rỗng (`""`), case phân biệt hoa/thường, và đặc biệt là xử lý chuỗi Unicode (tiếng Việt có dấu).
    *   AI giải thích cặn kẽ 8 điểm edge cases bằng tiếng Việt rất chuẩn xác bên cửa sổ Chat.
*   **Dẫn nguồn (Citation):**
    *   Cursor không cung cấp link dẫn nguồn (vì nó là mô hình sinh code nội bộ), nhưng nó xây dựng niềm tin bằng cách cho phép thực thi unit test để tự chứng minh tính đúng đắn của code (Code Verification thay vì Citation).

---
