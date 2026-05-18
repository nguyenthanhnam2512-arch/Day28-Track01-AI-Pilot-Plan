---
artifact: 5 — Solution Approach (phần khám phá)
bai-tap: Solution — tìm lời giải đã có sẵn trước khi tự xây
phase: Double Diamond vòng 2 · ◇ giãn (mở hết lựa chọn, chưa chốt)
time: ~8 phút (xem deck để biết khung giờ chính xác trong buổi)
input: 01-frame/3-FINAL-problem-framing.md · 00-context.md · prompts/04-find-solutions.md
nop-cuoi: Không — file trung gian (bản chốt ở 2-FINAL-solution.md)
---

# 1 — Find existing solutions (đừng xây lại từ số 0)

Mục tiêu: trước khi quyết Build / Buy / Boost / Partner, nhóm phải biết bài này đã có ai giải ở chỗ khác chưa, và họ giải bằng cách nào. Đây là nửa "giãn ra" của [Double Diamond](https://www.thefountaininstitute.com/blog/what-is-the-double-diamond-design-process) vòng 2 — mở hết các lời giải đang tồn tại, chưa chốt cái nào.

Lý do làm bước này: đây là chỗ nhiều nhóm hỏng mà không biết. Hỏng vì nhảy thẳng vào "tự build" cho oai, trong khi 80–90% nhu cầu nội bộ chỉ cần Boost hoặc Buy. Hỏng vì không hỏi "ai làm rồi" nên đi lại từ số 0. Gần như bài nào cũng đã có người giải ở một ngành khác — không thấy thì phí cả pilot.

Quy tắc: **không có nguồn = giả định.** Mỗi cái AI/web nói ra, hỏi lại "lấy ở đâu?". Không chỉ được nguồn thì đánh dấu 🧮 (giả định để giảng), đừng xài như fact.

---

## Bước 0 — Bài này thực ra là dạng bài gì?

- **Quick Win của nhóm, viết lại thành 1 dạng bài chung (không có chữ domain)**:
  > "Văn bản tự do (bài nộp) + bộ tiêu chí đánh giá (rubric) → feedback cá nhân hóa gồm: danh sách điểm yếu theo tiêu chí + tài liệu gợi ý tương ứng"
  
  Đây là dạng bài **Rubric-based Formative Feedback Generation** — đã có ở giáo dục, y tế, tuyển dụng, pháp lý.

- **Input → Output thực chất là gì**:
  - Input: Bài nộp dạng văn bản (500–2.000 chữ) + Rubric 5 tiêu chí (Gate 1–5) + Danh sách tài liệu có sẵn
  - Output: Checklist 3–5 điểm yếu (có trích dẫn mục rubric tương ứng) + 3 tài liệu gợi ý (có link/tên cụ thể)

- **Ràng buộc không bỏ được (từ `00-context.md`)**:
  1. Human review bắt buộc trước khi gửi học viên
  2. Citation bắt buộc — gợi ý tài liệu phải có nguồn thật
  3. Budget nhỏ — không build model riêng
  4. Formative only — không phải điểm chính thức

---

## Phần A — Deep research: ai giải dạng bài này rồi, giải sao?

| Tầng | Hỏi AI/web câu gì | Tìm được gì | Nguồn / 🧮 |
|---|---|---|---|
| **1 · Map** | "Rubric-based automated feedback generation — các hướng tiếp cận phổ biến là gì? Khi nào dùng cái nào?" | **5 hướng chính:** (A) Template matching — điền rubric vào template cố định; (B) LLM in-context prompting — đưa rubric vào system prompt, bài nộp vào user prompt; (C) RAG (Retrieval-Augmented Generation) — tìm tài liệu liên quan rồi kết hợp với LLM; (D) Fine-tuned model — train model riêng trên tập dữ liệu bài nộp + feedback cũ; (E) Hybrid (LLM + rule-based validation) — LLM sinh draft, rule kiểm tra logic. | 🧮 Tổng hợp từ survey EdTech AI (2023–2025); thiếu nguồn cụ thể → đánh dấu giả định |
| **2 · Tiền lệ** | "Nền tảng giáo dục nào đã dùng AI để sinh feedback theo rubric ở quy mô nhỏ (<500 người)? Họ dùng cách nào?" | **Gradescope** (UC Berkeley, 2024): dùng LLM in-context để group câu trả lời tương tự, giáo viên review và approve batch — giảm 70% thời gian chấm. **Turnitin Feedback Studio**: rubric-based comment generation, giáo viên enable/disable từng comment. **Khan Academy Khanmigo**: GPT-4 + rubric môn học in system prompt → hint cá nhân hóa. **EduFlow (startup)** 🧮: RAG trên tài liệu khóa học + rubric → gợi ý tài liệu xem lại. | Gradescope: [gradescope.com/research](https://gradescope.com) 🧮 chi tiết 70% không xác minh được; Turnitin: [turnitin.com](https://turnitin.com); Khanmigo: [khanacademy.org/khan-labs](https://www.khanacademy.org/khan-labs) |
| **3 · Phản chứng** | "Ca nào dùng AI sinh feedback theo rubric thất bại? Nguyên nhân gốc là gì?" | **Thất bại 1 — Feedback generic**: AI đưa nhận xét chung "cần cải thiện lập luận" thay vì trỏ đúng rubric item → học sinh không biết cần làm gì cụ thể. Gốc rễ: rubric đưa vào prompt quá mơ hồ, không có ví dụ pass/fail. **Thất bại 2 — Hallucination**: AI "bịa" tài liệu không tồn tại hoặc trích dẫn sai trang → mất trust hoàn toàn. Gốc rễ: không có bước verify citation. **Thất bại 3 — Low adoption**: giáo viên nhận feedback AI nhưng không review vì "không tin" → học sinh nhận feedback sai. Gốc rễ: không có training + onboarding cho người review. | 🧮 Tổng hợp từ case study EdTech AI failure (MIT Teaching Lab 2024, Stanford HAI 2023) — không xác minh được số cụ thể |
| **4 · Thu hẹp** | "Với ràng buộc: budget <$5 pilot, cần human review, cần citation thật, chạy trong 2 tuần — hướng nào khả thi nhất cho feedback theo rubric?" | **Hướng khả thi nhất: LLM in-context prompting (hướng B)**: Rubric 5 Gate của D28 đủ cụ thể để làm system prompt. Không cần fine-tune, không cần RAG phức tạp. Claude API hoặc OpenAI API chạy ngay. Citation được giải quyết bằng cách đưa danh sách tài liệu vào context và yêu cầu model chỉ trích dẫn từ danh sách đó — nếu không có thì nói "không biết". Human review giải quyết hallucination. | 🧮 Đánh giá của nhóm dựa trên so sánh 4 hướng vs ràng buộc — chưa có benchmark thực tế |

---

## Phần B — Rút về 2–3 hướng khả thi

| Hướng giải khả thi | Ai làm rồi (gần bài mình nhất) | Nguồn / 🧮 | Hợp ràng buộc `00-context`? |
|---|---|---|---|
| **A — LLM in-context (Boost)**: Rubric D28 làm system prompt + bài nộp làm user input → Claude API sinh checklist + gợi ý tài liệu từ danh sách có sẵn | Gradescope (batch grouping), Khanmigo (hint generation), Turnitin (comment generation) | Gradescope: xác minh được; Khanmigo: xác minh được; chi tiết 🧮 | **Có** — budget thấp ($0.36 pilot), human review được, citation controllable |
| **B — RAG + LLM**: Vector store tài liệu khóa → retrieve relevant chunks → LLM tổng hợp feedback có nguồn | EduFlow 🧮, nhiều RAG chatbot EdTech | 🧮 không xác minh được | Có nhưng **phức tạp hơn cần thiết** — pilot 2 tuần không đủ thời gian setup vector store |
| **C — Fine-tuned model**: Train trên bài nộp cũ + feedback coach của AI20k | Gradescope (partial) | 🧮 | **Không** — cần ít nhất 100+ cặp bài nộp/feedback để train; AI20k không có đủ data trong lab |

**"Đi từ 5 lên" — nhóm kế thừa cụ thể cái gì**:

```text
Kế thừa từ Gradescope: pattern "LLM group + human approve" — không để AI tự gửi,
luôn có người review và approve trước. Áp dụng: checklist AI sinh → coach review
→ coach approve → gửi học viên.

Kế thừa từ Khanmigo: rubric in system prompt với ví dụ pass/fail cụ thể mỗi Gate
→ tăng độ chính xác. Áp dụng: system prompt của nhóm sẽ có rubric 5 Gate kèm
ví dụ "bài đạt Gate 3 trông như thế nào".

Tránh từ ca thất bại: luôn constrain tài liệu gợi ý trong danh sách pre-approved
→ không để model tự bịa link/tên tài liệu.
```

---

## Phát hiện ban đầu

- **Hướng B (LLM in-context) vừa đủ** cho Quick Win này — không cần RAG hay fine-tune. Đây là trường hợp điển hình "Boost, không Build".
- **Hallucination trong citation là rủi ro lớn nhất** — giải pháp: constrain model chỉ được chọn từ danh sách tài liệu có sẵn (enumerate trong prompt), không tự sáng tạo.
- **Human review là điểm mấu chốt** không phải để hoàn hảo mà để giữ trust — coach review nhanh (≤5 phút) là yếu tố quyết định adoption.

## Câu hỏi mở (mang sang bước chốt)

- Danh sách tài liệu D28 có sẵn dưới dạng có thể enumerate trong prompt không (tên + link)?
- Claude vs GPT-4o — cái nào cho kết quả tốt hơn với rubric-based feedback? Cần test thực tế.
- System prompt tối ưu cần bao nhiêu ví dụ "pass/fail" mỗi Gate? 1 ví dụ hay 2–3?

---

## Tổng kiểm tra trước khi sang `2-FINAL-solution.md`

| Hạng mục | Xong? |
|---|---|
| Gọi được dạng bài trong 1 câu, không còn chữ domain | ✅ Rubric-based Formative Feedback Generation |
| Đủ 4 tầng deep research, tầng nào cũng có kết quả | ✅ |
| Mỗi kết quả có nguồn, hoặc đánh dấu 🧮 nếu là giả định | ✅ |
| Rút về 2–3 hướng + nói được "đi từ 5 lên" cái gì | ✅ 3 hướng; kế thừa Gradescope + Khanmigo pattern |

Sau bước này, mở `2-FINAL-solution.md` — chốt Build/Buy/Boost/Partner + data & ai review + bản vẽ trực quan.

*Liên quan: handbook §A5 · `prompts/04-find-solutions.md` · `00-context.md`*
