# Báo cáo cá nhân — MSSV_HoTen

> Đổi tên file theo quy tắc `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md` (MSSV trước, dấu `_`, họ tên viết liền không dấu). Sửa cả dòng tiêu đề phía trên cho khớp.
> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: copy template này thành file mới, điền, rồi commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên: Hà Phan Đại Dương
- MSSV: 2A202604119
- Email trường (không bắt buộc, repo có thể để public):
- Tên nhóm: Nhóm 02
- Link repo nhóm:

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
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3–5: Đọc và nhập dữ liệu thủ công. Giả định mất 3–5 phút/chứng từ. Nếu có 150 chứng từ/tháng, tổng thời gian khoảng 7,5–12,5 giờ/tháng, chưa tính kiểm tra và sửa lỗi. |
| Impact (nếu không giải thì sao) | Tốn thời gian, dễ nhập sai số tiền hoặc thông tin chứng từ, dữ liệu cập nhật chậm, ảnh hưởng tiến độ lập báo cáo và độ tin cậy của số liệu. |
| Success metric (baseline → target) | 	Thời gian xử lý/chứng từ: 4 phút → 1 phút. Tỷ lệ trường dữ liệu cần sửa sau nhập: 5% → dưới 1%. |
| Phương án không dùng AI | Chuẩn hóa mẫu Excel, yêu cầu gửi dữ liệu theo form cố định, dùng import CSV hoặc tích hợp xuất dữ liệu từ phần mềm hóa đơn điện tử. |
| Giả thuyết về AI (nếu có) | AI Document Extraction kết hợp OCR để đọc nhiều định dạng hóa đơn/chứng từ, trích xuất các trường cần thiết, sau đó cho kế toán kiểm tra và xác nhận trước khi ghi dữ liệu. |
| Cảm nhận nhanh | Workflow +  AI Agent |

Quy trình nháp hiện tại:

```text

```

### Problem Card #2

| Trường | Nội dung |
|---|---|
| Job Story | Khi …, tôi muốn …, để … |
| Actor | |
| Thời điểm / bối cảnh | |
| Quy trình hiện tại (3–7 bước) | |
| Bottleneck (bước nào, mất bao nhiêu phút) | |
| Impact (nếu không giải thì sao) | |
| Success metric (baseline → target) | |
| Phương án không dùng AI | |
| Giả thuyết về AI (nếu có) | |
| Cảm nhận nhanh | No AI / Rule / Workflow / Agent / Chưa biết |

Quy trình nháp hiện tại:

```text

```

### Problem Card #3

| Trường | Nội dung |
|---|---|
| Job Story | Khi …, tôi muốn …, để … |
| Actor | |
| Thời điểm / bối cảnh | |
| Quy trình hiện tại (3–7 bước) | |
| Bottleneck (bước nào, mất bao nhiêu phút) | |
| Impact (nếu không giải thì sao) | |
| Success metric (baseline → target) | |
| Phương án không dùng AI | |
| Giả thuyết về AI (nếu có) | |
| Cảm nhận nhanh | No AI / Rule / Workflow / Agent / Chưa biết |

Quy trình nháp hiện tại:

```text

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
| Pitch Problem Card | | |
| Phản biện bài của bạn khác | Câu hỏi tôi đã đặt: | |
| Nhận phản biện | Câu hỏi tôi nhận được: | Tôi đã sửa gì: |
| Gom cluster / cây OST | | |
| Chọn candidate problem | | |
| Kiểm chứng / research | | |
| Quy trình nhóm | | |
| Problem Statement | | |
| Mức can thiệp AI | | |
| Quyết định | | |

---

## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP1 Scan | | | | |
| CP2 Problem Card | | | | |
| CP4 Research | | | | |
| CP5 Quy trình | | | | |
| CP5–6 Problem Statement | | | | |
| CP6 Mức can thiệp / quyết định | | | | |

---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5). **Không dùng AI để viết thay.**

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**

**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**

**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**

**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**

**6.5. Điều khó nhất khi viết Problem Statement là gì?**

**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**

**6.7. Hiểu bài:** giải thích bằng 5–8 câu, không nhìn tài liệu, chuỗi *problem → quy trình → metric → boundary → mức can thiệp AI → quyết định* của bài nhóm mình.

---

## 7. Tài liệu tham khảo

-
