# Báo cáo nhóm — Day 02 Discovery & Problem Framing

> Chủ đề nhóm: xử lý Git merge conflict trong quá trình cộng tác lập trình bằng mô hình 3 Agent. Các số liệu chưa có log/bấm giờ độc lập được ghi rõ là ước tính hoặc baseline cần kiểm chứng.

## 1. Thông tin nhóm

- Tên nhóm: Nhóm 02
- Thành viên: Hà Phan Đại Dương, Nguyễn Thiên Long, Lê Bá Nguyên, Nguyễn Ngọc Bách, Nguyễn Văn Tuấn.
- Candidate problem được chọn: Khi nhiều thành viên cùng phát triển trên các branch, developer mất nhiều thời gian đọc và đối chiếu ý đồ của hai phía trong một merge conflict phức tạp, dễ hợp nhất sai logic và làm hỏng build.
- Quyết định cuối: **Not Yet** — nhóm đã chốt kiến trúc 3 Agent để pilot, nhưng cần kiểm chứng trên các ca conflict thực tế trước khi triển khai rộng.

---

## 2. Hội tụ nhóm (CP3)

### 2.1. Pitch

| # | Người đưa ra | Candidate (Job Story ngắn) | Actor | Bottleneck | Câu hỏi phản biện nhận được (ai hỏi) |
|---:|---|---|---|---|---|
| 1 | Hà Phan Đại Dương | Khi tổng hợp chứng từ cuối tháng, tôi muốn nhập các trường hóa đơn nhanh và chính xác để lập báo cáo chi phí. | Kế toán | Đọc và nhập từng chứng từ, 3–5 phút/chứng từ. | Dữ liệu có thật sự sẵn ở nhiều định dạng và đã được đo chưa? (Nhóm) |
| 2 | Hà Phan Đại Dương | Khi CEO hỏi chi phí tăng, tôi muốn truy xuất chứng từ liên quan để giải thích bằng số liệu. | Kế toán, CEO | Tìm và đối chiếu các khoản chi từ nhiều nguồn. | Thông tin tài chính mật được xử lý thế nào? (Nhóm) |
| 3 | Hà Phan Đại Dương | Khi phân loại hàng trăm khoản chi, tôi muốn gán đúng nhóm chi phí để báo cáo chính xác. | Kế toán | Phân loại thủ công và xử lý ngoại lệ. | Quy trình và output cuối có đủ rõ để làm trong lab không? (Nhóm) |
| 4 | Nguyễn Thiên Long | Khi học từ PDF bài giảng, tôi muốn tìm đúng phần giải thích để không phải lật nhiều trang. | Sinh viên | Đọc thủ công nhiều kết quả Ctrl+F. | Đây là pain cá nhân hay nhiều người cùng gặp? (Nhóm) |
| 5 | Nguyễn Thiên Long | Khi đọc bài báo tiếng Anh, tôi muốn lọc thuật ngữ chuyên ngành để hiểu nhanh ngữ cảnh. | Sinh viên/đồ án | Tra từng từ, dịch thô và đối chiếu lại. | Có thể giải bằng từ điển/quy tắc đơn giản không? (Nhóm) |
| 6 | Nguyễn Thiên Long | Khi tìm phòng trọ, tôi muốn lọc bài đăng theo tiêu chí để tránh tin không phù hợp. | Sinh viên | Thông tin bài đăng thiếu và không đồng nhất. | Dữ liệu Facebook có quyền truy cập và đủ cấu trúc không? (Nhóm) |
| 7 | Lê Bá Nguyên | Khi chốt cuối ngày, tôi muốn đối soát COD để biết dòng tiền và khoản lệch của từng shipper. | Kế toán, trưởng bưu cục | Gom và đối chiếu bảng tính, 60–90 phút/ngày. | Power Query hoặc công thức có giải quyết phần lớn không? (Nguyễn Văn Tuấn) |
| 8 | Lê Bá Nguyên | Khi có đơn hoàn/thất lạc/hư hỏng, tôi muốn biết trách nhiệm và khoản đền bù. | Kế toán, vận hành | Dữ liệu rải rác, quy định trách nhiệm phức tạp. | Phạm vi và baseline có quá rộng cho lab không? (Nhóm) |
| 9 | Nguyễn Ngọc Bách | Khi khách hàng mô tả output mơ hồ, tôi muốn hiểu đúng yêu cầu để tránh làm lại. | Nhóm thực hiện dự án | Làm rõ yêu cầu qua nhiều lượt trao đổi. | Cần tách pain “giao tiếp” khỏi giải pháp chatbot thế nào? (Nhóm) |
| 10 | Nguyễn Ngọc Bách | Khi tham gia dự án mới, tôi muốn nắm nhanh bối cảnh và tài liệu liên quan. | Thành viên mới | Tìm và tổng hợp thông tin dự án. | Actor, nguồn dữ liệu và metric cụ thể là gì? (Nhóm) |
| 11 | Nguyễn Ngọc Bách | Khi trao đổi trong team, tôi muốn truyền đạt đủ ngữ cảnh để tránh hiểu sai. | Thành viên nhóm | Thông tin nằm rải rác ở chat và tài liệu. | Có quy trình lặp lại nào để vẽ trước không? (Nhóm) |
| 12 | Nguyễn Văn Tuấn | Khi merge/rebase branch trước PR, tôi muốn xác định đúng code cần giữ để merge thành công mà không hỏng logic. | Developer trong nhóm 4 người | Đọc hai phiên bản, hỏi ý đồ và kiểm tra sau merge; conflict phức tạp khoảng 35–50 phút/lần theo báo cáo cá nhân. | AI can thiệp ở đâu và làm sao ngăn dev auto-merge mà không test? (Nhóm) |

### 2.2. Cluster

| Cluster | Các candidate | Pattern chung |
|---|---|---|
| A — Cộng tác và lập trình | Git conflict, review PR, trao đổi team, hiểu dự án mới | Mất ngữ cảnh khi nhiều người cùng làm và phải đọc/tổng hợp thay đổi trước khi hành động. |
| B — Dữ liệu và tài chính | Nhập liệu hóa đơn, phân loại chi phí, đối soát COD, đơn hoàn | Đối chiếu dữ liệu có cấu trúc; nhiều phần có thể giải bằng rule, form hoặc Power Query. |
| C — Tra cứu và yêu cầu | Tìm PDF, thuật ngữ tiếng Anh, lọc phòng trọ, output mơ hồ | Tìm, lọc và làm rõ thông tin không đồng nhất; khó giới hạn nguồn và đo chất lượng. |

### 2.3. Opportunity Solution Tree rút gọn

```text
OUTCOME: Giảm thời gian xử lý conflict phức tạp và giữ build/repo an toàn trong mỗi sprint
├── Opportunity A: Developer khó hiểu ý đồ của hai phiên bản code và commit liên quan
├── Opportunity B: Developer phải chờ thành viên khác giải thích phần logic bị đụng
├── Opportunity C: Sau khi chọn cách hợp nhất, việc kiểm chứng logic và test chưa nhất quán
└── Opportunity D: Một phần conflict có thể phòng ngừa bằng cách chia branch và đồng bộ thường xuyên
```

Những ý đã gạch bỏ vì là solution đội lốt opportunity:

- “Multi-agent tự động resolve và commit” — là solution, không phải nhu cầu.
- “AI phân tích AST”, “dashboard conflict”, “bot tự hỏi người viết code” — là cách triển khai cần thử sau khi xác nhận opportunity.

### 2.4. Chấm điểm shortlist (1–5)

| Candidate | Actor rõ | Quy trình rõ | Pain có bằng chứng | Impact đo được | Vừa sức lab | So sánh được No AI/Rule/Workflow/Agent | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Git merge conflict phức tạp | 5 | 5 | 4 | 5 | 5 | 5 | 5 | **34** |
| Đối soát COD cuối ngày | 5 | 5 | 3 | 5 | 4 | 5 | 4 | **31** |
| Tra cứu và tổng hợp tài liệu dự án | 4 | 3 | 3 | 3 | 4 | 4 | 3 | **24** |

**Candidate được chọn:** xử lý Git merge conflict phức tạp trong nhóm lập trình.

**Vì sao chọn:** actor và quy trình cụ thể; pain xảy ra trong sprint; bottleneck là bước đọc hiểu ý đồ logic, không chỉ là xóa conflict marker; có thể đo thời gian xử lý, tỷ lệ merge lỗi và số lần phải rollback; đồng thời cho phép so sánh giữa quy trình, rule và AI workflow.

**Vì sao loại các candidate còn lại:** đối soát COD chủ yếu là dữ liệu bảng có cấu trúc, công thức/Power Query và quy trình chuẩn có thể giải phần lớn; tra cứu tài liệu có scope nguồn và tiêu chí đúng/sai chưa rõ; các candidate tài chính còn thiếu bằng chứng độc lập và có rủi ro dữ liệu mật.

**Xử lý bất đồng:** nhóm không chọn theo số lượng agent. Nhóm quay lại quy trình, xác định bottleneck và chấm theo bảy tiêu chí. Sau phản biện, thống nhất chốt 3 Agent có HITL, giới hạn vòng lặp và không cho tự commit/push.

---

## 3. Kiểm chứng + research giải pháp đã có (CP4)

### 3.1. Assumption Map

| # | Giả định | Loại | Quan trọng (1–5) | Đã có bằng chứng (1–5) | Kiểm chứng trước? |
|---:|---|---|---:|---:|---|
| 1 | Conflict logic phức tạp xảy ra khoảng 2–3 lần/tuần trong giai đoạn sprint của nhóm sinh viên. | Value | 5 | 2 | Có |
| 2 | Một ca conflict logic mất khoảng 35–50 phút, trong đó 25 phút là đọc/đối chiếu ý đồ. | Value | 5 | 2 | Có |
| 3 | Commit history, diff, cấu trúc code và test có thể lấy làm input đủ để hỗ trợ quyết định. | Feasibility | 5 | 2 | Có |
| 4 | Developer hiểu được lý do của gợi ý và sẵn sàng sửa/reject thay vì chấp nhận mù quáng. | Usability | 5 | 2 | Có |
| 5 | Unit test/linter có thể phát hiện phần lớn lỗi syntax và một phần lỗi logic sau merge. | Feasibility | 4 | 2 | Có |
| 6 | Quy trình có developer duyệt cuối, không tự commit/push, phù hợp với quyền truy cập và chi phí của nhóm. | Viability | 4 | 3 | Sau pilot |

Giả định ưu tiên: tần suất và thời gian conflict; mức tin tưởng vào gợi ý; khả năng dùng diff/commit history/test làm input; và việc các tool có sẵn còn thiếu ngữ cảnh liên nhánh hay không.

### 3.2. Kiểm chứng

Cách đã dùng: trao đổi/phỏng vấn nhanh 2 developer ở lớp khác và research tài liệu/công cụ. Báo cáo cá nhân ghi nhận tín hiệu từ 2 người; nhóm chưa lưu được câu trích dẫn nguyên văn và chưa có log Git đủ lớn, vì vậy kết quả chỉ là tín hiệu định hướng, chưa phải bằng chứng kết luận.

| Nguồn | Số người / số mẫu | Tín hiệu xác nhận | Tín hiệu phản bác |
|---|---:|---|---|
| Trao đổi với developer ngoài nhóm | 2 người | Conflict logic cần hiểu ngữ cảnh; người dùng muốn xem giải thích và tự duyệt, không muốn hệ thống tự merge. | Không phải conflict nào cũng đau: import/format có thể xử lý bằng editor hoặc rule trong vài phút. |
| Kinh nghiệm nhóm được ghi trong báo cáo cá nhân | 1 báo cáo có số liệu cụ thể | 2–3 lần/tuần, 35–50 phút cho ca phức tạp, từng có nguy cơ mất logic. | Số liệu chưa được đối chiếu từ Git log hoặc bấm giờ độc lập. |
| Research tool/pattern | 3 nhóm công cụ/pattern | 3-way merge, merge editor, linter/test và trợ lý code đều là các mảnh có sẵn. | Chưa có bằng chứng đủ để khẳng định tool hiện có hiểu đầy đủ ý đồ nghiệp vụ của hai branch và tự merge an toàn. |

Interview snapshot tối thiểu cần bổ sung ở pilot: vai trò developer; ca conflict gần nhất; thời gian từng bước; workaround; câu nói nguyên văn; và kết quả test sau merge. Không ghi tên thật hoặc thông tin repo riêng tư.

**Nhóm đã sửa problem thế nào sau kiểm chứng:** thu hẹp từ “giải quyết mọi Git conflict” thành “hỗ trợ conflict logic phức tạp”. Conflict import/format được xem là phạm vi rule/editor; 3 Agent chỉ xử lý phần cần phân tích và sửa lặp, còn developer review/merge cuối. Nhóm bổ sung boundary, giới hạn vòng lặp và fallback thủ công.

### 3.3. Research giải pháp đã có

| Công cụ / case / pattern | Link | Giải bước nào trong quy trình? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
|---|---|---|---|---|---|
| Git 3-way merge | [Git merge documentation](https://git-scm.com/docs/git-merge) | Tìm common ancestor và hợp nhất thay đổi hai branch. | Nền tảng chuẩn, minh bạch, kiểm soát bằng diff. | Không giải thích ý đồ nghiệp vụ; conflict logic vẫn cần người quyết định. | Giữ 3-way merge làm fallback và baseline. |
| GitHub conflict resolution / PR workflow | [Resolving a merge conflict on GitHub](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/addressing-merge-conflicts/resolving-a-merge-conflict-on-github) | Xem conflict, sửa file, commit kết quả và tiếp tục PR. | Quy trình quen thuộc, có review trước merge. | Vẫn phụ thuộc người đọc code; dễ merge nhầm nếu test chưa đủ. | Không bỏ qua PR review, test và quyền xác nhận. |
| Merge editor + linter/test | [VS Code merge conflict resolution](https://code.visualstudio.com/docs/sourcecontrol/merge-conflicts) | Hiển thị ours/theirs/result và kiểm tra sau khi chọn. | Tốt cho conflict đơn giản, thao tác trực quan. | Không tự hiểu logic khi hai bên cùng thay đổi một hàm. | Rule/editor xử lý phần đơn giản; AI chỉ can thiệp phần mơ hồ. |

---

## 4. Quy trình trước/sau (CP5)

### 4.1. Quy trình hiện tại

```text
Developer merge/rebase main
  → Git báo conflict ở 3–5 file
  → Mở marker và đọc hai phiên bản
  → Hỏi người viết code để hiểu ý đồ  ← BOTTLENECK
  → Chọn/ghép code, xóa marker
  → Chạy test local
  → Commit và push; nếu fail thì rollback/debug
```

| Bước | Actor | Input | Output | Thời gian / tần suất | Ghi chú |
|---:|---|---|---|---|---|
| 1 | Developer | Branch feature, `main`, commit mới | Conflict được phát hiện | ~5 phút; 2–3 lần/tuần trong sprint | Có thể dùng rule để phân loại file/loại conflict. |
| 2 | Developer | Conflict markers, diff | Danh sách file và vùng xung đột | ~5 phút | Import/format thường đơn giản hơn. |
| 3 | Developer + teammate | Hai phiên bản, commit history, yêu cầu tính năng | Hiểu ý đồ và phương án giữ/ghép | ~25 phút; bottleneck | Phụ thuộc người kia online; dễ hiểu sai logic. |
| 4 | Developer | Phương án hợp nhất | File đã sửa và test local | ~10 phút | Có thể phát sinh lỗi logic chưa được test. |
| 5 | Developer | Kết quả test, diff cuối | Merge commit và push | ~5 phút | Nếu fail phải quay lại bước 3–4. |

**Bottleneck chính:** bước 3 — đọc và đối chiếu ý đồ logic của hai bên, không phải thao tác xóa marker.

### 4.2. Quy trình tương lai

```text
[DevOps Agent] Deploy branch, chạy test/linter, theo dõi log và phát hiện lỗi
  → Gửi lỗi/kết quả cho [BA Agent]
[BA Agent] Phân tích lỗi, đối chiếu yêu cầu và commit context,
            sau đó ra chỉ thị sửa có cấu trúc cho [Dev Agent]
  → [Dev Agent] Sửa code, chạy test và gửi branch/kết quả mới
  → [DevOps Agent] Deploy và kiểm tra lại
      ├─ Đạt: thông báo kết quả, chờ developer xác nhận merge
      └─ Chưa đạt: gửi kết quả mới về BA Agent để phân tích tiếp
```

**Vai trò 3 Agent:**

- **DevOps Agent:** deploy phiên bản cần kiểm tra, chạy linter/unit/integration test, theo dõi log, phát hiện lỗi và thông báo kết quả cho BA Agent. Agent này không tự kết luận cách sửa.
- **BA Agent:** nhận lỗi từ DevOps Agent, phân tích nguyên nhân ở mức yêu cầu/nghiệp vụ, đối chiếu diff/commit/spec và chuyển thành chỉ thị rõ ràng cho Dev Agent. Khi thiếu ngữ cảnh, BA Agent phải yêu cầu con người bổ sung.
- **Dev Agent:** nhận chỉ thị, sửa code, chạy test cục bộ và gửi phiên bản mới cho DevOps Agent kiểm tra lại.

Đây là vòng lặp **DevOps → BA → Dev → DevOps**. AI không được tự commit/push/approve PR, tự thay đổi test để làm test pass, hoặc tự quyết business logic khi không có bằng chứng. Developer/owner vẫn là người duyệt merge cuối cùng. Nếu vòng lặp quá số lần cho phép hoặc vẫn không xác định được nguyên nhân, hệ thống chuyển về 3-way merge thủ công và yêu cầu người phụ trách xử lý.

### 4.3. Before / after

| Chỉ số | Trước | Sau (kỳ vọng) | Ghi chú |
|---|---:|---:|---|
| Số bước chính | 5 | 5 nhóm bước | After tách rõ Rule, AI, người và fallback. |
| Tổng thời gian | ~50 phút/ca conflict phức tạp | <15 phút/ca trong pilot | Đo bằng timestamp từ lúc conflict xuất hiện đến lúc test pass. |
| Số bước thủ công | 5 | 2 bước chính: review và xác nhận | Test/lint chạy tự động nhưng người vẫn kiểm tra kết quả. |
| Bottleneck chính | Đọc hai bên và hỏi ý đồ, ~25 phút | Review đề xuất và xử lý ca không chắc | Không kỳ vọng AI loại bỏ hoàn toàn judgment. |
| Rủi ro mới phát sinh | Merge nhầm, mất code | Hallucination, gợi ý sai, false confidence | Boundary, giải thích, test và fallback bắt buộc. |

---

## 5. Problem Statement v0 (CP5)

| Trường | Nội dung |
|---|---|
| **Actor** | Developer trong nhóm 4 người đang merge/rebase branch trước PR. |
| **Quy trình** | Merge `main` → đọc conflict markers → đối chiếu code và hỏi teammate → chọn/ghép code → test → commit/push. |
| **Bottleneck** | Hiểu ý đồ logic của hai phiên bản khi cùng sửa một vùng code; khoảng 25 phút trong ca phức tạp. |
| **Impact** | Khoảng 50 phút/ca, 2–3 ca/tuần trong giai đoạn sprint; merge sai có thể làm hỏng build hoặc mất logic của nhóm. |
| **Success Metric** | Baseline 50 phút/ca → mục tiêu dưới 15 phút/ca; lỗi logic/hỏng build do merge nhầm từ 1 lần/sprint → 0 trong pilot. Đo bằng timestamp và kết quả test. |
| **Boundary** | Chưa xác định giải pháp tự động; không được đánh đổi an toàn build để lấy tốc độ. Developer phải kiểm tra trước khi merge. |

Phản biện nhận được và nhóm đồng ý: baseline có thể phóng đại nếu trộn conflict đơn giản với conflict logic; cần tách loại conflict. “Dùng multi-agent” cũng là solution-first; cần chứng minh Workflow không đủ trước khi chọn Agent.

---

## 6. Mức can thiệp AI (CP6)

### 6.1. Ma trận độ mơ hồ × độ phức tạp

Bài của nhóm nằm ở ô **độ mơ hồ cao × độ phức tạp cao** khi cần phối hợp nhiều bước kiểm tra và sửa lặp lại.

Thao tác Git và test có thể chuẩn hóa, nhưng việc xử lý không kết thúc ở một lần đề xuất: kết quả deploy/test có thể tạo lỗi mới, cần phân tích lại và đưa chỉ thị sửa tiếp. Vì vậy nhóm chốt mô hình 3 Agent có vai trò chuyên biệt và vòng lặp kiểm chứng, thay vì một Agent duy nhất tự làm toàn bộ.

### 6.2. So sánh 4 mức

| Mức | Phương án cho bài của nhóm | Đủ khi nào | Rủi ro | Chọn? |
|---|---|---|---|---|
| **No AI** | Chia module/branch rõ, pull thường xuyên, PR nhỏ, PR template, 3-way merge editor, test bắt buộc. | Conflict chủ yếu là import/format hoặc nhóm chưa có baseline. | Không hỗ trợ tốt conflict logic; vẫn phụ thuộc người hỏi nhau. | Nền tảng bắt buộc |
| **Rule** | Phân loại conflict, tự chạy linter/test, cảnh báo file nhạy cảm. | Mẫu conflict ổn định và có quy tắc rõ. | Không hiểu ý đồ nghiệp vụ. | Có |
| **Workflow** | Một chuỗi cố định: lấy diff → AI đề xuất → dev duyệt → test. | Đủ khi mỗi ca chỉ cần một lần phân tích/sửa. | Không linh hoạt khi test tạo lỗi mới hoặc cần phân tích lại. | Không chọn làm kiến trúc chính |
| **Agent** | 3 Agent DevOps–BA–Dev phối hợp: phát hiện/kết quả → phân tích/chỉ thị → sửa/test → kiểm tra lại. | Cần nhiều vai trò chuyên biệt và vòng lặp theo kết quả kiểm tra. | Dễ lặp vô hạn, khó audit, có rủi ro sửa sai hoặc vượt quyền. | **Chọn để pilot có giới hạn** |

**Mức chọn:** Agent — kiến trúc 3 Agent có Rule, vòng lặp giới hạn và Human-in-the-loop.

**Vì sao không chọn mức đơn giản hơn:** No AI/Rule chỉ phù hợp với conflict hình thức; Workflow một tuyến phù hợp khi đầu vào ổn định nhưng không đủ khi kết quả test/deploy tạo ra thông tin mới và cần quay lại phân tích. Ba Agent được tách vai trò để giảm việc một Agent tự vừa chẩn đoán vừa sửa vừa tự xác nhận kết quả. Nhóm vẫn giới hạn số vòng lặp, quyền truy cập và yêu cầu developer xác nhận merge.

### 6.3. AI Canvas rút gọn

| Thành phần | Nội dung |
|---|---|
| **Prediction** | DevOps Agent dự đoán trạng thái deploy/test; BA Agent dự đoán nguyên nhân và chỉ thị sửa; Dev Agent tạo patch. |
| **Judgment** | BA Agent phân tích hướng sửa trong phạm vi được phép; developer/owner quyết định business logic và xác nhận merge cuối. |
| **Action** | DevOps deploy/kiểm tra; BA phân tích/chỉ thị; Dev sửa/chạy lại; developer xác nhận commit/push. |
| **Outcome** | Thời gian xử lý, số vòng lặp, tỷ lệ test pass, tỷ lệ rollback/hỏng build và tỷ lệ chỉ thị bị reject. |
| **Input** | Diff, AST/cấu trúc file, commit history, PR/spec, log deploy, test/linter và feedback của developer. |
| **Feedback** | Kết quả deploy/test, patch được accept/reject/sửa, nguyên nhân vòng lặp thất bại và quyết định merge cuối. |

### 6.4. Hai câu hỏi của Google PAIR

- Người dùng muốn **được hỗ trợ (augment)**, không giao hẳn việc: họ cần hiểu vì sao đề xuất đúng và phải duyệt trước merge.
- **Bỏ sót hoặc gợi ý sai logic** đều nguy hiểm; trong pilot ưu tiên tránh gợi ý sai làm hỏng build. Khi không đủ context, hệ thống phải báo “không chắc” và chuyển về 3-way merge thủ công.

---

## 7. Problem Statement v1 + tiêu chí đánh giá (CP6)

| Trường | Nội dung |
|---|---|
| **Actor** | Developer trong nhóm sinh viên 4 người, xử lý conflict logic trước khi mở hoặc cập nhật PR. |
| **Quy trình** | Phát hiện và phân loại conflict → cung cấp diff/AST/commit context → nhận tóm tắt và đề xuất → developer review → linter/test → xác nhận merge hoặc fallback thủ công. |
| **Bottleneck** | Đối chiếu ý đồ logic và quyết định giữ/ghép code; baseline khoảng 25 phút trong ca phức tạp. |
| **Impact** | Khoảng 50 phút/ca, 2–3 ca/tuần theo báo cáo cá nhân; có nguy cơ mất logic, hỏng build và kéo thêm thời gian debug cho cả nhóm. |
| **Success Metric** | Trong 10 ca conflict logic: median thời gian giảm từ baseline đo thật xuống dưới 15 phút; 100% ca có test/lint pass trước merge; 0 ca hỏng build do đề xuất trong pilot. |
| **Boundary** | AI không tự commit/push/approve; không tự đổi test để pass; không tự quyết business logic; không gửi code ra ngoài phạm vi được phép; thiếu context thì dừng và yêu cầu người xử lý. |
| **AI intervention point** | Sau khi DevOps Agent phát hiện lỗi: BA Agent phân tích và ra chỉ thị; Dev Agent sửa; DevOps Agent kiểm tra lại theo vòng lặp. |
| **Mức chọn** | Agent — 3 Agent DevOps/BA/Dev |
| **Rủi ro & người kiểm tra** | Hallucination, bỏ sót dependency, vòng lặp vô hạn, false confidence: giới hạn số vòng, log toàn bộ, developer review và owner xác nhận merge. |

**Thay đổi so với v0 và lý do:**

| Trường | v0 | v1 | Vì sao đổi |
|---|---|---|---|
| Phạm vi | Mọi merge conflict | Chỉ conflict logic phức tạp | Conflict đơn giản đã có rule/editor xử lý tốt hơn. |
| Vai trò AI | Hỗ trợ giải quyết conflict | Tóm tắt và đề xuất, không tự hành động | Giảm rủi ro merge nhầm và solution-first. |
| Metric | 50 → 15 phút, lỗi → 0 | Median trên 10 ca, test pass 100%, build lỗi 0 | Bổ sung cách đo và chất lượng, không chỉ đo tốc độ. |
| Quyết định | Có thể dùng multi-agent | Chốt 3 Agent để pilot có giới hạn | Sau thảo luận, nhóm xác định cần vòng lặp DevOps–BA–Dev; chưa triển khai rộng vì evidence còn ít. |

**Tiêu chí đánh giá đầu ra của AI (3–5 tiêu chí):**

| # | Tiêu chí | Đạt khi | Không đạt khi |
|---:|---|---|---|
| 1 | Đúng ngữ cảnh diff | Nêu đúng file/hunk, phân biệt base/ours/theirs và trích được bằng chứng từ input. | Bịa file, nhầm branch hoặc khẳng định ngoài input. |
| 2 | Bảo toàn logic | Đề xuất compile được, không tự làm mất behavior đã có; test/lint pass. | Hỏng build, làm mất logic hoặc chỉ sửa để test pass. |
| 3 | Giải thích được | Developer hiểu lý do, trade-off và phần còn chưa chắc. | Chỉ đưa patch/command không giải thích. |
| 4 | Biết dừng và chuyển người | Nêu rõ thiếu context hoặc conflict vượt phạm vi và đề nghị fallback. | Tự tin đưa một phương án duy nhất khi dữ liệu không đủ. |
| 5 | Không vượt quyền | Chỉ tạo đề xuất/diff; không tự commit, push, approve hoặc thay test. | Có hành động thay đổi remote hoặc bypass review. |

---

## 8. Quyết định (CP6)

### 8.1. Bốn rủi ro

| Rủi ro | Câu hỏi | Mức độ rủi ro | Lý do / bằng chứng |
|---|---|---|---|
| **Value** | Developer có thật sự cần giảm thời gian xử lý conflict logic không? | TB–Cao | Có pain và ước tính 35–50 phút/ca, nhưng mới có mẫu nhỏ và chưa xác nhận bằng Git log. |
| **Usability** | Người dùng có hiểu và sửa được đề xuất không? | Cao | Code merge liên quan ngữ cảnh; gợi ý sai hoặc quá tự tin có thể khiến người dùng bỏ qua review. |
| **Feasibility** | Có đủ diff, history, AST và test để hỗ trợ không? | TB | Có thể lấy từ repo, nhưng dependency, code riêng tư và test coverage chưa được kiểm chứng. |
| **Viability** | Có phù hợp chi phí, quyền truy cập và quy trình nhóm không? | TB | 3 Agent chỉ pilot một repo, quyền hạn tối thiểu và có người duyệt; triển khai rộng sẽ tăng chi phí, quyền hạn và trách nhiệm. |

### 8.2. Kết luận

**Quyết định:** **Not Yet**.

**Lý do:** nhóm đã thống nhất ý tưởng cuối là mô hình 3 Agent DevOps–BA–Dev với vòng lặp kiểm tra/sửa. Tuy nhiên evidence hiện tại chủ yếu là báo cáo cá nhân và trao đổi mẫu nhỏ, nên chưa nên cấp quyền tự động rộng hoặc triển khai production khi chưa biết baseline thật, test coverage và tỷ lệ chỉ thị đúng.

**Nếu Not Yet — cần kiểm chứng gì trước:**

1. Thu thập ít nhất 10 ca conflict logic thật hoặc dataset đã ẩn thông tin; ghi thời gian từng bước, loại conflict và kết quả build/test.
2. Thử mô hình 3 Agent trên một repository nội bộ, giới hạn số vòng lặp và không cho quyền commit/push tự động.
3. Chấm từng output theo năm tiêu chí ở mục 7; ghi accept/reject/sửa và lý do.
4. Bổ sung interview snapshot có câu trích dẫn nguyên văn từ developer ngoài nhóm, không chỉ ghi tóm tắt.

**Ngưỡng dừng:** sau 10 ca pilot, nếu median không giảm ít nhất 30% so với baseline, có bất kỳ ca nào làm hỏng build hoặc có trên 20% đề xuất vi phạm tiêu chí đúng ngữ cảnh/bảo toàn logic, nhóm dừng phần AI và quay về No AI + Rule + 3-way merge thủ công.

---

## 9. Hạn chế và hướng tiếp theo

- Nhiều số liệu cá nhân là ước tính; cần thay bằng timestamp từ Git log, screen recording hoặc bảng bấm giờ có consent.
- Mẫu kiểm chứng chỉ có 2 developer ngoài nhóm và chưa có quote nguyên văn; chưa đủ đại diện cho các team có quy trình Git khác.
- Chưa có bộ conflict có đáp án chuẩn và chưa đo test coverage; “AI đề xuất đúng” chưa thể suy ra chỉ từ việc code compile.
- Pilot tiếp theo nên bắt đầu từ conflict logic trong một ngôn ngữ/repo cụ thể, dùng 3 Agent với quyền tối thiểu, giới hạn vòng lặp, log đầy đủ và fallback thủ công.

## 10. Tài liệu tham khảo

- [Worksheet — hướng dẫn checkpoint](../../docs/01-worksheet.md)
- [Bài deliverable mẫu](../../docs/02-deliverable-example.md)
- [Framework quốc tế dùng trong lab](../../docs/03-international-frameworks.md)
- [Git merge documentation](https://git-scm.com/docs/git-merge)
- [GitHub: Resolving a merge conflict](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/addressing-merge-conflicts/resolving-a-merge-conflict-on-github)
- [VS Code: Resolve merge conflicts](https://code.visualstudio.com/docs/sourcecontrol/merge-conflicts)
