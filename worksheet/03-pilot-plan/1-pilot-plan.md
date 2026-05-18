---
artifact: 7 — AI Pilot Plan core
bai-tap: Pilot Plan — cam kết hai chiều: xin – hứa – đo – dừng
phase: Double Diamond vòng 2 · ◇ giãn → ◆ siết (liệt kê hết rồi chốt gọn)
time: ~10 phút (xem deck để biết khung giờ chính xác trong buổi)
input: 02-solution/2-FINAL-solution.md · 00-context.md · prompts/06-pilot-plan-challenge.md
nop-cuoi: Không — file trung gian (bản nộp ở 2-FINAL-pitch.md)
---

# 1 — AI Pilot Plan core

Mục tiêu: viết phần kế hoạch xin pilot — scope, người, data, budget, timeline, metric, exit criteria, adoption, lời hứa, lời xin. Bước này giãn ra (liệt kê hết những thứ cần) rồi siết lại (chốt bản gọn đủ để stakeholder quyết).

Lý do làm bước này: đây là thứ stakeholder dùng để **quyết approve hay dừng**. AI Pilot Plan **không phải proposal xin tiền** — là *cam kết hai chiều*: nhóm xin nguồn lực, đổi lại hứa giao evidence + chấp nhận dừng nếu metric fail. Demo đẹp mà không nói được "xin gì, hứa gì, đo gì, dừng khi nào" → trượt Gate 5.

Quy tắc: **budget tách từng hạng mục, không gộp 1 cục; không có mục "miscellaneous".** Exit criteria phải có người có quyền thực thi, không chỉ trên giấy.

## Quy trình 10 phút

```text
6 phút  — Điền 10 mục core (kéo nguyên liệu từ 00 + 01-frame + 02-solution)
3 phút  — Phần exit criteria + adoption (chỗ nhóm hay bỏ quên)
1 phút  — Tự phản biện
```

---

## 10 mục core

### Trả lời

1. **Tóm vấn đề** (1 câu, từ Problem Framing):
   Học viên track Product (~80 người) không biết mình đang yếu chỗ nào sau D28 nên không thể ôn tập đúng trọng tâm trước 6 tuần thực chiến.

2. **Cách làm + lý do** (từ 02-solution, 1 câu):
   Boost — dùng Claude API phân tích bài nộp D28 của học viên (đối chiếu với rubric 5 Gate) để sinh ra checklist điểm yếu cá nhân + gợi ý 3 tài liệu cần xem lại, có coach review trước khi gửi.

3. **Scope pilot**:
   - Phục vụ: học viên track Product (~80 người), ưu tiên 20 học viên xung phong trong tuần đầu
   - Thời lượng: 2 tuần sau D28
   - Số phase: 2 phase (tuần 1: internal test + coach calibrate; tuần 2: gửi cho 20 học viên thử)

4. **Người**:
   - Nhóm làm: Nguyễn Thành Nam (PM/build prompt), Hoàng Kim Trí Thành (test + viết doc), Quách Gia Được (review flow)
   - Review output rủi ro cao: 2 coach track Product — xem qua checklist trước khi gửi học viên (mỗi bài ≤5 phút review)
   - Quyết định approve/dừng: Lead Coach chương trình AI20k

5. **Data**:
   - Dùng trong lab (giả định): 5 bài nộp D28 mẫu (ẩn danh) + rubric 5 Gate + danh sách 20 tài liệu khóa học có sẵn
   - Pilot thật: bài nộp thật của 20 học viên xung phong (có consent), không lưu trữ sau pilot
   - Privacy: không lưu tên học viên trong log AI; citation bắt buộc kèm mục rubric tương ứng khi gợi ý tài liệu

6. **Budget** (tách hạng mục):

   | Hạng mục | Chi tiết | Ước lượng |
   |---|---|---|
   | API (Claude/GPT) | ~1.500 token/bài × 80 bài × $0.003/1K token | ~$0.36 (≈9.000 VND) |
   | Thời gian nhóm | 3 người × 2 tuần × 5h/tuần (volunteer) | 30h — không trả tiền |
   | Thời gian coach review | 2 coach × 20 bài × 5 phút | ~3h tổng |
   | Prompt iteration + QA | 10h nhóm tuần 1 trước khi chạy thật | trong 30h trên |
   | Maintenance sau pilot | Không — pilot 2 tuần là đóng lại | $0 |

   > 🧮 Giả định: số token/bài ước lượng từ độ dài trung bình bài D28 (500-700 chữ). Cần đo lại thực tế.

7. **Timeline + cổng giữa phase**:

   ```text
   Phase 1 — Tuần 1 (nội bộ):
     - Build prompt + test trên 5 bài mẫu ẩn danh
     - Coach calibrate: xem 5 checklist, sửa prompt nếu cần
     → Cổng: ≥4/5 checklist coach chấp nhận gửi được cho học viên

   Phase 2 — Tuần 2 (pilot 20 học viên):
     - Chạy cho 20 học viên xung phong, coach review trước khi gửi
     - Thu feedback học viên (form 3 câu sau khi đọc checklist)
     → Cổng: ≥60% học viên thấy checklist phản ánh đúng điểm yếu của mình
   ```

8. **Metrics** (SMART + baseline + ngưỡng + ai đo):

   | Metric | Đo bằng gì · ai đo | Baseline | Ngưỡng đạt |
   |---|---|---|---|
   | % checklist coach chấp nhận (không cần sửa nhiều) | Coach đánh dấu pass/fail sau review · Lead Coach tổng hợp | 0% (chưa có hệ thống) | ≥70% |
   | % học viên thấy checklist phản ánh đúng điểm yếu | Form survey 1 câu sau khi đọc · nhóm thu thập | 0% (chưa có hệ thống) | ≥60% |
   | Thời gian coach review 1 checklist | Bấm giờ thực tế · coach tự ghi | N/A (không có baseline) | ≤5 phút/bài |

   **Leading indicator** (biết kết quả sớm trong 3–5 ngày): phản hồi định tính của coach sau khi xem 5 bài đầu tuần 1 — có thấy checklist đúng hướng không?

9. **Exit criteria** (định trước, ≥2 mức):

   | Mức | Điều kiện | Hành động | Ai có quyền dừng |
   |---|---|---|---|
   | Cảnh báo | Coach chấp nhận 50–70% checklist (tuần 1) HOẶC học viên thấy đúng 40–60% | Dừng gửi thêm, review lại prompt và rubric mapping, thử lại với 5 bài mới | Lead Coach + nhóm |
   | Nghiêm trọng | Coach chấp nhận <50% HOẶC có ≥1 checklist gây hiểu sai nghiêm trọng (vd: nói học viên yếu sai mục) HOẶC học viên phàn nàn về thông tin sai | Dừng ngay toàn bộ pilot, không gửi thêm, báo cáo lý do cho Lead Coach | Lead Coach (quyết định ngay, không cần họp) |

   *Liên hệ 2 Red Flag ở `00-context.md`:*
   - Red Flag 1 (cá nhân hóa giả): được chặn bởi mức Nghiêm trọng — nếu checklist không khác nhau giữa học viên → coach phát hiện ngay khi review
   - Red Flag 2 (không đo được "học viên có tốt lên không"): được chặn bởi metric % học viên thấy đúng + cổng phase 2

10. **Adoption** (tool không ai dùng = $0):
    - **Ai dùng đầu tiên**: 2 coach tình nguyện (không phải cả khóa), sau đó 20 học viên xung phong đăng ký qua form
    - **Workflow đổi ở đâu**: Coach không cần tự viết nhận xét điểm yếu từ đầu — dùng checklist AI làm bản nháp, chỉ cần xác nhận/sửa
    - **Ai train/support**: Nhóm tổ chức 1 session 20 phút hướng dẫn coach đọc checklist + cách sửa
    - **Nếu không ai dùng**: Thu phỏng vấn nhanh 3 coach lý do không dùng → ưu tiên giải quyết 1 điểm cản lớn nhất trước khi mở rộng

---

## Tự phản biện

- **Budget thiếu hạng mục ẩn nào không?**
  Thiếu: chi phí thiết kế form survey + thời gian phân tích kết quả (~2h). Thêm vào: 2h nhóm trong phase 2.

- **Exit criteria đủ mạnh để THẬT SỰ dừng, hay chỉ trên giấy?**
  Đủ mạnh nếu Lead Coach cam kết thực thi. Rủi ro: nếu Lead Coach muốn "thử thêm một tuần" dù metric fail → cần ghi rõ trước buổi kick-off pilot là "dừng ngay khi chạm mức Nghiêm trọng, không gia hạn".

- **Giả định quan trọng nhất sai → plan gì?**
  Giả định: coach có đủ thời gian review 20 bài trong 1 tuần. Nếu sai → giảm scope còn 10 bài, ưu tiên học viên sai nhiều nhất ở rubric Gate 4 + Gate 5.

---

## Tổng kiểm tra trước khi sang `2-FINAL-pitch.md`

| Hạng mục | Xong? |
|---|---|
| Tóm vấn đề trong 1 câu | ✅ |
| Budget tách hạng mục, không "miscellaneous" | ✅ |
| Metric có baseline + ngưỡng + ai đo | ✅ |
| Exit criteria có người có quyền thực thi (≥2 mức) | ✅ |
| Adoption: chỉ rõ ai dùng đầu tiên (không "cả khóa") | ✅ |

⚑ Coach kiểm tra ở Mốc 4: *"Xin gì? Hứa gì? Đo gì? Dừng khi nào?"*

Sau bước này, mở `2-FINAL-pitch.md` — dồn tất cả thành 5-slide pitch + AI Support Log.

*Liên quan: handbook §A7+§A8 · `templates/ai-pilot-plan-core.md` · `prompts/06-pilot-plan-challenge.md`*
