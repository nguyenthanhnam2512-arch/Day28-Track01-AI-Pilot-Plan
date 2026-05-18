---
artifact: 1 — Track & Big Ask + 2 — Tool Breakdown
bai-tap: Frame — nghe đúng đề rồi tách nhỏ
phase: Double Diamond vòng 1 · ◇ giãn (nghe rộng, chưa chốt)
time: ~12 phút (xem deck để biết khung giờ chính xác trong buổi)
input: 00-context.md · track card · prompts/01-breakdown.md
nop-cuoi: Không — file trung gian (bản chốt phase này ở 3-FINAL-problem-framing.md)
---

# 1 — Intake & Breakdown: nghe đúng đề, tách nhỏ

Mục tiêu: cả nhóm hiểu giống nhau "công cụ lớn stakeholder muốn", rồi tách nó thành 5–8 use case nhỏ làm được riêng. Đây là nửa "giãn ra" của [Double Diamond](https://www.thefountaininstitute.com/blog/what-is-the-double-diamond-design-process) vòng 1 — nghe rộng, tách rộng, chưa chọn.

Lý do làm bước này: hai cái bẫy chết người ở đây. Một, nhận đề literal ("làm con chatbot") rồi nhảy vào build — trong khi yêu cầu mơ hồ thường chỉ là triệu chứng. Hai, ôm cả công cụ lớn đi pitch "build cả platform" → trượt Gate 1 ngay. Tách nhỏ là động tác bắt buộc để từ "một ý tưởng to" sang "danh sách phần làm được".

Quy tắc: **nghe trước, tách trước, chưa chọn.** Bước này không được chốt Quick Win (việc đó ở file `2`).

## Bước 0 — Đọc track card + 00-context (2 phút)

Đọc track card được giao và `00-context.md` (mục 2 đã điền). Đừng lướt.

## Quy trình 12 phút

```text
2 phút  — Bước 0: đọc track card + context
4 phút  — Phần A: phát biểu lại Big Ask bằng lời nhóm
6 phút  — Phần B: tách 5–8 use case + check độc lập
```

---

## Phần A — Phát biểu lại Big Ask bằng lời nhóm

### Trả lời

- **Big Ask, viết lại bằng lời nhóm (2–3 câu)**:
  Lãnh đạo AI20k muốn xây một hệ thống AI giúp mỗi học viên trong ~500 người có lộ trình học riêng — thay vì tất cả đi theo cùng một đường. Hệ thống này cần "biết" học viên đang ở đâu (level, điểm yếu, mục tiêu nghề nghiệp) và từ đó tự gợi ý bước tiếp theo phù hợp.
  Stakeholder nói "cá nhân hóa lộ trình" — nhưng điều họ thực sự cần là: học viên biết mình cần làm gì tiếp theo vào đúng thời điểm, không phải một trang dashboard phức tạp.

- **Tại sao bây giờ**:
  AI20k vừa vào giai đoạn D28 — cửa ngõ trước 6 tuần thực chiến. Học viên có background rất khác nhau (PM, founder, engineer, operator) nhưng đang nhận cùng một lộ trình. Ở quy mô ~500 người, coach không thể nói chuyện 1-1 với từng người để hỏi "bạn đang yếu chỗ nào". Đây là khoảnh khắc đau nhất và cũng có dữ liệu sẵn nhất (bài nộp D28, quiz, rubric).

- **Người dùng đầu tiên cụ thể**:
  Học viên track Product (~80 người) vừa nộp bài D28, đang không biết nên ôn lại phần nào trước khi bước vào 6 tuần thực chiến — không phải "cả khóa 500 người".

---

## Phần B — Tách công cụ lớn thành 6 use case

| # | Use case (AI làm gì · cho ai · để họ làm được gì) | Người dùng | Làm được độc lập? |
|---|---|---|---|
| 1 | AI phân tích quiz đầu khóa + bài nộp đầu tiên → sinh báo cáo "bạn đang ở level nào, mục tiêu nào phù hợp" cho học viên để chọn track ngay từ đầu | Học viên (mới vào khóa) | **Có** |
| 2 | AI đọc mục tiêu nghề nghiệp học viên (PM/founder/engineer/operator) + kết quả quiz → sinh lộ trình học cá nhân hóa gồm thứ tự ưu tiên các ngày/module nên tập trung | Học viên | **Có** |
| 3 | AI phân tích bài nộp D28 của học viên (đối chiếu rubric 5 Gate) → sinh checklist điểm yếu cá nhân + gợi ý 3 tài liệu cần xem lại trước 6 tuần thực chiến | Học viên (đã nộp D28) | **Có** |
| 4 | AI theo dõi tiến độ học viên theo concept xuyên suốt khóa (D1–D28) → hiển thị "concept X bạn gặp 3 lần nhưng còn sai" để học viên biết chỗ nào chưa vững | Học viên | Không — phụ thuộc #1 (cần profile đầu khóa) |
| 5 | AI phân tích câu hỏi + điểm yếu của học viên → gợi ý 2–3 peer có điểm mạnh bổ sung để ghép cặp hỗ trợ nhau trong 6 tuần thực chiến | Học viên, Coach | Không — phụ thuộc #3 (cần biết điểm yếu trước) |
| 6 | AI tổng hợp dữ liệu toàn track → sinh view cho coach: danh sách học viên cần can thiệp (sai nhiều concept quan trọng, không có dấu hiệu tự ôn) kèm gợi ý hành động cụ thể | Coach | Không — phụ thuộc #3 (cần checklist điểm yếu đã có) |

**Kiểm tra độc lập**: Use case 1, 2, 3 làm được riêng lẻ → ≥3 use case độc lập. Use case 4, 5, 6 phụ thuộc nhau hoặc phụ thuộc #3, nhưng #3 khi chạy xong sẽ mở ra cả 3 cái sau.

---

## Phát hiện ban đầu

- Use case 3 (phân tích bài D28 → checklist điểm yếu) là **hinge point**: nếu làm được UC3, UC4/5/6 đều có thể build thêm dựa trên dữ liệu của nó.
- UC1 (chẩn đoán đầu khóa) và UC2 (lộ trình tổng) rất rộng — cần nhiều tháng để đo "có học tốt hơn không". Không phù hợp cho pilot 2 tuần.
- Dữ liệu sẵn có ngay bây giờ: bài nộp D28 + rubric 5 Gate + danh sách tài liệu khóa — đủ để chạy UC3 ngay.

## Câu hỏi mở (mang sang bước chọn Quick Win)

- UC3 cần bao nhiêu bài nộp để prompt đủ tốt? 5 bài có đủ để calibrate không?
- Coach có thực sự sẵn lòng review checklist AI trước khi gửi học viên, hay sẽ bỏ qua?
- Nếu học viên nhận checklist nhưng không làm theo — làm sao biết tool này có giá trị?

---

## Tổng kiểm tra trước khi sang `2-quick-win.md`

| Hạng mục | Xong? |
|---|---|
| Cả nhóm phát biểu lại Big Ask giống nhau, không cần nhìn card | ✅ |
| Có 5–8 use case dạng "AI làm X cho ai để Y" | ✅ (6 use case) |
| Có ≥4 use case thật sự độc lập | ✅ (UC1, UC2, UC3 độc lập; UC4/5/6 phụ thuộc UC3 nhưng UC3 độc lập) |
| Nhóm KHÔNG còn ý định pitch "build cả platform" | ✅ |

Sau bước này, mở `2-quick-win.md` — chấm điểm chọn 1 lát cắt làm trước.

*Liên quan: handbook §A1+§A2 · `prompts/01-breakdown.md` · `00-context.md`*
