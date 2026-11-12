# Guide xuyên suốt — 6 chặng trong 240 phút, bám 3 mốc

> **Cách dùng:** Một file, đọc theo thứ tự chặng. Mỗi chặng mở đầu bằng **các câu hỏi nhóm phải tự suy luận và trả lời** — đó là phần quan trọng nhất. Chặng đầu có thêm ví dụ nhỏ để bắt nhịp; càng về sau càng ít gợi ý, để nhóm tự quyết và sáng tạo. Không có bảng bắt buộc phải điền: thứ cần nộp là **bằng chứng và lập luận** cho từng quyết định (xem `03-spec-template.md`).

| Chặng | Phút | Mốc | Mục |
|---|---|---|---|
| 1 · Đọc đề | 10 | | §1 |
| 2 · Lường trước kịch bản | 35 | M1 | §2 |
| 3 · UX khi AI sai | 45 | | §3 |
| 4 · Mức tự chủ | 35 | M2 | §4 |
| Nghỉ | 15 | | |
| 5 · Prototype | 60 | M3 | §5 |
| 6 · Tốt là gì | 10 | | §6 |
| Demo | 30 | | §7 |

**Một quyết định = bốn ý.** Ở mọi chặng, mỗi khi nhóm chọn một thứ (một kịch bản để khoanh, một câu AI nói, một mức tự chủ, một chỗ trên màn hình), ghi lại: **đã cân nhắc những phương án nào · chọn phương án nào · vì sao · loại các phương án kia vì sao**, và **bằng chứng** (tool nào, dòng dữ liệu nào của track, điều gì trong mục "Sản phẩm thật hôm nay", hay chỗ nào trên prototype). Bài này là bài thiết kế: không chạy agent, bằng chứng là lập luận trỏ về một chỗ cụ thể. Đây là phần được chấm điểm nhiều nhất.

**Chia việc (nhóm 3 người).** Nhóm tự chia việc, không bắt buộc theo vai trò cố định. Bài nộp cần danh sách thành viên và mỗi người làm gì. Chặng 1–4 cả nhóm cùng làm thì tốt hơn; từ chặng 5 mỗi người giữ phần mình nhận. Ai cũng phải giải thích được phần có tên mình.

---

# §1 · ĐỌC ĐỀ *(10')*

## 1.1 Các câu hỏi phải tự trả lời

1. Lát cắt của track nói **ai** đang làm **việc gì**, và AI phải ra **quyết định gì**?
2. Hôm nay sản phẩm thật làm việc đó thế nào (mục "Sản phẩm thật hôm nay")? Khi tích hợp AI vào, AI được thêm **quyền làm gì** mà trước đây người dùng tự bấm?
3. Nếu AI sai, **ai chịu, chịu gì**? Sai theo hướng nào đắt hơn?
4. Ba thứ tính năng này sẽ **không** làm là gì?

*Ví dụ (một app giao đồ ăn, không thuộc track nào):* "AI được thêm quyền huỷ đơn thay khách. Huỷ sai thì khách mất bữa, quán mất món đã nấu; huỷ chậm thì tài xế đã chạy. Không làm: đổi món, đổi địa chỉ giao, hoàn tiền."

## 1.2 Đọc bảng tool như người thiết kế

Bảng tool trong track chỉ nói mỗi tool **làm gì** và **đảo lại được không** — chưa ai đặt mức tự chủ. Đọc lướt và tự hỏi:

- Tool nào chỉ **đọc**, tool nào **thay đổi** thứ gì đó (tiền, vé, hồ sơ, tin đã gửi)?
- Tool nào **không đảo lại được**? Đó là chỗ nhóm sẽ phải cẩn thận nhất ở chặng 3–4.
- Có việc nào người dùng sẽ đòi mà **không có tool** nào làm được không? AI nên nói gì khi đó?

**Đủ khi:** cả nhóm nói được lát cắt trong một câu, kiểu sai đắt nhất, và tool nào không đảo lại được.

---

# §2 · LƯỜNG TRƯỚC KỊCH BẢN *(35' → M1)*

## 2.1 Các câu hỏi phải tự trả lời

1. Với lát cắt này, chỗ nào AI **bịa** được (①)? Chỗ nào tin nhắn **mơ hồ, thiếu** (②)? Người dùng sẽ đòi gì **ngoài thẩm quyền** (③)? Sai cái gì thì **mất tiền, mất sức khoẻ, mất niềm tin ngay** (④)?
2. Người dùng thật sẽ nhắn thế nào — viết tắt, đang giận, gộp hai việc, nói thiếu? Kịch bản của bạn có giống người thật không?
3. Với từng kịch bản, một AI làm theo lời người dùng **có thể sai thế nào**? Gọi nhầm tool nào? Làm một việc không đảo được khi lẽ ra phải hỏi? Nói điều dữ liệu không có? Hứa điều không tool nào làm được?
4. Trong các chỗ sai, **hai chỗ nào đắt nhất**, và vì sao đắt hơn các chỗ khác?

## 2.2 Làm thế nào *(scaffold nhẹ)*

- Bắt đầu từ ba tin mồi và mục **Hard tests** của track. Viết **≥8 kịch bản** thẳng vào `spec.md` §2, mỗi lớp ①②③④ ít nhất một. Mỗi kịch bản một dòng: `tin người dùng nhắn | lớp | AI có thể sai thế nào | một sản phẩm tốt nên làm gì | nhãn`.
- Cột **"AI có thể sai thế nào"** là bằng chứng của chặng này: phải trỏ về **một tool hoặc một dòng dữ liệu** của track (hoặc chỗ dữ liệu *không có*). "AI trả lời sai" chưa đủ; "AI gọi `goi_y_san_pham` ngay vì tin nhắn không nói người dùng thuốc là trẻ 2 tuổi" là đủ.
- Gắn nhãn theo **mức hại nếu cái sai đó xảy ra**: **nhẹ** (người dùng tự thấy, tự sửa) / **sửa được** (tốn công, có người gỡ) / **không chấp nhận được** (mất tiền, sức khoẻ, niềm tin, không đảo lại được).
- Đặt tên cho lỗi bằng lời thường: "trấn an người đang bị lừa", "hứa việc mình không làm được", "đoán khi thiếu thông tin".

*Ví dụ một dòng (T2 Giáo dục):* `"cô ơi buổi 4 học gì, có cần chuẩn bị gì không" | ① nguồn sự thật | trang khoá học chỉ có tên buổi 4 "Trực quan hoá dữ liệu", chưa có tài liệu → AI dễ kể luôn "buổi 4 học biểu đồ cột và Tableau" | nói tên buổi 4 từ trang khoá học, nói rõ tài liệu chưa có | sửa được` · lỗi "bịa nội dung buổi chưa học".

**Tự kiểm:** kịch bản nào làm nhóm **sợ nhất** khi demo? Chưa có cái nào đáng sợ = chưa đủ hiểm.

**Đủ khi (M1):** ≥8 kịch bản phủ 4 lớp · mỗi kịch bản ghi AI có thể sai thế nào (trỏ về tool hoặc dữ liệu) và một sản phẩm tốt nên làm gì · 2 kịch bản đắt nhất được khoanh, kèm lý do vì sao đắt hơn các kịch bản còn lại.
**Tốt khi:** có kịch bản mà câu trả lời trông đúng nhưng vẫn rủi ro (đúng vì may, không vì thiết kế — ví dụ đúng chuyến khách cần nhưng đổi vé khi khách chưa xác nhận).

---

# §3 · KHI AI SAI THÌ NGƯỜI DÙNG THẤY GÌ *(45' · phần chính)*

## 3.1 Các câu hỏi phải tự trả lời

Chỉ làm cho **2 kịch bản đắt nhất**.

1. Lúc AI **không chắc**, nó nên làm gì: hỏi lại một câu, trả lời kèm giới hạn, hay dừng và chuyển người? Vì sao không chọn hai cách kia?
2. AI **nói** câu gì, nguyên văn? Câu đó có hứa điều AI không làm được không?
3. Người dùng **thấy** gì ngoài câu chữ: độ chắc, bằng chứng AI dựa vào, nút nào, nhãn nào?
4. Người dùng **làm gì tiếp** được: sửa, bỏ qua, hỏi người, hoàn tác? Nếu họ không làm gì thì chuyện gì xảy ra?
5. **Ai được báo**, sau bao lâu? Người đó thấy gì?
6. Lỗi này là lỗi **hệ thống**, lỗi **người dùng**, hay lỗi **ngữ cảnh** (hệ thống chạy đúng thiết kế nhưng sai với tình huống của người dùng — PAIR gọi là *context error*)? Điều đó đổi cách bạn nói xin lỗi và cách sửa thế nào? Lỗi ngữ cảnh thường phải sửa thiết kế, không chỉ sửa câu chữ.
7. Có lỗi nào mà **sửa câu chữ không cứu được**, chỉ thiết kế mới cứu được (AI nói đã làm việc nó không có quyền; AI dẫn nguồn không có)?

## 3.2 Bốn đường đi của trải nghiệm

Với lát cắt của nhóm, nghĩ đủ bốn đường: **happy path** · **low-confidence** (②) · **failure / không căn cứ** (①) · **correction** (người dùng sửa AI). Hai kịch bản đắt nhất thường rơi vào hai đường cuối.

## 3.3 Nguyên tắc HAX/PAIR — chọn 2–3, mỗi cái trỏ vào chỗ cụ thể

- **G1 — Làm rõ hệ thống làm được gì.** · **G2 — Làm rõ nó làm tốt đến đâu.** (Tại Việt Nam, Điều 11 khoản 1 Luật Trí tuệ nhân tạo 134/2025/QH15 — trách nhiệm minh bạch, hiệu lực 01/3/2026 — yêu cầu hệ thống AI tương tác trực tiếp cho người dùng biết họ đang làm việc với AI; xem [Công báo](https://congbao.chinhphu.vn/van-ban/luat-so-134-2025-qh15-468694.htm).)
- **G10 — Thu hẹp phạm vi khi nghi ngờ.** Không chắc → hỏi lại một câu, hoặc trả lời kèm giới hạn — không làm liều.
- **G8 — Gạt bỏ dễ dàng.** · **G9 — Sửa dễ dàng.** · **G11 — Giải thích vì sao.**
- **G15 — Mời feedback chi tiết** ("sai chỗ nào?").
- **PAIR:** *Explainability + Trust* (tin đúng mức > tin tối đa — hiển thị căn cứ để user tự kiểm) · *Errors + Graceful Failure* (mỗi loại lỗi một đường lui).

Viết như sau: "**G10** → câu AI nói ở kịch bản 1: hỏi lại 'bạn muốn huỷ cả đơn hay chỉ món trà sữa?' thay vì đoán." Ở chặng 5, mỗi nguyên tắc này phải chỉ được vào **một chỗ trên prototype**.

**Đủ khi:** mỗi kịch bản có câu AI nói nguyên văn, cái người dùng thấy, bước tiếp theo, người được báo; mỗi lựa chọn có phương án đã loại và vì sao; 2–3 nguyên tắc trỏ vào chỗ cụ thể; mỗi lỗi được gọi đúng loại (hệ thống / người dùng / cảm nhận) và cách nói, cách sửa theo loại đó.
**Tốt khi:** chỉ ra một lỗi sửa câu chữ không cứu được và thiết kế cứu nó thế nào.

---

# §4 · MỨC TỰ CHỦ *(35' → M2 · phần chính)*

## 4.1 Các câu hỏi phải tự trả lời

1. Với **từng tool**: nếu AI làm sai, **ai chịu gì**? **Đảo lại** được không, mất bao lâu, ai làm?
2. Nếu bắt AI **chờ người duyệt**, trong lúc chờ thì mất gì? Chờ có phải cũng là một kiểu sai không?
3. Tool nào **khó xếp nhất** — mức nào cũng có giá? Kịch bản nào ở chặng 2 cho thấy cái giá của mỗi phía?
4. Đổi một mức tự chủ thì **lời hứa với người dùng** đổi thế nào? (Cùng một model: "AI tự giải quyết cho bạn" khác hẳn "AI soạn sẵn, bạn bấm xác nhận".)

## 4.2 Ba mức, chọn theo cost-of-error

| Mức | Khi nào đúng |
|---|---|
| **tự làm** | Sai thì rẻ, người dùng tự thấy và sửa được, hoặc chờ người còn đắt hơn làm sai |
| **cần người duyệt** (khách hoặc nhân viên bấm xác nhận) | Sai thì đắt hoặc khó đảo, nhưng một bước xác nhận ngắn chặn được |
| **cấm** | Không thuộc thẩm quyền của AI, hoặc sai thì không đảo được mà một bước xác nhận cũng không đủ để chặn |

Lý do viết theo cost-of-error: *sai thì ai chịu gì, sửa đắt hay rẻ* — không viết "vì tiện", không viết "vì AI giỏi".

Trước khi chốt, tự hỏi: với tool cần người duyệt, **ai** duyệt, người đó **thấy gì** trước khi bấm, và nếu **không ai duyệt kịp** thì chuyện gì xảy ra?

## 4.3 Làm thế nào

Mỗi người tự xếp mức cho mọi tool trước, không bàn (5'); rồi cả nhóm so và chốt. Chỗ nào ba người lệch nhau thì đó thường là tool khó xếp nhất — ghi lại ai chọn gì, vì sao, và nhóm chốt thế nào. Muốn thêm một luật (với app giao đồ ăn ở §1: "chỉ huỷ khi khách đã chọn đúng đơn") hoặc tách một tool thành hai bước thì ghi rõ.

Rồi **thử mức vừa đặt** trên **2 kịch bản đắt nhất và 1 kịch bản bình thường**: với mức này, AI sẽ làm gì, người dùng thấy gì? Ba câu: cái sai ở chặng 2 **có bị chặn** không? Có việc nào AI **vẫn làm khi lẽ ra phải hỏi**? Người dùng bình thường có **phải chờ vô ích** không?

**Đủ khi (M2):** mọi tool có một mức và lý do theo cái giá khi sai · chỉ ra tool khó xếp nhất và cách chốt, kèm kịch bản cho thấy cái giá của mỗi phía · đã thử mức của nhóm trên 3 kịch bản theo ba câu trên · nói được một mức tự chủ đã đổi lời hứa nào với người dùng.
**Tốt khi:** nhóm thêm hoặc tách một tool (ví dụ "soạn sẵn" tách khỏi "gửi đi") và chỉ ra kịch bản nào nhờ đó được chặn.

---

# §5 · PROTOTYPE *(60' → M3 · phần chính)*

## 5.1 Các câu hỏi phải tự trả lời

1. Demo 4 phút thì **bấm vào đâu, thấy gì**? Màn hình nào cho thấy rõ nhất thiết kế ở chặng 3–4?
2. Người dùng nhìn vào có biết **AI chắc tới đâu**, và **dựa vào đâu** không?
3. Mỗi mức tự chủ ở chặng 4 **trông thế nào trên màn hình**? Việc AI tự làm thì hoàn tác ở đâu? Việc cần duyệt thì ai bấm, thấy gì trước khi bấm? Việc cấm thì người dùng đi đâu?
4. Mỗi nguyên tắc HAX/PAIR đã chọn nằm **ở chỗ nào** trên màn hình?
5. Khi có ca lạ mà nhóm chưa chuẩn bị, prototype **đi đường nào**?
6. Nhóm đã nghĩ tới cách hiện nào khác, và vì sao không chọn?

## 5.2 Ràng buộc

- **1–2 màn hình**, cho ca khó nhất. Dữ liệu giả, không đăng nhập, không backend. Không cần đẹp.
- Công cụ tuỳ nhóm: Lovable, v0.dev, Figma, một coding agent như Claude, Codex hoặc Gemini, hoặc một file HTML. Đăng ký tài khoản công cụ **trước giờ lab**.
- Có ≥1 lời gọi AI thật thì là bonus; nếu có, chỉ đưa dữ liệu dựng vào và **không để API key trong code nộp**.
- Mẫu của giảng viên: `prototype-sample/index.html` (ca "đổi sang sáng mai" của T3). Xem 3 phút để biết "đủ" trông thế nào, rồi đóng lại. **Nhóm T3 chọn một ca khó khác cho prototype của mình.**
- **Kẹt kỹ thuật quá 20 phút: gọi TA.** Không dựng được thì vẽ tay 2 màn hình rồi chụp lại: mất điểm "bấm qua được", vẫn được chấm các phần còn lại của R5.

**Đủ khi (M3):** bấm qua được ca khó · thấy ít nhất hai mức tự chủ khác nhau trên màn hình · mỗi nguyên tắc trỏ được vào một chỗ.
**Tốt khi:** nhóm tự tìm ra cách thể hiện mà không có trong mẫu.

---

# §6 · TỐT LÀ GÌ *(10' · nhẹ)*

## 6.1 Các câu hỏi phải tự trả lời

1. Ba điều gì, nếu AI làm đúng, thì nhóm dám đưa cho người dùng thật?
2. Một người ngoài nhóm đọc tiêu chí có chấm ra cùng kết quả không?
3. Thiết kế của nhóm (chặng 3–4 và prototype) đạt bao nhiêu tiêu chí trên **2 kịch bản đắt nhất**? Còn lỗi nào chưa sửa được?

Chỉ chấm trên những gì đã có ở chặng 2–5 — không làm thêm. Bộ eval đầy đủ học ở buổi Evaluation.

**Đủ khi:** 3 tiêu chí chấm được đạt / không đạt, đã chấm thử trên 2 kịch bản đắt nhất, ghi lỗi còn lại. Thiếu giờ thì bỏ chặng này.

---

# §7 · DEMO *(30' cuối)*

## 7.1 Các câu hỏi phải tự trả lời

1. Người xem cần thấy gì trong 30 giây đầu để hiểu lát cắt?
2. Ca khó nào cho thấy rõ nhất thiết kế khi sai và mức tự chủ?
3. Ai trong nhóm nói phần nào?

## 7.2 Một khối 30 phút

- Demo là **một khối 30 phút cuối**, không chia vòng cố định. Trong 30 phút đó, nhóm demo **trong zone** (cho TA và các nhóm cùng bàn hoặc cùng zone), hoặc **xung phong demo trước lớp** để được **bonus** (`04-rubric.md`).
- Mỗi lần demo: lát cắt (30") · bấm prototype qua ca khó · một mức tự chủ và cái giá khi sai · **ca lạ** do TA, nhóm bạn hoặc giảng viên đưa — nhóm nói hoặc bấm prototype sẽ làm gì.
- **Mỗi thành viên trình bày một phần.**

**Đủ khi:** người xem bấm hoặc nghe được ca khó, và nhóm trả lời ca lạ theo đúng mức tự chủ đã đặt.

## 7.3 Checklist nộp *(trước 23:59 ngày lab của lớp)*

- [ ] Repo mới, công khai, đặt tên đúng `K5-<lớp>-Day05-<track>-<tên nhóm>` (README → Nộp bài); mở được bằng cửa sổ ẩn danh
- [ ] `spec.md` theo `03-spec-template.md`, bảng thành viên ở đầu, mã học viên đúng
- [ ] `prototype/`: link hoặc file, kèm 1–2 ảnh đánh số các chỗ
- [ ] Cả nhóm trả lời được: "Hành động này sai thì ai mất gì?" · "Lỗi nguy hiểm nhất là gì?" · "Phần bạn làm là gì?"
