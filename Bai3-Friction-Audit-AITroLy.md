# Bài 3 — Friction Audit: AI Trợ Lý (ai-tro-ly.lucasnguyen.vn)
**Ngày audit:** 24/06/2026 | **Auditor:** Claude (thay mặt Lucas)
**Persona:** Nhân viên HR mới — lần đầu vào web, chưa có tài khoản

---

## 1. Hành trình thực tế (Journey Map)

| # | Bước | URL | Label | Ghi chú |
|---|------|-----|-------|---------|
| 0 | Vào landing page | `/` | — | Hero, 3 value props, CTA "Nhận tin khi mở cửa" |
| 1 | Click "Đăng nhập" | `/login` | — | Modal login + demo credentials hint |
| 2 | Click "Đăng ký" | `/register` | — | Form 4 trường: Họ tên, SĐT, Email, Mật khẩu |
| 3 | Submit register | `/login?registered=1` | **FRICTION** | Redirect về login — phải đăng nhập lại thủ công |
| 4 | Điền email + password, Submit | — | — | |
| 5 | Welcome modal | `/onboarding` | — | Video YouTube "Lucas AI" + nút "Bắt đầu →" |
| 6 | Bước 1/5: Chọn vai trò | `/onboarding` | **BUG** | Chỉ có 1 option: "Nhân sự / HR" |
| 7 | **Bước 3/5**: Intro đánh giá | `/onboarding` | **BUG** | Bước 2/5 biến mất — không tồn tại |
| 8–23 | Bước 4/5: Câu 1→16 | `/onboarding` | — | 16 câu, mỗi câu 1 màn hình riêng |
| 24 | Bước 5/5: Kết quả | `/onboarding` | **AHA** | Card cá nhân hóa: level 3/5, tags công việc |
| 25 | Click "Bắt đầu học ngay →" | `/cho-kich-hoat` | **DEAD END** | "Lộ trình đang được tạo — chờ email" |

**Tổng số bước từ landing → cố gắng vào học:** 25 bước

---

## 2. TFCA & Aha Moment

| Chỉ số | Giá trị | Nhận xét |
|--------|---------|----------|
| **Time to First Core Action (TFCA)** | **∞ (pre-activation) / ~15–20 phút (post-activation)** | Pre-activation: bị chặn hoàn toàn. Post-activation: landing → module đầu tiên mất ~15–20 phút do 25 bước onboarding + /lo-trinh blank → phải navigate thủ công vào /tro-ly rồi mới tìm thấy link module |
| **Thời gian đến điểm bị chặn** | ~8–12 phút | Từ landing đến `/cho-kich-hoat` (pre-activation) |
| **Aha Moment #1** | Bước 5/5 — kết quả đánh giá | Card cá nhân hóa với level + tags công việc — mạnh về mặt cảm xúc, nhưng bị phá vỡ ngay sau đó bởi activation gate |
| **Aha Moment #2** | Vào module đầu tiên — thấy prompt thực hành | Prompt framework 3 mảnh (Vai trò + Bối cảnh + Yêu cầu) → nút "Copy prompt" → link claude.ai → submit kết quả → AI chấm điểm. Loop hoàn chỉnh, rõ giá trị |
| **Core Action được định nghĩa** | Hoàn thành bài học đầu tiên (nộp bài + đạt ≥60 điểm) | Đạt được sau khi có activation — nhưng path để đến đó quá dài và có 1 bug (blank /lo-trinh) |

---

## 3. Friction Audit — Nhãn Keep / Remove / Delay / Simplify

### 🔴 REMOVE — Loại bỏ

| # | Điểm ma sát | Lý do |
|---|-------------|-------|
| R1 | **Demo credentials không hoạt động** | Login page hiển thị `nhanvien@congty.vn` + "Mật khẩu bất kỳ" nhưng bị báo "Email hoặc mật khẩu sai." → Tạo ấn tượng xấu đầu tiên ngay tại bước đầu tiên |
| R2 | **Double login sau register** | Sau khi đăng ký thành công, user phải đăng nhập lại thủ công. Session nên được tạo tự động sau register |
| R3 | **Số điện thoại ở form đăng ký** | Không cần SĐT để bắt đầu học. Tạo ma sát không cần thiết. Thu thập sau khi user đã có giá trị |
| R4 | **Trường hợp SĐT không phục vụ mục đích rõ ràng** | User không hiểu SĐT dùng để làm gì trong bối cảnh học AI |

### 🔴 REMOVE (Critical) — Chặn Core Action

| # | Điểm ma sát | Lý do |
|---|-------------|-------|
| R5 | **Activation gate `/cho-kich-hoat`** | Sau 25 bước, user không vào được nội dung. "Lộ trình đang được tạo" là **blocker cứng** — phá hủy toàn bộ momentum đã xây. Đây là vấn đề nghiêm trọng nhất |

### 🟡 SIMPLIFY — Đơn giản hóa

| # | Điểm ma sát | Đề xuất |
|---|-------------|---------|
| S1 | **16 câu assessment** | Quá dài cho lần đầu. Giảm xuống 5–7 câu cốt lõi (mảng HR chính + level AI + mục tiêu). Phần còn lại có thể hỏi inline trong lúc học |
| S2 | **Welcome video modal** | Video YouTube không auto-play, user phải chủ động bấm. Không phải rào cản lớn nhưng làm chậm. Cho phép bỏ qua rõ ràng hơn hoặc chuyển thành micro-animation thay vì modal |
| S3 | **Form đăng ký 4 trường → 2 trường** | Chỉ giữ Email + Password. Họ tên có thể hỏi trong onboarding. SĐT bỏ hoàn toàn |

### 🟠 DELAY — Trì hoãn

| # | Điểm ma sát | Đề xuất |
|---|-------------|---------|
| D1 | **16 câu đánh giá đầy đủ** | Hỏi 3 câu đầu tiên trước khi vào học. Hỏi phần còn lại sau bài học đầu tiên — khi user đã có value và động lực |
| D2 | **Thu thập SĐT / thông tin công ty** | Delay về sau khi user đã active ít nhất 1 tuần |

### 🟢 KEEP — Giữ nguyên

| # | Điểm tốt | Lý do |
|---|----------|-------|
| K1 | **Card-based role selection** | UX clean, visual, dễ click — phù hợp với user không quen web phức tạp |
| K2 | **Progress bar trong assessment** | "38% xong", "56% xong" giảm anxiety hiệu quả |
| K3 | **Kết quả đánh giá cá nhân hóa (Bước 5/5)** | Card với level (3/5), tags vai trò, danh sách module — tạo cảm giác được hiểu. Đây là **Aha Moment** thực sự của sản phẩm |
| K4 | **Nav đầy đủ sau login** | Lộ trình, Trợ lý AI, Xếp hạng, Tiến bộ, Kỹ năng, Hỏi đáp — hệ sinh thái rõ ràng |
| K5 | **Floating AI Assistant button** | "Mở trợ lý AI" luôn hiển thị — điểm vào nhanh cho Core Action phụ |
| K6 | **Tone copywriting** | "em cần hỏi anh/chị", "Tự đánh giá thật", "Mất 2 phút thôi" — thân thiện, không áp lực |
| K7 | **Cấu trúc bài học module** | `/lo-trinh/nhan-su-m1` có flow rõ ràng: (1) Xem framework → (2) Copy prompt → (3) Chạy trên claude.ai → (4) Nộp kết quả để AI chấm → (5) Unlock nội dung sâu hơn. Không lý thuyết thuần túy — thực hành ngay |
| K8 | **Progressive unlock trong module** | "Hỏi sâu hơn", "Khoảnh khắc à há", "Tóm tắt" bị lock cho đến khi nộp bài — tạo incentive hoàn thành step 1 trước |
| K9 | **AI grading loop** | Nộp text kết quả từ Claude → hệ thống chấm tự động "theo rubric nghề" — đây là differentiator mạnh, tạo feedback loop không cần human |
| K10 | **Safety reminder trong prompt** | "Dùng dữ liệu mẫu / ẩn danh", "Không dán số liệu thật" — thoughtful, builds trust với HR user |
| K11 | **Bảng xếp hạng (/bang-xep-hang)** | Leaderboard 3 chiều (Phòng / Cả công ty / Cá nhân) × Tuần/Tổng + Activity feed "Bảng tin". Gamification loop đầy đủ: hoàn thành bài → điểm → thứ hạng → social visibility. Seed data tốt (có activity từ "Dương Văn Hùng") giúp page không trống với user mới |
| K12 | **Hỏi đáp cộng đồng (/topic-cau-hoi)** | Community Q&A: câu hỏi AI không trả lời được → cộng đồng giải → người giải đúng nhận +15 điểm. Mechanic tốt: knowledge sharing + point incentive + peer learning. Role filter đủ 6 vai trò |
| K13 | **Bộ kỹ năng (/bo-ky-nang)** | Empty state copy rõ: "Học xong một bài, bấm để giữ kỹ năng vào đây." + CTA "Lưu skill" — user biết cần làm gì tiếp theo, không confused |

---

## 4. Bug List

| # | Bug | Mức độ |
|---|-----|--------|
| B1 | Demo credentials `nhanvien@congty.vn` trả về lỗi "Email hoặc mật khẩu sai" | 🔴 Critical |
| B2 | Onboarding hiển thị "Bước 1/5 → Bước 3/5" — **Bước 2/5 không tồn tại** | 🟡 Medium |
| B3 | Nút "Bắt đầu học ngay →" ở Bước 5/5 không navigate được ngay — phải chờ rồi mới redirect | 🟡 Medium |
| B4 | Landing page tuyên bố "5 vai trò" nhưng onboarding chỉ có **1 vai trò** (Nhân sự/HR) | 🟡 Medium (broken promise) |
| B5 | **/lo-trinh page blank sau activation** — `<main>` element hoàn toàn rỗng. User không thể tìm thấy module từ Lộ trình page. Workaround duy nhất: vào /tro-ly rồi click link từ đó | 🔴 Critical (post-activation blocker) |
| B6 | **/tien-bo (Tiến bộ) page blank** — `<main>` rỗng hoàn toàn. Cùng pattern với B5, có thể cùng nguyên nhân (data chưa load hoặc component chưa render) | 🔴 Critical |
| B7 | **Onboarding chỉ có 1 role (HR) nhưng /topic-cau-hoi dropdown đã có 6 roles** (HR, Kinh doanh, Kế toán, Marketing, Hành chính, Văn phòng) — roles tồn tại trong hệ thống nhưng chưa được expose ở onboarding | 🟡 Medium (inconsistency) |

---

## 5. Before / After — Đề xuất Onboarding tối ưu

### BEFORE (hiện tại) — 25 bước, TFCA = ∞
```
Landing → Đăng nhập → Đăng ký (4 trường) → [BUG: login lại]
→ Welcome video modal → Chọn vai trò (1 option) → [BUG: skip bước 2]
→ Intro đánh giá → 16 câu hỏi (16 màn hình)
→ Kết quả → [DEAD END: activation gate]
```

### AFTER (đề xuất) — ~8 bước, TFCA < 5 phút
```
Landing → Đăng ký Google OAuth 1-click [hoặc Email + Password]
→ Chọn vai trò (3–5 options)
→ 3 câu nhanh (mảng HR chính + level AI + mục tiêu)
→ KẾT QUẢ NGAY — mở Module đầu tiên không cần activation
→ [CORE ACTION: hoàn thành bài học đầu tiên]
→ Sau bài 1: hỏi thêm để tinh chỉnh lộ trình
```

---

## 6. North Star Metric & Active User Definition (đề xuất)

**Core Action:** Hoàn thành ≥ 1 bài học AI trong lộ trình cá nhân hóa

**Active User:** User hoàn thành ít nhất **1 bài học/tuần** trong vòng **4 tuần đầu**

**North Star Metric gợi ý:**
```
WAL = Weekly Active Learners × CLR (Completion Rate bài đầu)
```

**Measurement Ladder hiện tại:**
- Traffic → ✅ Landing page hoạt động
- Visitor → ✅ Register/Login hoạt động
- Activation → ✅ Onboarding hoàn chỉnh (sau khi fix bug) → kết quả cá nhân hóa
- **Core Action → ⚠️ Đạt được sau activation thủ công, nhưng path bị gián đoạn bởi B5 (/lo-trinh blank)**
- **Core Action (sau B5 fix) → ✅ Module /lo-trinh/nhan-su-m1 hoạt động tốt, flow rõ ràng**
- Retention → ❌ Chưa đo được (cần user quay lại tuần 2+)
- Revenue → ❌ Không thấy monetization layer trong flow hiện tại

---

## 7. Tóm tắt ưu tiên hành động

| Ưu tiên | Hành động | Impact | Effort |
|---------|-----------|--------|--------|
| 🔴 P0 | Bỏ activation gate — cho user vào module đầu tiên ngay | TFCA: ∞ → ~8 phút | Medium |
| 🔴 P0 | Fix demo credentials hoặc xóa demo hint nếu chưa sẵn sàng | Ấn tượng đầu cực xấu | Low |
| 🔴 P1 | Auto-login sau register — xóa double-login step | -1 bước masat | Low |
| 🟡 P2 | Giảm assessment từ 16 câu → 5 câu cốt lõi | TFCA giảm ~3 phút | Medium |
| 🟡 P2 | Fix Bước 2/5 biến mất trong onboarding | UX consistency | Low |
| 🟡 P3 | Bỏ SĐT khỏi form đăng ký | Reduce form friction | Low |
| 🟢 P4 | Mở 5 vai trò còn lại trong onboarding (logic đã có trong /topic-cau-hoi — chỉ cần expose) | Roles đã tồn tại, onboarding chưa dùng | Low |
| 🔴 P1 | Fix /tien-bo blank (B6) — cùng pattern với B5, có thể fix cùng lúc | Broken nav item = poor retention loop | Low |

---

## 8. Đánh giá Post-Activation — Chất lượng Core Experience

**Kết luận sau khi vào được `/lo-trinh/nhan-su-m1`:**

Sản phẩm bên trong **tốt hơn nhiều** so với những gì onboarding gợi ý. Khi user đến được module đầu tiên:

| Chiều đánh giá | Nhận xét |
|----------------|----------|
| **Clarity** | Rõ ràng: 12 phút, Nhập môn, Học bằng thực hành — expectation set đúng |
| **Prompt framework** | 3 mảnh (Vai trò + Bối cảnh + Yêu cầu) — dễ nhớ, dễ áp dụng |
| **Action design** | Copy → Chạy → Nộp → Nhận feedback. Loop hoàn chỉnh, không lý thuyết suông |
| **AI grading** | Differentiator thực sự — chấm tự động theo rubric nghề, scalable |
| **Progressive unlock** | Incentivizes completion trước khi unlock nội dung sâu |
| **Safety copy** | Reminder về dữ liệu mẫu — professional, builds trust |

**Vấn đề lớn nhất còn lại (post-activation):** /lo-trinh page blank (B5) — user không thể tự tìm thấy module. Nếu không có floating /tro-ly button gợi ý, user sẽ bounce ngay sau activation.

**Nếu fix B5 + bỏ activation gate (P0):** TFCA dự kiến giảm từ ∞ xuống ~10–12 phút — chấp nhận được cho sản phẩm B2B học AI.

---

## 9. Test AI Chat — Phân tích hành vi Trợ lý AI

**2 câu hỏi được gửi trong cùng 1 conversation:**

### Câu 1: "Em đang cần viết JD cho vị trí Chuyên viên tuyển dụng, dùng AI được không? Bắt đầu từ đâu?"
**AI phản hồi:** Redirect sang module học — "Module mà bạn cần học là: **Viết JD chuẩn từ một mô tả ngắn**. Học xong bài này, bạn sẽ tự làm được mà không cần hỏi lại nữa nhé!"
- ✅ Đúng với triết lý thiết kế: "dạy tự dùng AI, không làm hộ"
- ⚠️ Module được đề xuất ("Viết JD chuẩn từ một mô tả ngắn") **không có link** — user không biết đi đâu
- ⚠️ Module name này có thể không tồn tại trong lộ trình hiện tại (chỉ thấy M1: "Claude là gì & vì sao HR nên dùng Claude")

### Câu 2: "Vậy prompt để viết JD thì viết như thế nào? Cho em ví dụ luôn được không?"
**AI phản hồi:** **Làm hộ trực tiếp** — Đưa ra prompt mẫu 4 phần (Vai trò + Bối cảnh + Yêu cầu + Định dạng) kèm code block + nút "Copy prompt"
- ✅ Prompt chất lượng tốt, đúng framework 4-part
- ✅ Copy prompt button trong chat — UX tốt
- 🔴 **Inconsistency với thiết kế**: Câu 1 → dạy học. Câu 2 → làm hộ. Không có nguyên tắc rõ ràng phân biệt khi nào teach vs. do

### 🔴 Finding quan trọng — Tension giữa AI Chat và Learning Path
Nếu user có thể hỏi AI trong chat và nhận được prompt mẫu ngay lập tức → **không có lý do để hoàn thành module bài học**. Điều này tạo ra internal competition với Core Action (hoàn thành bài). 

**2 hướng xử lý:**
- **Option A — Consistent Teacher:** AI chat chỉ gợi ý / hướng dẫn, không bao giờ give away prompt trực tiếp. Luôn link về module tương ứng
- **Option B — Complement:** AI chat có thể làm hộ, nhưng học trong module cho điểm / badge / kỹ năng. Phân biệt rõ 2 value proposition khác nhau
