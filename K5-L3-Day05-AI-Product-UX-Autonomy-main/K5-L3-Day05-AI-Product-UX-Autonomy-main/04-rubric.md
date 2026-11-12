# Rubric — 100 điểm + tối đa 8 điểm bonus

> **Phạm vi & nguyên tắc:** chấm trên bài nộp (`spec.md`, `prototype/`) và phần demo — mỗi con điểm trỏ về một chỗ, phúc khảo được. Rubric chấm **chuỗi quyết định và bằng chứng**, không chấm điền đủ ô, không chấm độ đẹp của prototype. Đây là bài thiết kế, không chạy agent: bằng chứng là lập luận trỏ về một tool, một dòng dữ liệu của track, mục "Sản phẩm thật hôm nay", hoặc một chỗ trên prototype.

## PHẦN 1 — 100 ĐIỂM CHẤM

| Khối | Điểm | Chấm trên |
|---|---|---|
| R1 · Lát cắt & phạm vi | 5 | `spec.md` §1 |
| R2 · Kịch bản rủi ro | 10 | `spec.md` §2 |
| R3 · Khi AI sai | **25** | `spec.md` §3 |
| R4 · Mức tự chủ | **25** | `spec.md` §4 |
| R5 · Prototype | **25** | `spec.md` §5 + `prototype/` + demo |
| R6 · Tốt là gì | 5 | `spec.md` §6 |
| R7 · Demo & phân công | 5 | demo |

**R3 + R4 + R5 = 75 điểm.** Trong mỗi khối, phần lớn điểm là cho **lập luận**: đã cân nhắc gì, chọn gì, vì sao, loại gì và vì sao.

### R1 · Lát cắt & phạm vi — 5

| Điều kiện | Điểm |
|---|---|
| Lát cắt đúng của track, bản prototype không lệch khỏi lát cắt | 2 |
| ≥3 việc không làm, mỗi việc có lý do; bản prototype không vi phạm | 3 |

### R2 · Kịch bản rủi ro — 10

| Điều kiện | Điểm |
|---|---|
| ≥8 kịch bản phủ đủ 4 lớp ①②③④, giống tin người thật, không chung chung | 3 |
| Mỗi kịch bản ghi AI có thể sai thế nào, trỏ về một tool hoặc dòng dữ liệu cụ thể của track (không "AI có thể trả lời sai"), sản phẩm tốt nên làm gì, và nhãn mức hại | 3 |
| Lập luận chọn 2 kịch bản đắt nhất: vì sao đắt hơn, kịch bản nào suýt được chọn và vì sao không | 4 |

### R3 · Khi AI sai — 25

| Điều kiện | Điểm |
|---|---|
| Mỗi kịch bản đắt nhất có câu AI nói nguyên văn, cái người dùng thấy, bước tiếp theo, người được báo | 6 |
| **Lập luận:** chọn hỏi lại / trả lời kèm giới hạn / chuyển người — có phương án đã loại và vì sao | 8 |
| 2–3 nguyên tắc HAX/PAIR, mỗi nguyên tắc trỏ vào chỗ cụ thể (không chỉ ghi tên) | 5 |
| Phân biệt được loại lỗi (hệ thống / người dùng / ngữ cảnh) và cách nói, cách sửa khác nhau theo loại | 3 |
| Chỉ ra một lỗi sửa câu chữ không cứu được và thiết kế cứu nó thế nào | 3 |

### R4 · Mức tự chủ — 25

| Điều kiện | Điểm |
|---|---|
| Mọi tool có một mức của nhóm | 3 |
| **Lập luận theo cost-of-error cho từng tool:** sai thì ai chịu gì · đảo được không · chờ người thì mất gì — không "vì tiện", "vì AI giỏi" | 10 |
| Chỉ ra tool khó xếp nhất (mức nào cũng có giá): các phương án nhóm đã cân nhắc, cái giá của mỗi phía trỏ về kịch bản ở §2, và cách nhóm chốt | 5 |
| Thử mức đã đặt trên 2 kịch bản đắt nhất + 1 bình thường, theo ba câu (cái sai có bị chặn · còn làm khi lẽ ra phải hỏi · người dùng bình thường có phải chờ vô ích) | 4 |
| Nói được một mức tự chủ đã đổi lời hứa nào với người dùng | 3 |

### R5 · Prototype — 25

| Điều kiện | Điểm |
|---|---|
| Bấm qua được ca khó từ đầu tới cuối, không can thiệp tay giữa chừng (bản vẽ tay: 0 ở dòng này, vẫn chấm các dòng dưới) | 5 |
| Thấy được độ chắc hoặc bằng chứng AI dựa vào | 4 |
| Mức tự chủ hiện trên màn hình đúng như §4: tự làm có hoàn tác · cần duyệt có xác nhận · có đường chuyển người · việc cấm không có nút làm | 6 |
| **Mỗi nguyên tắc HAX/PAIR trỏ được vào chỗ cụ thể trong prototype** (ảnh đánh số) | 6 |
| **Lập luận:** cách hiện đã chọn, cách khác đã nghĩ tới và vì sao loại | 4 |

### R6 · Tốt là gì — 5

| Điều kiện | Điểm |
|---|---|
| 3 tiêu chí Pass/Fail chấm được không cần tranh luận | 3 |
| Đã chấm thử thiết kế của nhóm trên 2 kịch bản đắt nhất, ghi lỗi còn lại | 2 |

*Thiếu giờ mà bỏ chặng 6 thì mất tối đa 5 điểm này — đừng cắt chặng 3–5.*

### R7 · Demo & phân công — 5

| Điều kiện | Điểm |
|---|---|
| Ca lạ được xử lý đúng mức tự chủ nhóm đã đặt (nói hoặc bấm được prototype sẽ làm gì) | 3 |
| Mỗi thành viên trình bày một phần và giải thích được phần có tên mình | 2 |

## PHẦN 2 — BONUS, tối đa +8

*Không bắt buộc. Tổng sau khi cộng không quá 100.*

| Điều kiện | Điểm |
|---|---|
| **Xung phong demo trước lớp** trong khối demo 30 phút | +5 |
| Prototype có ≥1 lời gọi AI chạy thật ở quyết định chính (log hoặc ảnh trong `prototype/`), không lộ API key | +3 |

**Hai câu TA, giảng viên hỏi ở demo:**
1. "Chỉ cho tôi chỗ nào trên màn hình là **G__**." Không chỉ được thì không có điểm nguyên tắc đó ở R5.
2. "Hành động này **sai thì ai mất gì**, vì vậy nó ở mức nào?"

**Vibe-coding rule:** thành viên không giải thích được phần có tên mình → phần đó 0 điểm ở R7.

## PHẦN 3 — CHECKLIST XÁC MINH 3 MỐC *(TA đi qua bàn, khoảng 1 phút mỗi nhóm; mốc để giữ nhịp và cứu nhóm kẹt, không tính điểm riêng)*

| Mốc | Khi nào | Nhóm cần show | TA tích Có/Không |
|---|---|---|---|
| **M1 · Kịch bản** | Cuối chặng 2 (phút 45) | ≥8 kịch bản + AI có thể sai thế nào + 2 kịch bản đắt nhất | ☐ phủ 4 lớp ☐ mỗi kịch bản trỏ về tool hoặc dữ liệu ☐ có lý do chọn 2 kịch bản |
| **M2 · Mức tự chủ** | Cuối chặng 4 (phút 125) | Mức của nhóm cho mọi tool + thử trên 3 kịch bản | ☐ lý do theo cost-of-error ☐ chỉ ra tool khó xếp nhất và cách chốt ☐ đã thử mức trên 3 kịch bản |
| **M3 · Bấm được** | Cuối chặng 5 (phút 200) | Prototype bấm qua ca khó | ☐ bấm hết được ☐ thấy ≥2 mức tự chủ ☐ HAX trỏ được vào màn hình |
