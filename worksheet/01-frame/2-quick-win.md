# 2 — Quick Win: chọn lát cắt làm trước

Mục tiêu: từ 5–8 use case ở file `1`, chấm điểm nhanh và chốt **1 Quick Win** để pilot đầu tiên — kèm lý do chọn và lý do *không* chọn các phần khác. Đây là nửa "siết lại" của [Double Diamond](https://www.thefountaininstitute.com/blog/what-is-the-double-diamond-design-process) vòng 1.

Lý do làm bước này: đây là quyết định quan trọng nhất của phase Frame. Quick Win **không phải** phần dễ nhất hay nghe hay nhất — là phần *chứng minh được giá trị nhanh và có người ủng hộ*. Chọn sai → pilot fail → mất uy tín → khó xin pilot tiếp. Nhóm phải chọn được *và bảo vệ được bằng lý do*, không bằng cảm tính.

Quy tắc: **điểm số chỉ là gợi ý, không phải đáp án.** Đừng để con số quyết thay nhóm — nó chỉ giúp so sánh.

## Bước 0 — Lấy 4–6 use case mạnh nhất từ file `1` (1 phút)

## Quy trình 10 phút

```text
1 phút  — Bước 0: chọn 4–6 ứng viên
5 phút  — Phần A: chấm điểm 4 trục
3 phút  — Phần B: 1 lý do nên / 1 lý do không cho top 2
1 phút  — Phần C: chốt + ai ủng hộ + cái KHÔNG chọn
```

---

## Phần A — Chấm điểm 4 trục (1–5 mỗi trục)

Câu hỏi phụ (tự trả lời):

- "Risk" ở đây là *sai thì mất gì* — chọn đúng việc chính của user (task centrality) thì sai cũng đỡ đau; chọn việc lớn nhất thì sai rất đắt. Use case nào risk thấp thật?
- Use case nào có sẵn data + có người trong AI20k thật sự muốn dùng?

| Use case | Impact | Feasibility | Evidence nhanh | Risk (cao = an toàn) | Tổng |
|---|:--:|:--:|:--:|:--:|:--:|
| Tạo quiz formative 5-7 câu từ tài liệu bài học | 5 | 4 | 4 | 4 | 17 |
| Chấm câu trả lời quiz ngắn và giải thích sai/đúng | 4 | 4 | 3 | 3 | 14 |
| Phát hiện misconception theo câu trả lời cho coach | 5 | 3 | 3 | 3 | 14 |
| Gợi ý đoạn học lại kèm citation cho học viên | 5 | 4 | 4 | 4 | 17 |
| Dashboard misconception theo lớp/nhóm | 4 | 2 | 2 | 3 | 11 |

(Thang điểm chi tiết: `templates/quick-win-scoring.md`.)

## Phần B — 1 lý do nên / 1 lý do không, cho top 2

**Ứng viên A — Tạo quiz formative 5-7 câu từ tài liệu bài học**

```text
Nên chọn vì: có impact trực tiếp với học viên, dễ pilot bằng một vài bài học có sẵn, và tạo dữ liệu đầu vào cho các bước chấm/gợi ý/misconception sau này.
Không nên vì: nếu chỉ tạo câu hỏi mà không có feedback học lại thì giá trị dễ dừng ở mức "làm bài cho vui", chưa chắc sửa được hiểu sai.
```

**Ứng viên B — Gợi ý đoạn học lại kèm citation cho học viên**

```text
Nên chọn vì: đánh thẳng vào Red Flag "học viên không sửa được misconception"; citation giúp giảm bịa và tăng niềm tin vì feedback bám vào tài liệu khóa.
Không nên vì: cần đã có câu hỏi/câu trả lời hoặc ít nhất một cấu trúc quiz để biết học viên sai ở đâu, nên nếu làm riêng hoàn toàn sẽ thiếu tín hiệu đầu vào.
```

## Phần C — Chốt Quick Win

- **Quick Win nhóm chọn**: Quiz formative sau bài học: AI tạo 5-7 câu quiz từ tài liệu bài học, chấm câu trả lời, gắn misconception chính và gợi ý đoạn học lại có citation.
- **Vì sao chọn cái này trước** (2–4 câu, bám điểm + impact + evidence nhanh): Hai ứng viên mạnh nhất đều đạt 17 điểm, nhưng nếu tách riêng thì một bên thiếu feedback, một bên thiếu dữ liệu đầu vào. Vì vậy nhóm chọn một lát cắt nhỏ ghép vừa đủ vòng "quiz → chấm formative → học lại", chạy trên 1-2 bài học đầu tiên thay vì build full engine. Lát cắt này impact trực tiếp đến học viên, có sẵn tài liệu khóa làm evidence, và rủi ro thấp hơn auto-grading bài nộp vì không dùng làm điểm chính thức.
- **Ai trong AI20k sẽ ủng hộ pilot này** (và vì sao họ care — "có người ủng hộ" thường quan trọng hơn "impact cao"): Coach track Product sẽ ủng hộ vì họ cần biết sớm misconception phổ biến để nhắc lại trong coaching/live. Instructor cũng care vì có dữ liệu cụ thể để điều chỉnh nội dung, thay vì chỉ nghe phản hồi chung là "em chưa hiểu".
- **Nhóm KHÔNG chọn gì + vì sao** (≥2 use case bị loại): 1. Không chọn dashboard misconception theo lớp/nhóm trước vì cần dữ liệu quiz đủ lớn; build dashboard khi chưa có hành vi dùng thật dễ thành báo cáo đẹp nhưng rỗng.  2. Không chọn auto-grading bài nộp/submission trước vì rủi ro cao, cần rubric chuẩn và human calibration; dễ bị hiểu nhầm là chấm điểm chính thức.  3. Không chọn tạo ngân hàng câu hỏi biến thể trước vì giải quyết vấn đề vận hành của instructor nhiều hơn pain học viên sửa misconception.

---

## Phát hiện ban đầu

- Quick Win tốt nhất không phải một tính năng đơn lẻ, mà là một vòng formative rất nhỏ: tạo quiz, chấm nhẹ, chỉ ra hiểu sai, rồi dẫn về đúng tài liệu.

## Câu hỏi mở (mang sang Problem Framing)

- Baseline hiện tại học viên tự kiểm tra sau bài học là gì: không có quiz, quiz thủ công, hay chỉ hỏi trên Discord?
- Cần bao nhiêu câu/bao nhiêu học viên trong pilot để coach tin rằng tag misconception đủ hữu ích?

---

## Tổng kiểm tra trước khi sang `3-FINAL-problem-framing.md`

| Hạng mục | Xong? |
|---|---|
| Có bảng chấm 4 trục cho ≥4 use case | x |
| Chốt 1 Quick Win, lý do bám số/impact (không "nghe hay") | x |
| Nêu rõ ai ủng hộ pilot này | x |
| Ghi rõ ≥2 phần KHÔNG chọn + lý do | x |

⚑ Đây là phần coach kiểm tra ở Mốc 1: *"Vì sao không làm full tool? Vì sao chọn lát cắt này trước?"*

Sau bước này, mở `3-FINAL-problem-framing.md` — đóng khung vấn đề thật (bản nộp của phase Frame).

*Liên quan: handbook §A3 · `templates/quick-win-scoring.md` · `prompts/02-quick-win-challenge.md`*
