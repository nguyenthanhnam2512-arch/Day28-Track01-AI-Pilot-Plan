---
artifact: 8 — 5-slide Pitch + AI Support Log (bản nộp cuối lab)
bai-tap: Pilot Plan — dồn thành pitch, sẵn sàng phản biện
phase: Double Diamond vòng 2 · ◆ output (bản nộp cuối + present)
time: ~5 phút (xem deck để biết khung giờ chính xác trong buổi)
input: 1-pilot-plan.md + toàn bộ 01-frame + 02-solution · templates/5-slide-pitch.md
nop-cuoi: Có — bản nộp cuối lab (Part E · 5-slide Pitch + AI Support Log)
---

# 2 — FINAL: 5-slide Pitch + AI Support Log

Mục tiêu: dồn cả A3 Working Canvas thành 5 slide pitch (5 phút), chuẩn bị trả lời 3 câu phản biện, và ghi AI Support Log. Đây là bản nộp cuối cùng của lab.

Lý do làm bước này: nguyên tắc *demo đơn giản + lập luận chặt > demo đẹp + lập luận yếu*. Slide đẹp mà không trả lời được "số này lấy ở đâu" thì hỏng. Pitch không phải kể chuyện — là đưa evidence để stakeholder ra được một quyết định.

Quy tắc: **slide cuối phải là một lời xin rõ ràng** (xin gì · đổi lại hứa gì). Không có lời xin = stakeholder không biết approve cái gì.

---

## Phần A — 5 slide (mỗi slide 1 thông điệp)

| # | Slide | Lấy từ | Nội dung | Ai nói |
|---|---|---|---|---|
| 1 | Problem & User | 01-frame/3-FINAL | Xem chi tiết bên dưới | Hoàng Kim Trí Thành |
| 2 | Breakdown & Quick Win | 01-frame/1,2 | Xem chi tiết bên dưới | Hoàng Kim Trí Thành |
| 3 | Solution + bản vẽ trực quan | 02-solution/2-FINAL | Xem chi tiết bên dưới | Quách Gia Được |
| 4 | AI Pilot Plan | 03-pilot-plan/1 | Xem chi tiết bên dưới | Nguyễn Thành Nam |
| 5 | Metric · exit criteria · lời xin | 03-pilot-plan/1 | Xem chi tiết bên dưới | Nguyễn Thành Nam |
| Q&A / phản biện | — | — | Người mạnh nhất ứng câu khó | Nguyễn Thành Nam |

---

### Slide 1 — Vấn đề & User

> *Thông điệp: "80 học viên track Product không biết mình yếu chỗ nào — họ đang chuẩn bị cho 6 tuần thực chiến theo kiểu đoán mò."*

```text
Người đau:
  Học viên track Product (~80 người) vừa hoàn thành D28,
  chuẩn bị bước vào 6 tuần thực chiến.

Đau ở đâu trong công việc:
  Ngay sau D28, khi cần quyết định "tôi nên ôn lại phần nào trước khi thực chiến?"
  → Hiện tại: tự đoán, không có dữ liệu cá nhân.

Baseline hiện tại:
  🧮 Giả định: ~70% học viên ôn "đều tất cả" vì không có checklist cá nhân.
  Hậu quả: lãng phí thời gian ôn phần đã biết, bỏ sót phần thật sự yếu.

Vì sao xử lý bây giờ:
  6 tuần thực chiến bắt đầu ngay sau D28 — cửa sổ can thiệp chỉ có 1–2 tuần.
  Bài nộp D28 đang có sẵn: đây là bằng chứng tốt nhất về điểm yếu của từng học viên.
```

---

### Slide 2 — Bóc tách & Quick Win

> *Thông điệp: "Track 1 có 6 module lớn — chúng tôi KHÔNG làm tất cả. Chúng tôi chọn 1 lát cắt nhỏ nhất có thể chạy trong 2 tuần."*

```text
Công cụ lớn Track 1 gồm 6 module:
  1. Chẩn đoán kỹ năng đầu/giữa khóa
  2. Lộ trình riêng theo mục tiêu (PM/founder/engineer)
  3. Gợi ý bài cần xem lại
  4. Theo dõi tiến độ theo concept
  5. Gợi ý peer hỗ trợ
  6. View cho coach: ai cần can thiệp

Quick Win chọn: Module 3 — Gợi ý bài cần xem lại
  → Cụ thể: sau D28, phân tích bài nộp → sinh checklist điểm yếu cá nhân
    + gợi ý 3 tài liệu cần xem lại.

Vì sao chọn trước (chấm 4 trục):
  - Impact: cao — học viên dùng ngay trước thực chiến
  - Feasibility: cao — dữ liệu đã có (bài nộp D28 + rubric)
  - Evidence nhanh: có thể đo trong 1 tuần (coach review + survey học viên)
  - Risk: thấp — formative, có người review, không phải điểm chính thức

Không chọn gì + vì sao:
  Không làm Module 1 (chẩn đoán đầu khóa) — D28 là cuối khóa, quá muộn.
  Không làm Module 5 (peer matching) — cần thêm data hành vi chưa có.
```

---

### Slide 3 — Cách làm & Demo trực quan

> *Thông điệp: "Boost — không tự build từ số 0. Claude API + rubric D28 + coach review = chạy được trong 1 tuần."*

```text
Cách làm: BOOST
  Vì: lộ trình học cá nhân hóa KHÔNG phải lợi thế cạnh tranh cốt lõi của AI20k.
  Rubric D28 đã có sẵn → không cần train model riêng.
  Không Build vì: tốn 2–3 tháng; không Buy vì rubric đặc thù khóa học không có tool ngoài.

[ARTIFACT TRỰC QUAN — User Flow]

  INPUT                   XỬ LÝ                        OUTPUT
  ─────────               ──────────────────────────   ──────────────────────────
  Bài nộp D28     ──→    Claude API                   Checklist điểm yếu
  (học viên)              + Rubric 5 Gate      ──→    (3–5 mục, có dẫn mục rubric)
                          + Danh sách tài liệu         + 3 tài liệu gợi ý
                                                        ↓
                                               [👤 COACH REVIEW]
                                               Pass → Gửi học viên
                                               Fail → Sửa prompt / không gửi

  Chỗ con người review: SAU khi AI tạo checklist, TRƯỚC khi gửi học viên.
  Coach xem ≤5 phút/bài: xác nhận điểm yếu đúng không, tài liệu phù hợp không.
```

---

### Slide 4 — AI Pilot Plan

> *Thông điệp: "2 tuần, 20 học viên, 2 coach, ~$0.36 API — đủ nhỏ để chạy thật, đủ lớn để có evidence."*

```text
Phạm vi + thời lượng + số phase:
  - 20 học viên xung phong (track Product) + 2 coach
  - 2 tuần | 2 phase:
    Phase 1 (tuần 1): test nội bộ trên 5 bài mẫu → cổng: coach chấp nhận ≥4/5
    Phase 2 (tuần 2): chạy thật 20 học viên → cổng: ≥60% thấy checklist đúng

Người:
  - Làm: nhóm Track01 (3 người)
  - Review output: 2 coach track Product (≤5 phút/bài)
  - Quyết định approve/dừng: Lead Coach chương trình AI20k

Dữ liệu + ngân sách thô:
  - Lab dùng: 5 bài mẫu ẩn danh + rubric 5 Gate
  - Pilot thật: bài nộp 20 học viên có consent, xóa sau pilot
  - API: ~$0.36 tổng (≈9.000 VND) 🧮 giả định
  - Thời gian nhóm: 30h volunteer | Coach: ~3h tổng
```

---

### Slide 5 — Chỉ số, Tiêu chí dừng & Lời xin

> *Thông điệp: "Đây là cam kết hai chiều — chúng tôi xin 2 tuần + 3h coach, đổi lại hứa giao bằng chứng rõ ràng, kể cả khi kết luận là NÊN DỪNG."*

```text
Chỉ số chính + baseline + ngưỡng:
  1. % checklist coach chấp nhận    | baseline: 0% | ngưỡng: ≥70%
  2. % học viên thấy checklist đúng | baseline: 0% | ngưỡng: ≥60%
  3. Thời gian coach review/bài     | baseline: N/A | ngưỡng: ≤5 phút

Dừng pilot khi:
  🟡 Cảnh báo: coach chấp nhận 50–70%
     → Dừng gửi thêm, review prompt, thử lại (quyền dừng: Lead Coach + nhóm)
  🔴 Nghiêm trọng: coach chấp nhận <50% HOẶC có checklist gây hiểu sai
     → Dừng ngay, không gia hạn (quyền dừng: Lead Coach — quyết định ngay)

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
LỜI XIN:
  Xin:      2h coach/tuần × 2 tuần (2 coach)
            + ~$0.36 API (hoặc access API nội bộ nếu có)
            + bài nộp D28 ẩn danh của 20 học viên xung phong

  Hứa:     Cuối tuần 2 giao báo cáo gồm:
            - Số liệu thực tế 3 chỉ số trên
            - 3 ví dụ checklist tốt + 3 ví dụ còn lỗi
            - Khuyến nghị: nên mở rộng, sửa thêm, hay dừng hẳn

  Rủi ro:  Thấp — formative, không phải điểm chính thức,
           có người calibrate, dừng được ngay nếu cần
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## Phần B — Chuẩn bị 3 câu phản biện

**1. "Số liệu / giả định này lấy ở đâu?"**
> Con số 70% học viên "ôn đều tất cả" là 🧮 giả định — chưa có khảo sát thật. Chúng tôi dùng nó như giả định có ghi nguồn, không phải fact. Nếu cần, có thể chạy form 5 câu với 20 học viên trong 1 ngày để có số thật trước khi pilot. Con số API $0.36 ước tính từ ~1.500 token/bài — sẽ đo lại thực tế ở phase 1.

**2. "Nếu giả định quan trọng nhất của bạn sai thì sao?"**
> Giả định quan trọng nhất: coach có đủ thời gian review 20 bài trong 1 tuần (~3h tổng). Nếu sai → giảm scope còn 10 bài, ưu tiên học viên có điểm rubric thấp nhất. Giả định thứ hai: bài nộp D28 chứa đủ signal để phát hiện điểm yếu — nếu bài quá ngắn/sơ sài → báo cáo ngay và dừng phase 2, không ép chỉ số.

**3. "Tình huống nào sẽ khiến bạn dừng pilot?"**
> Hai tình huống rõ ràng đã viết trong slide 5: (1) coach chấp nhận <50% checklist — dừng ngay; (2) có bất kỳ checklist nào gây hiểu sai nghiêm trọng (vd: nói học viên yếu sai mục) — dừng ngay không gia hạn. Người có quyền dừng là Lead Coach, không cần họp, quyết định tức thì. Chúng tôi không cần "thêm 1 tuần nữa" nếu chạm mức Nghiêm trọng.

---

## Phần C — AI Support Log

| Câu hỏi | Trả lời |
|---|---|
| AI giúp được gì trong lab này? | AI (Claude) giúp dựng nháp các mục 3–10 của `1-pilot-plan.md` nhanh hơn, đặc biệt phần bảng metric và exit criteria — tiết kiệm ~15 phút so với viết từ đầu. AI cũng gợi ý format user flow cho slide 3. |
| AI đưa output nào nghe hợp lý nhưng nhóm phải sửa? | AI ban đầu đề xuất ngân sách "$5–10/tháng" cho API mà không tách hạng mục — nhóm phải tính lại từ token/bài để ra con số $0.36 thực tế hơn. AI cũng đề xuất exit criteria chỉ có 1 mức, nhóm phải thêm mức Cảnh báo. |
| Phần nào nhóm tự lập luận, KHÔNG copy AI? | Quyết định chọn Module 3 (Gợi ý tài liệu) thay vì Module 1 (Chẩn đoán đầu khóa) — lý do "D28 là cuối khóa, quá muộn để chẩn đoán đầu vào" là lập luận của nhóm, không phải AI. Phần adoption (ai dùng đầu tiên, ai train coach) cũng do nhóm tự điền từ kiến thức về bối cảnh khóa. |

---

## Tổng kiểm tra trước khi nộp

| Hạng mục | Xong? |
|---|---|
| 5 slide, mỗi slide 1 thông điệp, đã phân ai nói slide nào | ✅ |
| Slide 5 có lời xin rõ ràng (xin gì · hứa gì) | ✅ |
| Có câu trả lời sẵn cho cả 3 câu phản biện | ✅ |
| AI Support Log điền đủ 3 dòng | ✅ |
| Tất cả file worksheet/ đã commit + push, link dán vào Discord | ⬜ (làm sau khi pitch) |

Đây là file cuối. Pitch 5 phút + nhận phản biện theo bảng 5 Gate (`templates/rubric-gate-sheet.md`).

*Liên quan: handbook §A9 · `templates/5-slide-pitch.md` · `templates/ai-support-log.md`*
