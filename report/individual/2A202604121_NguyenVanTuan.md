# Báo cáo cá nhân — 2A202604121_NguyenVanTuan

> Đổi tên file theo quy tắc `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md` (MSSV trước, dấu `_`, họ tên viết liền không dấu). Sửa cả dòng tiêu đề phía trên cho khớp.
> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: copy template này thành file mới, điền, rồi commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên: Nguyễn Văn Tuấn
- MSSV: 2A202604121
- Email trường (không bắt buộc, repo có thể để public):
- Tên nhóm: Nhóm 2
- Link repo nhóm: https://github.com/DanielHa01/K5-L3B-DAY02-Nhom02-DiscoveryProblemFraming

---

## 2. Scan problem (CP1)

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

| # | Lăng kính | Job Story: Khi… tôi muốn… để… | Ai chịu ảnh hưởng? | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng) |
|---:|---|---|---|---|
| 1 | Lặp lại | Khi hợp nhất code (merge/rebase) từ nhánh `main` vào nhánh tính năng cá nhân trước khi tạo Pull Request, tôi muốn nhanh chóng xác định đúng đoạn code cần giữ và giải quyết xung đột, để code không bị hỏng logic và merge thành công vào repo nhóm | Sinh viên lập trình / Thành viên nhóm dự án (4 người) | 2–3 lần/tuần mỗi khi chạy sprint; mỗi lần gặp conflict phức tạp mất 35–50 phút kiểm tra thủ công, từng bị lỗi mất code logic của bạn 1 lần trong bài lab tuần trước |
| 2 | Tốn thời gian | Khi bắt đầu review Pull Request (PR) lớn (hơn 300 dòng code hoặc nhiều file) của thành viên khác trong nhóm, tôi muốn hiểu nhanh ý đồ thay đổi và các điểm rủi ro tiềm ẩn, để phản hồi chính xác trước khi approve code | Người review code (bản thân tôi), người tạo PR | Mất 30–45 phút mỗi PR lớn, trung bình 2 PR/tuần; tuần trước mất gần 1 tiếng đọc diff giữa 7 files chỉ để tìm xem bạn đổi cấu trúc database ở chỗ nào |
| 3 | Cần đọc, tổng hợp nhiều thông tin | Khi chuẩn bị nộp bài lab trước deadline 23h59, tôi muốn đối chiếu toàn bộ các file trong repo với rubric và checklist nộp bài của giảng viên, để đảm bảo không bị trừ điểm vì thiếu file, sai tên file hay sót tiêu chí bắt buộc | Sinh viên nộp bài (tôi), cả nhóm làm bài | 1 lần/tuần vào tối deadline; mất 40–50 phút mở đồng thời 4 tab (Rubric PDF, LMS checklist, Repo GitHub, file Markdown) để rà từng mục; đợt Day 01 từng bị trừ 1 điểm vì đặt sai quy tắc thư mục assets |
| 4 | Pain từ người khác | Khi thành viên mới hoặc bạn cùng nhóm pull code về và chạy thử dự án, họ muốn biết chính xác các bước cài đặt môi trường và các biến cấu hình cần thiết, để không phải nhắn tin hỏi đi hỏi lại người viết code chính | Thành viên khác trong nhóm, bản thân tôi (người phải support) | 3 lần trong đợt setup Day 01 bạn cùng nhóm nhắn tin hỏi lỗi `ModuleNotFoundError` và thiếu file `.env`; tôi mất tổng cộng gần 1 giờ để debug hộ qua tin nhắn/Call Discord |
| 5 | Lặp lại | Khi hoàn thành một tính năng hoặc fix xong một lỗi, tôi muốn viết nội dung mô tả Pull Request (PR description) chuẩn chỉ tóm tắt đúng các thay đổi chính, để người review hiểu ngay mà tôi không phải gõ lại từ đầu | Tôi và người review code trong nhóm | Trung bình 4–6 PR/tuần; mỗi PR mất 10–15 phút nhớ lại và gõ lại mô tả thủ công; có 2 PR tuần trước chỉ viết vội "fix bug", "update" khiến bạn cùng nhóm phải gọi hỏi lại |
| 6 | Tốn thời gian | Khi gặp một bug lạ hoặc lỗi stack trace dài trong lúc chạy code bài tập, tôi muốn định vị nhanh vị trí đoạn code gây lỗi và nguyên nhân cốt lõi trong codebase của nhóm, để sửa lỗi ngay thay vì phải đọc từng hàm và log thủ công | Bản thân tôi khi làm bài lập trình | Trung bình 2–3 lần/tuần khi code dự án; mỗi lần traceback phức tạp mất 45–60 phút tra Google, lục log và đặt print debug; có hôm mất cả buổi tối vì lỗi import vòng |
| 7 | Cần đọc, tổng hợp nhiều thông tin | Khi cần cập nhật tiến độ bài tập nhóm lên file báo cáo chung hoặc bảng phân công, tôi muốn tổng hợp nhanh danh sách commit, PR đã merge và task đã xong từ GitHub/Trello, để điền báo cáo tuần mà không phải mở từng trang lục lọi | Trưởng nhóm và các thành viên phụ trách ghi chép báo cáo | 1 lần/tuần trước giờ họp nhóm; mất 30 phút rà soát commit history và chat Discord để biết bạn nào đã làm xong phần nào |
| 8 | Pain từ người khác | Khi bạn cùng nhóm đọc tài liệu API hoặc hàm do tôi viết, họ muốn nắm được ngay kiểu dữ liệu đầu vào, đầu ra và ngoại lệ có thể xảy ra, để ghép module trơn tru mà không bị lỗi crash ngầm | Bạn ghép code cùng nhóm, tôi (người bị réo hỗ trợ) | Tuần trước bạn ghép module API gửi dữ liệu sai định dạng (JSON vs Form-data) làm lỗi mất 1 buổi chiều, nhóm phải họp khẩn 30 phút để sync lại |
| 9 | Tốn thời gian | Khi nhận tài liệu đặc tả yêu cầu hoặc đề bài lab dài 15–20 trang, tôi muốn trích xuất nhanh các yêu cầu chức năng (functional requirements) và ràng buộc kỹ thuật cốt lõi, để lập kế hoạch phân chia công việc cho nhóm trước khi bắt tay vào code | Cả nhóm làm bài lab (4 người) | 1 lần vào đầu mỗi bài lab lớn (khoảng 2 tuần/lần); mất 60–75 phút đọc quét và ghi chú ra Google Docs; từng sót 1 yêu cầu phi chức năng về response time ở môn trước |
| 10 | Lặp lại | Khi viết xong một đoạn code logic quan trọng, tôi muốn viết các ca kiểm thử đơn vị (unit test cases) bao quát các trường hợp biên (edge cases), để đảm bảo code không phát sinh lỗi khi người khác merge vào | Tôi và toàn bộ thành viên nhóm phụ thuộc vào module đó | Mỗi tuần mất khoảng 40–50 phút viết test tay cho các hàm cơ bản; hay bị lười viết test dẫn đến bug lọt sang khâu tích hợp |

**Nếu có dùng AI để gợi ý thêm:** ý nào AI gợi ý mà bạn giữ lại, ý nào bỏ và vì sao.

- **Ý kiến do AI gợi ý:** Sau khi tự scan 8 vấn đề từ trải nghiệm thực tế, tôi prompt AI gợi ý thêm 4 ý:
  1. *Trợ lý AI tự động quản lý dự án và phân chia task cho thành viên.*
  2. *Trích xuất yêu cầu và ràng buộc kỹ thuật từ đề bài lab dài.*
  3. *Tự động sinh unit test bao quát edge cases cho hàm logic.*
  4. *Chatbot hỏi đáp lỗi lập trình chung.*
- **Ý giữ lại (đã viết lại theo trải nghiệm thật):**
  - Giữ lại ý 2 (thành Problem #9) và ý 3 (thành Problem #10) vì đây là các công đoạn có quy trình rõ ràng, tốn nhiều thời gian và bản thân tôi thực sự gặp khó khăn trong các bài lab vừa qua, kèm số liệu đo lường cụ thể.
- **Ý loại bỏ và lý do:**
  - Bỏ ý 1 vì quá rộng, mang tính "trợ lý toàn năng", không có ranh giới và quy trình cụ thể cho sinh viên làm lab.
  - Bỏ ý 4 vì lỗi lập trình chung đã có StackOverflow, Google hoặc ChatGPT tra cứu độc lập rất tốt, không phản ánh điểm nghẽn quy trình phối hợp nội bộ trong nhóm.

---

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 | Giải quyết xung đột Git merge conflict khi làm việc nhóm (#1) | Quy trình rõ, xảy ra liên tục hằng tuần, rủi ro cao (mất code logic của bạn), có số phút đo thật (50 phút/lần) | Làm sao đảm bảo dev không ỷ lại vào gợi ý của AI mà bỏ qua bước kiểm tra logic và chạy unit test? |
| 2 | Rà soát checklist nộp bài lab và cấu trúc repo theo rubric (#3) | Nỗi đau lặp lại mỗi tối nộp bài, ảnh hưởng trực tiếp tới điểm số cả nhóm, có thể phân định rõ giữa kiểm tra quy tắc tĩnh và kiểm tra nội dung | Có cần AI không hay chỉ cần script Python/Bash check regex tên file và file markdown là đủ? |
| 3 | Review Pull Request lớn trong nhóm lập trình (#2) | Điểm nghẽn phổ biến làm chậm tiến độ sprint, reviewer mất nhiều thời gian đọc diff rời rạc không hiểu ngữ cảnh | Khó đo lường định lượng thế nào là một bản review "chất lượng tốt" ngoài số phút tiết kiệm được |

### Problem Card #1

| Trường | Nội dung |
|---|---|
| Job Story | Khi hợp nhất code (merge/rebase) từ nhánh `main` vào nhánh tính năng cá nhân trước khi tạo Pull Request, tôi muốn nhanh chóng xác định đúng đoạn code cần giữ và giải quyết xung đột, để code không bị hỏng logic và merge thành công vào repo nhóm |
| Actor | Sinh viên ngành Công nghệ thông tin / Thành viên phụ trách lập trình trong nhóm dự án (4 người) |
| Thời điểm / bối cảnh | Cuối sprint hoặc trước khi tạo Pull Request nộp bài lab, khi nhiều thành viên cùng push code lên các nhánh |
| Quy trình hiện tại (3–7 bước) | 1. Chạy `git pull origin main` hoặc `git merge main` trên máy cá nhân · 2. Git báo conflict ở 3–5 files, mở VS Code để xem conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`) · 3. Đọc hiểu cả 2 phiên bản code, nhắn tin/gọi Discord cho bạn cùng nhóm để hỏi ý đồ đoạn code bị đụng hàng · 4. Chọn giữ phần nào / kết hợp cả hai, xóa markers, lưu file và chạy test thử xem code còn chạy được không · 5. Commit `Merge branch 'main' into feature` và push lên GitHub |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3 (Hỏi và đối chiếu ý đồ logic code của cả hai bên để quyết định giữ gì bỏ gì): mất ~25 phút/lần, phụ thuộc vào việc bạn kia có online để trả lời không, rất dễ chọn nhầm làm mất code của nhau |
| Impact (nếu không giải thì sao) | Mất ~50 phút/lần conflict; xảy ra 2–3 lần/tuần trong giai đoạn nước rút (tổng mất ~100–150 phút/tuần/người). Nếu sửa sai logic thì làm hỏng toàn bộ build của repo, cả nhóm mất thêm cả tiếng để rollback và tìm lỗi |
| Success metric (baseline → target) | Tổng thời gian giải quyết conflict từ 50 phút/lần xuống dưới 15 phút/lần; tỷ lệ lỗi logic/hỏng build phát sinh do merge nhầm giảm từ 1 lần/sprint về 0 |
| Phương án không dùng AI | Thống nhất quy trình Git workflow chặt chẽ (chia nhỏ branch dưới 200 dòng, pull main mỗi sáng, chia task tách biệt module); dùng 3-way merge editor trực quan của VS Code. Giảm được tần suất conflict nhưng khi đụng logic chung vẫn mất 20–25 phút đối chiếu thủ công |
| Giả thuyết về AI (nếu có) | AI phân tích AST/ngữ cảnh và commit log của 2 nhánh, giải thích tóm tắt sự khác biệt về mặt ý đồ thuật toán của 2 bên và gợi ý đoạn code hợp nhất; developer chỉ cần review và xác nhận |
| Cảm nhận nhanh | Workflow (kết hợp phân tích context + gợi ý của AI + Developer bắt buộc review và chạy test) |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — 50 phút/lần conflict

[1 Chạy git merge main: 5'] → [2 Mở VS Code định vị conflict markers: 5']
→ [3 Đọc code 2 bên, chat Discord hỏi ý đồ bạn cùng nhóm: 25'] ← BOTTLENECK
→ [4 Chọn giữ/kết hợp code, xóa marker, chạy test local: 10']
→ [5 Commit merge & push lên remote: 5']
```

### Problem Card #2

| Trường | Nội dung |
|---|---|
| Job Story | Khi chuẩn bị nộp bài lab trước deadline 23h59, tôi muốn đối chiếu toàn bộ các file trong repo với rubric và checklist nộp bài của giảng viên, để đảm bảo không bị trừ điểm vì thiếu file, sai tên file hay sót tiêu chí bắt buộc |
| Actor | Trưởng nhóm / Thành viên chịu trách nhiệm kiểm tra bài nộp của nhóm |
| Thời điểm / bối cảnh | Tối trước hạn nộp bài lab (từ 21h30 đến 23h30) |
| Quy trình hiện tại (3–7 bước) | 1. Mở file `RUBRIC.md` và `SUBMISSION.md` trên LMS/repo để đọc danh sách yêu cầu · 2. Mở cấu trúc thư mục repo trên VS Code/GitHub · 3. Rà soát từng file xem có đúng định dạng tên không (ví dụ `MSSV_HoTen.md`) · 4. Mở từng file báo cáo kiểm tra xem có trường nào còn để trống hoặc `[cần điền]` không · 5. Kiểm tra link ảnh, assets và link markdown xem có bị 404/link hỏng không · 6. Tạo commit/tag nộp link lên LMS |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 4 (Kiểm tra từng mục trong báo cáo xem đã điền đủ nội dung, số liệu, rubric criteria chưa): mất 15–20 phút, dễ hoa mắt bỏ sót khi báo cáo dài cả trăm dòng |
| Impact (nếu không giải thì sao) | Mất 55 phút mỗi tối nộp bài; nếu sót một tiêu chí (như thiếu baseline, sai tên thư mục) thì bị trừ 1–5 điểm trực tiếp vào điểm tổng cả nhóm |
| Success metric (baseline → target) | Tổng thời gian kiểm tra giảm từ 55 phút xuống dưới 10 phút; số lỗi định dạng/thiếu file/thiếu trường rubric giảm từ 1–2 lỗi/lab về 0 |
| Phương án không dùng AI | Viết script Python hoặc GitHub Action CI chạy pre-commit hook kiểm tra tồn tại của file, regex check quy tắc đặt tên và lint markdown (giải quyết được 80% lỗi hình thức tĩnh) |
| Giả thuyết về AI (nếu có) | AI đọc Rubric và nội dung bài nộp, đối chiếu ngữ nghĩa xem từng mục đã trả lời đúng trọng tâm câu hỏi chưa, cảnh báo các câu trả lời hời hợt hoặc thiếu số liệu trước khi nộp |
| Cảm nhận nhanh | Rule (Script kiểm tra tĩnh cấu trúc file) kết hợp Workflow (nếu dùng AI rà soát ngữ nghĩa nội dung) |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — 55 phút/lần nộp bài

[1 Đọc rubric & submission guide: 10'] → [2 Mở cấu trúc thư mục repo: 5']
→ [3 Rà soát tên file theo quy ước: 10']
→ [4 Mở từng file báo cáo đọc xem có sót mục/thiếu số liệu: 15'] ← BOTTLENECK
→ [5 Kiểm tra link markdown và assets: 10']
→ [6 Commit nộp bài lên LMS: 5']
```

### Problem Card #3

| Trường | Nội dung |
|---|---|
| Job Story | Khi bắt đầu review Pull Request (PR) lớn (hơn 300 dòng code hoặc nhiều file) của thành viên khác trong nhóm, tôi muốn hiểu nhanh ý đồ thay đổi và các điểm rủi ro tiềm ẩn, để phản hồi chính xác trước khi approve code |
| Actor | Thành viên review code (Peer reviewer trong nhóm lập trình) |
| Thời điểm / bối cảnh | Khi có thành viên vừa tạo PR vào nhánh `develop`/`main` trước buổi họp sprint |
| Quy trình hiện tại (3–7 bước) | 1. Nhận thông báo PR trên GitHub/Discord · 2. Mở tab "Files changed", lướt qua danh sách 5–10 files thay đổi để nắm bức tranh tổng thể · 3. Đọc từng khối code diff, cố gắng liên kết với yêu cầu tính năng xem đoạn code này làm nhiệm vụ gì · 4. Kéo code về máy chạy thử (nếu cần kiểm tra runtime/test) · 5. Để lại comment góp ý và ấn Approve hoặc Request changes |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3 (Đọc và hiểu logic code diff không có ngữ cảnh rõ ràng): mất 25 phút/PR, đặc biệt mệt mỏi khi người viết PR viết mô tả sơ sài |
| Impact (nếu không giải thì sao) | Mất 50 phút/PR; 2 PR/tuần = 100 phút/tuần. Nếu review qua loa thì bug lọt vào main gây vỡ code của các bạn khác, mất thêm thời gian debug tích hợp |
| Success metric (baseline → target) | Thời gian review giảm từ 50 phút xuống 20 phút/PR; tăng số phát hiện lỗi logic/tiềm ẩn từ khâu review lên ít nhất 1 issue/PR |
| Phương án không dùng AI | Bắt buộc dùng PR template (yêu cầu ghi rõ: mục đích thay đổi, checklist test, ảnh chụp kết quả); giới hạn PR dưới 200 dòng code; tích hợp Linter/SonarQube tự động bắt lỗi syntax/formatting |
| Giả thuyết về AI (nếu có) | AI tự động tóm tắt diff theo từng tính năng, highlight các hàm thay đổi quan trọng và chỉ ra các case có thể gây lỗi logic / race condition để reviewer tập trung kiểm tra |
| Cảm nhận nhanh | Workflow (kết hợp Linter dạng Rule + AI tóm tắt diff & gợi ý rủi ro cho Reviewer) |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — 50 phút/PR

[1 Nhận thông báo PR: 2'] → [2 Lướt xem danh sách files thay đổi: 8']
→ [3 Đọc từng khối code diff, liên kết logic tính năng: 25'] ← BOTTLENECK
→ [4 Kéo code về máy chạy thử test: 10']
→ [5 Viết nhận xét & Approve: 5']
```

### Card muốn pitch nhất

- Card số: Problem Card #1 (Giải quyết xung đột Git merge conflict khi làm việc nhóm)
- Vì sao: Đây là nỗi đau thực tế và nhức nhối nhất của sinh viên khi làm dự án lập trình chung; tần suất xảy ra thường xuyên (2–3 lần/tuần); quy trình hiện tại có số liệu đo lường cụ thể (50 phút/lần); và đặc biệt là rủi ro mất code rất lớn gây ức chế tâm lý cho cả nhóm.
- Câu hỏi muốn nhóm phản biện: "Liệu việc giải quyết conflict bằng AI có làm developer chủ quan không kiểm tra lại logic và test kỹ, dẫn đến nguy cơ bug ngầm nghiêm trọng hơn việc tự đọc thủ công không? Ranh giới (boundary) an toàn nào cho AI can thiệp ở đây?"

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|---|---|---|
| Baseline 50 phút/lần conflict có thể bị phóng đại nếu chỉ là conflict vài dòng import đơn giản | Đồng ý một phần | Đã phân loại rõ: các conflict đơn giản (import, format) dùng rule/auto-resolve chỉ mất 2-3 phút; chỉ những conflict logic nghiệp vụ (thay đổi chung hàm, đổi kiểu dữ liệu) mới mất 35–50 phút và lấy trường hợp này làm baseline đo lường chính |
| Để AI tự động resolve conflict rồi auto-commit là cực kỳ rủi ro (nguy cơ hallucination, phá vỡ business logic) | Hoàn toàn đồng ý | Đã sửa thiết kế giải pháp: Boundary bắt buộc là AI chỉ dừng ở mức phân tích ý đồ hai bên và gợi ý đoạn code hợp nhất, con người (developer) bắt buộc phải trực tiếp review, chạy unit test và nhấn nút xác nhận merge |
| Một số conflict xảy ra do tổ chức phân chia công việc trong nhóm kém (2 người cùng sửa 1 file), sửa quy trình làm việc (No AI) có thể giải quyết được 70% vấn đề | Đồng ý | Đã bổ sung phương án Không dùng AI (quy ước chia nhỏ branch, pull daily, phân chia task độc lập theo module) vào phần so sánh, coi đó là giải pháp nền tảng song hành |

---

## 4. Tôi đã tham gia phần nào (CP3 → CP7)

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch Problem Card | Pitch Problem Card #1 "Giải quyết xung đột Git merge conflict khi làm việc nhóm" (bottleneck ở bước đọc hiểu code 2 bên và chat hỏi ý đồ logic mất ~25 phút; tổng 50 phút/lần) | Card được nhóm đánh giá cao về tính thực tế và đau đớn, lọt vào shortlist và được chọn làm Candidate Problem chính của nhóm |
| Phản biện bài của bạn khác | Đặt câu hỏi  về bài toán COD: "Quy trình đối soát COD phần lớn là đối chiếu bảng tính, liệu dùng công thức Excel/Power Query có giải quyết được 80% không, việc dùng AI ở đây có khả thi và thật sự cần thiết không?" | Bạn thừa nhận phần lớn giải được bằng Rule, nhóm nhận ra không nên vội vã dùng AI cho bài toán thuần bảng tính và hướng sự tập trung vào bài toán có độ mơ hồ cao hơn |
| Nhận phản biện | Nhận câu hỏi : "Cách AI sẽ can thiệp vào quy trình fix conflict như thế nào? Liệu có an toàn không nếu AI tự động gộp code làm vỡ logic? Tại sao không dùng quy tắc workflow đơn giản mà phải nghĩ đến multi-agent?" | Tôi đã sửa thiết kế giải pháp: Chấp nhận phương án không để AI tự trị hoàn toàn; thiết lập ranh giới cứng (Boundary) là AI chỉ phân tích AST/ngữ cảnh và gợi ý code, lập trình viên bắt buộc phải duyệt (HITL) và chạy unit test trước khi merge |
| Gom cluster / cây OST | Cùng nhóm phân loại 12 candidate thành 3 nhóm lớn: A (Quy trình cộng tác & lập trình nhóm - Git conflict), B (Đối soát dữ liệu & tài chính), C (Tra cứu & trích xuất tri thức tài liệu). Tham gia dựng cây Opportunity Solution Tree (OST) | Xác định rõ Outcome của nhóm là: "Giảm thời gian xử lý xung đột và rủi ro hỏng build khi cộng tác code trong sprint" |
| Chọn candidate problem | Cùng nhóm chấm điểm bảng ma trận shortlist (1–5) theo 7 tiêu chí; bảo vệ tính cấp thiết và khả năng đo lường của bài toán Git Merge Conflict | Bài toán Git Merge Conflict đạt điểm cao nhất (actor rõ, quy trình rõ, pain thật, impact đo được) và được nhóm chọn 100% |
| Kiểm chứng / research | Xây dựng Assumption Map (tập trung vào rủi ro Usability: dev có tin tưởng và hiểu code AI gợi ý không); phỏng vấn nhanh 2 bạn dev lớp khác; tìm hiểu các tool thị trường (GitHub Copilot diff, GitKraken, Sourcery) | Nhóm nhận ra các tool hiện có chỉ gợi ý cú pháp tại chỗ nhưng không hiểu ngữ cảnh commit history của 2 nhánh và thiếu bước tự động chạy test kiểm chứng logic |
| Quy trình nhóm | Trực tiếp phác thảo và chuẩn hóa sơ đồ quy trình Hiện tại (Before: 50 phút) và quy trình Tương lai (After: 15 phút), phân định rõ từng bước Rule, AI, và Con người | Định hình rõ ràng handoff giữa các bước và phương án quay về (fallback: quay về 3-way merge thủ công nếu gợi ý AI không vượt qua unit test) |
| Problem Statement | Dự thảo Problem Statement v0 với 6 trường; tiếp thu ý kiến phản biện của nhóm để nâng cấp lên v1 (bổ sung AI intervention point, boundary nghiêm ngặt và 3 tiêu chí eval đánh giá đầu ra của AI) | Bản Problem Statement v1 của nhóm có ranh giới rõ ràng, không bị lẫn giải pháp vào problem |
| Mức can thiệp AI | Tham gia tranh luận về việc chọn mức Workflow hay Agent; phân tích ma trận độ mơ hồ × độ phức tạp cho bài toán code conflict | Thuyết phục nhóm chọn mức Workflow trước thay vì vội vã làm Multi-Agent tự trị phức tạp; xác định rõ chỉ dùng Agent khi cần tự động gọi test runner lặp lại nhiều vòng |
| Quyết định | Cùng nhóm đánh giá 4 rủi ro cốt lõi (Value, Usability, Feasibility, Viability); đề xuất quyết định và ngưỡng dừng | Thống nhất quyết định: **Not Yet** (hoặc Go có điều kiện pilot hẹp trên 1 repository nội bộ): cần đo baseline thời gian thật trên 10 ca conflict và kiểm chứng độ chính xác của prompt phân tích AST trước khi xây dựng hệ thống hoàn chỉnh |

---

## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| **CP1 Scan** | Gợi ý thêm các pain points trong quá trình làm việc nhóm và lập trình bài lab | Gợi ý góc nhìn về việc trích xuất spec yêu cầu từ đề bài lab dài và sinh unit test edge cases (ý #9, #10) | Đưa ra các ý tưởng quá chung chung, sáo rỗng như "Trợ lý AI quản lý toàn diện dự án", "Chatbot trả lời lỗi lập trình chung" (không có quy trình cụ thể) | Loại bỏ các ý viển vông; chỉ giữ lại 2 ý có quy trình rõ, viết lại hoàn toàn theo chuẩn Job Story gắn với số liệu đau đớn thật của bản thân |
| **CP2 Problem Card** | Đóng vai lập trình viên senior hoài nghi để phản biện Card #1 (Merge Conflict) | Chỉ ra điểm yếu: baseline 50 phút có thể bị phóng đại với conflict dòng đơn; cảnh báo nguy cơ dev lười suy nghĩ nếu AI tự resolve | Đề xuất giải pháp cực đoan: "để AI tự resolve và commit luôn để tiết kiệm thời gian tối đa" | Bác bỏ đề xuất tự động hoàn toàn; thiết lập ranh giới cứng (Boundary): AI chỉ gợi ý kèm giải thích ngữ cảnh, developer bắt buộc phải review và chạy unit test (Human-in-the-loop) |
| **CP4 Research** | Tìm kiếm các giải pháp, công cụ và pattern hiện có giải quyết Git merge conflict bằng AI | Liệt kê nhanh các công cụ thị trường (GitKraken Merge Tool, GitHub Copilot, Sourcery) và nguyên lý 3-way merge | Đưa ra một số link tài liệu giả định/không tồn tại, phóng đại khả năng giải quyết conflict đạt 95% mà không có nguồn kiểm chứng | Tự tìm đọc tài liệu GitHub Docs, kiểm tra thực tế tính năng Copilot in VS Code và ghi nhận rõ hạn chế: AI hiện tại rất hay bị ảo giác ngữ cảnh nếu conflict giữa nhiều hàm phụ thuộc |
| **CP5 Quy trình** | Chuyển đổi mô tả quy trình dạng text sang sơ đồ quy trình dạng text trực quan | Định dạng sơ đồ nhanh, trực quan, phân chia luồng rõ ràng | Tự ý gộp bước "đọc hiểu code 2 bên" và "chạy test local" thành một bước, làm mờ đi nút thắt bottleneck chính | Tách bạch từng bước thành: [1. Script phát hiện] -> [2. AI phân tích AST/Context] -> [3. AI đề xuất] -> [4. Dev review & chọn] -> [5. Chạy test tự động]; giữ nguyên bottleneck ở bước đối chiếu logic |
| **CP5–6 Problem Statement** | Rà soát Problem Statement v0 để phát hiện từ ngữ chứa giải pháp (solution bias) | Soi ra chỗ tôi vô tình viết "cần một công cụ AI multi-agent..." vào phần mô tả quy trình | Phản biện hời hợt ở phần Success metric, khen ngợi chung chung thay vì chỉ ra cách đo lường cụ thể | Sửa lại hoàn toàn ngôn ngữ trung tính mô tả vấn đề thuần túy; bổ sung công thức đo Success Metric (baseline đo bằng bấm giờ, target giảm thời gian, giữ tỷ lệ hỏng build = 0) |
| **CP6 Mức can thiệp / quyết định** | So sánh ưu/nhược điểm giữa Workflow và Multi-Agent cho bài toán resolve conflict | Phân tích rõ ràng: Workflow phù hợp cho quy trình tuyến tính, Agent phù hợp khi cần tự động gọi công cụ (linter, compiler, test runner) lặp lại | Quá thiên vị Agent, khuyên nên xây hệ thống đa tác tử phức tạp ngay lập tức mà bỏ qua chi phí và rủi ro hallucination | Giữ lập trường thực tế: Ưu tiên thiết kế mức Workflow kiểm soát chặt chẽ trước; chỉ nâng lên Agent cho bước tự động chạy test và sửa lỗi vòng lặp nếu có đủ dữ liệu kiểm chứng |

---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5). **Không dùng AI để viết thay.**

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**
Tôi đã học được cách xác định phương pháp phân tích cách giới hạn Ai để chúng có thể thật sự làm việc theo đúng yêu và giải quyết đúng vấn đề.
**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**

**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**
Tôi có đổi ý. Ban đầu tôi định để Ai tự động hoàn toàn nhưng sau đó nhóm khiến tôi thay đổi ý kiến sang ai cần có sự giám sát, giới hạn trong quyền quyết định sửa, phạm vi sửa.
**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**

**6.5. Điều khó nhất khi viết Problem Statement là gì?**

Điều khó khăn và tốn nhiều công sức nhất khi chắp bút viết Problem Statement chính là việc định lượng Success Metric và thiết lập ranh giới an toàn.

**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**

Nếu có cơ hội thực hiện lại bài lab này từ đầu, điều đầu tiên tôi sẽ thay đổi là chuẩn bị sẵn dữ liệu thực nghiệm trước buổi học: tôi sẽ trích xuất lịch sử git log của ít nhất 5–10 ca merge conflict phức tạp từ các đồ án lập trình kỳ trước. Việc có sẵn tập dữ liệu thật (ground truth) ngay từ đầu sẽ giúp nhóm không phải mất thời gian tranh cãi dựa trên những con số ước lượng cảm tính.

**6.7. Hiểu bài:** giải thích bằng 5–8 câu, không nhìn tài liệu, chuỗi *problem → quy trình → metric → boundary → mức can thiệp AI → quyết định* của bài nhóm mình.

Bài toán của nhóm là sinh viên lập trình tốn trung bình 50 phút mỗi lần xử lý Git merge conflict phức tạp khi làm việc nhóm, dễ gây mất code logic và hỏng build repo. Quy trình giải quyết gồm phát hiện conflict bằng script, trích xuất AST và ngữ cảnh commit của hai nhánh, AI phân tích ý đồ logic và gợi ý đoạn code hợp nhất, developer trực tiếp review xác nhận và cuối cùng hệ thống tự động chạy linter kèm unit test trước khi merge. Metric cốt lõi là giảm thời gian xử lý một ca conflict từ 50 phút xuống dưới 15 phút, đồng thời giữ tỷ lệ lỗi logic và hỏng build sau merge ở mức bằng 0. Boundary bắt buộc là AI chỉ đóng vai trò phân tích ngữ cảnh và đề xuất phương án, tuyệt đối không được tự động commit hay push code lên remote repository mà phải có sự xác nhận của developer (Human-in-the-loop). Về mức can thiệp, nhóm xác định lựa chọn mức Workflow (các bước thực thi tuần tự được định sẵn bằng code, AI can thiệp ở khâu hiểu ngữ nghĩa), từ chối mức Agent tự trị để loại trừ rủi ro ảo giác và độ phức tạp không cần thiết. Quyết định cuối cùng của nhóm là **Not Yet**: nhóm cần tiến hành đo lường baseline thời gian trên 10 ca conflict thật và kiểm chứng độ chính xác của prompt phân tích diff trên pilot hẹp trước khi chính thức phát triển thành công cụ mở rộng.

---

## 7. Tài liệu tham khảo
- **Tài liệu bài giảng môn học**: Bộ slide và worksheet hướng dẫn Discovery & Problem Framing (Day 02), Học viện/Trường Đại học VinUniversity.
- **Biên bản thảo luận và phản biện nội bộ**: Nhóm 02 (các thành viên Hà Phan Đại Dương, Lê Bá Nguyên, Nguyễn Thiên Long, Nguyễn Ngọc Bách, Nguyễn Văn Tuấn).
