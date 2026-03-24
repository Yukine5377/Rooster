# PRD: Voice Speech Coaching App

**Version:** 1.0  
**Ngày tạo:** 24/03/2026  
**PO/PM / BA:** Stakeholder + AI BA Assistant  
**Status:** Draft  

---

## 1. Tổng quan (Overview)

### 1.1 Problem Statement
Học sinh/sinh viên thường mặc cảm về giọng nói, nói sai và sợ nói trước đám đông. Họ đang học qua YouTube/khóa offline nhưng thiếu phản hồi định lượng, thiếu lộ trình cá nhân hóa và khó theo dõi tiến bộ.

### 1.2 Product Vision
Xây dựng ứng dụng mobile AI-first giúp người học tự luyện nói riêng tư, chi phí hợp lý, có phản hồi rõ ràng theo từng yếu tố giọng nói và theo dõi tiến bộ dài hạn. Sau 1-2 năm, sản phẩm trở thành nền tảng luyện nói cá nhân hóa hàng ngày cho học sinh/sinh viên tại Việt Nam và mở rộng tiếng Anh.

### 1.3 Mục tiêu (Goals)
- **Business goal:** Tạo sản phẩm học nói có khả năng scale bằng AI và mô hình thu phí linh hoạt (lifetime + weekly subscription).
- **User goal:** Cải thiện giọng nói có thể đo lường, tự tin nói trước đám đông, luyện tập mọi lúc trên mobile.
- **Non-goal:** Không tập trung dạy từ vựng ở giai đoạn MVP; không có coach người thật trong MVP.

### 1.4 Success Metrics (KPIs)
| Metric | Baseline | Target | Thời hạn |
|--------|----------|--------|----------|
| % user hoàn thành >= 3 bài/tuần | Chưa có | >= 40% | 3 tháng sau launch |
| Tỷ lệ user quay lại tuần 4 | Chưa có | >= 30% | 3 tháng sau launch |
| % report AI xử lý đúng SLA 72h | Chưa có | >= 95% | Từ tháng vận hành đầu tiên |
| Tỷ lệ user thấy tiến bộ sau 30 ngày (self-report + score trend) | Chưa có | >= 70% | 3 tháng sau launch |

---

## 2. Quy trình nghiệp vụ (Business Processes)

### 2.1 Hiện trạng (AS-IS Process)
* Người dùng tự học phân mảnh qua YouTube/khóa offline.
* **Pain points gốc rễ**: thiếu phản hồi khách quan, thiếu cá nhân hóa, khó theo dõi tiến bộ, chi phí và tiện dụng chưa tối ưu.
* Đính kèm phân tích AS-IS: `Analysis/ba-process-analysis-voice-speech-coaching.md`

### 2.2 Quy trình đề xuất (TO-BE Process)
* Quy trình mới: mục tiêu -> ghi âm/import -> AI phân tích -> so sánh mẫu chuẩn + baseline -> AI giao bài -> theo dõi tiến bộ -> report khi cần.
* Sơ đồ flow chi tiết: `Analysis/ba-process-proposal-voice-speech-coaching.md`
* TO-BE giải quyết pain points bằng phản hồi định lượng, lộ trình cá nhân hóa, tracking tiến bộ và cơ chế kiểm soát chất lượng AI.

---

## 3. Stakeholders & Users

### 3.1 Stakeholders
| Vai trò | Tên/Team | Trách nhiệm |
|---------|----------|-------------|
| Product Owner | Business Owner | Quyết định phạm vi và ưu tiên sản phẩm |
| BA/PM | Product Team | Đặc tả yêu cầu, quản lý scope |
| Tech Lead | Engineering | Thiết kế kiến trúc, đánh giá feasibility |
| AI Engineer | ML Team | Phân tích giọng nói, recommendation |
| Super Admin | Operations | Duyệt xử lý report AI, phê duyệt cập nhật |
| Admin | Content/Ops | Quản trị nội dung, user, subscription, dashboard |

### 3.2 Target Users / Personas
**Persona 1: Học sinh/Sinh viên thiếu tự tin nói**
- **Mô tả:** 16-24 tuổi, thường xuyên cần thuyết trình hoặc giao tiếp học tập.
- **Pain points:** Mặc cảm giọng nói, nói sai, sợ nói trước đám đông.
- **Goals:** Nói rõ ràng hơn, tự tin hơn, có lộ trình luyện tập cụ thể.
- **Behavior:** Dùng mobile nhiều, thích học ngắn theo tình huống, nhạy cảm về chi phí.

### 3.3 User Journey (Happy Path)
1. User đăng nhập bằng SSO.
2. User tạo mục tiêu luyện nói và chọn tình huống.
3. User ghi âm hoặc import audio.
4. AI phân tích và trả điểm + nhận xét (<= 3 phút).
5. User xem so sánh với giọng mẫu + tiến bộ cá nhân.
6. AI giao bài học tiếp theo và giải thích lý do.
7. User luyện tập tiếp, nghe lại và theo dõi tiến bộ.

---

## 4. Mô hình tổng quan sản phẩm (Product Overview Model)

![Mô hình tổng quan sản phẩm](assets/pms_infographic.png)
*Mô tả: Có thể bổ sung infographic ở bước riêng theo workflow `/ba-infographic-gen`.*

| Tên thành phần | Ý nghĩa / Vai trò |
|----------------|-------------------|
| Mobile App | Kênh học chính cho user (iOS -> Android) |
| AI Analysis Engine | Chấm điểm và nhận xét giọng nói |
| Recommendation Engine | Sinh bài học/lộ trình theo mục tiêu |
| Voice Storage | Lưu audio theo tài khoản, hỗ trợ xóa |
| Web Admin Portal | Quản trị nội dung, user/subscription, dashboard |
| Super Admin | Duyệt xử lý report, kiểm soát chất lượng thay đổi |

---

## 5. Phạm vi dự án & Lộ trình (Scope & Roadmap)

### 4.1 Deployment Roadmap (Lộ trình triển khai tổng thể)
| Phase | Tên giai đoạn / Mục tiêu chính | Thời gian dự kiến |
|-------|--------------------------------|-------------------|
| Phase 1 (MVP) | Core loop luyện nói + web admin cơ bản | Q2/2026 |
| Phase 2 | Mở rộng Android + nâng cao analytics/subscription ops | Q3/2026 |
| Phase 3 | Mở rộng tiếng Anh + tối ưu AI quality/recommendation | Q4/2026 |

### 4.2 Triển khai trong Giai đoạn gần nhất (In-Scope - Phase 1 MVP)
- Đăng nhập SSO, onboarding user (bao gồm luồng minor cần phụ huynh đăng ký).
- Ghi âm/import audio có giới hạn độ dài.
- AI phân tích: điểm + nhận xét theo các tiêu chí giọng nói (trừ từ vựng).
- So sánh với giọng mẫu coach và baseline cá nhân.
- AI tạo bài học, cập nhật lộ trình mỗi 2 ngày có giải thích.
- Bài tập: đọc văn bản, đối thoại tình huống, lặp theo mẫu.
- Theo dõi % giống mẫu, tiến bộ theo thời gian, nghe lại audio.
- Report AI sai + xử lý bởi super admin theo SLA 72h.
- Web admin: quản trị nội dung, user/subscription, dashboard chỉ số chính.

### 4.3 Những Hạng mục CHƯA Triển khai (Out-of-Scope & Postponed)
| Tính năng/Hạng mục | Lý do hoãn (Nguyên nhân) | Dự kiến Phase tiếp theo |
|--------------------|---------------------------|-------------------------|
| Coach người thật (1-1) | Trái với định hướng MVP tự học 100% | Chưa xác định |
| Học từ vựng chuyên sâu | Không thuộc phạm vi "sửa giọng" hiện tại | Phase 3+ |
| Web learner portal | Giai đoạn đầu mobile-only | Review sau Phase 2 |

### 4.4 Assumptions & Dependencies
- **Assumptions (Giả định):** User chấp nhận upload audio lên cloud; sẵn sàng tự học không cần coach; mô hình weekly/lifetime đủ hấp dẫn phân khúc.
- **Dependencies (Phụ thuộc):** SSO provider, hạ tầng AI speech analysis, cloud storage, nền tảng notification/reminder.

---

## 6. Functional Requirements & Business Rules

> **Ưu tiên theo MoSCoW:** M = Must Have | S = Should Have | C = Could Have | W = Won't Have

### 5.1 Epic A — Learner Core Loop (Mobile)

**Mô tả Epic:** Chu trình chính để user đặt mục tiêu, ghi âm, nhận phân tích, luyện tập và theo dõi tiến bộ.

| ID | User Story | Acceptance Criteria | Priority |
|----|------------|---------------------|----------|
| FR-001 | As a learner, I want to sign in via SSO so that I can start quickly | Đăng nhập thành công qua SSO; tạo profile user | M |
| FR-002 | As a learner, I want to set one or more goals so that I can personalize learning | Cho phép tạo nhiều mục tiêu; lưu mục tiêu theo user | M |
| FR-003 | As a learner, I want to record or import audio so that AI can analyze my speech | Hỗ trợ ghi âm và import; enforce giới hạn độ dài | M |
| FR-004 | As a learner, I want speech scores and feedback so that I know what to improve | Trả điểm + nhận xét cho các tiêu chí giọng nói (trừ từ vựng) | M |
| FR-005 | As a learner, I want comparison with coach voice and my history so that progress is measurable | Hiển thị % giống mẫu và trend tiến bộ theo thời gian | M |
| FR-006 | As a learner, I want AI-generated lessons every 2 days with explanation so that I stay on track | Tạo bài học định kỳ 2 ngày/lần; có mô tả lý do giao bài | M |
| FR-007 | As a learner, I want to replay my recordings so that I can self-reflect | Cho phép nghe lại audio lịch sử | M |

**Business Rules & Workflows logic cho Epic A:**
- *Tính toán:* `% giống mẫu` và xu hướng tiến bộ tính trên baseline cá nhân + mẫu coach.
- *Validation cứng:* Chỉ chấm các tiêu chí thuộc phạm vi sửa giọng (không gồm từ vựng).
- *Trạng thái:* Recording -> Analyzed -> Lesson Generated -> Practiced -> Progress Updated.

### 5.2 Epic B — AI Quality Control

**Mô tả Epic:** Cơ chế đảm bảo chất lượng khi AI gợi ý sai.

| ID | User Story | Acceptance Criteria | Priority |
|----|------------|---------------------|----------|
| FR-008 | As a learner, I want to report wrong AI suggestions so that issues are reviewed | Có nút report trong app; report được ghi nhận đầy đủ context | M |
| FR-009 | As super admin, I want to resolve reports in 72h so that service quality is maintained | SLA xử lý <= 72h; trạng thái report theo dõi được | M |
| FR-010 | As super admin, I want to update related content sets and keep audit logs so that fixes are consistent and reversible | Cho phép cập nhật cụm nội dung liên quan; có audit log + rollback | M |

**Business Rules & Workflows logic cho Epic B:**
- *Validation cứng:* Chỉ Super Admin được duyệt thay đổi cuối.
- *Trạng thái:* Open -> In Review -> Updated -> Closed.

### 5.3 Epic C — Web Admin & Subscription Ops

**Mô tả Epic:** Công cụ vận hành nội dung và tăng trưởng.

| ID | User Story | Acceptance Criteria | Priority |
|----|------------|---------------------|----------|
| FR-011 | As admin, I want to manage exercise/scenario/coach voice/rubric/template so that learning content is controlled | CRUD + duyệt publish cho các nhóm nội dung đã xác nhận | M |
| FR-012 | As admin, I want to manage users and subscription plans so that I can operate the business | Quản lý danh sách user và gói subscription | M |
| FR-013 | As admin, I want dashboards for key metrics so that I can track product health | Có dashboard `last used`, `current user`, `peak user`, `churn`, `bounce`, `LTV` | M |

**Business Rules & Workflows logic cho Epic C:**
- *Validation cứng:* Mọi thay đổi xử lý report ảnh hưởng AI phải có dấu vết audit.
- *Trạng thái:* Draft -> Review -> Published cho nội dung quản trị.

---

## 7. Data & Technical Considerations

### 6.1 Architecture Notes
- Mobile-only cho learner ở MVP (ưu tiên iOS, sau đó Android).
- Web admin tách riêng để vận hành nội dung và subscription.
- Audio lưu cloud theo tài khoản, cho phép xóa; có thể dùng train model theo chính sách sản phẩm.
- Hỗ trợ offline mode (chi tiết sync strategy sẽ đặc tả ở tài liệu kỹ thuật).

### 6.2 Integrations
| Hệ thống | Loại tích hợp | Mục đích |
|----------|---------------|----------|
| SSO Provider | OAuth/OIDC | Đăng nhập user |
| Speech/AI Service | API | Phân tích giọng và sinh gợi ý |
| Cloud Storage | SDK/API | Lưu trữ audio và metadata |
| Notification Service | Push/Local Notification | Nhắc lịch luyện tập |

---

## 8. Non-Functional Requirements

### 7.1 Non-Functional Requirements (NFRs)
| Loại | Yêu cầu | Ghi chú |
|------|---------|---------|
| **Performance** | Thời gian phân tích mỗi lượt <= 3 phút | Theo yêu cầu stakeholder |
| **Availability** | Đáp ứng vận hành ổn định cho mobile MVP | Sẽ chốt SLO ở tài liệu kiến trúc |
| **Security** | Mã hóa data in-transit và at-rest; phân quyền role-based cho admin/super admin | Bắt buộc |
| **Privacy** | Cho phép user xóa audio; có chính sách dùng dữ liệu train model | Bắt buộc legal review |
| **Scalability** | Mở rộng từ iOS sang Android và tiếng Anh ở phase sau | Theo roadmap |

### 7.2 Analytics & Tracking Events
| Event Name | Parameter / Thuộc tính cần track | Nền tảng ghi nhận |
|------------|----------------------------------|-------------------|
| `goal_created` | `user_id`, `goal_type`, `timestamp` | Product Analytics |
| `recording_submitted` | `user_id`, `duration`, `input_type`(record/import) | Product Analytics |
| `analysis_completed` | `user_id`, `score_total`, `latency_ms` | Product Analytics |
| `lesson_completed` | `user_id`, `lesson_id`, `scenario_id` | Product Analytics |
| `report_submitted` | `user_id`, `report_type`, `content_id` | Product Analytics |
| `report_resolved` | `report_id`, `resolver_role`, `resolution_time_h` | Admin Analytics |

---

## 9. Risks & Open Q&A

### 8.1 Risks & Mitigation
| Rủi ro | Khả năng xảy ra | Mức độ ảnh hưởng | Cách giảm thiểu |
|--------|-----------------|------------------|-----------------|
| AI feedback chưa đủ chính xác với đa dạng giọng địa phương | Trung | Cao | Vòng report + super admin review + cập nhật cụm nội dung |
| Vấn đề pháp lý dữ liệu trẻ em và train model | Trung | Cao | Thiết kế consent flow phụ huynh + legal review sớm |
| Offline mode phức tạp khi đồng bộ lại | Trung | Trung | Giới hạn scope offline MVP, định nghĩa sync conflict policy |
| Người dùng bỏ cuộc sớm | Cao | Trung | Tăng giải thích lộ trình, nhắc lịch, hiển thị tiến bộ rõ ràng |

### 8.2 Open Questions
| # | Câu hỏi | Owner | Deadline | Status |
|---|---------|-------|----------|--------|
| 1 | Công thức chính xác cho `churn`, `bounce`, `LTV` theo business model nào? | Product Owner + Data | Trước tech design | Open |
| 2 | Permission matrix chi tiết cho admin thường/CSKH/super admin? | Product Owner + Ops | Trước implementation admin | Open |
| 3 | Chính sách offline/sync cụ thể (ưu tiên dữ liệu nào khi conflict)? | Tech Lead | Trước sprint build | Open |

---

## 10. Appendix (Phụ lục)
- Elicitation Tracking: `Elicitation/listQA/voice-speech-coaching-app.md`
- Elicitation Summary: `Elicitation/summary.md`
- AS-IS Analysis: `Analysis/ba-process-analysis-voice-speech-coaching.md`
- TO-BE Proposal: `Analysis/ba-process-proposal-voice-speech-coaching.md`
- Product Overview: `Analysis/ba-product-overview-gen.md`
- Epic/Use Case List: `Analysis/ba-usecase-list-voice-speech-coaching.md`
