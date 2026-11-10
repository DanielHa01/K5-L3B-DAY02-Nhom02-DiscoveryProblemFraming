# Báo cáo cá nhân — MSSV_HoTen

> Đổi tên file theo quy tắc `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md` (MSSV trước, dấu `_`, họ tên viết liền không dấu). Sửa cả dòng tiêu đề phía trên cho khớp.
> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: copy template này thành file mới, điền, rồi commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên: Hà Phan Đại Dương
- MSSV: 2A202604119
- Email trường (không bắt buộc, repo có thể để public):
- Tên nhóm: Nhóm 02
- Link repo nhóm: https://github.com/DanielHa01/K5-L3B-DAY02-Nhom02-DiscoveryProblemFraming

---

## 2. Scan problem (CP1)

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

| # | Lăng kính | Job Story: Khi… tôi muốn… để… | Ai chịu ảnh hưởng? | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng) |
|---:|---|---|---|---|
| 1 | Tốn thời gian | Khi đến kỳ tổng hợp chi phí hàng tháng, tôi muốn thu thập tất cả hóa đơn và giấy ghi nợ về một nơi, để không bỏ sót bất kỳ khoản chi nào. | Kế toán | Mỗi tháng 1 lần khoảng 4 tiếng |
| 2 | Lặp lại | Khi nhận được nhiều hóa đơn và chứng từ, tôi muốn trích xuất số tiền, ngày tháng, nhà cung cấp và nội dung chi phí nhanh chóng, để không phải nhập liệu từng chứng từ. | Kế toán | Tổng 10 giờ mỗi tháng |
| 3 | Cần đọc, tổng hợp nhiều thông tin | Khi tổng hợp các khoản chi trong tháng, tôi muốn xác định từng khoản thuộc nhóm chi phí nào, để báo cáo phản ánh chính xác cơ cấu chi tiêu của công ty. | Kế toán | Số lượng chi phí lên đến hàng trăm mỗi tháng |
| 4 | Cần đọc, tổng hợp nhiều thông tin | Khi số liệu chi tiêu từ nhiều nguồn không khớp nhau, tôi muốn xác định khoản nào bị thiếu, trùng hoặc sai, để đảm bảo báo cáo chính xác. | Kế toán | Tháng trước có 2 khoản bị sai |
| 5 | Pain từ người khác | Khi các phòng ban chưa gửi đầy đủ chứng từ, tôi muốn biết ai chưa nộp và đang thiếu giấy tờ nào, để hoàn tất báo cáo đúng hạn mà không phải liên tục nhắc nhở. | Kế toán | Số lần nhắc nhở có thể lên đến 10 lần cho các phòng ban |
| 6 | Lặp lại | Khi kết thúc mỗi tháng, tôi muốn tự động tổng hợp các khoản chi phí và biến động tài chính, để tạo báo cáo cho CEO nhanh hơn. | Kế toán, CEO | 10 giờ mỗi tháng |
| 7 | Pain từ người khác | Khi CEO hỏi tại sao chi phí tháng này tăng so với tháng trước, tôi muốn nhanh chóng truy xuất các khoản chi và chứng từ liên quan, để giải thích nguyên nhân bằng số liệu cụ thể. | Kế toán, CEO | CEO phải hỏi lại trung bình 2-3 lần |
| 8 | Pain từ người khác | Khi một hóa đơn được bổ sung sau khi tôi đã tổng hợp số liệu, tôi muốn cập nhật dữ liệu và báo cáo mà không phải làm lại nhiều bước, để đảm bảo bản báo cáo cuối cùng luôn chính xác. | Kế toán, CEO | Mỗi tháng có từ 4-5 dữ liệu cần bổ sung hay sai sót |

**Nếu có dùng AI để gợi ý thêm:** ý nào AI gợi ý mà bạn giữ lại, ý nào bỏ và vì sao.

-

---

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 | Nhập liệu thủ công (#2) | Quy trình rõ, nhiều người gặp, tốn thời gian | Dữ liệu đầu vào rộng, khó scan chính xác |
| 2 | Giải thích chi phí (#7) | Pain thật, nhiều người gặp | Xử lý các thông tin mật thế nào |
| 3 | Phân loại chi phí (#3) | Tốn thời gian | Chưa rõ quy trình, kết quả cuối |

### Problem Card #1

| Trường | Nội dung |
|---|---|
| Job Story | Khi nhận được nhiều hóa đơn và chứng từ, tôi muốn trích xuất số tiền, ngày tháng, nhà cung cấp và nội dung chi phí nhanh chóng, để không phải nhập liệu từng chứng từ. |
| Actor | Kế toán |
| Thời điểm / bối cảnh | Hằng tuần và đặc biệt vào cuối tháng khi cần tổng hợp chi phí để gửi CEO. Chứng từ có thể ở dạng PDF, ảnh chụp, Excel hoặc bản giấy. |
| Quy trình hiện tại (3–7 bước) | (1) Nhận chứng từ từ email, Zalo hoặc bản giấy. (2) Tải xuống, scan hoặc lưu file. (3) Mở từng chứng từ để đọc. (4) Xác định ngày, số chứng từ, nhà cung cấp, số tiền, thuế và nội dung. (5) Nhập vào Excel/phần mềm kế toán. (6) Kiểm tra lại dữ liệu với chứng từ gốc. |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3–5: Đọc và nhập dữ liệu thủ công. Mất 3–5 phút/chứng từ. Nếu có 150 chứng từ/tháng, tổng thời gian khoảng 7,5–12,5 giờ/tháng, chưa tính kiểm tra và sửa lỗi. |
| Impact (nếu không giải thì sao) | Tốn thời gian, dễ nhập sai số tiền hoặc thông tin chứng từ, dữ liệu cập nhật chậm, ảnh hưởng tiến độ lập báo cáo và độ tin cậy của số liệu. |
| Success metric (baseline → target) | 	Thời gian xử lý/chứng từ: 4 phút → 1 phút. Tỷ lệ trường dữ liệu cần sửa sau nhập: 5% → dưới 1%. |
| Phương án không dùng AI | Chuẩn hóa mẫu Excel, yêu cầu gửi dữ liệu theo form cố định, dùng import CSV hoặc tích hợp xuất dữ liệu từ phần mềm hóa đơn điện tử. |
| Giả thuyết về AI (nếu có) | AI Document Extraction kết hợp OCR để đọc nhiều định dạng hóa đơn/chứng từ, trích xuất các trường cần thiết, sau đó cho kế toán kiểm tra và xác nhận trước khi ghi dữ liệu. |
| Cảm nhận nhanh | Workflow +  AI Agent |

Quy trình nháp hiện tại:

```text
[1 Nhận hóa đơn / chứng từ] → [2 Lưu file hóa đơn / chứng từ] → [3 Đọc và trích xuất thông tin] → [4 Xác định các mục trong hóa đơn] → [5 Nhập vào Excel / phần mềm kế toán] ← BOTTLENECK → [6 Đối chiếu và sửa lỗi]
```

### Problem Card #2

| Trường | Nội dung |
|---|---|
| Job Story | Khi CEO yêu cầu giải thích vì sao một khoản chi phí tăng bất thường so với tháng trước, tôi muốn nhanh chóng tìm được các giao dịch và chứng từ liên quan, để đưa ra lời giải thích chính xác, có bằng chứng mà không phải tra cứu thủ công nhiều nguồn. |
| Actor | Kế toán, CEO |
| Thời điểm / bối cảnh | Khi CEO xem báo cáo tháng hoặc yêu cầu kiểm tra đột xuất một khoản chi. Dữ liệu có thể nằm ở Excel, phần mềm kế toán, hóa đơn, giao dịch ngân hàng và email. |
| Quy trình hiện tại (3–7 bước) | (1) CEO đặt câu hỏi về chi phí. (2) Kế toán xác định khoản mục và kỳ cần so sánh. (3) Mở báo cáo của các kỳ. (4) Lọc giao dịch liên quan. (5) Tìm chứng từ gốc để xác minh nguyên nhân. (6) Tổng hợp lời giải thích, gửi CEO. |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 4–5: Truy tìm giao dịch và chứng từ nằm ở nhiều nguồn. Giả định mất 20–45 phút/câu hỏi, tùy độ phức tạp. |
| Impact (nếu không giải thì sao) | CEO chờ lâu để nhận thông tin, kế toán bị gián đoạn công việc, khó đưa ra quyết định kịp thời; có nguy cơ giải thích không đầy đủ hoặc thiếu bằng chứng. |
| Success metric (baseline → target) | Thời gian trả lời một câu hỏi: 30 phút → dưới 5 phút. Tỷ lệ câu trả lời có thể truy ngược đến chứng từ: 70% → 100%. Baseline cần xác minh. |
| Phương án không dùng AI | Xây dashboard phân tích chi phí theo tháng, bộ lọc theo danh mục/nhà cung cấp, liên kết mỗi giao dịch với chứng từ gốc và báo cáo các biến động vượt ngưỡng. |
| Giả thuyết về AI (nếu có) | AI có thể nhận câu hỏi bằng ngôn ngữ tự nhiên, truy vấn dữ liệu được cấp quyền, tìm giao dịch liên quan và tạo bản giải thích có trích dẫn số liệu, chứng từ. |
| Cảm nhận nhanh | AI Agent |

Quy trình nháp hiện tại:

```text
[1 CEO đặt câu hỏi] → [2 Kế toán xác định thông tin] → [3 Mở báo cáo] → [4 Tìm giao dịch liên quan] → [5 Tìm chứng cứ] ← BOTTLENECK → [6 Tổng hợp thông tin và đưa ra câu trả lời]
```

### Problem Card #3

| Trường | Nội dung |
|---|---|
| Job Story | Khi tiếp nhận nhiều khoản chi có nội dung và cách mô tả khác nhau, tôi muốn xác định đúng danh mục chi phí cho từng giao dịch, để dữ liệu được tổng hợp nhất quán và phản ánh chính xác cơ cấu chi tiêu trong báo cáo. |
| Actor | Kế toán |
| Thời điểm / bối cảnh | Khi ghi nhận chứng từ phát sinh hoặc tổng hợp chi phí cuối tháng. Một nhà cung cấp có thể phát sinh nhiều loại chi phí khác nhau. |
| Quy trình hiện tại (3–7 bước) | (1) Nhận giao dịch đã được nhập liệu. (2) Đọc mô tả/nội dung chi. (3) Kiểm tra chứng từ liên quan. (4) Tra cứu danh mục hoặc tài khoản kế toán hiện có. (5) Chọn nhóm chi phí phù hợp. (6) Hỏi kế toán trưởng nếu không xác định được. (7) Cập nhật dữ liệu phân loại. |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3–6: Xác định nhóm phù hợp khi mô tả mơ hồ hoặc khoản chi có nhiều mục đích. Giả định 1–3 phút/giao dịch; 100 giao dịch cần phân loại có thể tốn 1,7–5 giờ/tháng. |
| Impact (nếu không giải thì sao) | Báo cáo thiếu nhất quán, phân tích chi phí giữa các tháng bị sai lệch, kế toán trưởng mất thời gian sửa danh mục; có thể ảnh hưởng việc hạch toán nếu phân loại sai tài khoản kế toán. |
| Success metric (baseline → target) | Thời gian phân loại/giao dịch: 2 phút → 30 giây. Tỷ lệ phân loại đúng ngay lần đầu: 85% → 95%. Baseline giả định, cần kiểm chứng. |
| Phương án không dùng AI | Xây bảng mapping theo nhà cung cấp, loại dịch vụ, mã hàng; chuẩn hóa danh mục và quy tắc phân loại; tạo danh sách lựa chọn trong Excel hoặc phần mềm kế toán. |
| Giả thuyết về AI (nếu có) | AI đề xuất danh mục dựa trên nội dung hóa đơn, mô tả giao dịch và các lần phân loại đã được kế toán phê duyệt. Trường hợp không chắc chắn sẽ chuyển người phụ trách xử lý. |
| Cảm nhận nhanh | Rule |

Quy trình nháp hiện tại:

```text
[1 Nhận giao dịch] → [2 Đọc mô tả, nội dung] → [3 Kiểm tra tài liệu liên quan] → [4 Tra cứu tài khoản hiện có] → [5 Chọn nhóm chi phí] → [6 Hỏi kế toán trưởng nếu không chọn được] ← BOTTLENECK → [7 Cập nhật dữ liệu]
```

### Card muốn pitch nhất

- Card số: 1
- Vì sao: Pain thực tế, có thể tiết kiệm được thời gian
- Câu hỏi muốn nhóm phản biện: Liệu có cần sử dụng AI hay chỉ cần Workflow?

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|---|---|---|
| Baseline 3-5 phút chỉ là giả định | Đồng ý | Đã kiểm tra khảo sát và sửa lại |
| Bottleneck quá rộng | Không đồng ý | Phương án Agent có thể tiết kiệm thời gian cho cả 3 bước |
| Impact chưa cho thấy độ đau thật sự | Không đồng ý | Các pain liệt ra như "dễ sai sót", "tốn thời gian" là pain mà actor gặp phải |

---

## 4. Tôi đã tham gia phần nào (CP3 → CP7)

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch Problem Card | Card nhập liệu báo cáo tài chính cho kế toán | Được đưa vào short list nhưng không phải lựa chọn cuối của team |
| Phản biện bài của bạn khác | Câu hỏi tôi đã đặt: Nếu sử dụng Agent để sửa merge conflict, làm sao để Agent biết được context của code để sửa cho chính xác với requirement | Team áp dụng multi agents, sử dụng nhiều agent làm các việc khác nhau |
| Nhận phản biện | Câu hỏi tôi nhận được: Hệ thống này liệu đã tồn tại, Agent có thực sự giúp tiết kiệm thời gian | Tôi đã sửa gì: Agent có thể giúp việc scan tài liệu và chuyển hóa sang dữ liệu nhanh hơn nhưng cần người kiểm tra độ chính xác |
| Gom cluster / cây OST | Tổng hợp lại các problem card của các member | Team có cái nhìn tổng quan hơn về các problem card |
| Chọn candidate problem | Vote cho candidate mà tôi thấy thú vị nhất kèm theo lí do | Team lựa chọn candidate mà tôi vote |
| Kiểm chứng / research | Dựa vào kinh nghiệm của tôi và đồng nghiệp đã từng trải nghiệm để đưa ra các pain point chính xác hơn | Team hiểu được pain thực tế từ những người đã trải qua |
| Quy trình nhóm | Làm team leader và hoàn thành group report | Group report được hoàn thành đúng giờ |

---

## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP1 Scan | Gợi ý thêm problem, phản biện lại các problem tôi đã đưa ra | AI gợi ý thêm được các problem mà tôi chưa nhìn ra | AI trả lời chi tiết, không hời hợt nhưng có bịa ra số liệu | Tôi chỉ thêm những problem tôi thấy hợp lý và không thêm số liệu do AI bịa ra |
| CP2 Problem Card | Nhờ AI phản biện card #1 | AI chỉ ra các lỗi tôi còn thiếu | Có một và lỗi AI chỉ ra vì thiếu context | Tôi thêm và sửa những lỗi AI chỉ ra mà tôi thấy hợp lý |
| CP5–6 Problem Statement | AI rà soát lại problem statement | AI đưa ra các nhận xét hữu ích về problem statement của team | AI bắt đầu thêm những ý không cần thiết và rườm rà | Team giữ nguyên problem statement, chỉ sửa cách diễn đạt |

---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5). **Không dùng AI để viết thay.**

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**

Cần phân biệt được đâu là pain point mà cần được giải quyết và impact trên vấn đề đó khi đưa ra phương án giải quyết

**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**

Có, khi đưa ra vấn đề về git merge conflict, có một vài thành viên lâp tức đưa ra giải pháp AI Agent trước khi phân tích vấn đề. Sau khi đi sâu vào và phân tích vấn đề, nhóm nhận ra là phương án đầu là chưa đủ và đã sửa và thêm vào giải pháp cuối.

**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**

Có, khi AI phản biện tôi về thời gian giả định tôi để ban đầu, tôi nhận ra tôi nên kiểm chứng đễ xem đây có phải vấn đề thực tế không thay vì giả định.

**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**

Không quá bất ngờ vì tôi cũng đã gặp phải vấn đề này cũng như thấy vấn đề này trong thực tế

**6.5. Điều khó nhất khi viết Problem Statement là gì?**

Xác định success metric, cần phải đưa ra số liệu cụ thể để có thể đo được độ thành công của giải pháp nhưng không có dự kiện nào để kiểm chứng. Khi làm phần này rất dễ overestimate giải pháp của mình và đưa ra các con số không hợp lý

**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**

Tôi sẽ phản biện nhiều hơn về các bằng chứng mà team đưa ra cho vấn đề của họ, liệu các con số đã được kiểm chứng và các vấn đề họ đưa ra thực sự có phải là vấn đề hay là 1 phần trong quy trình.

**6.7. Hiểu bài:** giải thích bằng 5–8 câu, không nhìn tài liệu, chuỗi *problem → quy trình → metric → boundary → mức can thiệp AI → quyết định* của bài nhóm mình.

Problem: Khi xảy ra merge conflict trong lúc làm việc nhóm, Dev mất thời gian trao đổi để sửa code
Quy trình: Phát hiện conflict → Trao đổi giữa các Dev → Sửa code dựa trên requirement → Build và test lại code → Merge
Metric: Thời gian sửa conflict và số lần phải sửa đi sửa lại
Boundary: AI chỉ đọc các tài liệu được đưa và không thay đổi tài liệu. AI chỉ code trên phần diff, không thêm bớt code không ảnh hưởng trong conflict. Dev review cuối trước khi merge
Mức can thiệp AI: Agent, AI chọn tài liệu đọc, sửa code, build và test
Quyết định: Not Yet, cần kiểm chứng thêm trước khi đưa ra quyết định cuối.

---

## 7. Tài liệu tham khảo

-
