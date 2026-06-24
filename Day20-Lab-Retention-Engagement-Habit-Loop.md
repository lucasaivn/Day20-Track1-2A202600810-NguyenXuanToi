# Day 20 Lab — Retention, Engagement & Habit Loop

> Tiếp tục prototype Ngày 18, áp dụng kiến thức Ngày 19 để đi từ use case và hành vi tự nhiên của người dùng tới core action, retention metric, onboarding và habit loop.

---

## Nộp bài

Nhóm tiếp tục sử dụng sản phẩm, scenario và prototype đã làm ở Ngày 18.

Nếu cần tạo repository riêng, đặt tên: `Day20-Lab-Track1-MSPV-Họ-Và-Tên`

Nhóm nộp **một liên kết duy nhất** tới prototype hoặc tập trình bày trực quan đã cập quyền xem.

---

## 1. Mục tiêu của bài lab

Ngày 18, mỗi nhóm đã được tự do chọn sản phẩm và scenario. Ngày 20 không yêu cầu lại đề bài hoặc tạo sản phẩm mới.

Bài lab sử dụng prototype Ngày 18 làm đầu vào để trả lời:

1. Use case nào đang được giải quyết?
2. Persona nào có use case đó?
3. Vấn đề xuất hiện với tần suất tự nhiên như thế nào?
4. Core action nào cho thấy người dùng thực sự nhận được value?
5. Ai được tính là active user?
6. Retention metric nào phù hợp và khớp sử dụng tự nhiên?
7. Onboarding cần đưa người dùng tới first core action như thế nào?
8. Nature và nurture được cân bằng ra sao?
9. Hook Model có phù hợp với sản phẩm không?
10. Cần tracking những event nào để tính các metric đã chọn?

**Logic của bài:**

```
Use case và persona
        ↓
Hành vi và tần suất tự nhiên
        ↓
Core action
        ↓
Định nghĩa active user
        ↓
Retention metric
        ↓
Onboarding + First core action / aha moment
        ↓
Nature + Nurture
        ↓
Habit Loop
        ↓
Tracking requirement
```

---

## 2. Điểm xuất phát

Nhóm tiếp tục một trong các sản phẩm đã chọn ở Ngày 18:

1. **AI Travel Planner.**
2. **AI Personal Assistant for Students.**
3. **AI Customer Support Agent.**
4. **Dự án nhóm đang phát triển** hoặc sản phẩm khác mà nhóm đã dùng trong bài Ngày 18.

Giữ lại: Sản phẩm, Scenario, Prototype đã chọn, Prototype và recovery flow Ngày 18.

Nhóm được chỉnh sửa prototype nếu phân tích Day 20 cho thấy onboarding chưa dẫn tới core action đủ nhanh hoặc chưa thể hiện rõ core value.

---

## 3. Đầu ra bắt buộc

Trong cùng prototype hoặc tập trình bày, nhóm bổ sung:

1. **Customer Retention Canvas — Use Case.**
2. **Core Action, Active User & Retention Metric.**
3. **Onboarding → First Core Action Journey** đã được audit và tối ưu.
4. **Measurement Ladder và North Star Metric.**
5. **Nature vs Nurture.**
6. **Hook Model.**
7. **Metric Tracking Requirement.**
8. **Phân chỉnh sửa prototype Ngày 18.**

Không cần nộp PRD hoặc worksheet riêng.

---

## Bài 1 — Hành vi tự nhiên và Use Case

Nền tảng của retention là hiểu đúng use case và persona.

Trước khi chọn DAU, WAU, MAU hoặc D7 Retention, nhóm phải xác định:

- **The Who:** Ai đang có vấn đề?
- **The Why:** Vì sao họ cần giải quyết vấn đề?
- **How Often:** Vấn đề tự nhiên xuất hiện bao lâu một lần?

---

## 4. Customer Retention Canvas — Use Case

Nhóm chỉ chọn **một use case chính** để phân tích sâu trong bài lab.

### 4.1. The Problem

**Câu hỏi:** Vấn đề được định nghĩa như thế nào bằng chính lời của người dùng?

Không mô tả bằng tính năng sản phẩm.

Không viết: *"Người dùng cần một AI assistant có dashboard thông minh."*

Hãy viết theo góc nhìn người dùng: *"Tôi mất quá nhiều thời gian để gom thông tin môn học và văn thường bỏ lỡ deadline."*

### 4.2. The Persona

**Câu hỏi:** AI là người đang có vấn đề đó?

Mô tả đủ cụ thể:
- Vai trò hoặc hoàn cảnh.
- Mục tiêu.
- Mức độ kinh nghiệm nếu có liên quan.
- Điều kiện làm thay đổi hành vi.

Đồng thời xác định **anti-persona**: *Ai không có vấn đề này hoặc không phải đối tượng của use case?*

Anti-persona giúp team tránh trộn dữ liệu của những nhóm có hành vi khác nhau.

### 4.3. The Why

**Câu hỏi:** Lý do hoặc động lực cốt lõi nào khiến persona muốn giải quyết vấn đề?

The Why phải giải thích outcome người dùng muốn đạt được, không chỉ lặp lại tính năng.

### 4.4. The Alternative

**Câu hỏi:** Hiện tại người dùng đang làm gì để giải quyết vấn đề mà chưa có sản phẩm của nhóm?

Alternative không nhất thiết là đối thủ trực tiếp.

Alternative có thể là: Làm thủ công, Dùng spreadsheet, Gọi điện hoặc nhắn tin, Tìm trên Google, Hỏi một người khác, Chấp nhận không giải quyết.

Alternative quan trọng vì nó cho thấy hành vi thật và giúp ước lượng natural frequency.

### 4.5. The Frequency

**Câu hỏi:** Người dùng trải nghiệm vấn đề này với tần suất như thế nào?

Chọn và giải thích:
- Nhiều lần mỗi ngày.
- Daily.
- Weekly.
- Monthly.
- Quarterly.
- Yearly.
- Theo project, mùa vụ hoặc không điều.

Không chọn frequency theo mong muốn của team.

Hãy quan sát: Người dùng thực hiện alternative bao lâu một lần? Frequency có thay đổi giữa các persona không? Frequency có thể đổi theo từng giai đoạn của use case không?

---

## 5. Canvas cần hoàn thành

| Thành phần | Câu hỏi | Câu trả lời của nhóm |
|---|---|---|
| The Problem | Vấn đề bằng lời của user là gì? | |
| The Persona | Ai có vấn đề đó? | |
| Anti-persona | Ai không thuộc use case này? | |
| The Why | Động lực cốt lõi là gì? | |
| The Alternative | Họ đang tự ải quyết bằng cách nào? | |
| The Frequency | Vấn đề tự nhiên xuất hiện bao lâu một lần? | |

### Ví dụ hướng dẫn

| Framework | Pinterest | HubSpot Sales Pro | Zillow |
|---|---|---|---|
| The Problem | "Tôi thấy chán" hoặc muốn mình quan tâm | Mất nhiều thời gian nhập CRM, follow-up và viết lại email | "Tôi muốn mua nhà" hoặc muốn theo dõi giá trị ngôi nhà |
| The Persona | Người dùng 25–40 tuổi | Sales rep cá nhân tại công ty cỡ trung | Người mua nhà lần đầu, hoặc homeowner theo dõi giá trị nhà |
| The Why | Quyết định nhanh, dễ và lưu lại để xem hoặc chia sẻ | Tự động hóa phần kém hiệu quả, tập trung vào chốt deal | Tìm và so sánh nhà hoặc nắm giá trị tài sản |
| The Alternative | Tạp chí, Google Images, hỏi chuyên gia | Gọi điện, nhắc thủ công, copy-paste email, nhập CRM bằng tay | Bảo đăng sẵn, môi giới, diễn đàn |
| The Frequency | Weekly với duyệt số thích; daily với lập kế hoạch dự án | Daily với sales rep; weekly với reporting | Yearly+ với mua bán nhà; thường xuyên hơn với Zestimate và content |

---

## Bài 2 — Từ Use Case tới Retention Metric

Metric phải đi từ use case, natural frequency và core behavior tạo value.

### 6. Xác định Core Action

**Câu hỏi:** Hành vi nào cho thấy người dùng thực sự nhận được value?

Core action:
- Gắn trực tiếp với use case.
- Gắn với việc giải quyết vấn đề.
- Có thể quan sát được.
- Không phải mọi click.

Ví dụ không đủ: Mở app, Đăng nhập, Xem một màn hình, Bấm bắt đầu nhưng chưa hoàn thành hành vi tạo value.

| Câu hỏi | Câu trả lời |
|---|---|
| Core job của use case là gì? | |
| Core action là gì? | |
| Vì sao action này cho thấy user nhận được value? | |
| Khi nào action này là dễ xảy ra? | |

### 7. Định nghĩa Active User

Slide Ngày 19 định nghĩa: *Active user là user được tính là "đang hoạt động" theo định nghĩa của team.*

Vì vậy nhóm phải trả lời:
- Chỉ mở app có được tính là active không?
- User phải thực hiện core action nào?
- Cần thực hiện bao nhiêu lần?
- Trong khoảng thời gian nào?

Hoàn thành câu: *"Một user được tính là active khi __________ trong __________."*

Ví dụ: *"Một sales rep được tính là active trong ngày khi hoàn thành ít nhất một automation task có giá trị."*

### 8. Chọn Retention Metric theo Natural Frequency

Retention trả lời: *Sau một khoảng thời gian, còn bao nhiêu user quay lại tiếp tục dùng sản phẩm?*

Nhóm không mặc định chọn D1, D7 hoặc D30.

Hãy chọn nhịp đo dựa trên frequency của use case:

| Natural Frequency | Metric có thể cân nhắc |
|---|---|
| Daily | DAU, D1/D7/D30 Retention, DAU/WAU hoặc DAU/MAU |
| Weekly | WAU, weekly cohort retention, WAU/MAU |
| Monthly | MAU, monthly cohort retention |
| Quarterly, yearly hoặc không đều | Chọn window phản ánh tần suất tự nhiên tiếp theo của use case; không áp daily retention |

| Thành phần | Câu trả lời |
|---|---|
| Persona và use case | |
| Natural frequency | |
| Core action | |
| Active user definition | |
| Retention metric | |
| Vì sao metric phù hợp với frequency? | |

### Ví dụ hướng dẫn

| Framework | Duolingo | Uber | Spotify |
|---|---|---|---|
| Use case | Học ngoại ngữ theo lộ trình. | Đặt xe khi cần di chuyển. | Nghe nhạc và podcast. |
| Natural cadence | Daily | Weekly | Daily |
| Core action | Học và duy trì học đồng học. | Hoàn thành chuyến đi. | Nghe nhạc. |
| Active user | User thực hiện ít nhất một học trong khoảng thời gian được chọn. | User hoàn thành ít nhất một chuyến đi được thực hiện thành toàn trong khoảng thời gian. | User có thể nghe trong khoảng thời gian. |
| Metric phù hợp | DAU | Rides per week | Time spent listening |

Không copy metric của sản phẩm khác. Bảng chỉ minh họa cách đi từ use case tới cadence, core action và metric.

---

## Bài 3 — Onboarding tới First Core Action

Mục tiêu của phần này là **thiết kế và tối ưu hành trình từ lúc user bắt đầu onboarding tới khi hoàn thành first core action và nhận được first value.**

Nhóm không chỉ định đầu first core action trên prototype cũ. Nhóm phải audit flow hiện tại, chỉ ra friction và sửa prototype.

### 9. Audit prototype Ngày 18

Trên prototype cũ, đánh dấu:

1. User bắt đầu onboarding ở đâu?
2. Họ phải đi qua những bước nào?
3. First core action xảy ra ở đâu?
4. Aha moment xảy ra ở đâu?
5. Time to First Core Action hiện dài bao lâu?
6. Time to Value hiện dài bao lâu?
7. Bước nào không cần thiết trước core action?
8. Recovery flow nào của Ngày 18 được giữ lại?

**Vẽ Current-State Journey:**

```
Entry point
        ↓
Onboarding step 1
        ↓
Onboarding step 2
        ↓
Setup
        ↓
First core action
        ↓
Aha moment / First value
```

**Friction Audit** — Đánh dấu mỗi bước bằng một trong bốn nhãn:

| Nhãn | Ý nghĩa |
|---|---|
| Keep | Bắt buộc trước first core action |
| Remove | Không cần thiết và chưa tạo value |
| Delay | Cần cho sản phẩm nhưng có thể hỏi sau first core action |
| Simplify | Cần thiết nhưng đang quá khó hoặc quá đài |

Kiểm tra:
- Có quá nhiều thông tin phải nhập không?
- Có yêu cầu tạo tài khoản hoặc cấp permission quá sớm không?
- Có bước giải thích dài trước khi user được thử không?
- Có cầu hình nào có thể Delay tới sau first value không?
- CTA trên mỗi màn hình có rõ không?
- User có biết mình đang tiến gần tới value không?

**Bảng Current State:**

| Chỉ số | Current state |
|---|---|
| Số bước tới first core action | |
| Số trường thông tin phải nhập | |
| Số permission phải cấp | |
| Time to First Core Action ước tính | |
| Time to Value ước tính | |
| Điểm drop-off có khả năng cao nhất | |

Nếu chưa có dữ liệu tracking, ghi rõ tính là ước tính từ prototype.

### 10. Thiết kế lại hành trình

Prototype phải theo:

```
1. User bước vào sản phẩm
        ↓
2. Hiểu value proposition
        ↓
3. Thực hiện minimum setup
        ↓
4. Bước hướng dẫn thực hiện hành vi ví thật
        ↓
5. First core action
        ↓
6. Evidence of value
        ↓
7. Aha moment / First value
        ↓
8. Bước tiếp theo
```

**Yêu cầu tối ưu.** Nhóm phải:
- Loại bỏ hoặc Delay bước không cần thiết trước core action.
- Chỉ giữ minimum setup cần đề tạo first value.
- Làm CTA rõ ràng trên mỗi màn hình đủ rõ.
- Giải thích permission đúng thời điểm.
- Cho user thực hiện hành vi ví thay vì chỉ xem product tour.
- Hiển thị evidence of value ngay sau core action.
- Giữ hoặc cải thiện ít nhất một recovery path từ Ngày 18.

**Activation và Time to Value.** Nhóm phải chỉ rõ:
- **Activation:** thời điểm user lần đầu thực sự nhận được giá trị.
- **Activation Rate:** tỷ lệ user đạt activation.
- **Time to First Core Action:** thời gian từ lúc bắt đầu onboarding tới core action đầu tiên.
- **Time to Value:** thời gian từ lúc vào sản phẩm tới first value.

Không bắt buộc activation, first core action và aha moment phải là cùng một event. Nhóm phải giải thích lựa chọn.

**Recovery Path.** Chọn ít nhất một trường hợp: User chưa có dữ liệu, User từ chối permission, Kết quả đầu tiên chưa phù hợp, Action thiết lại hoặc đi giản đoạn, User chưa sẵn sàng hoàn thành core action.

Recovery không được kết thúc ở màn hình lỗi. Nó phải đưa user quay lại journey tới core action.

**Before/After Comparison:**

| Tiêu chí | Before | After | Vì sao thay đổi? |
|---|---|---|---|
| Số bước tới core action | | | |
| Số trường phải nhập | | | |
| Permission trước core action | | | |
| Time to First Core Action | | | |
| Time to Value | | | |
| Điểm drop-off chính | | | |
| Evidence of value | | | |
| Recovery path | | | |

Nhóm không được nói "flow mới đã dùng được hơn". Phải chỉ ra thay đổi cụ thể trên prototype.

---

## Bài 4 — Measurement Ladder và North Star Metric

### 11. Đặt metric vào Measurement Ladder

Từ các metric trong slide Ngày 19, chọn những metric phù hợp với sản phẩm:

```
Marketing / Traffic
        ↓
Visitor
        ↓
Activation
        ↓
Core Action
        ↓
Retention
        ↓
Revenue
```

**Usage / Active:**
- Active user.
- DAU.
- WAU.
- MAU.

**Activation & Retention:**
- Activation.
- Activation Rate.
- Time to Value.
- Retention.
- D1/D7/D30 Retention.
- Cohort Retention.
- Churn.

**Engagement và Stickiness:**
- Engagement.
- Stickiness: DAU/MAU.
- DAU/WAU.
- WAU/MAU.
- Session Length.
- Frequency.
- Số session trên user trong tuần.
- Time spent trên user.

**Business:**
- CAC.
- LTV.
- Payback Period.
- Revenue.

Không cần dùng tất cả metric. Chỉ chọn metric trả lời được câu hỏi của sản phẩm.

### 12. North Star Metric và Input Metrics

North Star Metric là chỉ số cốt lõi phản ánh giá trị chính mà sản phẩm tạo ra.

North Star Metric cần:
- Thể hiện value.
- Đại diện cho vision và strategy.
- Là leading indicator.
- Không phải vanity metric.
- Có thể hành động được.
- Dễ hiểu.
- Có thể đo được.

Nhóm phải nộp:

1. Một North Star Metric.
2. Tối đa ba Input Metrics tác động tới North Star Metric.
3. Một kết quả business hoặc customer value ở trung hoặc dài hạn.
4. Xác định đâu là leading indicator và đâu là lagging indicator.

```
The Work
        ↓
Input Metrics
        ↓
North Star Metric
        ↓
Mid/Long-term Business Results
and Customer Value
```

Nhóm phải giải thích một trade-off có thể xảy ra.

Ví dụ: *"Tăng số vị trí quảng cáo có thể tăng ad revenue nhưng làm engagement giảm."*

---

## Bài 5 — Nature, Nurture và Habit Loop

### 13. Nature vs Nurture

**Nature** là nhịp nhu cầu tự nhiên của user:
- Vấn đề xảy ra bao lâu một lần?
- User tự nhiên quay lại với loại sản phẩm này theo nhịp nào?
- Nhịp đó khác nhau giữa các persona hoặc use case như thế nào?

**Nurture** là những gì sản phẩm hoặc team chủ động làm để nuôi dưỡng và khuyến đạc nhịp tự nhiên:
- Onboarding.
- Notification.
- Email reminder.
- Content.
- CRM.
- Trigger trong sản phẩm.

Nurture không tạo ra nhu cầu từ số 0.

Nhóm phải đề xuất:

| Nội dung | Câu trả lời |
|---|---|
| Natural frequency của use case | |
| Internal trigger | |
| External trigger hiện có | |
| Một hoạt động nurture phù hợp | |
| Vì sao nurture không quá đẩy hoặc quá thụa? | |
| Metric dùng để theo dõi tác động | |

Nếu core use case có frequency thấp, nhóm cần cân nhắc hành vi hoặc use case liên quan có frequency cao hơn để duy trì sự hiện diện.

Ví dụ từ Zillow: Core use case mua hoặc bán nhà xảy ra rất thưa. Zestimate và content tạo thêm các điểm chạm thường xuyên hơn. Không vì vậy mà giả định user sẽ mua nhà hàng ngày.

### 14. Hook Model

Chỉ thiết kế habit loop sau khi đã hiểu natural frequency.

#### 14.1. Kiểm tra sản phẩm có thực sự cần habit không

Trước khi thiết kế Hook Model, nhóm trả lời:

1. Vì sao business logic user có hành vi này trở thành habit?
2. Vấn đề nào của user đang được giải quyết?
3. Hành vi cụ thể nào nhóm muốn được lặp lại?
4. Hành vi đó tự nhiên xuất hiện với frequency nào?
5. Sản phẩm có đủ frequency hoặc perceived utility để đi vào habit zone không?

Nếu sản phẩm có frequency thấp hơn weekly, việc hình thành habit sẽ khó hơn đáng kể. Không dùng Hook Model để ép một use case vốn có frequency thấp thành habit hàng ngày.

#### 14.2. Trigger

Trigger là bước đầu tiên của Hook Model.

- **External trigger:** tác nhân bên ngoài chỉ cho user biết cần làm gì tiếp theo.
- **Internal trigger:** nhu cầu hoặc cảm xúc khiến user tự tìm tới sản phẩm.

External trigger có thể là paid, earned, relationship hoặc owned.

Nhóm thực hiện:

1. Chọn một persona cụ thể.
2. Xác định họ đang làm gì ngay trước core action.
3. Dùng kỹ thuật 5 Whys để tìm ba internal trigger có thể có.
4. Chọn internal trigger nào thường xuyên nhất.
5. Xác định external trigger nào xuất hiện ở đâu và lúc nào.

Hoàn thành câu: *"Mỗi khi user __________, họ cảm ________."*

Vẽ đâu là internal trigger. Về sau là hành vi nhóm muốn tạo ra.

#### 14.3. Action

**Câu hỏi:** Hành vi đơn giản nhất user cần thực hiện để nhận được reward là gì?

Một action xảy ra khi có đủ từ:
- Motivation.
- Ability.
- Trigger.

Mục tiêu thiết kế là làm cho action trở nên dễ thực hiện hơn.

Nhóm phải:

1. Điểm số bước từ lúc internal trigger xuất hiện tới khi user nhận được outcome.
2. Xác định rào cản cần làm giảm Ability.
3. Đề xuất ba cách có thể làm action dễ làm hơn.

Kiểm tra các loại rào cản:
- **Time:** mất quá nhiều thời gian.
- **Brain cycles:** khó hiểu hoặc phải suy nghĩ quá nhiều.
- **Money:** chi phí quá cao.
- **Physical effort:** cần quá nhiều thao tác hoặc công sức.
- **Social deviance:** hành vi khiến user không thoải mái về mặt xã hội.
- **Non-routine:** hành vi quá mới hoặc chưa có quy thường.

#### 14.4. Variable Reward

Ba loại variable reward trong slide:

- **The Tribe:** kết nối, công nhận hoặc cảm giác thuộc về.
- **The Hunt:** tìm kiếm tài nguyên hoặc thông tin.
- **The Self:** làm chủ, hoàn thành và cảm nhận tiến bộ.

Không phải sản phẩm nào cũng cần cả ba loại.

Nhóm trả lời:
- Reward nào giúp giải quyết nhu cầu cho pain của user?
- User thấy điều gì thỏa mãn, hữu ích hoặc đáng kích lệ?
- Reward thuộc The Tribe, The Hunt hay The Self?
- Reward có phục vụ core action hay chỉ là gamification gắn thêm?

#### 14.5. Investment

User bỏ vào sản phẩm một phần công sức để làm tăng khả năng quay lại.

Nhóm phải chỉ ra:
- User đầu tư gì?
- Investment lưu lại value dưới dạng content, data, followers, reputation hay skill?
- Investment đó tạo value cho lần sử dụng sau như thế nào?
- Investment tạo hook "load" trigger tiếp theo ra sao?
- Sau bao lâu trigger tiếp theo xuất hiện?

#### 14.6. Kiểm tra tác động lên người dùng

Trước khi điền Hook Model, nhóm trả lời:
- Thành viên trong nhóm có sẵn sàng sử dụng sản phẩm chế hay không?
- Hành vi có được thiết kế có thể chỉ thiện cuộc sống công việc của user không?
- Có lo có thể làm user mất kiểm soát hoặc thực hiện hành vi ngoài ý muốn không?

### 15. Hook Review cần hoàn thành

| Thành phần | Câu hỏi |
|---|---|
| Why Habit? | Vì sao user hoặc business cần hành vi này trở thành habit? |
| Intended Behavior | Hành vi cụ thể nào cần được lặp lại? |
| Frequency & Utility | Hành vi có đủ thường xuyên hoặc đủ hữu ích khi hình thành habit không? |
| Internal Trigger | Nhu cầu hoặc cảm xúc xuất hiện thường xuyên nhất? |

| Thành phần | Câu hỏi |
|---|---|
| External Trigger | Trigger nào xuất hiện đúng nơi và đúng thời điểm? |
| Action | Hành vi đơn giản nhất để nhận reward là gì? |
| Motivation | User muốn thực hiện action vì điều gì? |
| Ability | Rào cản nào cần được loại bỏ bỏ đề action dễ làm hơn? |
| Variable Reward | The Tribe, The Hunt hay The Self? |
| Investment | User bỏ ra content, data, reputation, skill hoặc công sức gì? |
| Next Trigger | Investment dẫn tới trigger tiếp theo như thế nào? |
| User Impact | Habit này có thực sự có ích cho user không? |

Sau khi điền bảng, nhóm sửa Hook Flow trực tiếp trên prototype:

```
Internal / External Trigger
        ↓
Action
        ↓
Variable Reward
        ↓
Investment
        ↓
Trigger cho vòng tiếp theo
```

Nếu câu trả lời là không, không ép habit loop giả tạo. Hãy quay lại Nature vs Nurture và chọn tác động phù hợp với nhịp thật.

> Tài liệu đọc thêm bắt buộc: *Hooked: How to Build Habit-Forming Products* — Supplemental Workbook, Nir Eyal và Ryan Hoover. Học viên không cần nộp workbook riêng.

---

## Bài 6 — Metric Tracking Requirement

Phần này không tạo thêm metric mới. Nhóm chỉ chuyển các metric đã chọn ở Bài 2 và Bài 4 thành yêu cầu tracking trong sản phẩm.

### 16. Bảng định nghĩa metric

Với mỗi metric được chọn, ghi:

| Trường | Nội dung |
|---|---|
| Tên metric | Dùng đúng tên metric đã chọn |
| Câu hỏi cần trả lời | Team muốn biết điều gì? |
| Đơn vị | Ai hoặc hành vi nào được đo? |
| Công thức | Tỷ số, mẫu số hoặc cách tính tổng hợp |
| Khoảng thời gian | Daily, weekly, monthly hoặc window khác |
| Segment | Metric áp dụng cho persona/use case nào? |
| Event cần có | Event nào cung cấp dữ liệu? |

### 17. Bảng yêu cầu tracking event

Chỉ tạo event cần thiết để tính các metric đã chọn.

| Trường | Nội dung |
|---|---|
| Event name | Tên event |
| Event được ghi khi nào? | Hành vi hoặc trạng thái nào xảy ra và thực tế sự việc xảy ra? |
| User identity | Dùng user_id, account_id hay định danh văn? |
| Properties | Dữ liệu nào cần thiết để tính metric hoặc phân tích segment? |
| Metric có đúng event | Metric nào dùng event này? |
| Tránh ghi trùng | Refresh, retry hoặc autosave được xử lý thế nào? |

### 18. Gắn event lên flow

Gắn event trực tiếp lên hành trình onboarding tới core action:

```
Onboarding bắt đầu
        ↓
[event]
        ↓
User hoàn thành bước cần thiết
        ↓
[event]
        ↓
First core action
        ↓
[event]
        ↓
Activation / Aha moment
```

### 19. Tiêu chí nghiệm thu tracking

Viết ít nhất bốn tiêu chí:

1. Event chỉ được ghi khi hành vi thực sự xảy ra.
2. Refresh, retry hoặc autosave không làm dữ liệu bị ghi trùng.
3. Event có đủ identity và properties cần thiết.
4. Timestamp và timezone phải quản lý.
5. Event có thể được dùng độc lập để tính metric đúng công thức.
6. Không thu thập dữ liệu cá nhân không cần thiết.

Ví dụ: *"Hệ thống chỉ ghi nhận task_completed khi nhiệm vụ chuyển từ trạng thái chưa hoàn thành sang hoàn thành. Tải lại trang không được tạo thêm event cho cùng lần chuyển trạng thái."*

---

## 20. Cấu trúc tệp gọi ý

```
00 — Prototype Ngày 18 / Current State
01 — Customer Retention Canvas
02 — Core Action & Active User
03 — Natural Frequency & Retention Metric
04 — Onboarding Audit
05 — Redesigned Onboarding + First Core Action
06 — Before/After & Recovery Path
07 — Measurement Ladder
08 — North Star & Input Metrics
09 — Nature vs Nurture
10 — Hook Review
11 — Metric Tracking Requirement
12 — Demo Path
```

---

## 21. Demo — 8 phút/nhóm

| Thời gian | Nội dung |
|---|---|
| 0:00–1:00 | Problem, Persons, Why và Alternative |
| 1:00–1:50 | Frequency, Core Action và Active User |
| 1:50–2:40 | Retention Metric và lý do chọn cadence |
| 2:40–4:20 | Current flow, redesigned onboarding, first core action và TTV |
| 4:20–5:15 | North Star, Input Metrics, leading và lagging indicators |
| 5:15–6:20 | Nature vs Nurture và Hook Model |
| 6:20–7:15 | Tracking requirement |
| 7:15–8:00 | Before/After và thay đổi quan trọng nhất |

---

## 22. Tiêu chí đánh giá đơn giản

| Tiêu chí | Sẽ đạt khi |
|---|---|
| Product logic | Use case, persona, natural frequency, core action và active user nối được nhau. |
| Onboarding → First Core Action | Có current flow, flow tối ưu, activation/TTV, recovery và Before/After rõ ràng. |
| Metrics & Habit | Retention metric, North Star, Nature/Nurture và Hook Model phù hợp với use case. |
| Tracking | Metric có định nghĩa, công thức, event và properties đủ để tính; cách tracking ghi nhận sai hoặc trùng. |

Mỗi tiêu chí được đánh dấu **Đạt** hoặc **Cần bổ sung**. Checklist bên dưới được dùng để phán xét chi tiết.

---

## 23. Checklist trước khi nộp

### Use case và natural behavior

- [ ] Chỉ tập trung vào một use case chính.
- [ ] Có The Problem, Persona, Anti-persona, Why và Alternative.
- [ ] Frequency được suy ra từ hành vi thật và alternatives.

### Core action và metric

- [ ] Core action cho thấy user nhận được value.
- [ ] Active user có định nghĩa và ngưỡng rõ.
- [ ] Retention metric phù hợp natural frequency.
- [ ] Không copy DAU, WAU, MAU hoặc D7 từ sản phẩm khác.

### Onboarding → First Core Action

- [ ] Có current-state journey.
- [ ] Mỗi bước được audit theo Keep, Remove, Delay hoặc Simplify.
- [ ] Có redesigned journey dẫn tới first core action.
- [ ] Có activation, Time to First Core Action, TTV và aha moment.
- [ ] Đã chỉ ra bước thừa hoặc friction trước core action.
- [ ] Có Before/After comparison.
- [ ] Giữ hoặc cải thiện recovery flow Ngày 18.

### Measurement

- [ ] Có Measurement Ladder.
- [ ] Có một North Star Metric và tối đa ba Input Metrics.
- [ ] Phân biệt leading và lagging indicator.
- [ ] Có một trade-off cần theo dõi.

### Nature, Nurture và Hook

- [ ] Phân biệt natural frequency với nurture.
- [ ] Nurture không quá đẩy hoặc quá thụa.
- [ ] Hook Review có Trigger, Action, Variable Reward và Investment.
- [ ] Đã xác định rào cản làm action khó thực hiện.
- [ ] Đã kiểm tra habit có thực sự có ích cho user không.
- [ ] Không ép habit nếu frequency và utility không phù hợp.

### Tracking

- [ ] Metric có định nghĩa, công thức, window và segment.
- [ ] Event map trực tiếp tới metric.
- [ ] Event được gắn lên flow onboarding/core action flow.
- [ ] Có ít nhất bốn tiêu chí nghiệm thu.

### Submission

- [ ] Chỉ nộp một liên kết đã đủ cấp quyền xem.
- [ ] Phần biệt nộp phần Ngày 18 và phần bổ sung Day 20.
- [ ] Có demo path.
- [ ] Demo không quá 8 phút.

---

*Day 20 Lab - Retention, Engagement & Habit Loop - Khoá 02*
