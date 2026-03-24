# Khơi gợi yêu cầu — App sửa giọng nói (Voice / Speech coaching)

**Dự án:** App ghi âm → phân tích → bài tập nói → mục tiêu → AI lộ trình học  
**Nguồn Ground Truth:** Product Owner / Stakeholder (chat 2026-03-24)  
**Loại dự án:** Greenfield (chưa mô tả hệ thống cũ cần thay thế)

---

## 🔎 Phân tích sơ bộ (BA)

- **Thực thể cốt lõi:** Người học, Bản ghi giọng, Phân tích giọng (metrics/feedback), Bài tập nói, Mục tiêu học tập, Bài học / lộ trình do AI sinh.
- **Ambiguity zones:** Đối tượng người dùng (B2C vs B2B, độ tuổi); “sửa giọng” theo nghĩa ngữ âm / giọng điệu / phát âm / hùng biện; tiêu chí đánh giá và chuẩn tham chiếu; mô hình AI (on-device vs cloud); quy định dữ liệu giọng nói và trẻ em.

---

## Bảng theo dõi câu hỏi

| ID | Mục | Trạng thái | Câu hỏi / chủ đề | Câu trả lời tham khảo / kết quả |
|:---|:---|:---:|:---|:---|
| VC-001 | Tầm nhìn sản phẩm | ✅ | App cho phép ghi giọng, phân tích, tạo bài tập nói tương ứng; người dùng đặt mục tiêu; AI tạo bài học để đạt mục tiêu | Đã xác nhận từ stakeholder (chat) |
| VC-002 | Vấn đề / pain cụ thể | ✅ | Người dùng mục tiêu đang gặp khó khăn gì hôm nay (thiếu phản hồi, không biết luyện gì, sợ nói trước đám đông…)? | Người dùng mục tiêu mặc cảm về giọng nói, nói sai, sợ nói trước đám đông |
| VC-003 | Phân khúc & đối tượng | ✅ | Ai là người dùng chính (sinh viên, MC, người đi làm quốc tế, trẻ em, người khuyết tật ngôn ngữ…)? Có nhóm ưu tiên MVP không? | Người dùng chính: học sinh, sinh viên; đây là nhóm ưu tiên cho MVP |
| VC-004 | Định nghĩa “sửa giọng” | ✅ | Sản phẩm tập trung vào nhánh nào: phát âm/từ vựng, ngữ điệu/ngắt nghỉ, tốc độ/rõ ràng, hơi thở/giọng rung, hay tổng hợp? | Tập trung tất cả yếu tố nói ngoại trừ từ vựng |
| VC-005 | Ngôn ngữ & giọng địa phương | ✅ | Hỗ trợ ngôn ngữ nào ở MVP? Có cần nhận diện accent / so sánh với bản ngữ không? | MVP: tiếng Việt; giai đoạn tiếp theo: tiếng Anh |
| VC-006 | Luồng: Ghi âm | ✅ | Giới hạn độ dài, định dạng file, ghi trong app hay import từ máy? Có cần ghi song song với nhạc nền / phòng họp không? | Ghi âm có giới hạn độ dài, chia theo tình huống; hỗ trợ cả ghi trực tiếp và import file |
| VC-007 | Luồng: Phân tích | ✅ | Phân tích cần trả về những loại output nào (điểm số, waveform, từ sai, gợi ý bài tập, so sánh với mẫu chuẩn)? | Trả về điểm số + nhận xét theo các đầu mục tại VC-004; so sánh với mẫu chuẩn; cho phép chọn/import giọng mẫu từ một số người |
| VC-008 | Chuẩn & metric | ✅ | Có chuẩn ngoài (CEFR, thang nội bộ, mẫu giọng “coach”) hay hoàn toàn tương đối theo tiến bộ cá nhân? | Dùng mẫu giọng coach và so với tiến bộ của chính người dùng theo thời gian |
| VC-009 | Bài tập nói | ✅ | Bài tập là đọc theo văn bản, đối thoại tình huống, lặp theo mẫu, game hóa? Ai/Cách tạo nội dung bài tập? | Gồm đọc văn bản, đối thoại tình huống, lặp theo mẫu; hệ thống giả lập 100 tình huống (kịch bản sẽ quyết định sau) |
| VC-010 | Mục tiêu người dùng | ✅ | Mục tiêu theo dạng nào (SMART, preset “chuẩn bị thuyết trình”, deadline, KPI giọng)? Có giới hạn số mục tiêu song song? | Không giới hạn số mục tiêu |
| VC-011 | AI lộ trình | ✅ | Lộ trình do AI điều chỉnh theo tiến độ thế nào (sau mỗi bài, hàng tuần)? Có cần giải thích “vì sao app giao bài này”? | Điều chỉnh sau mỗi 2 ngày; có cơ chế giải thích lý do giao bài |
| VC-012 | Coach người thật | ✅ | Có tích hợp huấn luyện viên người (review bản ghi, chat) hay 100% tự học? | 100% tự học |
| VC-013 | Cạnh tranh & thay thế | ✅ | Người dùng hiện đang dùng gì (YouTube, khóa offline, app khác)? Điểm khác biệt mong muốn? | Người dùng hiện dùng YouTube và khóa offline; khác biệt mong muốn: giá rẻ, tiện dùng, riêng tư, theo dõi tiến bộ rõ rệt |
| VC-014 | Mô hình kinh doanh | ✅ | Freemium, subscription, mua lẻ gói bài, B2B cho trường/doanh nghiệp? | Mua trọn đời hoặc subscription theo tuần |
| VC-015 | Quyền riêng tư & dữ liệu giọng | ✅ | Audio lưu ở đâu, bao lâu, có dùng để train model không, có xóa được không, có chế độ chỉ xử lý trên máy? | Audio lưu theo tài khoản vĩnh viễn; có dùng để train model; cho phép xóa; không xử lý on-device |
| VC-016 | Pháp lý & trẻ em | ✅ | Có nhắm độ tuổi dưới 13/16? Yêu cầu consent phụ huynh, vùng pháp lý (GDPR, v.v.)? | Có thể nhắm nhóm tuổi nhỏ; phụ huynh phải đăng ký tài khoản |
| VC-017 | Phi chức năng | ✅ | Yêu cầu độ trễ phân tích, offline mode, đa nền tảng (iOS/Android/Web) ưu tiên thứ tự nào? | Độ trễ tối đa 3 phút; có offline; mobile-only, ưu tiên iOS rồi Android |
| VC-018 | Tích hợp | ✅ | Cần đăng nhập SSO, calendar, nhắc lịch luyện, chia sẻ tiến độ mạng xã hội? | Cần tích hợp SSO và lịch nhắc luyện |
| VC-019 [NEW · 2026-03-24] | MVP scope | ✅ | Trong 3 tháng đầu, nhất thiết phải có tính năng nào và có thể cắt tính năng nào? | Bắt buộc có: ghi âm, tạo bài học, thực hiện bài học, so sánh % giống giọng mẫu, so sánh tiến bộ, cho phép nghe lại |
| VC-020 [NEW · 2026-03-24] | Rủi ro AI | ✅ | Khi AI phân tích sai hoặc gợi ý không phù hợp, mong muốn xử lý UX và escalation thế nào? | Người dùng nhấn nút report; admin review và cập nhật lại câu hỏi/nội dung |
| VC-021 [NEW · 2026-03-24] | Kênh quản trị | ✅ | Có cần hệ thống quản trị riêng cho nội dung và vận hành không? | Có: bổ sung web admin để quản lý nội dung |
| VC-022 [FOLLOW-UP · 2026-03-24] | Web admin phạm vi nội dung | ✅ | Admin cần quản trị những gì: ngân hàng bài tập, 100 tình huống, mẫu giọng coach, rubric chấm điểm, template bài học AI? | Chọn tất cả mục đã nêu trừ versioning/rollback (mục 7); bổ sung dashboard/admin analytics |
| VC-023 [FOLLOW-UP · 2026-03-24] | User & subscription admin | ✅ | Web admin cần thao tác gì với user/subscription: tạo/sửa/khóa tài khoản, hoàn tiền, đổi gói, xem lịch sử thanh toán, phân quyền CSKH? | Quản lý danh sách user và gói; theo dõi các chỉ số: last used, current user, peak user, churn rate, bounce rate, LTV |
| VC-024 [FOLLOW-UP · 2026-03-24] | Quy trình xử lý report AI | ✅ | SLA xử lý report là bao lâu, ai duyệt thay đổi nội dung, có cần versioning/audit log khi cập nhật câu hỏi hoặc kịch bản không? | SLA 72h; chỉ super admin được duyệt thay đổi; khi cần thiết cập nhật cả bộ liên quan; có audit log và cho phép rollback; không gửi thông báo phản hồi cho user |

---

## 📋 Changelog

| Ngày | Hành động | Nội dung tóm tắt |
|:---|:---|:---|
| 2026-03-24 | Tạo file | Khởi tạo tracking từ mô tả vision stakeholder (chat); VC-001 ✅; bổ sung câu hỏi gap VC-002…VC-020 |
| 2026-03-24 | Cập nhật từ stakeholder chat | Xác nhận VC-002…VC-021 thành ✅; bổ sung follow-up VC-022…VC-024 cho web admin/user/subscription/report workflow |
| 2026-03-24 | Cập nhật follow-up web admin | Xác nhận VC-022 và VC-023; chưa chốt VC-024 (SLA/quy trình duyệt/audit log xử lý report AI) |
| 2026-03-24 | Chốt follow-up report AI | Xác nhận VC-024: SLA 72h, duyệt bởi super admin, có audit log + rollback, không gửi phản hồi xử lý cho user |
