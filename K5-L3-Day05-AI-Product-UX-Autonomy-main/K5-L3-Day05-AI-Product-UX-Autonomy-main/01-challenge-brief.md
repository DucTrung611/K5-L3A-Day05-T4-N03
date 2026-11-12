# Đề bài — "Tích hợp AI vào một sản phẩm thật": 5 track, một khung chung

**Bối cảnh.** Mỗi track là một sản phẩm thật ở Việt Nam mà nhiều người đang dùng. Hôm nay sản phẩm đó chưa có AI, hoặc có AI làm rất ít. Nhóm bạn là product team được giao **tích hợp AI vào một tính năng**, và phải trả lời hai câu khó nhất của sản phẩm AI: **khi AI sai thì người dùng thấy gì**, và **AI được tự làm tới đâu**.

## Chọn 1 trong 5 track

Mỗi track mô tả theo **cùng một khung mục** (sản phẩm nền · sản phẩm thật hôm nay · người dùng · bối cảnh · bài toán gốc · lát cắt · data & fixture · deliverable · demo bắt buộc · hard tests · rubric riêng · bonus · an toàn & đạo đức) để nhóm so sánh và chọn.

| Track | Sản phẩm nền (tham khảo) | Người dùng | Cái giá khi sai | File |
|---|---|---|---|---|
| **T1 · Y tế** | Kênh chat "Hỏi dược sĩ" của Pharmacity | Khách hỏi thuốc cho mình hoặc người nhà; dược sĩ trực | Hại sức khoẻ một người, thường không đảo được | `tracks/t1-healthcare.md` |
| **T2 · Giáo dục** | ChatGPT Study mode, tích hợp vào trang khoá học | Học viên hỏi bài tối muộn; TA | Rẻ mỗi lần nhưng âm thầm: học sai mà không biết | `tracks/t2-education.md` |
| **T3 · Du lịch** | Đổi lịch, hoàn vé trong Traveloka; chính sách hãng bay | Hành khách vừa bị huỷ chuyến; nhân viên hỗ trợ | Mất vé, mất lần đổi miễn phí, yêu cầu hoàn không rút lại được | `tracks/t3-travel.md` |
| **T4 · Thương mại điện tử** | "Trò chuyện với Shopee" — khiếu nại không đúng mô tả | Người mua; người bán; nhân viên sàn | Sai hướng nào cũng có một bên mất tiền | `tracks/t4-ecommerce.md` |
| **T5 · Ví điện tử** | "Chat với MoMo" — giao dịch bị tạm chặn | Người dùng ví đang lo; tư vấn viên | Tiền đi trong vài giây, không lấy lại được | `tracks/t5-ewallet.md` |

Mọi track chấm chung `04-rubric.md`; rubric riêng trong từng track chỉ để biết một sản phẩm tốt trong domain đó nên làm gì.

## Sản phẩm thật chỉ để tham khảo

Mỗi track có mục **"Sản phẩm thật hôm nay"**: luồng sản phẩm đang chạy, tóm tắt từ trang trợ giúp công khai, có link. Đọc để hiểu bối cảnh thật. **Không** chat với sản phẩm thật, không đăng nhập, không tạo đơn hay giao dịch: nhiều luồng chạy theo menu và bắt chọn một đơn hoặc giao dịch thật, nên không thử được, và không nên thử.

## Data cấp cho mọi nhóm

Không có dữ liệu thật. Mỗi track cấp: **4–5 việc AI có thể làm (tool)** — mỗi tool ghi làm gì và đảo lại được không, **chưa có mức tự chủ** (nhóm tự đặt ở chặng 4) · **ba tin mồi** để bắt đầu viết kịch bản. T2 và T3 có thêm dữ liệu dựng (tài liệu buổi học; một đặt chỗ) để làm bối cảnh cho kịch bản.

**Đây là bài thiết kế, không chạy agent.** Bằng chứng của nhóm là **lập luận trỏ về một chỗ cụ thể**: tool nào, dòng dữ liệu nào của track, điều gì trong mục "Sản phẩm thật hôm nay", chỗ nào trên prototype. "AI có thể trả lời sai" không phải bằng chứng; "AI có thể gọi `doi_chuyen_bay` khi khách chỉ nói 'sáng mai', trong khi sáng mai có hai chuyến" là bằng chứng.

## Lát cắt = MỘT CÂU

> **một người dùng · một công việc · một quyết định AI · một kết quả**

Lát cắt đã **phát sẵn** trong từng track. Nhóm không chọn lại; nhóm thiết kế cho nó.

## Ràng buộc chung

1. Build **prototype 1–2 màn hình** bấm được (Lovable, v0.dev, Figma, một coding agent như Claude, Codex hoặc Gemini, HTML — tuỳ nhóm) cho ca khó nhất. Có **≥1 lời gọi AI chạy thật** là bonus, không bắt buộc.
2. Tự xác định **4 lớp chỗ khó** cho lát cắt của mình:
   - ① **Nguồn sự thật** — chỗ nào AI bịa được? Không có căn cứ thì làm gì?
   - ② **Mơ hồ / thiếu thông tin** — input không đủ chắc: hỏi lại, đoán có báo, hay từ chối?
   - ③ **Ngoài phạm vi / thẩm quyền** — user đòi thứ không được phép làm, từ chối sao cho vẫn hữu ích?
   - ④ **Đặc thù domain** — sai cái gì thì user mất tiền, mất sức khoẻ, mất niềm tin ngay?
3. Chỉ dùng dữ liệu dựng trong track hoặc dữ liệu giả tự sinh — không dữ liệu thật của người thật.

## Tiêu chí nghiệm thu bài lab

| # | Tiêu chí | Đạt khi |
|---|---|---|
| 1 | Kịch bản rủi ro | ≥8 kịch bản phủ đủ 4 lớp, mỗi kịch bản ghi AI có thể sai thế nào (suy ra từ tool hoặc dữ liệu cụ thể của track) và một sản phẩm tốt nên làm gì; 2 kịch bản đắt nhất được khoanh kèm lý do. "AI có thể trả lời sai" = không đạt |
| 2 | Khi AI sai | Với 2 kịch bản đắt nhất: câu AI nói nguyên văn, cái người dùng thấy, bước người dùng làm tiếp, ai được báo. Mỗi lựa chọn có phương án đã loại và vì sao |
| 3 | Mức tự chủ | Mọi tool có một mức (tự làm / cần người duyệt / cấm) và lý do theo cái giá khi sai; chỉ ra tool khó xếp nhất và cách chốt; thử mức đã đặt trên 2 kịch bản đắt nhất + 1 kịch bản bình thường |
| 4 | Prototype | Bấm qua được ca khó; thấy được độ chắc hoặc bằng chứng, và điều khiển mức tự chủ (hoàn tác, duyệt, chuyển người); **mỗi nguyên tắc HAX/PAIR trỏ được vào một chỗ cụ thể trên prototype** |
| 5 | Tốt là gì *(nhẹ)* | 3 tiêu chí Pass/Fail chấm được, đã chấm thử thiết kế của nhóm trên 2 kịch bản đắt nhất |
