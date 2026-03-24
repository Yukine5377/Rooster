# Lịch sử khơi gợi — App sửa giọng nói (lần đầu)

**Ngày:** 2026-03-24  
**Nguồn:** Product Owner / Stakeholder (nội dung chat)  
**Chủ đề:** Vision & phạm vi sản phẩm greenfield

---

## Định hướng sản phẩm (đã xác nhận)

Stakeholder mô tả một ứng dụng hỗ trợ **cải thiện giọng nói / kỹ năng nói**, trong đó người dùng **ghi âm giọng của mình trong app** (hoặc import file). Sau đó hệ thống **phân tích** bản ghi, trả về điểm số và nhận xét theo các đầu mục giọng nói. Dựa trên phân tích, app **tạo các bài tập nói phù hợp**. Người dùng có thể **đặt mục tiêu**; **AI** đảm nhiệm việc **tạo các bài học/lộ trình** nhằm **đạt các mục tiêu** đã đặt.

**Phân biệt:** Dự án là *greenfield* (chưa nêu hệ thống cũ cần thay thế), nhưng đã có thông tin rõ về đối tượng người dùng, phạm vi MVP và mô hình vận hành.

---

## Luồng nghiệp vụ mức khái niệm (đã làm rõ ở mức business)

| STT | Ai | Việc | Ghi chú |
|:---:|:---|:---|:---|
| 1 | Người dùng | Chọn tình huống và ghi âm hoặc import audio | Có giới hạn độ dài, chia theo tình huống luyện tập |
| 2 | Hệ thống | Phân tích bản ghi | Trả điểm số + nhận xét theo các yếu tố nói (trừ từ vựng), so với mẫu chuẩn |
| 3 | Hệ thống | Sinh/đề xuất bài tập phù hợp | Bài tập gồm: đọc văn bản, đối thoại tình huống, lặp theo mẫu; định hướng 100 tình huống |
| 4 | Người dùng | Thiết lập và theo đuổi mục tiêu | Không giới hạn số mục tiêu song song |
| 5 | AI | Cập nhật lộ trình định kỳ | Điều chỉnh sau mỗi 2 ngày và giải thích lý do giao bài |
| 6 | Người dùng | Theo dõi kết quả | Xem % giống giọng mẫu, tiến bộ theo thời gian, nghe lại audio |
| 7 | Người dùng/Admin | Xử lý gợi ý sai | Người dùng report; admin review và cập nhật nội dung/câu hỏi |

---

## Pain points (đã xác nhận)

- Người dùng mục tiêu mặc cảm về giọng nói.
- Người dùng nói sai và thiếu phản hồi khách quan để tự sửa.
- Người dùng sợ nói trước đám đông.

---

## Tài liệu / artifact cần xin thêm (khi có)

- Danh sách 100 tình huống dự kiến hoặc khung phân nhóm tình huống.
- Bộ tiêu chí chấm điểm chi tiết cho từng đầu mục giọng nói.
- Danh sách giọng mẫu chuẩn (coach) được phép sử dụng.
- Chính sách pháp lý chi tiết cho tài khoản trẻ em (flow phụ huynh đăng ký/đồng ý).
- Chính sách xử lý dữ liệu train model (consent, retention, xóa dữ liệu).

---

## Câu hỏi mở (xem file tracking)

`Elicitation/listQA/voice-speech-coaching-app.md` — đã chốt các follow-up VC-022, VC-023, VC-024.

---

## Ghi nhận bổ sung về sản phẩm & vận hành

- **Người dùng chính:** học sinh, sinh viên (ưu tiên MVP).
- **Ngôn ngữ:** MVP tiếng Việt, sau đó mở rộng tiếng Anh.
- **Mô hình học:** 100% tự học (không coach người thật).
- **Khác biệt cạnh tranh mong muốn:** giá rẻ, tiện dùng, riêng tư, theo dõi tiến bộ rõ rệt.
- **Doanh thu:** mua trọn đời hoặc subscription theo tuần.
- **NFR:** độ trễ tối đa 3 phút; hỗ trợ offline; mobile-only (ưu tiên iOS rồi Android).
- **Tích hợp:** SSO, lịch nhắc luyện.
- **Bổ sung hệ thống:** có web admin để quản lý nội dung, user và subscription.
- **Phạm vi admin nội dung:** quản trị ngân hàng bài tập, tình huống, giọng mẫu, rubric, template AI, duyệt nội dung; không yêu cầu versioning nội dung ở phạm vi câu hỏi VC-022.
- **Dashboard chỉ số admin:** last used, current user, peak user, churn rate, bounce rate, LTV.
- **Quy trình report AI:** SLA 72h; chỉ super admin duyệt; khi cần cập nhật cả bộ liên quan; có audit log và rollback; không gửi thông báo phản hồi cho user.
