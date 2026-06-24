# Day 20 Lab — Retention, Engagement & Habit Loop

**Sản phẩm:** AI Trợ Lý — `ai-tro-ly.lucasnguyen.vn`
**Track 1 — MSSV 2A202600810 — Nguyễn Xuân Tới**
**Đầu vào:** Prototype Ngày 18 (AI Trợ Lý) + Friction Audit Ngày 18 (xem `Bai3-Friction-Audit-AITroLy.md`)

---

## 0. Điểm xuất phát — Prototype Ngày 18

**AI Trợ Lý** là nền tảng dạy nhân viên văn phòng *tự dùng AI cho việc nghề* bằng thực hành, không học lý thuyết suông. Vòng giá trị cốt lõi của một bài học:

```
Xem framework prompt (Vai trò + Bối cảnh + Yêu cầu)
        ↓
Copy prompt → chạy trên claude.ai
        ↓
Nộp kết quả → AI chấm điểm theo rubric nghề
        ↓
Đạt ≥60đ → unlock nội dung sâu hơn + lưu kỹ năng
```

Persona chính của prototype: **nhân viên HR** (tuyển dụng / C&B / hành chính). Scenario, recovery flow và prototype giữ nguyên từ Ngày 18; Day 20 chỉ phân tích và đề xuất chỉnh sửa onboarding.

---

# Bài 1 — Hành vi tự nhiên và Use Case

Chọn **một use case chính** để phân tích sâu: *"Hoàn thành một tác vụ nghề HR bằng AI mà tự tin kết quả đủ tốt để dùng thật."*

## 4. Customer Retention Canvas — Use Case

| Thành phần | Câu hỏi | Câu trả lời của nhóm |
|---|---|---|
| **The Problem** | Vấn đề bằng lời của user là gì? | "Sếp bảo phải dùng AI cho nhanh, nhưng em mở Claude/ChatGPT ra lại không biết hỏi gì. Gõ vài câu thì nó trả lời chung chung, sửa tới sửa lui còn lâu hơn tự làm — nên cuối cùng em quay về làm tay cho chắc." |
| **The Persona** | Ai có vấn đề đó? | Nhân viên HR 24–35 tuổi tại công ty SME/midsize Việt Nam (tuyển dụng, C&B, hành chính nhân sự). Không phải dân kỹ thuật. Được công ty yêu cầu nâng năng suất bằng AI nhưng chưa được đào tạo bài bản. Mục tiêu: làm xong việc nhanh, đúng, không bị tụt lại khi công ty chuyển đổi số. |
| **Anti-persona** | Ai không thuộc use case này? | (1) Dân kỹ thuật / prompt engineer đã thạo AI — họ không cần dạy cơ bản. (2) Sinh viên chưa đi làm — không có bối cảnh nghề thật để áp prompt. (3) Lãnh đạo chỉ duyệt mua công cụ chứ không tự thao tác hằng ngày. Tách 3 nhóm này để không trộn dữ liệu hành vi. |
| **The Why** | Động lực cốt lõi là gì? | Muốn **xong việc nhanh hơn và được công nhận là "người biết dùng AI"** trong phòng, tránh cảm giác lỗi thời/áp lực khi cả công ty chuyển sang AI. (Outcome, không phải tính năng.) |
| **The Alternative** | Họ đang tự giải quyết bằng cách nào? | Tự mò ChatGPT free; xem video YouTube lẻ tẻ; copy prompt trôi nổi trên các group Facebook; hỏi đồng nghiệp giỏi hơn; hoặc bỏ cuộc, làm tay như cũ. |
| **The Frequency** | Vấn đề xuất hiện bao lâu một lần? | **Weekly** ở giai đoạn học (mỗi tuần gặp vài tác vụ HR cần làm: JD, email mời/từ chối, mô tả công việc, đánh giá...). Khi đã thạo, nhịp *dùng AI* tăng lên gần daily. Frequency suy từ alternative: HR gặp tác vụ "viết/soạn" vài lần mỗi tuần. |

**Giải thích chọn Weekly:** quan sát nhịp làm alternative — HR không viết JD mỗi ngày, nhưng tuần nào cũng có ít nhất một tác vụ soạn thảo cần chất lượng. Nhịp này quyết định toàn bộ lựa chọn metric ở Bài 2.

---

# Bài 2 — Từ Use Case tới Retention Metric

## 6. Core Action

| Câu hỏi | Câu trả lời |
|---|---|
| Core job của use case là gì? | Biến một tác vụ nghề HR thành kết quả đủ tốt để dùng thật, bằng prompt AI. |
| **Core action là gì?** | **Hoàn thành 1 bài học = nộp kết quả thực hành và đạt ≥60 điểm do AI chấm theo rubric nghề.** |
| Vì sao action này cho thấy user nhận được value? | Nộp + đạt chuẩn nghĩa là user đã tự tay tạo ra một output nghề bằng AI và được xác nhận đạt chất lượng — đúng giá trị họ cần (xong việc, tự tin dùng thật). Không phải "mở app" hay "xem màn hình". |
| Khi nào action này dễ xảy ra? | Khi có prompt framework sẵn để copy + có task thật để áp + ngưỡng nộp đủ thấp (chỉ dán kết quả từ Claude). |

**Loại trừ (không tính là core action):** đăng nhập, xem video welcome, lướt lộ trình, bấm "Bắt đầu" mà chưa nộp bài.

## 7. Định nghĩa Active User

> **"Một học viên được tính là active trong tuần khi hoàn thành ít nhất 1 bài học (nộp bài đạt ≥60đ) trong vòng 7 ngày."**

- Chỉ mở app → **không** tính active.
- Phải thực hiện core action (nộp bài đạt chuẩn).
- Số lần tối thiểu: 1 bài / tuần.
- Khoảng thời gian: cửa sổ 7 ngày.

## 8. Retention Metric theo Natural Frequency

| Thành phần | Câu trả lời |
|---|---|
| Persona và use case | HR — hoàn thành tác vụ nghề bằng AI và tự tin dùng thật |
| Natural frequency | **Weekly** (giai đoạn học) |
| Core action | Hoàn thành 1 bài học đạt ≥60đ |
| Active user definition | ≥1 bài/tuần trong cửa sổ 7 ngày |
| **Retention metric** | **Weekly cohort retention — W1 / W2 / W4** (kèm WAU và stickiness WAU/MAU phụ trợ) |
| Vì sao metric phù hợp với frequency? | Nhịp học tự nhiên là weekly, nên đo theo tuần phản ánh đúng "user còn quay lại học không". **Không** dùng D1/D7 daily retention vì sẽ phạt oan user có hành vi đúng (học 1–2 lần/tuần). Cohort theo tuần cho thấy bao nhiêu % học viên tuần 1 còn học ở tuần 2, tuần 4. |

**Không copy DAU/MAU của sản phẩm khác** — chọn weekly cohort vì nó khớp tần suất thật của tác vụ HR.

---

# Bài 3 — Onboarding tới First Core Action

> Phân tích đầy đủ (journey map 25 bước, friction audit Keep/Remove/Delay/Simplify, bug list 7 lỗi, đánh giá post-activation, test AI chat) nằm ở file **`Bai3-Friction-Audit-AITroLy.md`**. Dưới đây là phần tổng hợp theo đúng yêu cầu Bài 3.

## 9. Audit prototype Ngày 18 — Current State

**Current-State Journey (rút gọn từ 25 bước):**

```
Landing (/) → Đăng nhập → Đăng ký 4 trường (Họ tên/SĐT/Email/MK)
   → [FRICTION: redirect login, phải đăng nhập lại]
   → Welcome video modal → Chọn vai trò (chỉ 1 option HR)
   → [BUG: nhảy Bước 1/5 → 3/5, mất bước 2]
   → 16 câu assessment (16 màn hình) → Kết quả cá nhân hóa (AHA)
   → [DEAD END: /cho-kich-hoat "Lộ trình đang được tạo — chờ email"]
```

| Chỉ số | Current state |
|---|---|
| Số bước tới first core action | 25 bước (và bị **chặn cứng** bởi activation gate → core action = ∞ ở pre-activation) |
| Số trường thông tin phải nhập | 4 (đăng ký) + 16 (assessment) = 20 trường |
| Số permission phải cấp | 0 OAuth, nhưng yêu cầu tạo tài khoản đầy đủ sớm |
| Time to First Core Action ước tính | ∞ pre-activation / ~15–20 phút post-activation |
| Time to Value ước tính | ~8–12 phút tới Aha #1 (kết quả assessment), rồi bị phá bởi gate |
| Điểm drop-off cao nhất | `/cho-kich-hoat` (activation gate) — phá toàn bộ momentum |

*Ghi chú: chưa có tracking thật → các số là **ước tính từ prototype**.*

**Friction Audit (nhãn):** chi tiết R1–R5 (Remove), S1–S3 (Simplify), D1–D2 (Delay), K1–K13 (Keep) trong file Bài 3. Điểm cốt lõi: **R5 — Activation gate** và **B5 — `/lo-trinh` blank** là 2 blocker nghiêm trọng nhất.

## 10. Thiết kế lại hành trình — Redesigned Journey

```
1. Landing → 2. Đăng ký Google OAuth 1-click (hoặc Email+MK)
   → 3. Chọn vai trò (3–5 options) → 4. 3 câu nhanh (mảng HR + level AI + mục tiêu)
   → 5. Mở Module đầu tiên NGAY (bỏ activation gate)
   → 6. FIRST CORE ACTION: copy prompt → chạy Claude → nộp bài
   → 7. AI chấm điểm + card "đạt chuẩn" (EVIDENCE OF VALUE / AHA)
   → 8. Sau bài 1: hỏi thêm để tinh chỉnh lộ trình
```

**Activation & Time to Value (sau redesign):**
- **Activation:** thời điểm user nộp bài đầu tiên và nhận điểm ≥60 (AI xác nhận đạt chuẩn).
- **Activation Rate:** % user hoàn thành bài đầu đạt chuẩn / tổng user đăng ký.
- **Time to First Core Action:** từ vào onboarding tới lúc nộp bài đầu — mục tiêu **< 5 phút**.
- **Time to Value:** từ vào sản phẩm tới card "đạt chuẩn" — mục tiêu **< 6 phút**.
- *Lựa chọn:* activation = first core action = aha (cùng một event "lesson_passed") vì sản phẩm này value rất tập trung: làm được 1 việc thật bằng AI là đã thấy giá trị.

**Recovery Path (chọn: "User chưa sẵn sàng hoàn thành core action"):** Nếu user copy prompt nhưng chưa nộp trong 10 phút → hiện gợi ý "Dán thử kết quả mẫu để xem AI chấm thế nào" + cho dùng task mẫu sẵn, **không** kết thúc ở màn hình lỗi → kéo user về đúng bước nộp bài. Giữ và cải thiện recovery flow Ngày 18 (trước đây gate là dead-end → nay thành nhánh dẫn về core action).

## Before/After Comparison

| Tiêu chí | Before | After | Vì sao thay đổi? |
|---|---|---|---|
| Số bước tới core action | 25 (bị chặn) | ~6 | Bỏ activation gate, gộp bước, vào module ngay |
| Số trường phải nhập | 20 | 2–5 (OAuth + 3 câu) | Bỏ SĐT, cắt 16→3 câu assessment, hỏi phần còn lại sau bài 1 |
| Permission trước core action | Tạo tài khoản đầy đủ | 1-click OAuth | Giảm ma sát đăng ký, giải thích permission đúng lúc |
| Time to First Core Action | ∞ / ~15–20 phút | < 5 phút | Bỏ gate + cắt bước thừa |
| Time to Value | bị phá bởi gate | < 6 phút | Evidence of value (AI chấm) ngay sau core action |
| Điểm drop-off chính | `/cho-kich-hoat` | (đã loại bỏ) | Gate bị xóa hoàn toàn |
| Evidence of value | Card assessment (rồi bị chặn) | Điểm AI chấm + "đạt chuẩn" ngay sau bài | Cho user thấy giá trị thật từ hành vi của họ |
| Recovery path | Dead-end (chờ email) | Nhánh dẫn về nộp bài (task mẫu) | Recovery phải đưa user về core action, không kết ở lỗi |

---

# Bài 4 — Measurement Ladder và North Star Metric

## 11. Measurement Ladder

```
Marketing / Traffic  → Lượt truy cập landing
        ↓
Visitor              → Đăng ký / Đăng nhập
        ↓
Activation           → Activation Rate, Time to Value (nộp bài đầu đạt ≥60đ)
        ↓
Core Action          → Số bài học hoàn thành đạt chuẩn; WAU
        ↓
Retention            → Weekly cohort retention W1/W2/W4; Churn
        ↓
Revenue              → Seat expansion / gia hạn license B2B; LTV
```

Engagement/Stickiness phụ trợ: WAU/MAU, số session/tuần, số bài/tuần trên mỗi user.

## 12. North Star Metric và Input Metrics

```
The Work (sản xuất bài học + AI grading + lộ trình theo vai trò)
        ↓
Input Metrics
   1. Activation Rate (% user hoàn thành bài đầu đạt chuẩn trong 24h)
   2. Weekly Active Learners — WAL (số user nộp ≥1 bài đạt chuẩn/tuần)
   3. Lesson Completion Rate (số bài nộp đạt chuẩn / số bài bắt đầu)
        ↓
NORTH STAR METRIC
   "Số bài học thực hành hoàn thành đạt chuẩn mỗi tuần"
   (Weekly Completed-to-Standard Lessons)
        ↓
Mid/Long-term Business Result + Customer Value
   Năng suất HR tăng → công ty gia hạn & mở rộng số ghế (seat) → B2B revenue
```

**Vì sao đây là North Star tốt:** thể hiện value thật (user *làm được việc* bằng AI, không chỉ ghé thăm); là leading indicator của retention & revenue; không phải vanity metric (không phải lượt xem/đăng ký); hành động được (cải onboarding/nội dung là đẩy được); dễ hiểu; đo được qua event.

**Leading vs Lagging:**
- *Leading:* Activation Rate, Completion Rate, WAL, North Star (báo trước sức khỏe sản phẩm).
- *Lagging:* Weekly retention W4, seat expansion, revenue, LTV (kết quả đến sau).

**Trade-off cần theo dõi:** Hạ ngưỡng AI chấm từ 60 → 40 điểm sẽ **tăng** Completion Rate và North Star về số lượng, nhưng **loãng** chất lượng "đạt chuẩn" → học viên không thật sự làm được việc → retention W4 và seat expansion giảm. → Phải giữ ngưỡng gắn với chất lượng thật, không tối ưu con số.

---

# Bài 5 — Nature, Nurture và Habit Loop

## 13. Nature vs Nurture

| Nội dung | Câu trả lời |
|---|---|
| Natural frequency của use case | Weekly (gặp tác vụ HR cần soạn thảo vài lần/tuần) |
| Internal trigger | Cảm giác **kẹt + áp lực thời gian** khi đối mặt một task nghề mới mà chưa biết hỏi AI sao cho ra kết quả dùng được |
| External trigger hiện có | Floating "Mở trợ lý AI"; progressive unlock trong module; leaderboard phòng; (đề xuất thêm) email tuần "bài tiếp theo + thứ hạng của bạn" |
| Một hoạt động nurture phù hợp | **Email/notification weekly**: "Tuần này có bài *Viết email từ chối ứng viên* — 8 phút, phòng bạn đã có 4 người hoàn thành" → đẩy đúng nhịp weekly |
| Vì sao nurture không quá đẩy / quá thụ động? | Nhịp gửi = weekly khớp natural frequency (không spam daily vì user không gặp task mỗi ngày); có nội dung giá trị (bài cụ thể) chứ không chỉ "quay lại đi"; gắn social proof nhẹ (đồng nghiệp), không ép |
| Metric theo dõi tác động | Email→active conversion; WAL tuần có gửi vs không; weekly retention |

**Frequency thấp → bù bằng hành vi liên quan:** core use case (làm task lớn) có thể không xảy ra mỗi tuần với mọi HR. Bổ sung điểm chạm tần suất cao hơn: **floating AI Trợ Lý** cho câu hỏi nhanh hằng ngày + **Hỏi đáp cộng đồng** (+15đ khi trả lời) — giống cách Zillow dùng Zestimate/content quanh use case mua nhà thưa. Không giả định HR sẽ "học bài lớn" mỗi ngày.

## 14–15. Hook Model

**Kiểm tra trước (14.1):** Sản phẩm có cần habit không? — Có, nhưng là habit *"khi gặp task nghề thì mở AI Trợ Lý"* (nhịp weekly + theo task), **không** ép habit daily. Frequency weekly + perceived utility cao (làm được việc thật) → đủ để vào habit zone dạng "trigger theo nhu cầu".

**Hook Review:**

| Thành phần | Câu trả lời |
|---|---|
| Why Habit? | Để HR hình thành phản xạ "mở AI Trợ Lý khi gặp task mới" thay vì làm tay → công ty thấy năng suất tăng, gia hạn license |
| Intended Behavior | Mở app → hoàn thành/áp dụng 1 bài học (prompt) cho một task nghề thật |
| Frequency & Utility | Weekly, utility cao → đủ hình thành habit theo-task; **không** ép daily |
| Internal Trigger | Cảm giác kẹt + lo "làm không kịp / không đủ tốt" khi có task nghề mới |
| External Trigger | Owned (email weekly bài mới), in-product (floating AI, progressive unlock), relationship (leaderboard phòng, đồng nghiệp) |
| Action | Copy 1 prompt framework → chạy Claude → dán kết quả nộp. Hành vi đơn giản nhất để nhận reward |
| Motivation | Muốn xong việc nhanh + được công nhận biết dùng AI |
| Ability (rào cản cần bỏ) | **Time** (25 bước onboarding), **Brain cycles** (16 câu assessment, không biết bắt đầu đâu). 3 cách giảm: (1) Google 1-click login, (2) 3 câu thay 16, (3) bỏ activation gate + prompt có sẵn để copy |
| Variable Reward | **The Self** (điểm AI chấm + level + "đạt chuẩn" + tiến bộ skill) là chính; **The Tribe** (leaderboard phòng, +15đ trả lời cộng đồng) phụ; **The Hunt** (mở khóa nội dung sâu hơn) phụ. Reward phục vụ core action, không phải gamification gắn thêm |
| Investment | Nộp bài → lưu skill vào "Bộ kỹ năng"; tích điểm/thứ hạng; lịch sử học + lộ trình cá nhân hóa |
| Next Trigger | Hoàn thành bài → unlock bài kế tiếp + email tuần sau nhắc bài tiếp → load vòng hook mới |
| User Impact | Có ích thật: học kỹ năng nghề dùng được ngay, dữ liệu ẩn danh (safety copy). Không tạo hành vi gây nghiện vô ích |

**5 Whys (rút gọn) tìm internal trigger:** Vì sao mở AI Trợ Lý? → vì có task khó. → Vì sao thấy khó? → không biết hỏi AI sao. → Vì sao lo? → sợ làm chậm/sai. → Vì sao sợ? → bị đánh giá kém. → **Internal trigger lõi: lo bị tụt lại + áp lực thời gian.**

Hoàn thành câu: *"Mỗi khi user **gặp một task HR mới mà chưa biết bắt đầu**, họ cảm thấy **kẹt và lo không làm kịp** → mở AI Trợ Lý."*

**Hook Flow (đã sửa trên prototype):**
```
Internal trigger (kẹt với task) / External (email bài mới)
        ↓
Action: copy prompt → chạy Claude → nộp bài
        ↓
Variable Reward: AI chấm điểm "đạt chuẩn" + thứ hạng phòng
        ↓
Investment: lưu skill + tích điểm + lộ trình cá nhân hóa
        ↓
Next Trigger: unlock bài kế + email tuần sau
```

---

# Bài 6 — Metric Tracking Requirement

## 16. Bảng định nghĩa metric

| Tên metric | Câu hỏi cần trả lời | Đơn vị | Công thức | Khoảng thời gian | Segment | Event cần có |
|---|---|---|---|---|---|---|
| North Star — Weekly Completed-to-Standard Lessons | Mỗi tuần có bao nhiêu bài thực hành hoàn thành đạt chuẩn? | Bài học | COUNT(`lesson_passed` với score≥60) | Weekly | Theo vai trò (HR…) | `lesson_passed` |
| Activation Rate | % user mới đạt giá trị đầu? | User | users có `lesson_passed` trong 24h ÷ users `signup_completed` | Theo cohort ngày | Vai trò | `signup_completed`, `lesson_passed` |
| WAL (Weekly Active Learners) | Bao nhiêu user thật sự học mỗi tuần? | User | COUNT DISTINCT user có ≥1 `lesson_passed` | Weekly | Vai trò, phòng | `lesson_passed` |
| Lesson Completion Rate | Bài bắt đầu có được hoàn thành không? | % | `lesson_passed` ÷ `lesson_started` | Weekly | Theo bài học | `lesson_started`, `lesson_passed` |
| Weekly Cohort Retention W1/W2/W4 | Học viên còn quay lại học không? | % | % user của cohort tuần 0 có `lesson_passed` ở tuần N | Weekly cohort | Vai trò | `lesson_passed` |
| Time to Value | Vào sản phẩm bao lâu thì nhận value đầu? | Phút | timestamp(`lesson_passed` đầu) − timestamp(`onboarding_started`) | Theo user | Vai trò | `onboarding_started`, `lesson_passed` |

## 17. Bảng yêu cầu tracking event

| Event name | Ghi khi nào? | User identity | Properties | Metric dùng event | Tránh ghi trùng |
|---|---|---|---|---|---|
| `signup_completed` | Tài khoản tạo thành công (sau OAuth/email) | user_id | method (google/email), role (nếu có) | Activation Rate | 1 event/account; idempotent theo account_id |
| `onboarding_started` | User vào màn onboarding đầu | user_id | entry_source | Time to Value | Chỉ ghi lần đầu/onboarding session |
| `role_selected` | User chọn vai trò | user_id | role | Segment | Ghi giá trị mới nhất, không cộng dồn |
| `lesson_started` | User mở 1 bài & thấy framework prompt | user_id | lesson_id, role | Completion Rate | Dedup theo (user_id, lesson_id, session) |
| `prompt_copied` | User bấm "Copy prompt" | user_id | lesson_id | (phân tích funnel) | Đếm theo lần bấm nhưng gắn session để lọc retry |
| `lesson_submitted` | User dán kết quả & bấm nộp | user_id | lesson_id, attempt_no | Completion funnel | Mỗi lần nộp = 1 attempt; phân biệt attempt_no |
| `lesson_passed` | AI chấm xong & score≥60 (chuyển trạng thái chưa đạt→đạt) | user_id | lesson_id, score, role, ts | **North Star, WAL, Activation, Retention, TTV** | Chỉ ghi khi *lần đầu* bài chuyển sang "đạt"; nộp lại không tạo trùng |
| `skill_saved` | User lưu kỹ năng vào "Bộ kỹ năng" | user_id | skill_id, lesson_id | Investment tracking | Dedup theo (user_id, skill_id) |

## 18. Gắn event lên flow

```
Onboarding bắt đầu      → [onboarding_started]
        ↓
Đăng ký xong            → [signup_completed]
        ↓
Chọn vai trò            → [role_selected]
        ↓
Mở bài đầu tiên         → [lesson_started]  → [prompt_copied]
        ↓
Nộp kết quả             → [lesson_submitted]
        ↓
First core action / Aha → [lesson_passed]  (= Activation)
        ↓
Lưu kỹ năng             → [skill_saved]    (= Investment)
```

## 19. Tiêu chí nghiệm thu tracking (≥4)

1. `lesson_passed` chỉ ghi khi bài thực sự chuyển từ "chưa đạt" → "đạt" (score≥60); nộp lại bài đã đạt **không** tạo event mới.
2. Refresh / retry / autosave không nhân bản event — mọi event quan trọng dedup theo khóa `(user_id, lesson_id, session_id)` hoặc trạng thái chuyển đổi.
3. Mỗi event có đủ identity (`user_id`) và properties tối thiểu để tính metric (`lesson_id`, `score`, `role`, `timestamp`).
4. Timestamp lưu chuẩn UTC kèm timezone gốc (Asia/Saigon) để cohort theo tuần tính đúng mốc.
5. Mỗi event đủ dữ liệu để tính metric độc lập theo đúng công thức ở mục 16 (không phải join thủ công nhiều nguồn).
6. Không thu thập dữ liệu cá nhân không cần thiết (không lưu nội dung bài làm chứa dữ liệu thật của user — chỉ lưu điểm và metadata; nhất quán với safety copy "dùng dữ liệu ẩn danh").

---

## Bản đồ đáp ứng đầu ra bắt buộc

| Đầu ra bắt buộc (mục 3 đề bài) | Vị trí |
|---|---|
| 1. Customer Retention Canvas — Use Case | Bài 1 |
| 2. Core Action, Active User & Retention Metric | Bài 2 |
| 3. Onboarding → First Core Action (audit + tối ưu) | Bài 3 + `Bai3-Friction-Audit-AITroLy.md` |
| 4. Measurement Ladder & North Star Metric | Bài 4 |
| 5. Nature vs Nurture | Bài 5 §13 |
| 6. Hook Model | Bài 5 §14–15 |
| 7. Metric Tracking Requirement | Bài 6 |
| 8. Phần chỉnh sửa prototype Ngày 18 | Bài 3 §10 (Redesigned Journey) + Before/After |

---

*Day 20 Lab — Retention, Engagement & Habit Loop — Track 1 — Khoá 02*
