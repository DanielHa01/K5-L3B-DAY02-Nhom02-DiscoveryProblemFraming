# Báo cáo nhóm — Day 02 Discovery & Problem Framing

> Bản chung của nhóm, viết trên repo do nhóm trưởng fork. Không copy file này sang repo cá nhân.
> Template chi tiết và prompt mẫu: [docs/01-worksheet.md](../../docs/01-worksheet.md). Bài mẫu: [docs/02-deliverable-example.md](../../docs/02-deliverable-example.md).

## 1. Thông tin nhóm

- Tên nhóm:
- Thành viên: xem `TEAM.md`
- Candidate problem được chọn (1 câu):
- Quyết định cuối: Go / Not Yet / No-Go

---

## 2. Hội tụ nhóm (CP3)

### 2.1. Pitch

| # | Người đưa ra | Candidate (Job Story ngắn) | Actor | Bottleneck | Câu hỏi phản biện nhận được (ai hỏi) |
|---:|---|---|---|---|---|
| 1 | Nguyễn Thiên Long | Tìm thông tin trong bài giảng PDF | Học sinh, sinh viên | Đọc slide và tài liệu thủ công | Nếu các tài liệu có nhắc đến tài liệu ngoài thì hệ thống xử lý thế nào? (Dương) |
| 2 | Nguyễn Thiên Long | Lọc và bóc tách thuật ngữ chuyên ngành tiếng Anh | Học sinh, sinh viên | Đọc và tra từ điển tốn thời gian | Làm sao để Agent biết được context của từ cần dịch và dịch đúng nghĩa mà từ đấy đang diễn đạt? (Dương) |
| 3 | Nguyễn Thiên Long | Tự động tìm kiếm và lọc phòng trọ trên Facebook | Người có nhu cầu thuê trọ | Thời gian tìm, nhắn tin cho từng chủ trọ | Hệ thống này đã tồn tại từ các trang web bất động sản, Agent có giúp ích gì trong trường hợp này? (Bách) |
| 4 | Lê Bá Nguyên | Đối soát COD cuối ngày  | Kế toán | Tìm nguyên nhân sai sót | Khi các thông tin đã được chuẩn hóa thì các quy trình này có thể được thay thế bằng workflow có sẵn để tiết kiệm thời gian (Dương) |
| 5 | Lê Bá Nguyên | Đơn hoàn, thất lạc, hư hỏng | Kế toán, logistic | Mất thời gian chờ để tổng hợp thông tin | Các thông tin này đã được các công ty số hóa nên việc tổng hợp thông tin đơn giản hơn (Long) |
| 6 | Lê Bá Nguyên | Xuất hóa đơn điện tử cho Shopee | Kế toán, nhân viên bán hàng | Kiểm tra thông tin và sửa lỗi bằng tay dễ sai | Làm sao để bảo vệ thông tin khách hàng khi để Agent tự do đọc hóa đơn chứng từ (Tuấn) |
| 7 | Nguyễn Ngọc Bách | Tìm hiểu thông tin dự án mới | Dev mới vào dự án | Tìm và tổng hợp tài liệu từ nhiều nơi | Các công ty lớn thường coi trọng việc ghi chép và lưu trữ tài liệu, senior dev, BA, PO có thể tạo ra các tài liệu hướng dẫn và mô tả code để giúp dev mới vào, đây có phải là pain thật không? (Dương) |
| 8 | Nguyễn Ngọc Bách | Yêu cầu mơ hồ từ khách hàng | PM, PO, Dev | Hỏi vòng vo để làm rõ yêu cầu | Làm sao để biết được quyết định của Agent giống với quyết định của khách hàng, có nhiều rủi ro? (Nguyên) |
| 9 | Nguyễn Văn Tuấn | Review Pull Request lớn trong nhóm lập trình | Dev, Peer reviewer | Mất thời gian đọc diff và hiểu code | Khi peer review, phần quan trọng là đọc từng dòng diff để bắt lỗi, không chỉ là lỗi logic mà cần kiểm tra độ clean của code, đây có phải vấn đề thực tế? (Dương) |
| 10 | Nguyễn Văn Tuấn | Giải quyết xung đột Git merge conflict khi làm việc nhóm | Dev, PO, Tech Lead | Đi hỏi, đối chiếu code, test | Làm sao để Agent biết context của code để sửa chính xác với yêu cầu của khách hàng? (Dương) |
| 11 | Nguyễn Văn Tuấn | Rà soát checklist nộp bài lab và cấu trúc repo theo rubric | Học sinh, sinh viên làm bài tập nhóm | Kiểm tra, rà soát lại trước khi nộp bài | Kiểm tra lại bài là một phần trong việc học, đây có phải là pain mà người thật đang gặp phải? (Long) |
| 12 | Hà Phan Đại Dương | Nhập liệu thủ công | Kế toán | Mất thời gian tổng hợp, phân loại và nhập dữ liệu | Có thể đảm bảo về vấn đề bảo mật khi sử dụng Agent? (Tuấn) |
| 13 | Hà Phan Đại Dương | Giải thích chi phí | Kế toán, CEO | Mất thời gian tra cứu thông tin để trả lời câu hỏi của CEO | Có thật sự mất thời gian khi trả lời câu hỏi của CEO, CEO có hỏi về vấn đề này thường xuyên? (Nguyên) |
| 14 | Hà Phan Đại Dương | Phân loại chi phí | Kế toán | Xác định và phân loại các chi phí khi làm báo cáo | Có thể chuẩn hóa quy trình và không cần sử dụng AI được không? (Long) |

### 2.2. Cluster

| Cluster | Các candidate | Pattern chung |
|---|---|---|
| A | 1, 2, 7, 13 | Tìm kiếm, đọc hiểu và tổng hợp thông tin từ nhiều nguồn. |
| B | 4, 6, 11, 12, 14 | Xử lý dữ liệu có cấu trúc, đối soát, phân loại và tự động hóa công việc lặp lại. |
| C | 3, 5, 8, 9, 10 | Xử lý tình huống phức tạp, thông tin không đầy đủ và các trường hợp cần suy luận. |

### 2.3. Opportunity Solution Tree rút gọn

Gốc là **1 outcome**. Nhánh là **opportunity** (nhu cầu, pain), không phải tính năng hay công cụ.

```text
OUTCOME: Giảm thời gian và công sức thực hiện công việc,
đồng thời đảm bảo chất lượng và độ chính xác.
├── Opportunity A: Người dùng mất nhiều thời gian tìm kiếm, đọc hiểu và tổng hợp thông tin từ nhiều nguồn.
├── Opportunity B: Người dùng phải thực hiện nhiều thao tác lặp lại khi nhập liệu, kiểm tra, đối soát và phân loại dữ liệu.
└── Opportunity C: Người dùng gặp khó khăn khi xử lý các tình huống mơ hồ, ngoại lệ hoặc cần ra quyết định dựa trên nhiều ngữ cảnh.
```

Những ý đã gạch bỏ vì là solution đội lốt opportunity:

- Xây workflow giúp giảm thời gian cho các công việc lặp lại
- Dùng RAG/LLM/OCR tự động hóa việc tra cứu, lưu trữ tài liệu

### 2.4. Chấm điểm shortlist (1–5)

| Candidate | Actor rõ | Quy trình rõ | Pain có bằng chứng | Impact đo được | Vừa sức lab | So sánh được No AI/Rule/Workflow/Agent | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Giải quyết xung đột Git merge conflict khi làm việc nhóm | 5 | 5 | 5 | 4 | 5 | 5 | 5 | 34 |
| Tìm hiểu thông tin dự án mới | 3 | 4 | 1 | 3 | 5 | 1 | 5 | 24 |
| Nhập liệu thủ công | 5 | 4 | 4 | 5 | 5 | 3 | 2 | 28 |

**Candidate được chọn:** Giải quyết xung đột Git merge conflict khi làm việc nhóm

**Vì sao chọn:** Các thành viên đều có kinh nghiệm trong domain này và đây là một vấn đề khá thú vị

**Vì sao loại các candidate còn lại:** Các vấn đề kia 1 là đã có phương án khác, 2 là các thành viên không hiểu rõ vấn đề

**Xử lý bất đồng (nếu có):**

---

## 3. Kiểm chứng + research giải pháp đã có (CP4)

### 3.1. Assumption Map

| # | Giả định | Loại (Value / Usability / Feasibility / Viability) | Quan trọng (1–5) | Đã có bằng chứng (1–5) | Kiểm chứng trước? |
|---:|---|---|---:|---:|---|
| 1 | Agent có thể sửa và test được code | Feasibility | 5 | 5 | ✅ |
| 2 | Agent đọc được context của code dựa trên ticket hay issue | Feasibility | 5 | 5 | ✅ |
| 3 | Dev gặp khó khăn trong việc sửa conflict | Value | 3 | 3 | - |
| 4 | Agent chạy theo vòng lặp có thể đốt token | Usability | 5 | 5 | ✅ |

*Điền 4–6 giả định; xóa dòng thừa.*

Giả định nhóm kiểm chứng trong buổi này:

### 3.2. Kiểm chứng

Cách đã dùng: Phỏng vấn / Survey / Log, ticket, review

Interview snapshot (mỗi buổi phỏng vấn một bảng, hoặc đặt file trong `report/assets/cp4-interview-snapshot-N.md`):

| Trường | Nội dung |
|---|---|
| Người được hỏi (vai trò, không ghi tên thật) | Dev, sinh viên đẫ từng làm việc nhóm và gặp vấn đề này |
| Câu nói đáng nhớ nhất (nguyên văn) | Khi gặp phải merge conflict thì quy trình sửa là gì? Mất bao lâu để sửa? |
| Lần gần nhất gặp vấn đề này: chuyện gì đã xảy ra? | Ngày hôm qua, 2 dev có conflict ngồi với nhau để trao đổi |
| Hiện đang xử lý bằng cách nào (workaround)? | Các dev ngồi lại với nhau mỗi khi có conflict |
| Mất bao lâu, bao lần? | Mỗi lần mất tầm 15-30 phút tùy từng conflict |
| Insight / opportunity rút ra | Pain này có thật nhưng có nhiều rủi ro |

Tổng hợp:

| Nguồn | Số người / số mẫu | Tín hiệu xác nhận | Tín hiệu phản bác |
|---|---:|---|---|
| Phỏng vấn | 10 | 10/10 đã từng sửa conflict và muốn dùng AI để sửa nhanh hơn | 8/10 còn nghi ngờ về khả năng để AI tự sửa |

**Nhóm đã sửa problem thế nào sau kiểm chứng:** Thêm Agent để giúp Agent code có thêm context và 1 Agent build và test trước và sau khi sửa để đảm bảo độ chính xác

### 3.3. Research giải pháp đã có

| Công cụ / case / pattern | Link | Giải bước nào trong quy trình? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
|---|---|---|---|---|---|
| GitHub Copilot – Agent Merge | https://docs.github.com/en/copilot/how-tos/copilot-on-github/use-copilot-agents/watch-and-fix-pull-requests?utm_source=chatgpt.com | Theo dõi PR → phát hiện conflict → AI sửa code → chạy CI → cập nhật PR | Tự động kích hoạt khi PR bị conflict; chạy trên cloud; kết hợp auto-merge. | Cần Copilot trả phí và quyền tổ chức phù hợp; chưa hỗ trợ stacked PR và PR từ fork; không thay thế review | Event-driven Agent tự động xử lý conflict khi phát sinh, không cần developer khởi chạy thủ công |
| GitHub Copilot – Fix with Copilot | https://docs.github.com/en/copilot/how-tos/use-copilot-agents/cloud-agent/use-cloud-agent-on-github?utm_source=chatgpt.com | Developer kích hoạt → AI phân tích conflict → sửa code → build/test/lint → yêu cầu review | Tích hợp ngay trên GitHub PR; có thể gọi bằng @copilot; agent tự push bản sửa. | Cần người chủ động kích hoạt; test pass không bảo đảm giữ đúng nghiệp vụ | Áp dụng human-in-the-loop, AI tạo bản sửa nhưng developer xác nhận trước khi merge |
| Cursor – AI Resolve Conflicts | https://docs.cursor.com/en/more/ai-commit-message?utm_source=chatgpt.com | Developer gặp conflict → Resolve in Chat → agent phân tích hai phía → đề xuất sửa → developer áp dụng | Tương tác bằng ngôn ngữ tự nhiên; phù hợp conflict cần hiểu logic code. | Chưa phải hệ thống tự phát hiện và xử lý PR trên server; cần developer review và thao tác | Xây dựng context-aware resolver hiểu ý định thay đổi thay vì chỉ chọn ours/theirs |

---

## 4. Quy trình trước/sau (CP5)

### 4.1. Quy trình hiện tại

Sơ đồ (ASCII, Mermaid hoặc link ảnh trong `report/assets/`):

```text
[1 Dev phát hiện conflict khi merge/rebase]
→ [2 Đọc diff, lịch sử commit và ticket của hai nhánh]
→ [3 Trao đổi với dev liên quan để thống nhất ý định thay đổi] ← BOTTLENECK
→ [4 Sửa conflict, build/test và sửa lại nếu lỗi]
→ [5 Peer review, dev xác nhận và merge]
```

| Bước | Actor | Input | Output | Thời gian / tần suất | Ghi chú |
|---:|---|---|---|---|---|
| 1 | Dev tích hợp | Hai nhánh cần tích hợp | Danh sách file bị conflict | Mỗi lần phát sinh conflict; chưa đo riêng | Chưa có số liệu tần suất theo tuần |
| 2 | Dev tích hợp | Diff, commit, ticket/issue | Ngữ cảnh thay đổi của hai phía | Chưa đo riêng | Thiếu ticket phải hỏi tác giả |
| 3 | Dev tích hợp và tác giả hai nhánh | Ngữ cảnh và điểm xung đột | Thống nhất hành vi cần giữ | Chưa đo riêng | Phụ thuộc người liên quan có sẵn để trao đổi |
| 4 | Dev tích hợp | Phương án đã thống nhất | Bản sửa và kết quả build/test | Chưa đo riêng; có thể lặp lại | Test pass chưa đủ chứng minh đúng nghiệp vụ |
| 5 | Peer reviewer và dev tích hợp | Diff sau sửa, kết quả test | Bản sửa được duyệt và merge | Tổng cả quy trình khoảng 15–30 phút/lần theo phỏng vấn | Cần bấm giờ để xác nhận baseline |

**Bottleneck chính:** Đọc hiểu ý định thay đổi của cả hai nhánh và trao đổi với tác giả để giữ đúng logic khi sửa conflict. Thời gian chờ trao đổi và thời gian sửa chưa được đo tách biệt.

### 4.2. Quy trình tương lai

Ghi rõ bước nào **Rule**, bước nào **AI**, bước nào **con người**, **boundary** ở đâu, **phương án quay về** khi AI sai.

```text
[1 AI BA: Nhận conflict, lấy và cung cấp ticket cho AI DEV và phạm vi được sửa]
→ [2 AI CICD: lấy diff ba phía (base/ours/theirs), commit; build/test từng nhánh trước sửa]
→ [3 AI DEV: đọc context, đề xuất và sửa conflict trên bản làm việc cách ly]
→ [4 AI CICD: build/test/lint sau sửa; AI đọc lỗi, chọn đọc thêm context hoặc sửa lại]
→ [5 CON NGƯỜI: kiểm diff, đối chiếu nghiệp vụ, duyệt và tự merge]

BOUNDARY: AI chỉ đọc dữ liệu được cấp và sửa trong phạm vi cho phép;
không tự push/merge, không sửa hoặc xóa test để che lỗi, không truy cập secret.
Giới hạn đề xuất: tối đa 2 vòng sửa, 5 phút chạy AI và 20.000 token/lần;
chạm bất kỳ giới hạn nào hoặc thiếu context → dừng, báo dev.
PHƯƠNG ÁN QUAY VỀ: giữ nguyên nhánh gốc, bỏ bản sửa AI;
dev trao đổi với tác giả và sửa thủ công theo quy trình hiện tại.
```

### 4.3. Before / after

| Chỉ số | Trước | Sau (kỳ vọng) | Ghi chú |
|---|---:|---:|---|
| Số bước | 5 | 5 | Giữ bước người duyệt; không dùng số bước để thay thế thước đo hiệu quả |
| Tổng thời gian | 15–30 phút/lần | Trung vị ≤ 10 phút/lần | Trước là tự báo cáo; sau là mục tiêu đề xuất, gồm thời gian review và fallback |
| Số bước thủ công | 5/5 | 2/5 | Dev khởi chạy và duyệt; trường hợp thiếu context vẫn phải trao đổi |
| Bottleneck chính | Đọc context và hỏi tác giả | Dev kiểm nghiệp vụ của bản sửa | Chưa có kết quả thực nghiệm |
| Rủi ro mới phát sinh | Sửa tay có thể bỏ sót logic | AI sửa sai nhưng test vẫn pass; tốn token; lộ code | Giới hạn quyền, ngân sách và bắt buộc review |

---

## 5. Problem Statement v0 (CP5)

| Trường | Nội dung |
|---|---|
| **Actor** | Dev hoặc sinh viên lập trình làm việc nhóm, trực tiếp tích hợp hai nhánh có conflict. |
| **Quy trình** | Phát hiện conflict → đọc diff/commit/ticket → hỏi tác giả → sửa và test → review, merge. |
| **Bottleneck** | Mất thời gian tìm context và thống nhất cách giữ đúng ý định thay đổi của cả hai phía. |
| **Impact** | Theo phỏng vấn, mỗi lần xử lý mất khoảng 15–30 phút và cần các dev trao đổi; chưa biết tần suất nên chưa quy đổi thành giờ/tuần. |
| **Success Metric** (baseline → target, cách đo) | Baseline tự báo cáo 15–30 phút/lần → mục tiêu trung vị ≤ 10 phút/lần. Bấm giờ từ phát hiện conflict đến bản sửa được duyệt, gồm cả thời gian chờ và sửa lại, trên 10 ca thử nghiệm. |
| **Boundary** (AI không được làm gì; khi nào cần con người kiểm tra — HITL) | AI không tự merge/push hoặc tự quyết nghiệp vụ khi thiếu yêu cầu. Dev liên quan kiểm diff và hành vi trước khi chấp nhận bản sửa. |

Phản biện nhận được (từ AI hoặc nhóm khác) và nhóm có đồng ý không:

- Phản biện của Dương ở phần pitch: “Làm sao để Agent biết context của code để sửa chính xác với yêu cầu của khách hàng?” Đồng ý: cần ticket/issue, lịch sử hai nhánh và dev xác nhận ý định; build/test chỉ là một lớp kiểm tra, không bảo đảm đúng nghiệp vụ.

---

## 6. Mức can thiệp AI (CP6)

### 6.1. Ma trận độ mơ hồ × độ phức tạp

Bài của nhóm nằm ở ô: Độ mơ hồ cao × độ phức tạp cao đối với conflict có xung đột logic.

Vì sao: Một đoạn code có nhiều cách hòa giải nhưng phải giữ ý định hai nhánh; cần đối chiếu code, commit, ticket và kết quả test. Bước đọc thêm file hay sửa tiếp phụ thuộc kết quả trước đó. Conflict đơn giản về định dạng không thuộc phạm vi cần Agent.

### 6.2. So sánh 4 mức

| Mức | Phương án cho bài của nhóm | Đủ khi nào | Rủi ro | Chọn? |
|---|---|---|---|---|
| **No AI** (sửa quy trình) | Chia nhỏ PR, đồng bộ nhánh thường xuyên, thống nhất người sửa conflict | Conflict ít, dễ hiểu và tác giả sẵn sàng trao đổi | Vẫn cần đọc và sửa tay khi xung đột logic | Giữ làm baseline và fallback |
| **Rule** | Git/merge tool phát hiện conflict; script lấy diff và chạy test | Conflict có quy tắc rõ như định dạng | Không suy ra ý định nghiệp vụ; chọn ours/theirs có thể mất logic | Dùng cho bước xác định và kiểm tra |
| **Workflow** | Lấy context cố định → AI đề xuất một lần → test → dev duyệt | Context đã đủ, không cần tự chọn bước tiếp theo | Có thể dừng ở bản sửa thiếu context | Là phương án so sánh; ưu tiên nếu đạt cùng chất lượng |
| **Agent** | AI tự chọn file liên quan để đọc, sửa và đọc lỗi test trong phạm vi cho phép | Conflict logic cần điều chỉnh bước xử lý theo kết quả | Sửa sai nghiệp vụ, mở rộng phạm vi, lặp tốn token | Chọn để thử nghiệm có giới hạn |

**Mức chọn:** Agent có giới hạn để kiểm chứng trên conflict logic; dùng Rule cho thu thập dữ liệu và chạy kiểm tra.

**Vì sao không chọn mức đơn giản hơn:** No AI và Rule vẫn phù hợp khi conflict đơn giản. Với conflict logic, workflow cố định có thể thiếu bước đọc thêm context hoặc sửa theo lỗi test. Tuy nhiên, hiện chưa có bằng chứng Agent tốt hơn Workflow; cần so sánh hai mức trên cùng bộ ca trước khi quyết định triển khai, không mặc định cần nhiều Agent.

### 6.3. AI Canvas rút gọn

| Thành phần | Nội dung |
|---|---|
| **Prediction** — AI dự đoán / tạo ra gì? | Bản sửa conflict kèm giải thích ý định được giữ từ mỗi nhánh và những điểm chưa chắc chắn. |
| **Judgment** — con người cân nhắc, quyết định gì? | Dev tác giả và reviewer xác nhận logic đúng yêu cầu, quyết định chấp nhận hay sửa lại. |
| **Action** — hành động cuối cùng là gì, ai làm? | Dev áp dụng bản sửa đã duyệt và tự merge sau khi kiểm tra. |
| **Outcome** — đo kết quả bằng gì? | Thời gian đến khi được duyệt, số ca đạt tiêu chí, số ca sửa lại/fallback và token mỗi ca. |
| **Input** — AI cần dữ liệu đầu vào gì mỗi lần chạy? Có sẵn không? | Base/ours/theirs, diff, commit, file liên quan, ticket và lệnh build/test. Code có trong repo; ticket, quyền truy cập và độ đầy đủ của test cần kiểm tra trước thử nghiệm. |
| **Feedback** — lấy phản hồi ở đâu để cải thiện? | Diff reviewer sửa lại, lý do từ chối, log test và lỗi nghiệp vụ phát hiện sau review; ghi nhận vào bộ ca đánh giá. |

### 6.4. Hai câu hỏi của Google PAIR

- Người dùng muốn **được hỗ trợ (augment)** hay **giao hẳn việc (automate)**? Bằng chứng: Augment. 10/10 muốn AI giúp sửa nhanh nhưng 8/10 nghi ngờ để AI tự sửa; tín hiệu này ủng hộ bản nháp có người duyệt, chưa chứng minh sẵn sàng giao toàn bộ việc.
- AI sai kiểu nào tệ hơn, **báo nhầm** hay **bỏ sót**? Vì sao, và thiết kế đã xử lý thế nào: Bỏ sót lỗi logic và kết luận bản sửa đúng nguy hiểm hơn báo cần kiểm tra thêm, vì có thể đưa lỗi vào nhánh chung. Vì vậy kiểm cả ý định hai nhánh, chạy test và bắt buộc reviewer duyệt; thiếu context thì chuyển người xử lý.

---

## 7. Problem Statement v1 + tiêu chí đánh giá (CP6)

| Trường | Nội dung |
|---|---|
| **Actor** | Dev/sinh viên tích hợp conflict logic trong repo nhóm có ticket, test chạy được và người hiểu thay đổi của hai nhánh để review. |
| **Quy trình** | Chọn ca và phạm vi → lấy context, kiểm tra trước sửa → đề xuất bản sửa → kiểm tra sau sửa → dev review và merge. |
| **Bottleneck** | Hiểu và hòa giải ý định thay đổi giữa hai nhánh; chưa biết phần thời gian nào thực sự có thể giảm bằng AI. |
| **Impact** | 15–30 phút/lần theo phỏng vấn, có phối hợp giữa các dev; mức tiết kiệm thực tế và tần suất chưa được xác nhận. |
| **Success Metric** (baseline → target, cách đo) | Trên 10 ca thử trong 2 tuần: bấm giờ baseline thủ công và phương án có AI ở các ca tương đương; mục tiêu trung vị ≤ 10 phút/ca và giảm ≥ 30% so với baseline đo lại. Ít nhất 8/10 ca được duyệt không cần sửa logic; không có lỗi nghiệp vụ nghiêm trọng lọt qua review. Ghi cả thời gian fallback, token và chi phí; các target đều là đề xuất. |
| **Boundary** | Chỉ sửa bản làm việc cách ly trong phạm vi được cấp; không tự push/merge, không đọc secret, không xóa/sửa test để che lỗi. Dừng khi thiếu context hoặc chạm giới hạn 2 vòng sửa, 5 phút AI hay 20.000 token; dev tiếp quản. |
| **AI intervention point** | Sau khi có diff, ticket và kết quả kiểm tra trước sửa; trước khi con người review. AI được chọn đọc thêm context và sửa lại theo log test trong giới hạn. |
| **Mức chọn** | Agent có giới hạn, chưa triển khai thực tế trước khi kiểm chứng |
| **Rủi ro & người kiểm tra** | AI có thể giữ sai nghiệp vụ dù test pass: dev tác giả hai nhánh và peer reviewer kiểm diff với ticket; người phụ trách thử nghiệm theo dõi token, log và phạm vi thay đổi. |

**Thay đổi so với v0 và lý do:**

| Trường | v0 | v1 | Vì sao đổi |
|---|---|---|---|
| Phạm vi, metric và boundary | Dev gặp conflict; ưu tiên giảm thời gian, dev duyệt | Thu hẹp conflict logic có context/test; thêm chất lượng, so sánh baseline và giới hạn chạy | 8/10 nghi ngờ AI tự sửa; nhanh hơn và test pass chưa chứng minh đúng nghiệp vụ |

**Tiêu chí đánh giá đầu ra của AI (3–5 tiêu chí):**

| # | Tiêu chí | Đạt khi | Không đạt khi |
|---:|---|---|---|
| 1 | Giữ đúng ý định hai nhánh | Dev tác giả/reviewer đối chiếu ticket và xác nhận không mất hành vi cần giữ | Mất logic một phía, suy diễn yêu cầu hoặc còn điểm mơ hồ chưa hỏi |
| 2 | Kiểm tra kỹ thuật có bằng chứng | Hết conflict marker; có log build/test/lint trước và sau sửa, không phát sinh lỗi mới trên các kiểm tra chạy được | Còn marker, phát sinh lỗi mới, bỏ qua lỗi hoặc khẳng định pass khi chưa chạy |
| 3 | Bản sửa có thể kiểm soát và review | Diff trong phạm vi cho phép, giải thích có căn cứ từ code/ticket; dừng đúng giới hạn, chuyển người khi thiếu context | Sửa ngoài phạm vi, che lỗi bằng sửa test, giải thích không có căn cứ hoặc tự push/merge |

---

## 8. Quyết định (CP6)

### 8.1. Bốn rủi ro

| Rủi ro | Câu hỏi | Mức độ rủi ro (Thấp = an toàn / TB / Cao = nguy hiểm) | Lý do / bằng chứng |
|---|---|---|---|
| **Value** | Người dùng có thật sự cần và sẽ dùng không? | TB | 10/10 từng sửa conflict và muốn nhanh hơn; chưa có tần suất, log thời gian hoặc bằng chứng sử dụng thực tế |
| **Usability** | Người dùng có dùng được, có hiểu và sửa được đầu ra của AI không? | TB | Dev quen diff/review nhưng 8/10 còn nghi ngờ; cần thử bản sửa kèm giải thích và đo công review |
| **Feasibility** | Có đủ dữ liệu, công cụ, kỹ năng để làm không? | Cao | Nhóm hiểu domain nhưng chưa có bộ ca và kết quả chứng minh giữ đúng nghiệp vụ; test pass không đủ và context có thể thiếu |
| **Viability** | Có hợp chi phí, pháp lý, quy định tổ chức không? Ai vận hành? | TB | Chưa đo token/chi phí và chưa xác nhận quyền gửi code nội bộ; thử trước bằng repo lab được phép, nhóm phân công người quản lý log và ngân sách |

### 8.2. Kết luận

**Quyết định:** Not Yet

**Lý do:** Pain có tín hiệu thực tế nhưng rủi ro Feasibility còn Cao. Chưa đủ bằng chứng để kết luận Agent sửa đúng nghiệp vụ hoặc tốt hơn Workflow; cần kiểm chứng trước khi dùng trên PR thật.

**Nếu Go — pilot nhỏ nhất:** Sau khi vượt bước kiểm chứng, thử 2 tuần trên một repo lab được phép với 10 ca conflict logic; dùng công cụ sẵn có, dev chủ động kích hoạt và duyệt mọi bản sửa, chưa xây hệ thống nhiều Agent.

**Nếu Not Yet — cần kiểm chứng gì trước:** Trong 2 tuần, chuẩn bị 10 ca tái hiện được kèm ticket, test và tiêu chí nghiệp vụ do dev xác nhận. So sánh thủ công, Workflow một lượt và Agent giới hạn trên các bản sao cùng ca; đổi thứ tự/người xử lý để giảm ảnh hưởng đã biết lời giải. Ghi thời gian, chất lượng review, fallback, token và chi phí. Chỉ chuyển Go nếu đạt metric mục 7, xác nhận quyền dùng dữ liệu và ngân sách; nếu Workflow đạt tương đương thì chọn Workflow.

**Nếu No-Go — nên làm gì thay AI:** Chưa chọn No-Go. Nếu không giảm được rủi ro hoặc review tốn hơn sửa tay, dùng PR nhỏ, đồng bộ nhánh thường xuyên, merge tool, checklist test và trao đổi trực tiếp với tác giả.

**Ngưỡng dừng** (nếu sau … mà … thì quay về …): Mỗi ca dừng AI khi chạm một giới hạn ở mục 4.2 và chuyển sửa tay. Dừng thử nghiệm ngay nếu có truy cập dữ liệu ngoài quyền hoặc lỗi nghiệp vụ nghiêm trọng lọt qua review. Sau 2 tuần, nếu dưới 8/10 ca được duyệt không cần sửa logic, thời gian trung vị > 10 phút hoặc giảm < 30% so với baseline, quay về quy trình thủ công/Workflow và xem lại phạm vi.

---

## 9. Hạn chế và hướng tiếp theo

- Mẫu phỏng vấn chỉ có 10 người; khoảng 15–30 phút là tự báo cáo, chưa có log, tần suất và thời gian chờ tách riêng. Cần đo lại trên các ca cụ thể.
- Mong muốn dùng AI chưa chứng minh mức sử dụng thực tế. Các mục tiêu thời gian, chất lượng và giới hạn chạy trong phần 4–8 là đề xuất, chưa phải kết quả thử nghiệm.
- Chưa có bằng chứng cần nhiều Agent riêng cho context, sửa code và test; thử công cụ hiện có và Workflow trước khi tăng độ phức tạp.
- Bộ test có thể thiếu tình huống nghiệp vụ; cần tác giả hai nhánh xác nhận hành vi mong muốn, bổ sung kiểm tra và ghi cả ca AI thất bại.
- Hướng tiếp theo: hoàn thiện bộ 10 ca, xác nhận quyền dùng dữ liệu và ngân sách, thực hiện so sánh ở mục 8 rồi cập nhật quyết định theo kết quả.

## 10. Tài liệu tham khảo

-
