---
artifact: 4 — Problem Framing (bản nộp phase Frame)
bai-tap: Frame — đóng khung vấn đề thật
phase: Double Diamond vòng 1 · ◆ output (chốt — owner xác nhận)
time: ~13 phút (xem deck để biết khung giờ chính xác trong buổi)
input: 2-quick-win.md · prompts/03-problem-framing-challenge.md
nop-cuoi: Có — đây là bản nộp của phase Frame (Part A · A3 Working Canvas mục Problem Framing)
---

# 3 — FINAL: Problem Framing

Mục tiêu: đóng khung Quick Win đã chọn cho thật cụ thể. Đây **không phải** bản đề xuất giải pháp — là tài liệu trả lời đúng 1 câu: *"nhóm đã hiểu đúng vấn đề chưa?"*. Đây là output chốt của [Double Diamond](https://www.thefountaininstitute.com/blog/what-is-the-double-diamond-design-process) vòng 1, và là một mục trong A3 Working Canvas nộp cuối buổi.

Lý do làm bước này: một AI Pilot Plan cho vấn đề SAI — dù viết hay — vẫn sai. Đa số nhóm trượt Gate 3 vì khung chung chung ("học viên cần học tốt hơn", "coach quá tải") — câu đó không đo được, không ai chịu trách nhiệm, không biết khi nào thành công.

Quy tắc: **pain phải có số.** "Nhiều người phàn nàn" không phải evidence. "200 câu hỏi/tuần × 20 phút = 67 giờ/tuần" mới là evidence. Trong lab dùng số giả định cũng được, nhưng phải nói rõ số đến từ đâu.

## Quy trình 13 phút

```text
9 phút  — Điền 9 mục Problem Framing
3 phút  — Tự phản biện
1 phút  — Chốt: owner (giả định) có xác nhận đúng vấn đề không
```

---

## 9 mục Problem Framing

### Trả lời

**1. Original Ask** (stakeholder nói gì, nguyên văn):

> "Xây hệ thống cá nhân hóa lộ trình học cho từng học viên dựa trên mục tiêu, level, tiến độ, điểm yếu, hành vi học."
*(Track 1 card — AI20k Learning OS)*

---

**2. Reframed problem** (vấn đề thật sau khi tách):

Học viên track Product (~80 người) vừa hoàn thành D28 nhưng không biết mình **đang yếu ở Gate nào trong rubric 5 Gate**, dẫn đến không thể ôn tập đúng trọng tâm trong 1–2 tuần trước khi bước vào 6 tuần thực chiến.

> Vấn đề không phải là "cần lộ trình dài hạn" (quá lớn). Vấn đề là: ở đúng khoảnh khắc quan trọng nhất — sau D28, trước thực chiến — học viên thiếu một gương phản chiếu cá nhân để biết mình cần làm gì tiếp theo.

---

**3. Current workflow** (hiện tại đang xử lý thế nào):

```text
Học viên nộp bài D28
   ↓
Coach đọc bài thủ công (mỗi bài ~20–30 phút)
   ↓
Coach ghi nhận xét chung (không phân theo Gate cụ thể)
   ↓
Học viên nhận feedback chung, không biết ưu tiên ôn chỗ nào
   ↓
Học viên tự đoán điểm yếu hoặc ôn "đều tất cả"
   ↓
6 tuần thực chiến bắt đầu — không có chuẩn bị cá nhân hóa
```

Hiện tại không có bước nào giúp học viên **biết mình yếu Gate nào cụ thể** và **nên đọc tài liệu gì trước**. Đây là khoảng trống thật sự.

---

**4. Pain evidence — bằng SỐ**:

```text
Quy mô pain:
  🧮 Giả định: ~80 học viên track Product nộp bài D28.
  🧮 Giả định: ~70% (≈56 học viên) không nhận feedback cá nhân theo Gate
     → ôn tập theo kiểu "đoán mò" hoặc "đọc đều tất cả 5 Gate".
  (Nguồn giả định: ước lượng từ tỷ lệ coach/học viên ~1:40 trong AI20k)

Chi phí của pain:
  - Mỗi học viên mất 2–4h ôn tập "sai chỗ" vì không có checklist cá nhân.
  🧮 Giả định: 56 học viên × 3h/người = 168h học không đúng trọng tâm.
  - Coach mất ~20 phút/bài để đọc và ghi nhận xét thủ công.
  🧮 Giả định: 80 bài × 20 phút = 26h coach time.

Khoảnh khắc đau nhất:
  Ngay sau khi nộp bài D28 và chờ đợi feedback — không biết nên làm gì tiếp.
  Cửa sổ này chỉ kéo dài 1–2 tuần trước khi thực chiến bắt đầu.

Lưu ý: tất cả số trên là 🧮 giả định dùng trong lab. Cần khảo sát thật để xác nhận.
```

---

**5. Affected people**:

| Vai | Ai cụ thể | Vì sao họ quan trọng |
|---|---|---|
| Người dùng chính (đau nhất) | Học viên track Product (~80 người) vừa nộp D28 | Họ là người nhận checklist và cần hành động dựa trên đó |
| Người quyết định dùng tool | Coach track Product (2–3 người) | Coach phải review output trước khi gửi → nếu coach không tin, học viên không nhận được gì |
| Người approve/dừng pilot | Lead Coach / Giảng viên chương trình AI20k | Họ có thể dừng pilot nếu output gây hại |
| Người review/expert nội dung | Coach + Instructor (biết rubric sâu nhất) | Cần calibrate: checklist AI có phản ánh đúng rubric không? |

---

**6. Constraints** (từ `00-context.md`):

- **Privacy**: Bài nộp D28 là dữ liệu học viên — cần consent trước khi đưa vào AI. Trong pilot: dùng 5 bài mẫu ẩn danh; pilot thật: học viên xung phong đồng ý.
- **Human review**: Output AI (checklist) là rủi ro cao vì ảnh hưởng trực tiếp đến quyết định học của học viên → coach phải review 100% trước khi gửi. AI không tự gửi.
- **Citation**: Gợi ý tài liệu phải trỏ đúng mục cụ thể trong handbook/LMS, không được viết chung chung.
- **Budget nhỏ**: Ưu tiên Boost (API sẵn có) không Build từ đầu. Chi phí API pilot ước ~$0.36.
- **Formative ≠ summative**: Checklist chỉ là feedback định hướng ôn tập — không phải điểm chính thức, không thay thế đánh giá của coach.
- **Adoption**: Pilot không ép buộc — học viên xung phong đăng ký, coach tình nguyện review. Tool không ai dùng = $0 dù chạy được.

---

**7. Quick Win đã chọn** (1 dòng):

> Phân tích bài nộp D28 của học viên (đối chiếu rubric 5 Gate) → sinh checklist điểm yếu cá nhân (3–5 mục) + gợi ý 3 tài liệu cần xem lại, có coach review trước khi gửi — chạy trong 2 tuần với 20 học viên xung phong track Product.

---

**8. Open questions** (còn chưa biết gì):

- Bài nộp D28 thực tế có đủ "signal" để AI phân biệt điểm yếu cá nhân không — hay đa số bài quá ngắn/giống nhau?
- Coach có sẵn lòng dành 3h/tuần để review checklist không, hay chỉ làm nếu được tính vào KPI công việc?
- Học viên nhận checklist có thực sự đọc và làm theo không — hay chỉ đọc rồi quên? (adoption risk)
- Nếu 2 học viên có bài nộp giống nhau, checklist có khác nhau không? Cách đảm bảo "cá nhân hóa thật" chứ không phải "cá nhân hóa giả"?
- Baseline chính xác cần một khảo sát thật: bao nhiêu % học viên hiện tại biết mình yếu Gate nào?

---

**9. Validation** (đóng vai owner: *"đúng, đây là vấn đề đáng giải"*):

```text
Đóng vai Lead Coach AI20k — xem xét Problem Framing này:

"Đúng — học viên track Product sau D28 đang không có công cụ nào giúp họ
biết cần ôn gì trước thực chiến. Coach cũng không có thời gian viết feedback
chi tiết theo Gate cho từng người trong 1–2 tuần.

Nếu nhóm có thể sinh ra checklist cá nhân theo đúng rubric 5 Gate,
có coach review trước khi gửi, và học viên thấy đúng với bài mình nộp —
đây là vấn đề ĐÁNG GIẢI và ĐÁNG pilot.

Tôi sẵn lòng cung cấp 2 coach tình nguyện review checklist trong 2 tuần
và bộ 5 bài mẫu ẩn danh từ các buổi trước."

→ Validation: CÓ — owner (giả định) xác nhận đây là vấn đề đáng giải.
   Điều kiện: output phải bám đúng rubric 5 Gate, không phải nhận xét chung chung.
```

---

## Tự phản biện

- **Khung này còn câu chung chung không?**
  Không còn "học viên cần học tốt hơn". Đã cụ thể: học viên track Product (~80 người), khoảnh khắc sau D28, pain là không biết mình yếu Gate nào cụ thể.

- **Thử trả lời 1 trong 3 câu phản biện:**
  *"Số/giả định lấy ở đâu?"* → Tất cả số đều đánh dấu 🧮 giả định, ước lượng từ tỷ lệ coach/học viên và kinh nghiệm vận hành khóa. Nếu cần số thật: chạy khảo sát 5 câu với 20 học viên trong 1 ngày trước khi pilot để có baseline thực tế.

---

## Tổng kiểm tra trước khi sang `02-solution/`

| Hạng mục | Xong? |
|---|---|
| Chỉ rõ 1 nhóm người + 1 khoảnh khắc cụ thể (không "user nói chung") | ✅ Học viên track Product, ngay sau D28 |
| Pain có số (hoặc kế hoạch lấy số), nói rõ số từ đâu | ✅ Số giả định đánh dấu 🧮, có kế hoạch khảo sát thật |
| Có baseline (hoặc cách đo baseline) + ≥1 chỉ số có ngưỡng | ✅ Baseline: 0% có checklist cá nhân; ngưỡng: ≥60% học viên thấy đúng |
| Mục 9: owner (giả định) xác nhận đúng vấn đề = qua cổng phase Frame | ✅ Lead Coach xác nhận (giả định) |

⚑ Coach kiểm tra ở Mốc 2: *"Ai đau? Baseline là gì? Không có baseline thì đo thế nào?"*

Owner xác nhận → mở `../02-solution/1-find-existing-solutions.md`.

*Liên quan: handbook §A4 · `prompts/03-problem-framing-challenge.md`*
