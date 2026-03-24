# Market Research Report — Voice Speech Coaching App (VN)

**Version:** 1.0  
**Date:** 24/03/2026  
**Owner:** Product/PO  
**Scope:** Vietnam, B2C student segment (high school + university), mobile-first

---

## 1) Executive Summary

### 3 key findings
1. **Nhu cầu thị trường đang có thật**: nhóm sản phẩm language/speech learning tăng trưởng nhanh toàn cầu, với AI + self-learning là trục chính.  
2. **Khoảng trống tại VN cho phân khúc sinh viên/học sinh**: đa số giải pháp hiện tại hoặc quá thiên về tiếng Anh tổng quát, hoặc định giá cao/ít "local context".  
3. **Cơ hội khác biệt khả thi**: "rẻ hơn + riêng tư + theo dõi tiến bộ rõ rệt + tình huống Việt hóa" phù hợp trực tiếp pain point đã khơi gợi.

### Top recommendation
- Ra mắt MVP mobile (iOS trước) với core loop: ghi âm/import -> AI feedback theo tiêu chí giọng nói -> bài tập cá nhân hóa -> tracking tiến bộ; đồng thời có web admin để kiểm soát chất lượng nội dung và xử lý report AI trong 72h.

### Next steps (4 tuần)
- Tuần 1: Chốt metric definitions (`churn`, `bounce`, `LTV`) + pricing hypothesis.  
- Tuần 2: 8-10 interviews + survey nhanh 150 mẫu trong nhóm sinh viên/học sinh.  
- Tuần 3: Prototype test 5-8 người + refine onboarding và feedback UI.  
- Tuần 4: Freeze scope MVP + backlog sprint 1.

---

## 2) Research Methodology

## 2.1 Research objectives (SMART)
- Xác định quy mô cơ hội thị trường đủ lớn để launch sản phẩm luyện giọng tại VN.
- Xác định 3-5 yếu tố khác biệt có thể thắng trong 12 tháng đầu.
- Xác định mô hình giá khả thi cho nhóm user mục tiêu nhạy cảm chi phí.

## 2.2 Research questions (prioritized)
### Market
1. Thị trường học ngoại ngữ/speech learning tăng trưởng ra sao?  
2. Xu hướng AI speech feedback có đang tăng adoption không?  

### User
3. User học sinh/sinh viên hiện giải quyết pain point nói sai/sợ nói như thế nào?  
4. Mức sẵn sàng trả phí hợp lý theo tuần/lifetime là bao nhiêu?  

### Competitive
5. Những đối thủ trực tiếp/gián tiếp nào đang cover use case này?  
6. Khoảng trống nào chưa được phục vụ tốt tại thị trường VN?

## 2.3 Methods used in report này
- **Desk research** (secondary data): industry reports, competitor pricing pages, app listings/reviews, trend signals.
- **Limitation:** Chưa chạy primary research trong tài liệu này; các giả định giá và conversion cần validate tiếp.

---

## 3) Market Overview

## 3.1 Market sizing (directional)
> Lưu ý: con số dưới đây là **ước lượng định hướng** để ra quyết định product discovery, không thay thế financial due diligence.

### TAM (Global adjacent market)
- Theo tổng hợp từ kết quả tìm kiếm nguồn industry reports, thị trường online/language learning toàn cầu ở mức hàng chục tỷ USD và tăng trưởng mạnh (CAGR 2 chữ số).
- Một nguồn phổ biến (Grand View Research) nêu online language learning market 2024 khoảng **USD 22.1B**, dự báo 2030 khoảng **USD 54.8B**.

### SAM (Vietnam edtech + language/speaking slice)
- Một số nguồn market-intel (GlobalData summary) cho thấy Vietnam EdTech 2024 cỡ **USD 3.6B**.
- Với focus ban đầu vào speaking coaching cho học sinh/sinh viên, có thể lấy một phần nhỏ trong K-12 + self-learning mobile.

### SOM (12-24 tháng đầu, product-level)
- Dùng giả định bottom-up để quản trị mục tiêu:
  - 100,000 MAU mục tiêu sau 24 tháng
  - 3-5% trả phí
  - ARPPU theo weekly/lifetime blended: USD 3-6/tháng tương đương
- SOM doanh thu thường niên ước lượng: khoảng **USD 108K - 360K** giai đoạn đầu (directional, phụ thuộc retention).

## 3.2 PESTLE highlights
- **Political/Legal:** Có rủi ro compliance dữ liệu giọng nói và user vị thành niên; cần luồng parental consent rõ ràng.  
- **Economic:** Nhóm học sinh/sinh viên nhạy cảm giá; mô hình weekly + lifetime có lợi thế thử nhanh.  
- **Social:** Nhu cầu cải thiện giao tiếp/thuyết trình tăng cùng áp lực học tập và tuyển dụng.  
- **Technological:** AI speech scoring/recommendation đã đủ trưởng thành để tạo feedback tức thời.  
- **Environmental:** Ít tác động trực tiếp ở phase hiện tại.

## 3.3 Key trends (2026)
1. **AI-first self-learning** thay thế khóa học cứng.  
2. **Micro-practice theo tình huống** hiệu quả hơn giáo trình dài.  
3. **Outcome visibility** (điểm + tiến bộ) là yếu tố giữ chân quan trọng.  
4. **Privacy-aware learning** tăng quan trọng với dữ liệu giọng nói.  
5. **Freemium/subscription hybrid** vẫn là chuẩn trong mảng learning apps.

---

## 4) User Insights (from elicitation + secondary signal)

## 4.1 Personas (working draft)

### Persona A — Sinh viên thiếu tự tin khi thuyết trình
- **Goal:** Nói rõ, ít run, tự tin trước lớp.  
- **Pain:** Mặc cảm giọng nói, không biết luyện đúng cách, khó đo tiến bộ.  
- **Behavior:** Dùng YouTube, học ngắt quãng, thích app mobile nhanh gọn.

### Persona B — Học sinh chuẩn bị thi/hùng biện
- **Goal:** Cải thiện giọng, ngữ điệu, độ rõ để trình bày tốt hơn.  
- **Pain:** Thiếu phản hồi cá nhân hóa; chi phí khóa học cao.  
- **Behavior:** Dùng điện thoại nhiều, ưa bài ngắn theo tình huống.

## 4.2 JTBD (top)
1. **When** cần thuyết trình trước lớp, **I want** luyện nói có feedback ngay, **so I can** tự tin và ít lỗi hơn.  
2. **When** tự học một mình, **I want** app chỉ rõ tôi sai ở đâu, **so I can** cải thiện nhanh mà không cần thuê coach.  
3. **When** tôi bỏ lỡ lịch luyện, **I want** lộ trình đơn giản và dễ quay lại, **so I can** duy trì thói quen.

## 4.3 Key user assumptions cần validate
- User sẵn sàng gửi audio lên cloud nếu có quyền xóa và chính sách minh bạch.  
- Weekly subscription phù hợp khả năng chi trả hơn annual.  
- % tiến bộ hiển thị rõ sẽ tăng retention tuần 4.

---

## 5) Competitive Landscape

## 5.1 Competitor set
- **Direct:** ELSA Speak, BoldVoice, Orai, Yoodli (speech/public speaking AI apps).  
- **Indirect:** YouTube/free content, khóa offline/public speaking classes.

## 5.2 Competitor snapshot (desk research)
| Competitor | Positioning | Pricing signal | Strength | Weakness/Gap |
|---|---|---|---|---|
| ELSA Speak | AI pronunciation coach (English) | Annual plan around premium price tier | Brand mạnh, kho bài lớn, AI feedback tốt | Có thể "overwhelming", chưa tối ưu cho use-case "nói trước đám đông VN" |
| BoldVoice | Accent training | Monthly/annual mid-high | UX đơn giản, coaching format rõ | Chủ yếu accent niche, local VN context thấp |
| Orai | Public speaking coach | Monthly + annual + enterprise | Tập trung public speaking behaviors | Chưa localize sâu cho tiếng Việt/học sinh |
| Yoodli | AI speaking coach (individual/team) | Free + paid tiers | B2B/team analytics mạnh | Có thể quá nặng cho phân khúc sinh viên giá nhạy cảm |

## 5.3 Competitive matrix (target perspective)
| Tiêu chí | Sản phẩm đề xuất | ELSA | Orai | BoldVoice | YouTube/Offline |
|---|---|---|---|---|---|
| Tiếng Việt native-first | ✅ | ⚠️ (không phải trọng tâm chính) | ⚠️ | ❌ | ⚠️ |
| Giá rẻ cho học sinh/sinh viên | ✅ (chiến lược) | ⚠️ | ⚠️ | ⚠️ | ✅/❌ |
| Tracking tiến bộ rõ rệt | ✅ | ✅ | ✅ | ✅ | ❌ |
| Tình huống Việt hóa | ✅ | ❌/⚠️ | ❌ | ❌ | ⚠️ |
| Privacy controls (xóa dữ liệu) | ✅ | ✅/⚠️ | ✅/⚠️ | ✅/⚠️ | ❌ |

## 5.4 Strategic gaps
- **Blue ocean:** Speech coaching tiếng Việt theo ngữ cảnh học sinh/sinh viên, giá thấp, privacy-first, có admin QA loop.  
- **Table stakes:** AI feedback tức thời, replay, progress tracking, SSO, reminder.  
- **Differentiator:** 100 tình huống Việt hóa + baseline cá nhân + vòng report 72h có rollback.

---

## 6) Synthesis & Opportunities

## 6.1 Top findings (Insight -> Evidence -> Implication -> Recommendation)
1. **Insight:** Nhu cầu luyện nói có feedback tức thời ngày càng rõ.  
   **Evidence:** Tăng trưởng mạnh mảng language/speech learning AI trong nhiều nguồn market reports.  
   **Implication:** MVP phải tối ưu time-to-feedback.  
   **Recommendation:** Giữ SLA phân tích <= 3 phút như PRD.

2. **Insight:** Phân khúc mục tiêu nhạy cảm giá.  
   **Evidence:** Hành vi dùng YouTube/khóa offline, ưu tiên chi phí thấp.  
   **Implication:** Giá quyết định conversion ban đầu.  
   **Recommendation:** Test 2 gói: weekly low entry + lifetime anchor.

3. **Insight:** Cạnh tranh mạnh ở tiếng Anh tổng quát, yếu ở bối cảnh tiếng Việt học đường.  
   **Evidence:** Nhiều đối thủ global thiên về accent/public speaking generic.  
   **Implication:** Local context là lợi thế chính.  
   **Recommendation:** Ưu tiên 100 tình huống Việt hóa trong MVP nội dung.

4. **Insight:** AI quality trust là rào cản adoption.  
   **Evidence:** Reviews competitor thường than phiền algorithm mismatch trong một số bối cảnh.  
   **Implication:** Cần governance loop.  
   **Recommendation:** Bắt buộc report flow + super admin SLA + audit + rollback.

5. **Insight:** Theo dõi tiến bộ là driver giữ chân quan trọng.  
   **Evidence:** Hành vi học kỹ năng cần thấy tiến bộ để duy trì thói quen.  
   **Implication:** Nếu không có progress visibility, churn tăng cao.  
   **Recommendation:** Ưu tiên UX dashboard "before/after" ngay sprint đầu.

## 6.2 Opportunity list + ICE scoring
| Opportunity | Impact (1-10) | Confidence (1-10) | Ease (1-10) | ICE |
|---|---:|---:|---:|---:|
| VN-localized speaking scenarios (100 tình huống) | 9 | 7 | 6 | 42.0 |
| Progress intelligence (% giống mẫu + trend) | 9 | 8 | 6 | 48.0 |
| Weekly low-entry pricing experiment | 8 | 7 | 8 | 56.0 |
| Report quality loop (72h SLA + rollback) | 8 | 8 | 7 | 56.0 |
| Offline-lite mode for practice continuity | 7 | 5 | 4 | 23.3 |

## 6.3 Prioritized recommendations
1. **Go-to-market wedge:** "Luyện nói riêng tư cho học sinh/sinh viên Việt, giá dễ vào, thấy tiến bộ rõ".  
2. **Pricing experiment từ sớm:** A/B weekly vs lifetime entry offer.  
3. **Content moat:** Tăng tốc xây và QA 100 tình huống Việt hóa.  
4. **Trust moat:** Vận hành report SLA 72h và minh bạch lịch sử thay đổi nội dung.

---

## 7) Validation Checklist & Next Actions

## 7.1 Validation status (current)
- [x] Có problem statement và business goal ở mức product direction.  
- [x] Có desk research và benchmark cạnh tranh sơ bộ.  
- [ ] Có ít nhất 5-8 interviews thực tế (chưa làm).  
- [ ] Có survey 100+ mẫu để validate pricing/retention assumptions (chưa làm).  
- [ ] Có triangulation dữ liệu >= 2 nguồn cho từng insight định lượng (một phần chưa đủ).

## 7.2 Next-step execution plan
- **Nghiên cứu người dùng (primary):** 8-10 interviews + 150 survey responses.  
- **Pricing validation:** test willingness-to-pay theo 3 mức weekly + 1 mức lifetime.  
- **Product validation:** prototype usability test (5-8 users).  
- **Decision gate:** Chỉ chốt release scope khi đạt đủ bằng chứng cho 3 giả định lớn: giá, retention week-4, trust AI.

---

## 8) References

1. Grand View Research — Online Language Learning Market report page:  
   https://grandviewresearch.com/industry-analysis/online-language-learning-market-report  
2. HolonIQ — Southeast Asia EdTech notes:  
   https://www.holoniq.com/notes/2024-southeast-asia-edtech-50  
3. GlobalData listing (Vietnam EdTech market summary page):  
   https://www.globaldata.com/store/report/vietnam-edtech-market-analysis/  
4. Orai pricing page:  
   https://orai.com/pricing/  
5. Yoodli pricing page:  
   https://yoodli.ai/pricing  
6. ELSA pricing page (public page):  
   https://en-dev.elsaspeak.com/pricing-b2c

> Ghi chú: Một số số liệu thị trường trong ngành đến từ nguồn trả phí/summary pages; cần mua full report hoặc dùng nguồn nội bộ để finalize financial model.
