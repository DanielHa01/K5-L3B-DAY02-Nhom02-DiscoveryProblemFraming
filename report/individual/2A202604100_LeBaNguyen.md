# Báo cáo cá nhân — 2A202604100_LeBaNguyen

> Đổi tên file theo quy tắc `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md` (MSSV trước, dấu `_`, họ tên viết liền không dấu). Sửa cả dòng tiêu đề phía trên cho khớp.
> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: copy template này thành file mới, điền, rồi commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên: Lê Bá Nguyên
- MSSV: 2A202604100
- Email trường (không bắt buộc, repo có thể để public):
- Tên nhóm: Nhóm 02
- Link repo nhóm:git@github.com:DanielHa01/K5-L3B-DAY02-Nhom02-DiscoveryProblemFraming.git

---

## 2. Scan problem (CP1)

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

|   # | Lăng kính     | Job Story: Khi… tôi muốn… để…                                                                                                                              | Ai chịu ảnh hưởng?                  | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng)         |
| --: | ------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------- | ----------------------------------------------------------------- |
|   1 | Lặp lại       | Khi chốt cuối ngày, tôi muốn thấy tổng tiền COD đã thu hộ theo từng shipper và bưu cục cùng số đơn giao thành công, để biết ai còn nợ trước khi đóng sổ    | Kế toán, trưởng bưu cục, shipper    | Mỗi ngày 60-90 phút gom và đối chiếu bằng tay                     |
|   2 | Tốn thời gian | Khi Shopee gửi bảng kê đối soát phí vận chuyển cuối kỳ, tôi muốn tự so khớp với dữ liệu đơn của công ty, để tìm chênh lệch trước hạn khiếu nại             | Kế toán, kinh doanh, đối tác Shopee | Bảng hàng chục nghìn dòng, 1-2 ngày mỗi kỳ bằng VLOOKUP           |
|   3 | Dễ sai sót    | Khi có đơn hoàn, thất lạc hoặc hư hỏng, tôi muốn thấy ngay đơn đó đã đền bù chưa và ai chịu trách nhiệm, để hạch toán đúng và không bỏ sót khoản truy thu  | Kế toán, vận hành, bưu cục          | Mỗi tháng vài chục đơn thiếu chứng từ hoặc chưa rõ người chịu phí |
|   4 | Lặp lại       | Khi tính thù lao theo đơn cho shipper, tôi muốn có sẵn số đơn giao thành công, thưởng và phạt của từng người, để khỏi gom từ nhiều file và ít bị khiếu nại | Kế toán, shipper, trưởng bưu cục    | Một ngày mỗi kỳ lương, vài khiếu nại mỗi kỳ                       |
|   5 | Tốn thời gian | Khi chốt tháng, tôi muốn có sẵn doanh thu và chi phí theo từng bưu cục hoặc tuyến, để lập báo cáo cho giám đốc đúng hạn                                    | Kế toán, giám đốc, trưởng bưu cục   | 2-3 ngày chốt sổ, nhiều lần sửa số                                |
|   6 |               |                                                                                                                                                            |                                     |                                                                   |
|   7 |               |                                                                                                                                                            |                                     |                                                                   |
|   8 |               |                                                                                                                                                            |                                     |                                                                   |

**Nếu có dùng AI để gợi ý thêm:** ý nào AI gợi ý mà bạn giữ lại, ý nào bỏ và vì sao.

- ***

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3

| Rank | Problem                              | Vì sao chọn                                                                                                                                | Điều còn chưa chắc                                                                                                                |
| ---: | ------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------- |
|    1 | Đối soát COD cuối ngày (#1)          | Làm mỗi ngày, quy trình rõ, tốn thời gian, đo baseline được bằng cách bấm giờ và đếm số chênh lệch; dữ liệu nằm trong hệ thống của công ty | Dữ liệu COD nằm ở mấy nguồn và có xuất được tự động không? “Khớp” nghĩa là chênh lệch bằng 0 hay có dung sai?                     |
|    2 | Đơn hoàn, thất lạc, hư hỏng (#3)     | Thất thoát tiền thật, ảnh hưởng nhiều bên (kế toán, vận hành, bưu cục)                                                                     | Phạm vi rộng, dữ liệu rải rác ở nhiều bộ phận, khó đo baseline; việc xác định ai chịu phí phụ thuộc quy định và thỏa thuận đền bù |
|    3 | Xuất hóa đơn điện tử cho Shopee (#5) | Quy trình rõ, đo được bằng số hóa đơn phải hủy hoặc điều chỉnh mỗi tháng và thời gian sửa                                                  | Lỗi đến từ dữ liệu đối soát hay từ thông tin đối tác (MST, tên công ty)? Có phụ thuộc Shopee xác nhận số liệu trước không?        |

> Các con số ghi "ước tính" là giả định để làm mẫu, cần thay bằng số tự bấm giờ hoặc đếm trong 1-2 tuần gần nhất.

### Problem Card #1

| Trường                                    | Nội dung                                                                                                                                                                                                                                     |
| ----------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Job Story                                 | Khi chốt cuối ngày, tôi muốn thấy tổng tiền COD đã thu hộ theo từng shipper và bưu cục cùng số đơn giao thành công, để biết ai còn nợ trước khi đóng sổ                                                                                      |
| Actor                                     | Kế toán phụ trách thu hộ COD                                                                                                                                                                                                                 |
| Thời điểm / bối cảnh                      | Cuối ngày làm việc, sau khi shipper nộp tiền về bưu cục và trước khi đóng sổ ngày                                                                                                                                                            |
| Quy trình hiện tại (3–7 bước)             | 1. Export đơn giao thành công từ hệ thống vận đơn · 2. Lấy số tiền shipper đã nộp từ bưu cục, sao kê, Zalo · 3. Gom về một file Excel · 4. Đối chiếu từng shipper · 5. Tìm nguyên nhân các dòng lệch · 6. Nhắc shipper nộp thiếu · 7. Ghi sổ |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 5, tìm nguyên nhân dòng lệch: khoảng 30 phút/ngày (ước tính); cả quy trình khoảng 75 phút/ngày (ước tính)                                                                                                                               |
| Impact (nếu không giải thì sao)           | ~27 giờ/tháng cho 1 kế toán (ước tính); khoản lệch kéo sang hôm sau làm công nợ shipper khó theo dõi và có nguy cơ chuyển trễ tiền thu hộ cho Shopee                                                                                         |
| Success metric (baseline → target)        | Thời gian đối soát từ ~75 phút xuống dưới 20 phút mỗi ngày; số khoản lệch chưa giải thích cuối ngày không tăng                                                                                                                               |
| Phương án không dùng AI                   | Công thức hoặc Power Query so khớp tự động + bảng công nợ theo shipper + checklist đóng sổ; giải quyết phần lớn bước 3-4                                                                                                                     |
| Giả thuyết về AI (nếu có)                 | AI không làm phần so khớp số. Chỉ gợi ý nguyên nhân các dòng lệch còn lại (đơn trùng, nộp sau giờ, sai mã đơn) và soạn tin nhắn nhắc shipper; kế toán xác nhận                                                                               |
| Cảm nhận nhanh                            | Rule (phần chính giải bằng công thức; AI chỉ có chỗ ở phần ngoại lệ)                                                                                                                                                                         |

Quy trình nháp hiện tại:

```text
Export đơn giao thành công từ hệ thống vận đơn
-> Lấy số tiền shipper đã nộp (bưu cục báo, sao kê, Zalo)
-> Gom về một file Excel
-> Đối chiếu từng shipper
-> Tìm nguyên nhân các dòng lệch
-> Nhắc shipper nộp thiếu
-> Ghi sổ
```

### Problem Card #2

| Trường                                    | Nội dung                                                                                                                                                                                                                   |
| ----------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Job Story                                 | Khi có đơn hoàn, thất lạc hoặc hư hỏng, tôi muốn thấy ngay đơn đó đã đền bù chưa và ai chịu trách nhiệm, để hạch toán đúng và không bỏ sót khoản truy thu                                                                  |
| Actor                                     | Kế toán xử lý đền bù và công nợ                                                                                                                                                                                            |
| Thời điểm / bối cảnh                      | Khi bưu cục hoặc Shopee báo sự cố, và khi chốt công nợ cuối tháng                                                                                                                                                          |
| Quy trình hiện tại (3–7 bước)             | 1. Nhận thông tin sự cố (Zalo, email, file) · 2. Xin chứng từ từ bưu cục (ảnh, biên bản, hành trình) · 3. Xác định nguyên nhân và ai chịu phí theo quy định · 4. Hạch toán đền bù hoặc truy thu · 5. Theo dõi đến khi xong |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 2 và 3, chờ chứng từ từ nhiều bộ phận và đọc lại hồ sơ để quyết định trách nhiệm: vài chục phút đến vài ngày mỗi vụ (ước tính)                                                                                        |
| Impact (nếu không giải thì sao)           | Mỗi tháng vài chục vụ (ước tính); một số vụ thiếu chứng từ nên bị bỏ sót khoản truy thu hoặc hạch toán sai kỳ                                                                                                              |
| Success metric (baseline → target)        | Thời gian xử lý trung bình mỗi vụ giảm so với baseline đo được; tỉ lệ vụ có đủ chứng từ khi chốt tháng tăng                                                                                                                |
| Phương án không dùng AI                   | Biểu mẫu chuẩn cho bưu cục, bảng theo dõi trạng thái từng vụ, thời hạn phản hồi giữa các bộ phận                                                                                                                           |
| Giả thuyết về AI (nếu có)                 | AI tóm tắt hồ sơ một vụ từ hành trình và ghi chú, gợi ý nguyên nhân và bên chịu phí theo quy định nội bộ; kế toán duyệt trước khi hạch toán                                                                                |
| Cảm nhận nhanh                            | Workflow (AI chỉ hỗ trợ đọc hồ sơ; nút thắt chính là quy trình giữa các bộ phận nên cần đo lại trước khi kết luận)                                                                                                         |

Quy trình nháp hiện tại:

```text
Nhận thông tin sự cố (Zalo, email, file)
-> Xin chứng từ từ bưu cục (ảnh, biên bản, hành trình)
-> Xác định nguyên nhân và ai chịu phí theo quy định
-> Hạch toán đền bù hoặc truy thu
-> Theo dõi đến khi xử lý xong
```

### Problem Card #3

| Trường                                    | Nội dung                                                                                                                                                                                                        |
| ----------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Job Story                                 | Khi cuối tháng xuất hóa đơn điện tử cho Shopee, tôi muốn lấy sẵn dữ liệu đã đối soát, để lập đúng ngay lần đầu và không phải hủy hay điều chỉnh                                                                 |
| Actor                                     | Kế toán lập hóa đơn                                                                                                                                                                                             |
| Thời điểm / bối cảnh                      | Cuối tháng hoặc cuối kỳ đối soát, sau khi hai bên đã chốt số liệu                                                                                                                                               |
| Quy trình hiện tại (3–7 bước)             | 1. Lấy bảng đối soát đã chốt · 2. Nhập hoặc import số liệu vào phần mềm hóa đơn · 3. Kiểm tra thông tin đối tác (MST, tên, địa chỉ) và số tiền · 4. Phát hành · 5. Gửi hóa đơn · 6. Hủy hoặc điều chỉnh nếu sai |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3 và 6, kiểm tra bằng mắt và sửa hóa đơn sai: khoảng nửa ngày/tháng (ước tính)                                                                                                                             |
| Impact (nếu không giải thì sao)           | Vài hóa đơn phải điều chỉnh mỗi tháng (ước tính), mỗi lần tốn thời gian làm việc với bên kia và có thể ảnh hưởng kê khai thuế đúng kỳ                                                                           |
| Success metric (baseline → target)        | Số hóa đơn hủy hoặc điều chỉnh từ vài cái mỗi tháng xuống dưới 1; thời gian lập hóa đơn giảm một nửa                                                                                                            |
| Phương án không dùng AI                   | Quy tắc kiểm tra tự động (định dạng MST, tổng tiền khớp bảng đối soát) + template import hàng loạt vào phần mềm hóa đơn                                                                                         |
| Giả thuyết về AI (nếu có)                 | AI rà dữ liệu trước khi phát hành, đánh dấu dòng bất thường (tên không khớp MST, số tiền lệch) kèm lý do; kế toán duyệt, AI không tự phát hành                                                                  |
| Cảm nhận nhanh                            | Workflow (dữ liệu -> kiểm tra -> kế toán duyệt -> phát hành; quy tắc làm được phần lớn, AI cho bất thường khó viết thành quy tắc)                                                                               |

Quy trình nháp hiện tại:

```text
Lấy bảng đối soát đã chốt
-> Nhập hoặc import số liệu vào phần mềm hóa đơn
-> Kiểm tra thông tin đối tác (MST, tên, địa chỉ) và số tiền
-> Phát hành hóa đơn
-> Gửi hóa đơn cho đối tác
-> Hủy hoặc điều chỉnh nếu phát hiện sai
```

### Card muốn pitch nhất

- Card số: 1 (Đối soát COD cuối ngày)
- Vì sao: Làm mỗi ngày, quy trình rõ, tốn khoảng 75 phút/ngày (ước tính) và đo baseline được bằng cách bấm giờ và đếm số chênh lệch; dữ liệu nằm trong hệ thống của công ty. Phần lớn giải được bằng rule, nên đây là card dễ kiểm chứng và tránh "solution-first" với AI.
- Câu hỏi muốn nhóm phản biện: Dữ liệu COD nằm ở mấy nguồn và có xuất được tự động không? "Khớp" nghĩa là chênh lệch bằng 0 hay có dung sai? Nếu Power Query đã giải được bước 3-4 thì phần ngoại lệ còn lại có đủ lớn để cần AI không?

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra                                                                                           | Đồng ý?         | Đã sửa gì                                                                                                                             |
| ------------------------------------------------------------------------------------------------------------ | --------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| Success metric chỉ có tốc độ (dưới 20 phút), chưa có chất lượng: làm nhanh mà bỏ sót khoản lệch thì vô nghĩa | Đồng ý          | Thêm metric chất lượng: số khoản lệch bị bỏ sót hoặc giải thích sai mỗi tuần không tăng so với baseline                               |
| Có thể công thức hoặc Power Query đã giải quyết phần lớn, giả thuyết về AI chưa cần thiết                    | Đồng ý một phần | Thử công thức trước và đo lại; chỉ giữ AI cho phần ngoại lệ còn lại sau khi đo, ghi vào danh sách giả định cần kiểm chứng             |
| Gợi ý để AI tự nhắn shipper hoặc tự chốt công nợ cho nhanh                                                   | Không đồng ý    | Giữ “kế toán xác nhận trước khi nhắn và trước khi ghi sổ” làm ranh giới, vì sai một khoản là liên quan đến tiền của shipper và Shopee |

---

## 4. Tôi đã tham gia phần nào (CP3 → CP7)

| Hoạt động                  | Tôi đã làm gì?                                                                                                         | Kết quả / ảnh hưởng tới bài nhóm                                                                         |
| -------------------------- | ---------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | --- | --- |
| Pitch Problem Card         | Pitch card "Đối soát COD cuối ngày" (kế toán thu hộ COD, bottleneck ở bước tìm nguyên nhân dòng lệch)                  | Không vào shortlist; nhóm chọn chủ đề multi-agent giải quyết conflict khi làm việc với GitHub trong team |
| Phản biện bài của bạn khác | Câu hỏi tôi đã đặt: "Các agent sẽ đảm nhận vai trò gì trong một flow giải quyết conflict?"                             | Nhóm phải làm rõ vai trò của từng agent trong flow thay vì chỉ nói chung "dùng multi-agent"              |     |
| Chọn candidate problem     | Chấm điểm shortlist, đồng ý chọn chủ đề conflict GitHub                                                                | Card của tôi bị loại; tôi chuyển sang hỗ trợ candidate của nhóm                                          |     |     |
| Mức can thiệp AI           | Tiếp tục câu hỏi về vai trò agent: phần nào trong flow chỉ cần các bước cố định (Workflow), phần nào thật sự cần agent | Góp phần để nhóm cân nhắc mức Workflow trước khi chọn Agent                                              |

---

## 5. Dùng AI

| Checkpoint                     | Tôi dùng AI để làm gì?                                                            | AI hữu ích ở đâu?                                                    | AI sai hoặc hời hợt ở đâu?                        | Tôi sửa gì bằng nhận định của mình?                                               |
| ------------------------------ | --------------------------------------------------------------------------------- | -------------------------------------------------------------------- | ------------------------------------------------- | --------------------------------------------------------------------------------- |
| CP1 Scan                       | Gợi ý thêm problem cho vai trò kế toán công ty vận chuyển                         | Nhắc thêm vài việc lặp lại cuối kỳ                                   | Có ý quá rộng, không có quy trình thật            | Chỉ giữ problem có actor, quy trình và dấu hiệu rõ                                |
| CP2 Problem Card               | Nhờ AI phản biện card #1 (đối soát COD)                                           | Chỉ ra metric chỉ đo tốc độ; nhắc công thức/Power Query có thể đã đủ | Gợi ý để AI tự nhắn shipper, tự chốt công nợ      | Thêm metric chất lượng; giữ ranh giới kế toán xác nhận trước khi nhắn và ghi sổ   |
| CP6 Mức can thiệp / quyết định | Hỏi AI các agent có thể đảm nhận vai trò gì trong flow giải quyết conflict GitHub | Liệt kê nhanh các vai trò có thể có                                  | Đề xuất quá nhiều agent, nhiều vai trò chồng nhau | Rút lại, chỉ giữ vai trò có bước rõ trong flow và cần người duyệt trước khi merge |

---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5). **Không dùng AI để viết thay.**

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**

Khi nghe top 3 của các bạn, tôi thấy problem của các bạn rõ ràng hơn và là những vấn đề thực tế thật sự cần đến AI. Ngược lại, khi nhìn lại card đối soát COD của mình, phần lớn quy trình có thể giải bằng công thức hoặc Power Query, AI chỉ còn chỗ ở phần ngoại lệ. Tôi học được rằng một problem tốt cho bài này không chỉ cần tốn thời gian, mà còn phải có phần việc mà quy tắc cố định khó làm được.

**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**

Lúc đầu nhóm chỉ định dùng 1 agent để giải quyết conflict khi làm việc với GitHub, nhưng thấy vấn đề hơi nhỏ nên quyết định dùng nhiều agent để giải quyết bài toán lớn hơn. Nhìn lại, đây có phần là nghĩ theo giải pháp trước: nhóm chọn số lượng agent trước khi làm rõ từng bước trong quy trình xử lý conflict. Vì vậy tôi đã hỏi các agent sẽ đảm nhận vai trò gì trong flow, để nhóm phải gắn mỗi agent với một bước cụ thể thay vì chỉ nói chung là "dùng multi-agent".

**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**

Có. Card đối soát COD của tôi không vào shortlist, và tôi nghĩ lý do là card chưa đủ sâu. Các con số trong card đều là ước tính, chưa bấm giờ thật, và khi bị phản biện thì chính tôi cũng phải thừa nhận phần chính có thể giải bằng công thức. Sau phản biện, tôi đã thêm metric chất lượng (số khoản lệch bị bỏ sót hoặc giải thích sai không tăng) và giữ ranh giới kế toán xác nhận trước khi nhắn shipper và ghi sổ.

**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**

Điều làm tôi bất ngờ là mình chưa có đủ bằng chứng thật như mình nghĩ. Khi xem lại card của mình, các con số như 75 phút mỗi ngày hay 27 giờ mỗi tháng đều chỉ là ước tính, chưa được kiểm chứng bằng cách bấm giờ hay hỏi người làm kế toán. Tôi nhận ra một problem nghe hợp lý vẫn có thể yếu nếu thiếu dữ liệu thật, và đây cũng là điều nhóm cần kiểm chứng kỹ hơn với bài conflict GitHub.

**6.5. Điều khó nhất khi viết Problem Statement là gì?**

Khó nhất là chỗ xác định quy trình và Success Metric. Với quy trình, khó ở chỗ chia đúng các bước để thấy bottleneck nằm ở đâu, không gộp hai bước làm một. Với metric, lúc đầu tôi chỉ nghĩ tới tốc độ (từ khoảng 75 phút xuống dưới 20 phút), đến khi bị phản biện mới thấy cần thêm metric chất lượng, vì làm nhanh mà sai thì không có ý nghĩa.

**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**

Nếu làm lại, tôi sẽ tìm hiểu kỹ hơn vấn đề để xác định metric, cụ thể là đo baseline thật thay vì để số ước tính. Với bài của nhóm, tôi sẽ phản biện mạnh hơn ở chỗ đo thế nào là giải quyết conflict "thành công" và vì sao cần nhiều agent thay vì một workflow có các bước cố định.

**6.7. Hiểu bài:** giải thích bằng 5–8 câu, không nhìn tài liệu, chuỗi _problem → quy trình → metric → boundary → mức can thiệp AI → quyết định_ của bài nhóm mình.

Problem của nhóm là: khi nhiều thành viên cùng sửa code trên GitHub, lập trình viên gặp merge conflict và phải tự xử lý bằng tay. Quy trình hiện tại gồm pull hoặc rebase, phát hiện conflict, đọc thay đổi của cả hai bên, hỏi người viết code nếu chưa hiểu ý định, sửa, chạy test rồi push để review; bottleneck nằm ở bước hiểu ý định của hai bên thay đổi. Metric là thời gian xử lý một conflict giảm so với baseline nhóm sẽ đo, đồng thời số lỗi phát sinh sau merge không tăng. Boundary là AI không tự merge, không tự push, chỉ đề xuất cách gộp kèm giải thích, và lập trình viên phải duyệt trước khi commit. Về mức can thiệp, tôi cho rằng nên thử Workflow trước (phát hiện conflict bằng rule, AI giải thích và đề xuất, người duyệt), chỉ dùng multi-agent khi chứng minh được có bước không đoán trước được. Quyết định tôi đề xuất là Not Yet: cần đo baseline thời gian xử lý conflict và làm rõ vai trò từng agent trước khi Go.

---

## 7. Tài liệu tham khảo

-
