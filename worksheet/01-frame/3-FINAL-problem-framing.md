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

Câu hỏi phụ (tự trả lời trước khi điền):

- Một người ngoài đọc khung này có biết CHÍNH XÁC ai đau, đau cái gì không?
- Nếu KHÔNG có baseline thì nhóm đo "tốt hơn" bằng cách nào?
- Mục Open Questions trống = nguy hiểm (chưa nghĩ đủ). Nhóm còn chưa biết gì?

### Trả lời

1. **Original Ask** (stakeholder nói gì, nguyên văn): Tạo quiz từ bài học, chấm formative, phát hiện misconception và gợi ý học lại.
2. **Reframed problem** (vấn đề thật sau khi tách): Học viên track Product cần một cách kiểm tra hiểu bài ngay sau mỗi bài/lab và biết chính xác nên học lại phần nào khi sai. Hiện tại coach/instructor chỉ nhìn thấy hiểu sai khi học viên hỏi trên Discord, làm lab sai, hoặc đến lúc review bài nộp; lúc đó phản hồi đã trễ và khó xử lý ở quy mô 80 học viên track Product.
3. **Current workflow** (hiện tại đang xử lý thế nào, kể cả "không ai làm gì"): Sau bài học, học viên chủ yếu tự đọc lại, hỏi bạn/coach trên Discord, hoặc chờ đến lab/submission mới biết mình sai. Coach trả lời thủ công các câu hỏi rải rác và chỉ phát hiện pattern khi thấy nhiều người hỏi cùng một lỗi. Instructor không có baseline đều đặn về misconception sau từng bài, nên việc nhắc lại trong live/coaching dựa nhiều vào cảm nhận và một vài case nổi bật.
4. **Pain evidence — bằng SỐ** (ai đau · đau ở khoảnh khắc nào trong việc · tần suất · quy mô; số giả định ghi rõ nguồn giả định):

```text
Nguồn số: giả định lab dựa trên 00-context.md, dùng để đóng khung pilot; sẽ cần xác nhận bằng log Discord/LMS trong pilot.

Quy mô: track Product khoảng 80 học viên.
Giả định 1: mỗi bài học có 40% học viên chưa chắc ít nhất 1 khái niệm chính = khoảng 32 học viên/bài.
Giả định 2: chỉ 25% số học viên này hỏi công khai trên Discord/coaching = khoảng 8 câu hỏi/bài; 24 học viên còn lại có thể giữ hiểu sai đến lab/submission.
Giả định 3: coach mất trung bình 6-8 phút để đọc câu hỏi, hỏi lại ngữ cảnh, trả lời và dẫn tài liệu = 48-64 phút/bài cho phần câu hỏi lặp lại.
Baseline cần đo trong pilot: số câu hỏi misconception trên Discord sau bài, tỉ lệ học viên trả lời đúng quiz lần 1, tỉ lệ sửa đúng sau gợi ý học lại, và số tag misconception được coach xác nhận là đúng.
```

5. **Affected people** (ai dùng · ai quyết · ai là người review/expert): Người dùng chính là học viên track Product làm quiz sau bài học. Người hưởng lợi vận hành là coach track Product vì có tín hiệu misconception sớm. Người quyết định/pilot owner giả định là instructor hoặc program lead track Product. Người review/expert là instructor/coach, chịu trách nhiệm duyệt câu hỏi, đáp án mẫu, tag misconception và citation trước khi dùng rộng.
6. **Constraints** (từ `00-context.md`: privacy / human review / citation / budget / formative / adoption): Chỉ dùng dữ liệu mẫu hoặc dữ liệu học viên đã được giới hạn cho pilot; không đưa dữ liệu nhạy cảm/Discord riêng tư vào prompt nếu chưa được phép. Kết quả chấm là formative, không dùng làm điểm chính thức. Câu hỏi, đáp án, misconception và gợi ý học lại phải bám tài liệu khóa và có citation; thiếu nguồn thì nói không đủ căn cứ. Coach/instructor cần human review trước khi phát hành quiz hoặc dùng insight để can thiệp. Pilot phải nhỏ, chi phí thấp, ưu tiên tool/API sẵn có và workflow đủ dễ để học viên thực sự dùng.
7. **Quick Win đã chọn** (1 dòng, lấy từ file `2`): Quiz formative sau bài học: AI tạo 5-7 câu quiz từ tài liệu bài học, chấm câu trả lời, gắn misconception chính và gợi ý đoạn học lại có citation.
8. **Open questions** (còn chưa biết gì — không được để trống): Bài học nào nên chọn cho pilot đầu tiên để có misconception rõ nhưng không quá khó? Tài liệu khóa đã đủ cấu trúc/citation chưa, hay cần đánh số section trước? Coach sẽ review bao nhiêu câu hỏi trước khi phát hành để không quá tải? Ngưỡng thành công nên là bao nhiêu: ví dụ ≥60% học viên làm quiz, ≥50% câu sai được sửa đúng sau gợi ý, và ≥80% tag misconception được coach xác nhận?
9. **Validation** (đóng vai owner: *"đúng, đây là vấn đề đáng giải"* — Có / Chưa, vì sao):

```text
Có. Với vai trò owner track Product, tôi xác nhận đây là vấn đề đáng giải trước vì nó xảy ra ngay sau mỗi bài học, ảnh hưởng trực tiếp đến khả năng làm lab/submission, và hiện chưa có tín hiệu đủ sớm để coach/instructor can thiệp. Phạm vi pilot đủ nhỏ: 1-2 bài học, khoảng 80 học viên track Product, quiz formative không tính điểm, có human review và citation.
```

---

## Tự phản biện

- Khung này còn câu chung chung kiểu "cần học tốt hơn" không?
- 3 câu sẽ bị hỏi: *số/giả định lấy ở đâu · giả định chính sai thì sao · tình huống nào khiến dừng.* Trả lời thử 1 câu.

Trả lời thử:

- Khung này đã chỉ rõ người đau là học viên track Product sau bài học và coach/instructor khi cần phát hiện misconception sớm; không dùng framing chung chung kiểu "học tốt hơn".
- Số hiện tại là giả định lab dựa trên quy mô trong `00-context.md`, chưa phải số thật. Pilot phải đo lại bằng LMS/quiz log/Discord tag; nếu tỉ lệ misconception thấp hơn nhiều hoặc học viên không dùng quiz, nhóm sẽ thu hẹp sang bài học khó hơn hoặc dừng trước khi build tiếp.
- Tình huống dừng: quiz không đạt adoption tối thiểu 60% trong nhóm pilot, citation sai/thiếu khiến coach không tin, hoặc tag misconception được coach xác nhận đúng dưới 70%.

---

## Tổng kiểm tra trước khi sang `02-solution/`

| Hạng mục | Xong? |
|---|---|
| Chỉ rõ 1 nhóm người + 1 khoảnh khắc cụ thể (không "user nói chung") | x |
| Pain có số (hoặc kế hoạch lấy số), nói rõ số từ đâu | x |
| Có baseline (hoặc cách đo baseline) + ≥1 chỉ số có ngưỡng | x |
| Mục 9: owner (giả định) xác nhận đúng vấn đề = qua cổng phase Frame | x |

⚑ Coach kiểm tra ở Mốc 2: *"Ai đau? Baseline là gì? Không có baseline thì đo thế nào?"*

Owner chưa xác nhận → quay lại file `1`/`2`, đừng sang Solution. Owner xác nhận → mở `../02-solution/1-find-existing-solutions.md`.

*Liên quan: handbook §A4 · `prompts/03-problem-framing-challenge.md`*
