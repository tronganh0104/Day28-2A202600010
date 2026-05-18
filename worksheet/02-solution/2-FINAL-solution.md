# 2 — FINAL: Solution Approach + Demo/Mockup/Flow

Mục tiêu: chốt cách làm cho Quick Win (Build / Buy / Boost / Partner), nói rõ data & ai review cần có, và tạo 1 bản vẽ trực quan để stakeholder *nhìn* được. Đây là nửa "siết lại" của [Double Diamond](https://www.thefountaininstitute.com/blog/what-is-the-double-diamond-design-process) vòng 2 và là bản nộp của phase Solution.

Lý do làm bước này: hai cái bẫy. Một, "tự build" cho oai — trong khi 80–90% nhu cầu nội bộ chỉ cần Boost/Buy; tự build là quyết định khó rút lại nhất. Hai, chỉ nói bằng chữ — stakeholder không duyệt một đoạn văn, họ duyệt khi *nhìn thấy* flow. Không có bản vẽ → trượt Gate 4 dù lập luận tốt.

Quy tắc: **bản vẽ trực quan là BẮT BUỘC; demo chạy được chỉ là điểm cộng.** *Demo đơn giản + lập luận chặt > demo đẹp + lập luận yếu.*

## Quy trình 12 phút

```text
4 phút  — Phần A: chốt Build/Buy/Boost/Partner (decision tree + ego check)
3 phút  — Phần B: data & ai review cần có
5 phút  — Phần C: vẽ 1 artifact trực quan + đánh dấu chỗ người review
```

---

## Phần A — Chốt cách làm

Đi decision tree, đừng chọn theo cảm giác:

```text
Bài này có phải LỢI THẾ CẠNH TRANH CỐT LÕI không?
 ├─ CÓ  → đội có AI engineer mạnh? CÓ → Build · KHÔNG → Boost
 └─ KHÔNG (chỉ là productivity layer) → có tool sẵn?
          CÓ → Buy · KHÔNG → Boost (model sẵn + data riêng)
```

Câu hỏi phụ:

- Nhóm chọn cách này vì *cần* hay vì *thích tự build*? Một câu thành thật.
- Hướng nào ở file `1` (đã tìm được người làm rồi) khớp với cách này — "đi từ 5 lên"?

### Trả lời

- **Cách làm chốt**: Boost
- **Lý do CẦN (không phải thích), 2–3 câu**: Đây không phải lợi thế cạnh tranh cốt lõi cần tự build platform; giá trị nằm ở việc áp dụng đúng vào tài liệu AI20k và workflow coach. Boost cho phép dùng model/API sẵn có, form/sheet/LMS hiện có, nhưng vẫn thêm data riêng của khóa, citation và human review. Cách này đủ nhanh cho pilot 6 tuần và giảm rủi ro so với làm một quiz engine đầy đủ.
- **Vì sao KHÔNG "Build từ số 0"**: Build từ số 0 sẽ tốn thời gian vào đăng nhập, giao diện quiz, lưu điểm, dashboard, phân quyền, ngân hàng câu hỏi; những phần này chưa chứng minh được pain chính. Pilot cần chứng minh trước rằng feedback có citation và tag misconception thật sự giúp học viên sửa hiểu sai.
- **Tool / API / vendor cần + ước lượng chi phí thô** (budget nhỏ, ưu tiên sẵn có): Google Forms/Sheets hoặc LMS hiện có để phát quiz và thu câu trả lời; một model/API LLM để sinh câu hỏi, chấm formative và gợi ý học lại; tài liệu khóa được chia section để làm citation; reviewer là coach/instructor. Chi phí thô cho pilot: thấp, chủ yếu là API theo lượt quiz + thời gian review; có thể giới hạn 1-2 bài học, 80 học viên, 5-7 câu/bài.

## Phần B — Data & ai review (cách làm này cần gì để chạy được)

| Cần gì | Có sẵn trong AI20k? | Trong lab dùng (mẫu/giả định) | Privacy? |
|---|---|---|---|
| Data: Tài liệu bài học đã chia section/citation | Có một phần trong LMS/tài liệu khóa | Dùng 1-2 bài học mẫu, đánh số section như `Bài 1.2`, `Bài 1.3` | Không nhạy cảm nếu là tài liệu khóa; vẫn không đưa tài liệu nội bộ ngoài phạm vi pilot nếu chưa được phép |
| Data: Learning objective và misconception dự kiến | Có thể cần instructor/coach bổ sung | Dùng bảng mẫu gồm objective, khái niệm đúng, lỗi hiểu sai thường gặp | Không chứa dữ liệu cá nhân |
| Data: Câu trả lời quiz của học viên | Có sau khi chạy pilot | Dùng câu trả lời giả định hoặc ẩn danh trong lab | Có dữ liệu học viên; cần tối thiểu hóa, ẩn danh khi phân tích |
| Data: Rubric chấm formative/đáp án mẫu | Cần coach/instructor duyệt | Dùng rubric 3 mức: đúng, gần đúng, sai do misconception X | Không nhạy cảm, nhưng ảnh hưởng chất lượng feedback |

- **Output nào rủi ro cao** (sai gây hậu quả): Câu hỏi/đáp án sai làm học viên học lệch; tag misconception sai khiến coach hiểu nhầm vấn đề; gợi ý học lại không có nguồn hoặc sai nguồn làm mất niềm tin. Điểm/chấm đúng-sai cũng nhạy cảm nếu học viên tưởng là điểm chính thức.
- **Ai review + bao nhiêu mẫu + pass/fail theo gì**: Instructor/coach review 100% câu hỏi, đáp án, citation trước khi phát hành quiz đầu tiên. Sau khi chạy, coach review tối thiểu 20-30 câu trả lời mẫu hoặc toàn bộ câu bị AI gắn misconception. Pass nếu ≥80% câu hỏi/citation được duyệt ở lần review đầu, ≥80% tag misconception trong mẫu được coach xác nhận đúng, và không có feedback bịa nguồn.
- **Có cần citation / nói "không biết" khi thiếu nguồn không**: Có. Mọi giải thích và gợi ý học lại phải trỏ về section tài liệu khóa; nếu không tìm thấy nguồn đủ rõ, output phải ghi "không đủ căn cứ từ tài liệu hiện có" và chuyển cho coach review.

## Phần C — Bản vẽ trực quan (BẮT BUỘC)

Chọn **1** dạng nhẹ nhất đủ rõ (xem `templates/demo-examples.md`): mockup 2–3 màn hình · user flow trước/sau · prompt flow · agent flow · 1 cặp input–output thật. Vẽ tay / ASCII / bảng đều được.

```text
FLOW PILOT: QUIZ FORMATIVE CÓ CITATION

Trước buổi học / trước khi phát quiz

  [Tài liệu bài học]
        |
        v
  [Chia section + learning objective]
        |
        v
  [AI draft 5-7 câu quiz + đáp án + misconception + citation]
        |
        v
  [COACH/INSTRUCTOR REVIEW]
        |  pass
        v
  [Google Form / LMS Quiz phát cho học viên]

Khi học viên làm quiz

  [Học viên trả lời]
        |
        v
  [AI chấm formative: đúng / gần đúng / sai]
        |
        v
  [AI gắn misconception + gợi ý học lại section có citation]
        |
        +--------------------------+
        |                          |
        v                          v
  [Feedback cho học viên]     [Bảng tổng hợp cho coach]
  - Câu này sai vì...         - Top misconception
  - Học lại: Bài 1.3          - Câu có nhiều lỗi nhất
  - Không tính điểm           - Mẫu cần review

Ví dụ 1 cặp input-output:

INPUT
Tài liệu nguồn: Bài 1.3 - "Formative feedback dùng để giúp người học sửa hiểu sai trong quá trình học; không phải điểm summative."
Câu hỏi: "Vì sao quiz trong pilot này không nên dùng làm điểm chính thức?"
Câu trả lời học viên: "Vì AI chấm chưa chắc chính xác nên chỉ để tham khảo."

OUTPUT
Mức formative: Gần đúng.
Misconception: Học viên mới nêu rủi ro accuracy, chưa nêu bản chất formative khác summative.
Feedback: Câu trả lời đúng một phần. Quiz này không dùng làm điểm chính thức vì mục tiêu là phát hiện và sửa hiểu sai trong quá trình học, chưa phải đánh giá cuối cùng đã được calibrate bởi người dạy.
Học lại: Bài 1.3 - Formative vs summative feedback.

Chỗ con người review (output rủi ro cao) nằm ở:
1. Coach/instructor review toàn bộ câu hỏi, đáp án, misconception và citation trước khi phát quiz.
2. Coach review mẫu câu trả lời bị gắn misconception sau khi chạy pilot.
3. Nếu AI không tìm được citation hoặc confidence thấp, chuyển sang "cần coach review", không trả feedback chắc chắn.
```

Câu hỏi phụ — một người đóng vai stakeholder nhìn 20 giây: *hiểu user làm gì, nhận lại gì, không cần giải thích thêm không? Có chỗ nào "đẹp nhưng rỗng" không?*

---

## Tổng kiểm tra trước khi sang `../03-pilot-plan/`

| Hạng mục | Xong? |
|---|---|
| Cách làm có lý do CẦN, không phải "mặc định tự build" | x |
| Nói rõ data cần + ai review output rủi ro cao | x |
| Có ≥1 bản vẽ trực quan, người ngoài hiểu trong ~20 giây | x |
| Có đánh dấu chỗ con người review | x |

⚑ Coach kiểm tra ở Mốc 3: *"Stakeholder nhìn vào đâu để hiểu flow? Mockup/sketch/demo đâu?"* Chỉ nói bằng chữ = chưa qua.

Sau bước này, mở `../03-pilot-plan/1-pilot-plan.md`.

*Liên quan: handbook §A5+§A6 · `templates/demo-examples.md` · `prompts/05-demo-challenge.md`*
