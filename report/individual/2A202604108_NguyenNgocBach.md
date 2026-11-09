# Báo cáo cá nhân — MSSV_HoTen

> Đổi tên file theo quy tắc `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md` (MSSV trước, dấu `_`, họ tên viết liền không dấu). Sửa cả dòng tiêu đề phía trên cho khớp.
> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: copy template này thành file mới, điền, rồi commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên: Nguyễn Ngọc Bách
- MSSV: 2A202604108
- Email trường (không bắt buộc, repo có thể để public):
- Tên nhóm: 2
- Link repo nhóm: https://github.com/DanielHa01/K5-L3B-DAY02-Nhom02-DiscoveryProblemFraming.git

---

## 2. Scan problem (CP1)

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

| # | Lăng kính | Job Story: Khi… tôi muốn… để… | Ai chịu ảnh hưởng? | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng) |
|---:|---|---|---|---|
| 1 | Lặp lại | Khi triển khai chức năng mới, tôi muốn kiểm tra các chức năng có thể bị ảnh hưởng, để đảm bảo thay đổi không gây lỗi cho hệ thống hiện tại | developer, QA | 30p/lần |
| 2 | Pain từ người khác |Khi tiếp nhận yêu cầu từ khách hàng, tôi muốn xác định rõ kết quả đầu ra mà họ mong đợi, để tránh triển khai sai và phải chỉnh sửa sau khi demo. | cả team, khách hàng | Demo không đúng khách hàng mong muốn, phải feedback và rework liên tục |
| 3 | Cần đọc, tổng hợp nhiều thông tin | Khi được phân công tham gia một dự án đang triển khai, tôi muốn nhanh chóng nắm được kiến trúc, yêu cầu và tiến độ hiện tại, để có thể bắt đầu công việc mà không mất nhiều thời gian tìm hiểu lại từ đầu. | cả team | 30p tổng hợp file trong telegram |
| 4 | Pain từ người khác | Khi bàn giao đặc tả chức năng cho frontend developer, tôi muốn các yêu cầu và trường hợp xử lý được hiểu thống nhất, để giảm thời gian giải thích lại và tránh triển khai sai. | frontend developer, PM | frontend developer hỏi liên tục |
| 5 | Tốn thời gian | Khi team gặp một vấn đề kỹ thuật có nhiều hướng giải quyết, tôi muốn có đủ thông tin để so sánh ưu nhược điểm của từng phương án, để đưa ra quyết định phù hợp mà không phải họp và thay đổi hướng triển khai nhiều lần. | cả team | 1h họp mỗi ngày cho đến khi ra dược phương án |


**Nếu có dùng AI để gợi ý thêm:** ý nào AI gợi ý mà bạn giữ lại, ý nào bỏ và vì sao.

- Sau khi tự scan 5 vấn đề, tôi tham khảo AI và quyết định giữ lại ý #2, #3 và #4 vì có ảnh hưởng thực tế đến tiến độ và hiệu quả làm việc

---

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 | Khách hàng yêu cầu output mơ hồ (#2) | impact rộng | |
| 2 | Tìm hiểu thông tin dự án mới (#3)| Pain thật, tốn giời gian và nhiều người gặp | |
| 3 | trao đổi trong team (#4)| nhiều người đau | |

### Problem Card #1

| Trường | Nội dung |
|---|---|
| Job Story | Khi được phân công tham gia một dự án đang triển khai, tôi muốn nhanh chóng nắm được kiến trúc, yêu cầu và tiến độ hiện tại, để có thể bắt đầu công việc mà không mất nhiều thời gian tìm hiểu lại từ đầu. |
| Actor | Developer mới tham gia dự án |
| Thời điểm / bối cảnh | Khi được phân công vào một dự án đã có tài liệu và lịch sử trao đổi trên Telegram |
| Quy trình hiện tại (3–7 bước) | Nhận phân công -> Tìm tài liệu -> Tổng hợp file -> Đọc tài liệu -> Xác nhận thông tin với team |
| Bottleneck (bước nào, mất bao nhiêu phút) | 	Tìm và tổng hợp tài liệu phân tán trên Telegram, khoảng 30 phút |
| Impact (nếu không giải thì sao) | Chậm tiếp nhận công việc, có nguy cơ bỏ sót thông tin quan trọng |
| Success metric (baseline → target) | Thời gian tìm và tổng hợp tài liệu: 30 phút → mục tiêu thử nghiệm 10 phút |
| Phương án không dùng AI | Tập trung tài liệu vào một thư mục chung, chuẩn hóa tên file, tạo README và mục lục dự án |
| Giả thuyết về AI (nếu có) | Sử dụng tìm kiếm ngữ nghĩa để hỗ trợ truy xuất tài liệu và tổng hợp thông tin liên quan |
| Cảm nhận nhanh | Workflow |

Quy trình nháp hiện tại:

```text
[1 Export Telegram: 10'] -> [2 lọc file cần thiết: 5']
-> [3 Tổng hợp Docs: 15'] -> [4 Viết narrative: 25'] 
-> [5 Review + format: 10'] -> [6 Gửi: 5']
```

### Problem Card #2

| Trường | Nội dung |
|---|---|
| Job Story | Khi bàn giao đặc tả chức năng cho frontend developer, tôi muốn các yêu cầu và trường hợp xử lý được hiểu thống nhất, để giảm thời gian giải thích lại và tránh triển khai sai. |
| Actor | 	Người viết spec, frontend developer |
| Thời điểm / bối cảnh | 	Khi frontend bắt đầu triển khai chức năng mới |
| Quy trình hiện tại (3–7 bước) | 	Viết spec → Gửi frontend → Frontend đọc → Hỏi lại → Giải thích → Triển khai |
| Bottleneck (bước nào, mất bao nhiêu phút) | Các vòng hỏi đáp để làm rõ yêu cầu; chưa đo thời gian |
| Impact (nếu không giải thì sao) | Gián đoạn công việc, chậm triển khai, có nguy cơ phát sinh rework|
| Success metric (baseline → target) | Số lượt hỏi làm rõ trên mỗi spec: baseline cần đo → mục tiêu giảm 50% |
| Phương án không dùng AI | Chuẩn hóa template spec, bổ sung acceptance criteria, ví dụ input/output và edge cases |
| Giả thuyết về AI (nếu có) | 	Hỗ trợ rà soát spec để phát hiện nội dung thiếu hoặc mơ hồ trước khi bàn giao |
| Cảm nhận nhanh | Agent |

Quy trình nháp hiện tại:

```text
[1 Export Telegram: 10'] -> [2 lọc file cần thiết: 5']
-> [3 Tổng hợp Docs: 15'] -> [4 Viết narrative: 25'] 
-> [5 Review + format: 10'] -> [6 Gửi: 5']

```

### Problem Card #3

| Trường | Nội dung |
|---|---|
| Job Story | 	Khi tiếp nhận yêu cầu từ khách hàng, tôi muốn xác định rõ kết quả đầu ra mà họ mong đợi, để tránh triển khai sai và phải chỉnh sửa sau khi demo. |
| Actor | 	Khách hàng, PM/BA, developer và người phụ trách demo. |
| Thời điểm / bối cảnh | Khi tiếp nhận yêu cầu mới và chuẩn bị demo hoặc bàn giao tính năng. |
| Quy trình hiện tại (3–7 bước) | Nhận yêu cầu → diễn giải yêu cầu → thống nhất phương án -> triển khai -> demo -> nhận phản hồi -> sửa và demo lại. |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 6–7: phản hồi và rework do lệch kỳ vọng. |
| Impact (nếu không giải thì sao) |	Tăng chi phí triển khai, chậm bàn giao và giảm niềm tin của khách hàng. |
| Success metric (baseline → target) |  Số vòng rework do hiểu sai output ban đầu trên mỗi tính năng: cần đo → giảm 50% (mục tiêu đề xuất). Chỉ số phụ: tỷ lệ demo được chấp nhận lần đầu. |
| Phương án không dùng AI | Checklist làm rõ yêu cầu, mẫu output, mockup, acceptance criteria và xác nhận bằng văn bản trước triển khai. |
| Giả thuyết về AI (nếu có) |	Hỗ trợ phân tích yêu cầu mơ hồ, sinh danh sách câu hỏi xác nhận và soát độ đầy đủ của acceptance criteria. |
| Cảm nhận nhanh | Agent |

Quy trình nháp hiện tại:

```text
[1. Tiếp nhận yêu cầu: 15']
  -> [2. Phân tích và làm rõ: 30']
  -> [3. Thống nhất output dự kiến: 20']
  -> [4. Triển khai: thời lượng biến thiên, CẦN ĐO theo task]
  -> [5. Demo: 30' ]
  -> [6. Nhận / phân loại feedback: 20' ]
  -> [7. Rework: thời lượng biến thiên, 50'] <-- BOTTLENECK GIẢ THUYẾT
         | nếu chưa đạt kỳ vọng -> quay lại bước 2–5
```

### Card muốn pitch nhất

- Card số:
- Vì sao:
- Câu hỏi muốn nhóm phản biện:

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|---|---|---|
| | | |

---

## 4. Tôi đã tham gia phần nào (CP3 → CP7)

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch Problem Card | 	Chuẩn bị: pitch Card #3 về output khách hàng chưa rõ, nêu hậu quả rework và metric số vòng sửa. | Thêm option ý tưởng cho nhóm 
| Phản biện bài của bạn khác | Câu hỏi dự kiến: “pitch này đã thực tiễn hay chưa, có thực sự cần AI hay không?” | Thu gọn số lượng iption pitch của nhóm |
| Nhận phản biện | Câu hỏi tôi nhận được: quy trình này không phải áp dụng vào BA hay sale tốt hơn sao?   | Tôi đã sửa gì: thêm ý tưởng về agent BA gữa developer và khách hàng |
| Gom cluster / cây OST | | |
| Chọn candidate problem | Đề xuất cá nhân: vấn đề output khách hàng mơ hồ. | vấn đề conflict khi deploy git dự án lớn|
| Kiểm chứng / research | 	Kế hoạch: kiểm tra 5–10 demo/ticket gần đây, phân loại nguyên nhân rework; hỏi PM, developer, khách hàng nếu có thể. | |
| Quy trình nhóm | conflict xuất hiện -> agent devops raise vấn đề -> code agent sửa -> agent devop deploy lại -> loop | conflict xuất hiện -> agent devops raise vấn đề -> BA agent phân tích -> code agent sửa -> agent devop deploy lại -> loop |
| Problem Statement | Khi yêu cầu output chưa được xác nhận đủ rõ trước triển khai, team có nguy cơ demo sai kỳ vọng và phải rework. | conflict khi deploy git dự án lớn cần sửa thủ công tốn thời gian |
| Mức can thiệp AI | AI agent can thiệp sâu  | AI Agents can thiệp sâu  |
| Quyết định | agent | multi agents |

---

## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP1 Scan | 	Sau khi tự liệt kê 5 vấn đề, nhờ AI đánh giá, sàng lọc. | Giúp phân biệt pain với hoạt động bình thường và chỉ ra thiếu bằng chứng. | Có thể xem thời gian thực hiện là lãng phí dù chưa đo tác động. | Giữ #2–#4, tạm giữ #5 để xác minh và không ưu tiên #1. |
| CP2 Problem Card | Nhờ AI cấu trúc card, gợi ý metric, non-AI baseline và phản biện. | Làm rõ actor, bước nghẽn, metric và giải pháp đối chứng. | Đề xuất số phút/mục tiêu khi chưa có quan sát; dễ nhầm số minh họa với số thật. | Gắn nhãn mọi ước lượng; giữ 30 phút Telegram là baseline đã nêu; sửa quy trình copy nhầm. |
| CP4 Research | Dự kiến nhờ AI thiết kế câu hỏi phỏng vấn và bảng phân loại rework. | Có thể giúp giảm câu hỏi dẫn dắt | Không thể tự xác minh lời kể hoặc suy ra tỷ lệ rework. | Tự mở từng link; kiểm trang giá Slack: gói Pro chỉ có tóm tắt cơ bản |
| CP5 Quy trình | Dự kiến dùng AI rà soát các bước và điểm quay lại. | Có thể phát hiện thiếu nhánh và trách nhiệm. | Có thể bịa thời gian từng bước. | |
| CP5–6 Problem Statement | | | | |
| CP6 Mức can thiệp / quyết định | | | | |

---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5). **Không dùng AI để viết thay.**

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**

**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**

Nhóm luôn lên problem first

**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**

Tôi đổi ý về ý tuongr sử dụng agent đẻ tối ưu kết quả nhận được

**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**


**6.5. Điều khó nhất khi viết Problem Statement là gì?**

ĐÓ là có được 1 chủ để khỏi nguồn, nhận biết được problem có solution cụ thể ko

**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**
Nếu được làm lại, tôi sẽ dành nhiều thời gian hơn để xác minh vấn đề trước khi nghĩ đến giải pháp. Ban đầu, tôi thường đánh giá một vấn đề dựa trên cảm nhận cá nhân, chẳng hạn như công việc mất nhiều thời gian hoặc phải thực hiện lặp đi lặp lại. Tuy nhiên, không phải công việc nào tốn thời gian cũng là một pain cần giải quyết. Tôi sẽ thu thập thêm bằng chứng cụ thể như tần suất xảy ra, thời gian thực hiện và mức độ ảnh hưởng đến những người liên quan.

**6.7. Hiểu bài:** giải thích bằng 5–8 câu, không nhìn tài liệu, chuỗi *problem → quy trình → metric → boundary → mức can thiệp AI → quyết định* của bài nhóm mình.

Đầu tiên, cần xác định problem thực sự mà người dùng gặp phải, dựa trên bằng chứng thay vì cảm nhận chủ quan. Tiếp theo, phân tích quy trình hiện tại để xác định bước nào đang gây khó khăn hoặc mất nhiều thời gian nhất. Sau đó, lựa chọn metric phù hợp để đo lường mức độ nghiêm trọng của vấn đề và đánh giá hiệu quả cải thiện. Boundary giúp giới hạn phạm vi giải quyết, xác định rõ những gì nằm trong và ngoài bài toán. Dựa trên đặc điểm của quy trình, nhóm đánh giá mức can thiệp AI, từ không sử dụng AI, áp dụng rule, workflow cho đến agent. Không phải vấn đề nào cũng cần AI, đặc biệt khi các quy tắc hoặc cải tiến quy trình đơn giản đã có thể giải quyết hiệu quả. Cuối cùng, nhóm đưa ra quyết định dựa trên bằng chứng, tính khả thi, chi phí và lợi ích dự kiến, thay vì lựa chọn công nghệ trước rồi mới tìm vấn đề để áp dụng.

---

## 7. Tài liệu tham khảo

- Worksheet môn học: docs/01-worksheet.md
- ý kiến của các thành viên trong team 
