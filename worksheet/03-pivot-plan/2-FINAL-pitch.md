# 2 — FINAL: 5-slide Pitch + AI Support Log

Mục tiêu: dồn cả A3 Working Canvas thành 5 slide pitch (5 phút), chuẩn bị trả lời 3 câu phản biện, và ghi AI Support Log. Đây là bản nộp cuối cùng của lab.

Lý do làm bước này: nguyên tắc *demo đơn giản + lập luận chặt > demo đẹp + lập luận yếu*. Slide đẹp mà không trả lời được "số này lấy ở đâu" thì hỏng. Pitch không phải kể chuyện — là đưa evidence để stakeholder ra được một quyết định.

Quy tắc: **slide cuối phải là một lời xin rõ ràng** (xin gì · đổi lại hứa gì). Không có lời xin = stakeholder không biết approve cái gì.

## Quy trình 5 phút

```text
3 phút  — Dồn 5 slide (mỗi slide 1 thông điệp)
1 phút  — Chuẩn bị 3 câu phản biện
1 phút  — AI Support Log
```

---

## Phần A — 5 slide (mỗi slide 1 thông điệp)

Kéo nguyên liệu từ các file đã làm, đừng viết mới. Khung đầy đủ: `templates/5-slide-pitch.md`.

| # | Slide | Lấy từ | Nội dung 1–2 gạch đầu dòng | Ai nói |
|---|---|---|---|---|
| 1 | Problem & user | 01-frame/3-FINAL | Học viên track Product cần biết mình hiểu sai phần nào ngay sau bài học, nhưng coach/instructor thường chỉ phát hiện muộn qua Discord, lab hoặc submission. Pilot tập trung vào khoảng 80 học viên track Product, không triển khai cho cả khóa 500 người. | Thành viên giữ Problem Framing |
| 2 | Breakdown & Quick Win | 01-frame/1,2 | Không build full Quiz & Auto-Grading Engine. Quick Win là quiz formative 5-7 câu sau bài học: tạo quiz từ tài liệu, chấm nhẹ, gắn misconception và gợi ý học lại có citation. | Thành viên giữ Problem Framing |
| 3 | Solution + bản vẽ trực quan | 02-solution/2-FINAL | Chọn Boost: dùng model/API sẵn có + Google Forms/Sheets hoặc LMS + tài liệu AI20k đã chia section. Human review nằm trước khi phát quiz và sau khi AI gắn misconception cho câu trả lời mẫu. | Thành viên lo Solution |
| 4 | AI Pilot Plan | 03-pivot-plan/1 | Chạy 3 tuần trên 1-2 bài học: tuần 1 chuẩn hóa tài liệu/review quiz, tuần 2 phát quiz, tuần 3 đo kết quả và quyết định mở rộng/dừng. Data dùng tối thiểu, có ẩn danh câu trả lời và citation bắt buộc. | Thành viên dựng Pilot Plan |
| 5 | Metric · exit criteria · **lời xin** | 03-pivot-plan/1 | Xin approve pilot nhỏ: 1-2 bài học, 80 học viên Product, quyền dùng Forms/LMS + API LLM, và 4-6 giờ review của coach/instructor. Đổi lại nhóm hứa giao evidence: adoption ≥60%, citation đúng ≥80%, tag misconception đúng ≥80%, không có feedback bịa nguồn; fail thì dừng, không scale. | Thành viên dựng Pilot Plan |

## Phần B — Chuẩn bị 3 câu phản biện

Business owner/instructor sẽ hỏi mỗi nhóm 1–2 câu. Viết sẵn câu trả lời:

1. *"Số liệu / giả định này lấy ở đâu?"* → Số quy mô lấy từ `00-context.md`: khóa khoảng 500 học viên, track Product khoảng 80 học viên. Các số như 40% học viên chưa chắc khái niệm, 8 câu hỏi/bài và 6-8 phút/câu là giả định lab để đóng khung pilot; pilot sẽ đo lại bằng Forms/LMS log, Discord/coaching log và review của coach.
2. *"Nếu giả định quan trọng nhất của bạn sai thì sao?"* → Giả định quan trọng nhất là học viên sẽ làm quiz trong 48 giờ sau bài học. Nếu adoption <60%, nhóm không scale; sẽ phỏng vấn nhanh 5-7 học viên, rút quiz còn 3-5 câu hoặc gắn quiz vào workflow live/LMS rõ hơn. Nếu vẫn thấp, dừng hướng học viên tự dùng và chuyển sang hỗ trợ coach tạo quiz.
3. *"Tình huống nào sẽ khiến bạn dừng pilot?"* → Dừng nếu có feedback bịa nguồn, học viên hiểu nhầm kết quả là điểm chính thức, tag misconception đúng dưới 70%, hoặc sau 3 tuần không đạt ít nhất 2 metric chính. Người có quyền dừng là instructor/pilot owner track Product.

## Phần C — AI Support Log

| Câu hỏi | Trả lời |
|---|---|
| AI giúp được gì trong lab này? | AI giúp tách Big Ask lớn thành use case nhỏ, gợi ý hướng existing solutions, soạn bảng metric/exit criteria và biến flow thành pitch 5 slide dễ trình bày. |
| AI đưa output nào nghe hợp lý nhưng nhóm phải sửa? | AI dễ đề xuất build một quiz engine/dashboard đầy đủ hoặc auto-grading rộng. Nhóm sửa lại thành Quick Win nhỏ hơn: quiz formative sau 1-2 bài học, có human review và không dùng làm điểm chính thức. |
| Phần nào nhóm tự lập luận, KHÔNG copy AI? | Nhóm tự chốt lựa chọn Boost thay vì Build, tự ưu tiên Red Flag về misconception/citation, tự đặt ngưỡng dừng và lời xin pilot phù hợp với ràng buộc AI20k. |

---

## Tổng kiểm tra trước khi nộp

| Hạng mục | Xong? |
|---|---|
| 5 slide, mỗi slide 1 thông điệp, đã phân ai nói slide nào | x |
| Slide 5 có lời xin rõ ràng (xin gì · hứa gì) | x |
| Có câu trả lời sẵn cho cả 3 câu phản biện | x |
| AI Support Log điền đủ 3 dòng | x |
| Tất cả file worksheet/ đã commit + push, link dán vào Discord | Chưa — cần nhóm tự commit/push sau khi rà soát |

Đây là file cuối. Pitch 5 phút + nhận phản biện theo bảng 5 Gate (`templates/rubric-gate-sheet.md`).

*Liên quan: handbook §A9 · `templates/5-slide-pitch.md` · `templates/ai-support-log.md`*
