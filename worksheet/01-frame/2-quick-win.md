---
artifact: 3 — Quick Win Selection
bai-tap: Frame — chọn lát cắt làm trước
phase: Double Diamond vòng 1 · ◆ siết (hội tụ về 1 lựa chọn)
time: ~10 phút (xem deck để biết khung giờ chính xác trong buổi)
input: 1-intake-breakdown.md · prompts/02-quick-win-challenge.md
nop-cuoi: Không — file trung gian (bản chốt phase này ở 3-FINAL-problem-framing.md)
---

# 2 — Quick Win: chọn lát cắt làm trước

Mục tiêu: từ 5–8 use case ở file `1`, chấm điểm nhanh và chốt **1 Quick Win** để pilot đầu tiên — kèm lý do chọn và lý do *không* chọn các phần khác. Đây là nửa "siết lại" của [Double Diamond](https://www.thefountaininstitute.com/blog/what-is-the-double-diamond-design-process) vòng 1.

Lý do làm bước này: đây là quyết định quan trọng nhất của phase Frame. Quick Win **không phải** phần dễ nhất hay nghe hay nhất — là phần *chứng minh được giá trị nhanh và có người ủng hộ*. Chọn sai → pilot fail → mất uy tín → khó xin pilot tiếp. Nhóm phải chọn được *và bảo vệ được bằng lý do*, không bằng cảm tính.

Quy tắc: **điểm số chỉ là gợi ý, không phải đáp án.** Đừng để con số quyết thay nhóm — nó chỉ giúp so sánh.

## Bước 0 — Lấy 4–6 use case mạnh nhất từ file `1` (1 phút)

Lấy UC1, UC2, UC3, UC6 (4 ứng viên có potential cao nhất) — UC4 và UC5 phụ thuộc UC3 nên loại ngay ở vòng này.

## Quy trình 10 phút

```text
1 phút  — Bước 0: chọn 4–6 ứng viên
5 phút  — Phần A: chấm điểm 4 trục
3 phút  — Phần B: 1 lý do nên / 1 lý do không cho top 2
1 phút  — Phần C: chốt + ai ủng hộ + cái KHÔNG chọn
```

---

## Phần A — Chấm điểm 4 trục (1–5 mỗi trục)

> Thang điểm: Impact × 0.30 + Feasibility × 0.25 + Evidence × 0.25 + Risk an toàn × 0.20

| Use case | Impact (×.30) | Feasibility (×.25) | Evidence nhanh (×.25) | Risk an toàn (×.20) | Tổng | Hạng |
|---|:---:|:---:|:---:|:---:|:---:|:---:|
| UC1 — Chẩn đoán kỹ năng đầu khóa → sinh báo cáo level + track phù hợp | 4 | 2 | 2 | 3 | 2.85 | 4 |
| UC2 — Sinh lộ trình học cá nhân theo mục tiêu nghề nghiệp | 5 | 2 | 1 | 2 | 2.65 | — |
| **UC3 — Phân tích bài nộp D28 → checklist điểm yếu + 3 tài liệu gợi ý** | **4** | **5** | **5** | **4** | **4.45** | **1** |
| UC6 — View coach: ai cần can thiệp sau D28 | 4 | 3 | 3 | 3 | 3.30 | 2 |

**Giải thích điểm quan trọng:**
- UC3 Feasibility = 5: rubric 5 Gate + bài nộp D28 + danh sách tài liệu đều sẵn có ngay, không cần build thêm infrastructure.
- UC3 Evidence nhanh = 5: coach review checklist trong tuần 1 → biết ngay chất lượng; học viên survey 3 câu → biết kết quả trong 1 tuần.
- UC2 Evidence nhanh = 1: lộ trình cá nhân hóa cần đo sau nhiều tuần mới biết có "học tốt hơn" không — không fit pilot ngắn.
- UC6 Feasibility = 3: cần tổng hợp dữ liệu từ nhiều nguồn, coach workflow chưa rõ → phức tạp hơn UC3.

---

## Phần B — 1 lý do nên / 1 lý do không, cho top 2

**Ứng viên A — UC3: Phân tích bài nộp D28 → checklist điểm yếu + 3 tài liệu gợi ý**

```text
Nên chọn vì:
  Đây là khoảnh khắc đau nhất và có data sẵn nhất: học viên vừa nộp D28,
  bài nộp đang nằm trên hệ thống, rubric 5 Gate rõ ràng, danh sách tài liệu có sẵn.
  Không cần xây thêm gì — chỉ cần prompt + Claude API + coach review là chạy được trong 1 tuần.
  Kết quả đo được ngay: coach xem checklist trong 5 phút và biết đúng/sai.

Không nên vì:
  Nếu bài nộp D28 quá ngắn hoặc sơ sài (học viên viết vội), AI không đủ signal
  để phát hiện điểm yếu thật — checklist sẽ generic, không cá nhân hóa được.
  Rủi ro: tool chạy được nhưng output không có giá trị thật.
```

**Ứng viên B — UC6: View coach — ai cần can thiệp sau D28**

```text
Nên chọn vì:
  Coach là người quyết định can thiệp học viên nào — nếu AI tổng hợp được
  danh sách "10 học viên cần gặp ngay", coach tiết kiệm rất nhiều thời gian đọc bài.
  Impact trực tiếp đến chất lượng coaching toàn track.

Không nên vì:
  UC6 phụ thuộc vào dữ liệu đã được xử lý từ UC3 (checklist điểm yếu từng học viên).
  Nếu làm UC6 trước UC3, coach chỉ nhận thông báo chung chung, không đủ chi tiết để hành động.
  UC6 cũng cần xây thêm aggregation layer — phức tạp hơn nhiều so với UC3.
```

---

## Phần C — Chốt Quick Win

- **Quick Win nhóm chọn**: **UC3 — Phân tích bài nộp D28 → checklist điểm yếu cá nhân + gợi ý 3 tài liệu cần xem lại trước 6 tuần thực chiến**

- **Vì sao chọn cái này trước**:
  UC3 đạt điểm cao nhất (4.45/5) nhờ tổ hợp feasibility cao (data sẵn) + evidence nhanh (biết kết quả trong 1 tuần) + risk thấp (formative, không phải điểm chính thức). Quan trọng hơn: cửa sổ can thiệp chỉ có 1–2 tuần ngay sau D28 — nếu không làm bây giờ, học viên bước vào 6 tuần thực chiến mà không biết mình yếu chỗ nào. UC3 là use case duy nhất vừa có dữ liệu sẵn, vừa có thể đo kết quả ngay, vừa có thể dừng an toàn nếu không work.

- **Ai trong AI20k sẽ ủng hộ pilot này**:
  - **Coach track Product**: được giảm thời gian đọc bài thủ công — checklist AI làm bản nháp, coach chỉ cần xác nhận.
  - **Học viên xung phong**: muốn biết mình yếu chỗ nào trước khi thực chiến — đây là pain họ tự nhận ra.
  - **Lead program**: ít rủi ro (formative, không phải điểm chính thức), chi phí thấp (~$0.36 API), có thể mở rộng sang track khác nếu thành công.

- **Nhóm KHÔNG chọn gì + vì sao**:
  1. **UC2 (lộ trình cá nhân theo mục tiêu)** — cần đo kết quả sau nhiều tuần học, không phù hợp pilot 2 tuần; cũng cần dữ liệu hành vi học nhiều hơn chỉ 1 bài nộp.
  2. **UC1 (chẩn đoán đầu khóa)** — D28 là cuối khóa, quá muộn để làm chẩn đoán đầu vào; logic không phù hợp với thời điểm hiện tại.
  3. **UC6 (view coach)** — phụ thuộc UC3; làm UC3 trước là bước đúng để UC6 có data chạy được sau.

---

## Phát hiện ban đầu

- UC3 là "hinge point" — thành công của UC3 mở ra khả năng làm UC4, UC5, UC6 trong các sprint sau.
- Quick Win không phải là phần impact cao nhất (UC2 có impact 5/5) mà là phần có thể **chứng minh giá trị nhanh nhất trong bối cảnh hiện tại**.
- Nếu UC3 thành công: nhóm có evidence để xin pilot rộng hơn (80 học viên, tất cả track).

## Câu hỏi mở (mang sang Problem Framing)

- Baseline cụ thể là gì? Hiện tại bao nhiêu % học viên biết mình yếu ở Gate nào?
- Coach có đủ bandwidth review 20 checklist trong 1 tuần không — hay cần giảm scope xuống 10?
- Nếu bài nộp D28 có chất lượng khác nhau rất lớn (người viết 200 chữ, người viết 2.000 chữ) thì cách chuẩn hóa input như thế nào?

---

## Tổng kiểm tra trước khi sang `3-FINAL-problem-framing.md`

| Hạng mục | Xong? |
|---|---|
| Có bảng chấm 4 trục cho ≥4 use case | ✅ |
| Chốt 1 Quick Win, lý do bám số/impact (không "nghe hay") | ✅ |
| Nêu rõ ai ủng hộ pilot này | ✅ |
| Ghi rõ ≥2 phần KHÔNG chọn + lý do | ✅ (3 phần không chọn) |

⚑ Đây là phần coach kiểm tra ở Mốc 1: *"Vì sao không làm full tool? Vì sao chọn lát cắt này trước?"*

Sau bước này, mở `3-FINAL-problem-framing.md` — đóng khung vấn đề thật (bản nộp của phase Frame).

*Liên quan: handbook §A3 · `templates/quick-win-scoring.md` · `prompts/02-quick-win-challenge.md`*
