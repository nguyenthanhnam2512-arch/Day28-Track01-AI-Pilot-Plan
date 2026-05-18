---
artifact: 5 — Solution Approach + 6 — Demo/Mockup/Flow (bản nộp phase Solution)
bai-tap: Solution — chốt cách làm + cho stakeholder nhìn thấy
phase: Double Diamond vòng 2 · ◆ siết (chốt 1 cách làm + 1 artifact trực quan)
time: ~12 phút (xem deck để biết khung giờ chính xác trong buổi)
input: 1-find-existing-solutions.md · 00-context.md · templates/demo-examples.md · prompts/05-demo-challenge.md
nop-cuoi: Có — bản nộp của phase Solution (Part B + C · A3 mục Solution Approach + Demo/Mockup/Flow)
---

# 2 — FINAL: Solution Approach + Demo/Mockup/Flow

Mục tiêu: chốt cách làm cho Quick Win (Build / Buy / Boost / Partner), nói rõ data & ai review cần có, và tạo 1 bản vẽ trực quan để stakeholder *nhìn* được. Đây là nửa "siết lại" của [Double Diamond](https://www.thefountaininstitute.com/blog/what-is-the-double-diamond-design-process) vòng 2 và là bản nộp của phase Solution.

Lý do làm bước này: hai cái bẫy. Một, "tự build" cho oai — trong khi 80–90% nhu cầu nội bộ chỉ cần Boost/Buy; tự build là quyết định khó rút lại nhất. Hai, chỉ nói bằng chữ — stakeholder không duyệt một đoạn văn, họ duyệt khi *nhìn thấy* flow. Không có bản vẽ → trượt Gate 4 dù lập luận tốt.

Quy tắc: **bản vẽ trực quan là BẮT BUỘC; demo chạy được chỉ là điểm cộng.** *Demo đơn giản + lập luận chặt > demo đẹp + lập luận yếu.*

---

## Phần A — Chốt cách làm

### Decision tree

```text
Bài này có phải LỢI THẾ CẠNH TRANH CỐT LÕI của AI20k không?
 └─ KHÔNG — sinh feedback theo rubric là productivity layer,
             không phải điểm khác biệt mà AI20k cạnh tranh bằng đó.
             → Có tool/API sẵn có giải được không?
                └─ CÓ — Claude API / GPT-4o đủ mạnh để đọc rubric
                         + bài nộp → sinh checklist + gợi ý tài liệu.
                         → BOOST ✅
```

### Ego check

> *"Nhóm chọn cách này vì CẦN hay vì THÍCH tự build?"*
> → Vì CẦN: rubric D28 đã có sẵn và rất cụ thể (5 Gate rõ ràng). Đưa rubric vào system prompt là đủ — không cần train model riêng hay xây vector store. Build từ đầu sẽ tốn 2–3 tháng cho kết quả tương đương.

### Trả lời

- **Cách làm chốt**: **BOOST** — LLM in-context prompting (Claude API hoặc GPT-4o)

- **Lý do CẦN (không phải thích), 2–3 câu**:
  Rubric 5 Gate của D28 đủ cụ thể để làm system prompt mà không cần fine-tune. Danh sách tài liệu khóa học có thể enumerate trong prompt để tránh hallucination. Toàn bộ setup có thể chạy trong 1 tuần với chi phí API ~$0.36 — đúng bối cảnh budget nhỏ và cần evidence nhanh.

- **Vì sao KHÔNG "Build từ số 0"**:
  Fine-tune cần ≥100 cặp bài nộp/feedback calibrate — AI20k chưa có đủ data trong lab. RAG phức tạp hơn cần thiết khi tài liệu có thể enumerate trực tiếp trong prompt (chỉ ~20 tài liệu). Tự build pipeline cũng tốn thêm 4–6 tuần deploy + maintain — vượt xa scope pilot 2 tuần.

- **Tool / API / vendor cần + ước lượng chi phí thô**:

  | Tool | Dùng để làm gì | Chi phí ước lượng |
  |---|---|---|
  | Claude 3.5 Sonnet API (Anthropic) | Sinh checklist + gợi ý tài liệu từ bài nộp + rubric | ~$0.003/1K token; 80 bài × ~1.500 token = ~$0.36 tổng 🧮 |
  | Google Form / Typeform (miễn phí) | Thu feedback học viên sau khi nhận checklist | $0 |
  | Google Sheets | Coach ghi log review (pass/fail + ghi chú) | $0 |
  | Python script đơn giản | Gọi API + format output + batch xử lý 80 bài | Thời gian nhóm, không tốn tiền |

  > Phương án dự phòng: GPT-4o mini nếu Claude không available — chi phí tương đương, chất lượng đủ cho formative feedback.

---

## Phần B — Data & ai review

| Cần gì | Có sẵn trong AI20k? | Trong lab dùng (mẫu/giả định) | Privacy? |
|---|---|---|---|
| Bài nộp D28 của học viên (văn bản) | Có — nằm trên LMS sau deadline | 5 bài mẫu ẩn danh từ buổi trước | Nhạy cảm — cần consent; ẩn danh hóa trước khi đưa vào API; không lưu log |
| Rubric 5 Gate (Gate 1–5, tiêu chí đạt/không đạt) | Có — `templates/rubric-gate-sheet.md` | Dùng nguyên rubric có sẵn | Không nhạy cảm |
| Danh sách tài liệu gợi ý (tên + link/mục) | Có — handbook, LMS, slide skeleton | Enumerate ~20 tài liệu vào prompt | Không nhạy cảm |
| Ví dụ pass/fail mỗi Gate (calibration) | Có một phần — bài mẫu cũ | 2 ví dụ/Gate (1 đạt + 1 chưa đạt) | Ẩn danh hóa |

- **Output nào rủi ro cao**:
  Checklist điểm yếu cá nhân — nếu sai (vd: nói học viên yếu Gate 3 trong khi thực ra họ đạt) → học viên ôn sai chỗ, mất thời gian, mất tin tưởng vào tool. Rủi ro cao hơn nếu học viên tin tuyệt đối mà không tự đọc lại.

- **Ai review + bao nhiêu mẫu + pass/fail theo gì**:
  2 coach track Product review 100% checklist trước khi gửi học viên. Tiêu chí pass/fail: (1) Điểm yếu được liệt kê có khớp với bài thật không? (2) Tài liệu gợi ý có thật và có liên quan không? Coach ghi pass/fail + ghi chú ngắn vào Google Sheets. Thời gian mục tiêu: ≤5 phút/bài.

- **Có cần citation / nói "không biết" khi thiếu nguồn không**:
  Có — bắt buộc. System prompt sẽ yêu cầu model: (1) Chỉ gợi ý tài liệu từ danh sách enumerate; (2) Nếu không tìm thấy tài liệu phù hợp → viết "Không có tài liệu cụ thể — hỏi coach"; (3) Không được tự tạo tên tài liệu hoặc link mới.

---

## Phần C — Bản vẽ trực quan (BẮT BUỘC)

**Dạng dùng**: Kết hợp Dạng 3 (Luồng prompt) + Dạng 5 (Ví dụ vào–ra thật)

### C1 — Luồng prompt (Prompt Flow)

```text
╔══════════════════════════════════════════════════════════════════╗
║                    LUỒNG XỬ LÝ TOÀN BỘ                          ║
╚══════════════════════════════════════════════════════════════════╝

┌─────────────────────────────────┐
│  INPUT (từ LMS + coach)         │
│  ─────────────────────────────  │
│  • Bài nộp D28 của học viên     │
│    (văn bản, ẩn danh hóa)       │
│  • Rubric 5 Gate (Gate 1–5)     │
│  • Danh sách ~20 tài liệu       │
│    (tên + mục cụ thể)           │
└────────────────┬────────────────┘
                 │
                 ▼
┌─────────────────────────────────────────────────────────────────┐
│  SYSTEM PROMPT (cố định, nhóm viết 1 lần)                       │
│  ─────────────────────────────────────────────────────────────  │
│  "Bạn là trợ lý phân tích bài nộp theo rubric AI20k.            │
│   Rubric gồm 5 Gate: [Gate 1 – Breakdown ... Gate 5 – Pilot]    │
│   Tài liệu được phép gợi ý: [Danh sách enumerate]               │
│   Nhiệm vụ: Đọc bài nộp, xác định Gate nào chưa đạt,            │
│   sinh checklist ≤5 điểm + gợi ý ≤3 tài liệu từ danh sách.     │
│   Nếu không có tài liệu phù hợp → ghi 'hỏi coach'.             │
│   KHÔNG tự tạo tài liệu ngoài danh sách."                       │
└────────────────┬────────────────────────────────────────────────┘
                 │
                 ▼
┌─────────────────────────────────┐
│  Claude API / GPT-4o            │
│  xử lý ~1.500 token/bài         │
│  thời gian: ~10–15 giây/bài     │
└────────────────┬────────────────┘
                 │
                 ▼
┌─────────────────────────────────────────────────────────────────┐
│  OUTPUT DRAFT (AI sinh ra)                                       │
│  ─────────────────────────────────────────────────────────────  │
│  Checklist điểm yếu (3–5 mục, kèm Gate tương ứng)              │
│  + 3 tài liệu gợi ý (tên + mục cụ thể từ danh sách)            │
└────────────────┬────────────────────────────────────────────────┘
                 │
                 ▼
╔═════════════════════════════════════════════════════════════════╗
║  👤 COACH REVIEW — ĐIỂM CON NGƯỜI BẮT BUỘC                     ║
║  ─────────────────────────────────────────────────────────────  ║
║  Coach đọc checklist (≤5 phút/bài):                            ║
║  ✅ PASS → Gửi học viên                                         ║
║  ❌ FAIL → Sửa tay hoặc chạy lại với ghi chú bổ sung           ║
║  📝 Ghi log vào Google Sheets: pass/fail + ghi chú ngắn        ║
╚═════════════════════════════════════════════════════════════════╝
                 │
        ┌────────┴─────────┐
        ▼                  ▼
┌──────────────┐   ┌──────────────────────────────┐
│  GỬI HỌC    │   │  KHÔNG GỬI — lưu vào log      │
│  VIÊN qua   │   │  "fail" để cải thiện prompt   │
│  email/LMS  │   └──────────────────────────────┘
└──────┬───────┘
       │
       ▼
┌─────────────────────────────────┐
│  HỌC VIÊN đọc checklist         │
│  → Điền form survey 3 câu        │
│    (checklist có đúng không?)   │
└─────────────────────────────────┘
```

---

### C2 — Ví dụ vào–ra thật (Sample Input/Output)

```text
INPUT (bài nộp D28 mẫu — ẩn danh hóa, rút gọn):
  """
  Quick Win nhóm chọn: AI tự động sinh quiz cho học viên.
  Lý do: nghe có vẻ hay và học viên sẽ thích.
  Solution: build chatbot từ đầu, dùng React + Node.js.
  Budget: "khoảng vài triệu".
  Timeline: "1–2 tháng".
  Dừng khi: "khi không hiệu quả".
  """

OUTPUT DRAFT (AI sinh ra — trước khi coach review):
  """
  📋 CHECKLIST ĐIỂM YẾU CÁ NHÂN

  ❌ Gate 2 — Quick Win: Lý do chọn "nghe có vẻ hay" không bám
     4 trục chấm điểm (Impact · Feasibility · Evidence · Risk).
     → Gợi ý đọc lại: Handbook §A3 "Quick Win Selection" +
       templates/quick-win-scoring.md

  ❌ Gate 4 — Solution: Chọn "Build từ số 0" mà không qua
     decision tree Build/Buy/Boost/Partner.
     → Gợi ý đọc lại: Handbook §A5 "Solution Approach" +
       templates/demo-examples.md (xem ví dụ Boost)

  ❌ Gate 5 — Pilot Plan: Budget "vài triệu" không tách hạng mục;
     exit criteria "khi không hiệu quả" không có ngưỡng đo được,
     không có người có quyền dừng.
     → Gợi ý đọc lại: Handbook §A7 "AI Pilot Plan core" +
       templates/ai-pilot-plan-core.md (mục 6, 9)

  ✅ Gate 1 — Breakdown: Đã tách use case khá rõ.
  ✅ Gate 3 — Problem Framing: Đã có user cụ thể và pain có số.

  📚 3 TÀI LIỆU NÊN ĐỌC TRƯỚC THỰC CHIẾN:
  1. templates/quick-win-scoring.md — Bảng chấm 4 trục
  2. Handbook §A7 — AI Pilot Plan core (12 mục)
  3. templates/ai-pilot-plan-core.md — Ví dụ điền đầy đủ
  """

👤 Coach review: PASS (sau khi sửa nhỏ Gate 3 → học viên này
   thực ra chưa có baseline, coach thêm ghi chú vào mục Gate 3)

Vì sao ví dụ này thuyết phục:
  Rõ ràng Gate nào đạt/không đạt, tài liệu trỏ đúng file có thật,
  không generic, học viên biết chính xác cần đọc gì.

Input nào sẽ làm tool LỘ ĐIỂM YẾU:
  Bài nộp quá ngắn (<200 chữ) hoặc chỉ liệt kê bullet không giải thích
  → AI không đủ signal, checklist sẽ chung chung. Cần báo coach review
  kỹ hơn khi bài dưới ngưỡng độ dài nhất định.
```

**Kiểm qua mắt stakeholder (nhìn 20 giây)**:
- Hiểu user làm gì (nộp bài) → nhận lại gì (checklist + tài liệu) ✅
- Thấy rõ chỗ AI làm vs chỗ người review (hộp coach rõ ràng) ✅
- Không có gì "đẹp nhưng rỗng" — flow đơn giản, thẳng vào vấn đề ✅

**Chỗ con người review (output rủi ro cao) nằm ở**:
> Giữa "Output Draft AI sinh ra" và "Gửi học viên" — Coach review là bắt buộc, không có bước này thì tool không được phép chạy.

---

## Tổng kiểm tra trước khi sang `../03-pilot-plan/`

| Hạng mục | Xong? |
|---|---|
| Cách làm có lý do CẦN, không phải "mặc định tự build" | ✅ BOOST — vì rubric sẵn có, API đủ mạnh, budget nhỏ |
| Nói rõ data cần + ai review output rủi ro cao | ✅ Coach review 100% trước khi gửi |
| Có ≥1 bản vẽ trực quan, người ngoài hiểu trong ~20 giây | ✅ Prompt flow + ví dụ vào–ra thật |
| Có đánh dấu chỗ con người review | ✅ Hộp 👤 COACH REVIEW trong flow |

⚑ Coach kiểm tra ở Mốc 3: *"Stakeholder nhìn vào đâu để hiểu flow? Mockup/sketch/demo đâu?"* Chỉ nói bằng chữ = chưa qua.

Sau bước này, mở `../03-pilot-plan/1-pilot-plan.md`.

*Liên quan: handbook §A5+§A6 · `templates/demo-examples.md` · `prompts/05-demo-challenge.md`*
