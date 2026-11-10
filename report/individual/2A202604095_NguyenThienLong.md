# Báo cáo cá nhân — MSSV_HoTen

> Đổi tên file theo quy tắc `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md` (MSSV trước, dấu `_`, họ tên viết liền không dấu). Sửa cả dòng tiêu đề phía trên cho khớp.
> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: copy template này thành file mới, điền, rồi commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên: Nguyễn Thiên Long
- MSSV: 2A202604095
- Email trường (không bắt buộc, repo có thể để public):
- Tên nhóm: Nhóm 02
- Link repo nhóm: https://github.com/DanielHa01/K5-L3B-DAY02-Nhom02-DiscoveryProblemFraming

---

## 2. Scan problem (CP1)

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

| # | Lăng kính | Job Story: Khi… tôi muốn… để… | Ai chịu ảnh hưởng? | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng) |
|---:|---|---|---|---|
| 1 | Tìm thông tin trong bài giảng | Khi chuẩn bị thi học kỳ mà tài liệu môn học là tập hợp 5–10 file slide PDF hàng trăm trang, tôi muốn đặt câu hỏi bằng văn bản tự nhiên để AI chỉ rõ vị trí thông tin kèm giải thích ngắn, để không phải mò mẫm lật từng slide.| Sinh viên ôn thi cuối kỳ các môn lý thuyết| Mất 20–30 phút mỗi lần lật từng slide để tìm lại một định nghĩa hoặc khái niệm.|
| 2 | Tập luyện tại nhà| Khi muốn tự tập thể dục hoặc tập gym tại nhà mà không có HLV hướng dẫn riêng, tôi muốn chụp ảnh hoặc mô tả dụng cụ có sẵn (tạ đơn, dây kháng lực, ghế) để hệ thống tự động thiết kế lộ trình tập luyện ngắn trong ngày, để không phải mất thời gian tìm kiếm các video bài tập rời rạc trên mạng.| Người tự tập thể dục tại nhà| Mất 15–20 phút mở YouTube tìm bài tập và hay bị nản giữa chừng vì lịch tập không đồng bộ.|
| 3 | Quản lý làm việc nhóm| Khi nhận một đề tài đồ án lớn từ giảng viên kèm theo danh sách các yêu cầu và tài liệu dài dằng dặc, tôi muốn hệ thống tự động bóc tách thành các mốc thời gian (milestones) và danh sách công việc nhỏ theo từng tuần, để nhóm không bị dồn việc vào sát ngày deadline.| Sinh viên làm đồ án tốt nghiệp, bài tập lớn nhóm.| Các thành viên trong nhóm thường xuyên cãi nhau hoặc bối rối vì không biết tuần này phải nộp cái gì, ai chịu trách nhiệm phần nào, không giám sát dc thành viên trong nhóm có làm việc hay không|
| 4 | Tìm thuật ngữ tiếng Anh| Khi đọc các bài báo chuyên ngành tiếng Anh để làm đồ án, tôi muốn dán đoạn văn vào để tự động bóc tách các cụm thuật ngữ quan trọng kèm câu ví dụ thực tế, để không phải vừa đọc vừa dùng Google Translate dịch từng từ rời rạc.| Sinh viên làm đồ án, đọc tài liệu chuyên ngành| Mất hơn 40 phút cho một trang tài liệu tiếng Anh vì ngắt quãng tra từ quá nhiều.|
| 5 | Tìm phòng trọ| Khi tìm phòng trọ mới trên các hội nhóm Facebook, tôi muốn tự động lọc các bài đăng theo tiêu chí (giá tiền, khu vực, có ban công/điều hòa) và loại bỏ bài đăng của môi giới/cò đất, để không mất thời gian nhắn tin hỏi nhầm.| Sinh viên cần chuyển phòng trọ| Tốn hàng giờ lướt feed Facebook và nhắn tin 10 chủ bài thì 8 người là môi giới dẫn dắt.|
| 6 | | | | |
| 7 | | | | |
| 8 | | | | |

**Nếu có dùng AI để gợi ý thêm:** ý nào AI gợi ý mà bạn giữ lại, ý nào bỏ và vì sao.

-

---

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 |Tìm thông tin trong bài giảng PDF (# 1) | Không mất thời gian tìm đúng cị trí nội dung cần, tránh việc Ctrl + F ra nhiều kết quả | AI có trích xuất chính xác vị trí số trang và ngữ cảnh chuẩn xác không, hay bị nói nhảm (hallucination)?|
| 2 |Lọc và bóc tách thuật ngữ chuyên ngành tiếng Anh (#4) | Giúp tăng tốc độ đọc hiểu báo cáo khoa học và tài liệu tham khảo khi làm đồ án tốt nghiệp| AI có phân biệt được thuật ngữ chuyên ngành với từ vựng thông dụng trong ngữ cảnh cụ thể không?|
| 3 | Tự động tìm kiếm và lọc phòng trọ trên Facebook| Giải quyết nhu cầu thiết thực của sinh viên khi đi tìm phòng, giúp lọc sạch các bài đăng môi giới/cò đất ảo.| Các bài đăng trên Facebook có chứa đủ thông tin để AI lọc chính xác tiêu chí giá và tiện ích không?|

### Problem Card #1

| Trường | Nội dung |
|---|---|
| Job Story | Khi chuẩn bị thi học kỳ mà tài liệu môn học là tập hợp 5–10 file slide PDF hàng trăm trang, tôi muốn đặt câu hỏi bằng văn bản tự nhiên để AI chỉ rõ vị trí thông tin kèm giải thích ngắn, để không phải mò mẫm lật từng slide.|
| Actor | Bản thân sinh viên ôn thi cuối kỳ các môn lý thuyết nặng.|
| Thời điểm / bối cảnh | Khi ôn tập chuẩn bị thi cuối kỳ hoặc cần tra cứu lại một khái niệm/công thức cụ thể trong lúc làm bài tập.|
| Quy trình hiện tại (3–7 bước) | 1. Mở file PDF slide môn học trên máy tính. 2. Nhấn Ctrl+F gõ từ khóa. 3. Lật qua lật lại hàng chục trang kết quả. 4. Đọc thủ công từng slide để tìm đoạn giải thích phù hợp. 5. Ghi chú lại vào sổ/file cá nhân.|
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3 & 4 (Lật từng slide và đọc thủ công) — Mất khoảng 20–30 phút cho mỗi lần tra cứu một định nghĩa hoặc khái niệm phức tạp.|
| Impact (nếu không giải thì sao) | Tốn nhiều thời gian, làm gián đoạn luồng tư duy ôn tập, dễ gây nản lòng và quá tải trước khối lượng tài liệu lớn.|
| Success metric (baseline → target) | Giảm thời gian tra cứu từ 20–30 phút xuống dưới 3 phút cho mỗi câu hỏi.|
| Phương án không dùng AI | Dùng tính năng tìm kiếm Ctrl+F của ứng dụng đọc PDF: Chỉ tìm được đúng từ khóa chính xác, không trả lời được các câu hỏi mang tính tổng hợp hoặc giải thích ý nghĩa.|
| Giả thuyết về AI (nếu có) | AI đọc nội dung file PDF slide, nhận diện câu hỏi bằng ngôn ngữ tự nhiên và trả lời chính xác thông tin kèm trích dẫn số trang cụ thể.|
| Cảm nhận nhanh | Workflow  |

Quy trình nháp hiện tại:

```text
1. Mở file PDF slide môn học trên máy tính. 2. Nhấn Ctrl+F gõ từ khóa. 3. Lật qua lật lại hàng chục trang kết quả. 4. Đọc thủ công từng slide để tìm đoạn giải thích phù hợp. 5. Ghi chú lại vào sổ/file cá nhân.
```

### Problem Card #2

| Trường | Nội dung |
|---|---|
| Job Story |  Khi đọc các bài báo khoa học hoặc tài liệu kỹ thuật tiếng Anh dài để làm đồ án, tôi muốn dán đoạn văn vào hệ thống để tự động bóc tách các cụm thuật ngữ chuyên ngành kèm câu ví dụ thực tế, để không phải vừa đọc vừa dùng Google Translate dịch từng từ rời rạc.|
| Actor | Sinh viên cần tham khảo tài liệu nước ngoài|
| Thời điểm / bối cảnh | Trong quá trình thu thập tài liệu và viết báo cáo đồ án tốt nghiệp|
| Quy trình hiện tại (3–7 bước) | 1. Mở file PDF bài báo tiếng Anh. 2. Copy đoạn văn không hiểu sang Google Translate. 3. Đọc bản dịch thô đôi khi không chuẩn ngữ cảnh kỹ thuật. 4. Mở thêm từ điển chuyên ngành để tra lại từng từ. 5. Tự tổng hợp lại vào file ghi chú.|
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 2, 3 & 4 (Vừa đọc vừa tra từ điển rời rạc) — Mất hơn 40 phút cho mỗi trang tài liệu tiếng Anh vì bị ngắt quãng liên tục.|
| Impact (nếu không giải thì sao) | Tốc độ đọc tài liệu rất chậm, dễ nản chí, làm chậm tiến độ hoàn thành chương tổng quan tài liệu của đồ án.|
| Success metric (baseline → target) | Giảm thời gian xử lý và hiểu một trang tài liệu từ 40 phút xuống dưới 10 phút.|
| Phương án không dùng AI | Dùng Google Translate hoặc từ điển Anh-Việt thông thường: Phải tra từng từ một, không hiểu được nghĩa theo đúng ngữ cảnh chuyên ngành kỹ thuật.|
| Giả thuyết về AI (nếu có) | AI hiểu ngữ cảnh kỹ thuật, lọc ra đúng các cụm thuật ngữ khó và giải thích ngắn gọn, dễ hiểu bằng tiếng Việt.|
| Cảm nhận nhanh |  Workflow  |

Quy trình nháp hiện tại:

```text
1. Mở file PDF bài báo tiếng Anh. 2. Copy đoạn văn không hiểu sang Google Translate. 3. Đọc bản dịch thô đôi khi không chuẩn ngữ cảnh kỹ thuật. 4. Mở thêm từ điển chuyên ngành để tra lại từng từ. 5. Tự tổng hợp lại vào file ghi chú.
```

### Problem Card #3

| Trường | Nội dung |
|---|---|
| Job Story | Khi tìm phòng trọ mới trên các hội nhóm Facebook, tôi muốn tự động lọc các bài đăng theo tiêu chí cụ thể (giá tiền, khu vực, có ban công/điều hòa) và loại bỏ bài đăng của môi giới/cò đất, để không mất thời gian nhắn tin hỏi nhầm.|
| Actor | Người có nhu cầu chuyển trọ, tìm trọ|
| Thời điểm / bối cảnh | Trước thời điểm bắt đầu học kỳ mới hoặc khi cần đổi chỗ ở.|
| Quy trình hiện tại (3–7 bước) | 1. Lướt feed các hội nhóm cho thuê phòng trọ trên Facebook. 2. Đọc lướt từng bài viết để xem giá và địa chỉ. 3. Nhắn tin hỏi chủ bài xem còn phòng trống không hoặc giá chuẩn là bao nhiêu. 4. Phát hiện ra bài đăng cũ hoặc do môi giới đăng ảo câu khách.|
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 2, 3 & 4 (Lướt tìm và nhắn nhầm môi giới) — Tốn hàng giờ đồng hồ lướt mạng xã hội mỗi ngày nhưng tỷ lệ tìm được phòng thực tế rất thấp.|
| Impact (nếu không giải thì sao) | Mất rất nhiều thời gian vô ích, dễ bị lừa đảo hoặc gặp thông tin giá ảo, gây ức chế tâm lý.|
| Success metric (baseline → target) | Tiết kiệm thời gian tìm kiếm từ 2 giờ/ngày xuống dưới 20 phút bằng danh sách lọc sẵn.|
| Phương án không dùng AI | Dùng thanh tìm kiếm từ khóa trên Facebook: Kết quả trả về thường lẫn lộn nhiều bài cũ, bài trùng lặp và quảng cáo của môi giới.|
| Giả thuyết về AI (nếu có) | AI đọc nội dung các bài đăng trong group, tự động trích xuất đúng mức giá, diện tích, vị trí và gắn nhãn cảnh báo bài của môi giới.|
| Cảm nhận nhanh | Workflow  |

Quy trình nháp hiện tại:

```text
1. Lướt feed các hội nhóm cho thuê phòng trọ trên Facebook. 2. Đọc lướt từng bài viết để xem giá và địa chỉ. 3. Nhắn tin hỏi chủ bài xem còn phòng trống không hoặc giá chuẩn là bao nhiêu. 4. Phát hiện ra bài đăng cũ hoặc do môi giới đăng ảo câu khách.
```

### Card muốn pitch nhất

- Card số: Card #2 (Lọc và bóc tách thuật ngữ chuyên ngành tiếng Anh khi đọc tài liệu làm đồ án)
- Vì sao: Đỡ mất nhiều thời gian khi vừa phải tìm cụm từ và dịch nó sang tiếng anh và tìm thêm 1 công đoạn nữa thì mới hiểu dc cách dùng từ đấy trong đúng ngũ cảnh, đỡ bị dùng sai 
- Câu hỏi muốn nhóm phản biện:

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|---|---|---|
| Tài liệu chuyên ngành kỹ thuật thường có các công thức toán học và ký hiệu đặc biệt mà AI dễ dịch nhầm.| Đồng ý| Xác định rõ phạm vi (boundary): Chỉ tập trung bóc tách các cụm danh từ, thuật ngữ chuyên ngành kỹ thuật ở dạng đoạn văn bản thuần túy, không xử lý các công thức phức tạp trong ảnh.|
| Đề xuất mở rộng thành một hệ thống dịch toàn bộ toàn văn bài báo khoa học dài 50 trang sang tiếng Việt.| Không đồng ý| Giữ nguyên ranh giới cốt lõi: "AI chỉ đóng vai trò bóc tách nhanh các cụm thuật ngữ cốt lõi và giải thích theo ngữ cảnh, sinh viên vẫn giữ quyền kiểm soát việc đọc hiểu toàn văn."|
---

## 4. Tôi đã tham gia phần nào (CP3 → CP7)

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch Problem Card | Trình bày 3 problem cards cá nhân tập trung vào vấn đề tra cứu, đặc biệt nhấn mạnh Card #2 (bóc tách thuật ngữ chuyên ngành tiếng Anh).| Cung cấp cho nhóm góc nhìn về các nỗi đau liên quan đến việc xử lý thông tin phi cấu trúc và khó khăn về rào cản ngôn ngữ.|
| Phản biện bài của bạn khác | Câu hỏi tôi đã đặt: Bài toán Git merge conflict có thực sự là pain lớn không khi các IDE như VSCode hiện nay đã hỗ trợ giao diện merge rất trực quan?| Giúp tác giả (bạn Tuấn) làm rõ và khoanh vùng lại rằng: IDE chỉ hỗ trợ UI, còn bottleneck thực sự nằm ở việc "đọc hiểu logic" của nhánh code lạ.|
| Nhận phản biện | Câu hỏi tôi nhận được: "Nguồn dữ liệu có đủ cấu trúc để lọc không?", "Tiêu chí để đánh giá AI làm đúng hay sai đối với bài toán lọc thông tin là gì?"| Tôi đã sửa gì: Nhận ra giới hạn về nguồn dữ liệu và độ khó trong việc đo lường (success metric) của bài toán cá nhân, từ đó đồng ý hạ độ ưu tiên của các candidate này.|
| Gom cluster / cây OST | Cùng nhóm nhóm các ý tưởng lại. Các ý tưởng của tôi được xếp vào Cluster C (Tra cứu và yêu cầu).| Giúp nhóm nhận diện pattern chung của cụm ý tưởng là "tìm, lọc thông tin không đồng nhất" để dễ dàng so sánh và đánh giá với các cụm khác.|
| Chọn candidate problem | Tham gia chấm điểm các candidate theo 7 tiêu chí. Thống nhất loại Cluster C của mình để ủng hộ ý tưởng "Git merge conflict" của Nguyễn Văn Tuấn.| Nhóm chốt được 1 Candidate Problem duy nhất có tính khả thi cao, có Actor, Workflow và Bottleneck rõ ràng để đi tiếp.|
| Kiểm chứng / research | Tìm hiểu về quy trình resolve conflict hiện tại của các developer và giới hạn của các công cụ No-AI (merge thủ công).| Củng cố bằng chứng và dữ liệu cho thấy việc đọc hiểu code lạ khi conflict gây mất rất nhiều thời gian, làm gián đoạn flow làm việc.|
| Quy trình nhóm | Đóng góp vào việc phác thảo Current Workflow từ lúc bị conflict đến lúc merge xong.| Giúp nhóm chốt được vị trí chính xác của Bottleneck là bước "đọc hiểu ý đồ logic của đoạn code bị conflict".|
| Problem Statement | Hỗ trợ tinh chỉnh lại câu chữ cho phát biểu vấn đề cuối cùng, đảm bảo đủ các thành phần (Job Story, Actor, Impact).| Hoàn thiện Problem Statement rõ ràng, súc tích, phản ánh đúng trọng tâm vấn đề đưa vào báo cáo.|
| Mức can thiệp AI | Thảo luận và đề xuất AI chỉ nên đóng vai trò phân tích, giải thích logic và gợi ý cách gộp (Human-in-the-loop), không tự động merge.| Giúp nhóm định hình giải pháp 3 Agent an toàn, tránh rủi ro hỏng build hoặc sai logic nghiệp vụ của dự án.|
| Quyết định | Bỏ phiếu tán thành và thống nhất 100% với hướng đi cuối cùng của nhóm.| Nhóm đạt được sự đồng thuận tuyệt đối để kết thúc giai đoạn Discovery và sẵn sàng cho các bước tiếp theo.|

---

## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP1 Scan | Prompt AI gợi ý thêm các nỗi đau (pain points) dựa trên lăng kính "Tốn thời gian".| Gợi ý được nhiều bối cảnh đa dạng mà sinh viên thường gặp (tìm tài liệu, ôn thi).| Đưa ra một số ý tưởng quá vĩ mô hoặc không có thật (ví dụ: AI tự động đi thi hộ, học hộ).| Bỏ qua các ý tưởng phi thực tế, chỉ chọn lọc và tinh chỉnh các pain thật như tìm phòng trọ, lọc thuật ngữ tiếng Anh.|
| CP2 Problem Card | Nhờ AI đóng vai "Kẻ phản biện khó tính" để tìm lỗ hổng trong ý tưởng lọc thuật ngữ chuyên ngành.| Chỉ ra được điểm yếu chí mạng là AI dễ dịch sai ngữ cảnh nếu gặp công thức toán học hoặc ký hiệu lạ.| AI gợi ý giải pháp đao to búa lớn là xây dựng cả một hệ thống dịch toàn bộ văn bản dài 50 trang.| Không theo giải pháp của AI, tự giới hạn lại biên giới (boundary) là chỉ bóc tách các cụm từ tĩnh.|
| CP4 Research | Nhờ AI tóm tắt các tính năng xử lý merge conflict của các IDE hiện hành (VSCode, GitLens).| Liệt kê đầy đủ và nhanh chóng các công cụ No-AI đang có trên thị trường.| AI chỉ liệt kê tính năng UI (hiển thị 3-way merge) mà không phân tích được nguyên nhân cốt lõi gây tốn thời gian.| Tự nhận định lại rằng: Tool UI tốt nhưng bottleneck thực sự nằm ở việc con người phải "đọc hiểu logic code lạ".|
| CP5 Quy trình | Yêu cầu AI vẽ nháp Current Workflow cho một lập trình viên khi gặp Git merge conflict.| Phân chia các bước cơ bản khá logic từ lúc pull code đến lúc commit.| Các bước quá chung chung, không làm nổi bật được bước nào là bước thắt cổ chai (bottleneck) tốn thời gian nhất.| Gộp các thao tác gõ lệnh lại, tách riêng bước "Đọc hiểu ý đồ của nhánh code kia" làm Bottleneck chính.|
| CP5–6 Problem Statement | Gọt giũa lại câu chữ cho Job Story để đảm bảo đúng format "Khi... tôi muốn... để...".| Giúp câu văn mượt mà, súc tích và đúng cấu trúc.|AI làm mất đi các con số định lượng về Impact (thời gian, tỷ lệ lỗi) mà nhóm đã chốt. | Thêm lại các từ khóa về mức độ nghiêm trọng và số liệu ước lượng rủi ro hỏng build vào phát biểu vấn đề.|
| CP6 Mức can thiệp / quyết định |Hỏi AI về các mức độ can thiệp phù hợp (Automation vs Human-in-the-loop) cho bài toán code. | Đề xuất được mô hình Agent đóng vai trò như một người review code độc lập.|AI khuyên nên cho hệ thống tự động gộp (Auto-merge) 100% để tối ưu thời gian tuyệt đối. | Bác bỏ việc Auto-merge vì quá rủi ro cho logic nghiệp vụ. Chốt lại AI chỉ phân tích và đề xuất, Dev là người quyết định.|

---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5). **Không dùng AI để viết thay.**

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**
Nghe bài nhóm khác mới thấy ý tưởng của mình hơi khó đo lường. Ý tưởng lọc phòng trọ của mình thực tế phết, nhưng không biết lấy data đâu để đánh giá. Bài Git Conflict của Tuấn thì rõ ràng hơn hẳn, lỗi phát là hỏng build, đo lường được ngay.
**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**
Có chứ. Lúc bàn vụ tìm phòng trọ, cả bọn toàn nhảy vào cãi nhau xem cào data Facebook kiểu gì, dùng model NLP nào. Xong ngớ người ra là còn chưa chốt được user kẹt ở khâu lướt tin hay đi xem phòng. Thế là phải phanh gấp, quay lại vạch cái luồng các bước ra trước.
**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**
Mình bỏ luôn ý tưởng bóc thuật ngữ tiếng Anh. Lúc bảo vệ thì hăng lắm, nhưng bị hỏi "tiêu chí nào đánh giá AI giải thích đúng ngữ cảnh" thì chịu. Tính chủ quan cao quá, khó làm nên mình nhượng bộ luôn.
**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**
Lúc research khá bất ngờ là mấy tool xịn như VSCode hay GitLens thực ra chỉ giải quyết được cái phần giao diện (chia màn hình cho dễ nhìn). Còn cái lõi tốn thời gian nhất là "đọc hiểu logic code lạ của người khác" thì chả có tool nào làm hộ cả.
**6.5. Điều khó nhất khi viết Problem Statement là gì?**
Khó nhất là không bị lậm giải pháp vào câu chữ. Mình quen tay toàn viết kiểu "tôi muốn dùng AI đọc code", trong khi đúng ra phải viết mong muốn cốt lõi là "tôi muốn hiểu nhanh ý đồ đoạn code này".
**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**
Nếu làm lại, mình sẽ cãi gắt hơn ở đoạn cấp ngữ cảnh cho AI. Code liên quan đến cả project, nếu ném mỗi cái file bị conflict vào bắt AI hiểu thì dễ ảo giác và gợi ý sai logic ngay.
**6.7. Hiểu bài:** giải thích bằng 5–8 câu, không nhìn tài liệu, chuỗi *problem → quy trình → metric → boundary → mức can thiệp AI → quyết định* của bài nhóm mình.
Bài toán xuất phát từ việc dev tốn quá nhiều thời gian dò ý đồ code của nhau khi bị merge conflict. Phân tích quy trình thì thấy kẹt nhất ở khâu đoán logic nhánh code lạ. Mục tiêu là giảm thời gian xử lý và giảm lỗi hỏng build, với giới hạn là chỉ phân tích file text chứ không tự động chạy test. Vì rủi ro hỏng hệ thống cao nên mức can thiệp bắt buộc là Human-in-the-loop (AI phân tích, người chốt cuối). Quyết định cuối cùng là thiết kế 3 Agent review chéo để tư vấn dev gộp code an toàn nhất.
---

## 7. Tài liệu tham khảo
Báo cáo nhóm Nhóm 02: K5-L3B-DAY02-Nhom02-DiscoveryProblemFraming.

Tài liệu hướng dẫn Resolve Merge Conflict của Git và VSCode Documentation.

Các trao đổi trong phiên họp nhóm (CP3 - CP7).
-
