# Tóm tắt khơi gợi — App sửa giọng nói

**Cập nhật:** 2026-03-24

## Đã xác nhận (Ground Truth)

- Ứng dụng cho phép người dùng **ghi giọng nói** vào app.
- Hệ thống **phân tích** giọng / nói sau khi ghi.
- Từ kết quả phân tích, tạo **bài tập nói tương ứng**.
- Người dùng có thể **đặt mục tiêu** học tập / cải thiện.
- **AI** sinh **bài học / lộ trình** hướng tới mục tiêu đó.
- Người dùng mục tiêu: **học sinh/sinh viên**, thường mặc cảm về giọng, nói sai, sợ nói trước đám đông.
- Phạm vi “sửa giọng”: toàn bộ yếu tố nói (trừ từ vựng).
- MVP ngôn ngữ: **tiếng Việt**; giai đoạn sau mở rộng **tiếng Anh**.
- Phân tích trả về điểm số + nhận xét, so sánh mẫu chuẩn; hỗ trợ chọn/import giọng mẫu.
- Chuẩn đánh giá: dựa trên giọng coach + theo dõi tiến bộ cá nhân theo thời gian.
- Bài tập: đọc văn bản, đối thoại tình huống, lặp theo mẫu; mục tiêu 100 tình huống mô phỏng.
- Điều chỉnh lộ trình AI mỗi 2 ngày, có cơ chế giải thích.
- Mô hình vận hành: 100% tự học (không coach người thật).
- Giá trị khác biệt: giá rẻ, tiện dùng, riêng tư, theo dõi tiến bộ rõ rệt.
- Mô hình doanh thu: mua trọn đời hoặc subscription theo tuần.
- Dữ liệu audio lưu vĩnh viễn theo tài khoản, dùng để train model, có quyền xóa, không xử lý on-device.
- Có thể phục vụ nhóm tuổi nhỏ; phụ huynh phải đăng ký tài khoản.
- NFR: độ trễ tối đa 3 phút, hỗ trợ offline, mobile-only (ưu tiên iOS rồi Android).
- Tích hợp yêu cầu: SSO và lịch nhắc luyện.
- MVP bắt buộc: ghi âm, tạo & thực hiện bài học, so sánh % giống mẫu, so sánh tiến bộ, nghe lại.
- Luồng xử lý AI sai: người dùng report, admin review và cập nhật nội dung.
- Bổ sung yêu cầu: có **web admin** quản lý nội dung, user và subscription.
- Web admin nội dung: chọn tất cả nhóm quản trị đã đề xuất, trừ versioning/rollback cho nội dung.
- Web admin user/subscription: theo dõi `last used`, `current user`, `peak user`, `churn rate`, `bounce rate`, `LTV`.
- Report AI: SLA 72h; chỉ super admin duyệt; khi cần cập nhật cả bộ liên quan; có audit log + rollback; không gửi thông báo phản hồi cho user.

## Chưa làm rõ (ưu tiên vòng tiếp theo)

- Định nghĩa công thức tính và nguồn dữ liệu cho từng chỉ số admin (`churn`, `bounce`, `LTV`).
- Chi tiết permission matrix trong web admin (super admin, admin thường, CSKH...).
- Điều kiện chính xác cho chế độ offline và chiến lược đồng bộ lại khi online.

**File chi tiết:** `Elicitation/listQA/voice-speech-coaching-app.md`
