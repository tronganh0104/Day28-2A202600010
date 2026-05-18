# 1 — Find existing solutions (đừng xây lại từ số 0)

Mục tiêu: trước khi quyết Build / Buy / Boost / Partner, nhóm phải biết bài này đã có ai giải ở chỗ khác chưa, và họ giải bằng cách nào. Đây là nửa "giãn ra" của [Double Diamond](https://www.thefountaininstitute.com/blog/what-is-the-double-diamond-design-process) vòng 2 — mở hết các lời giải đang tồn tại, chưa chốt cái nào.

Lý do làm bước này: đây là chỗ nhiều nhóm hỏng mà không biết. Hỏng vì nhảy thẳng vào "tự build" cho oai, trong khi 80–90% nhu cầu nội bộ chỉ cần Boost hoặc Buy. Hỏng vì không hỏi "ai làm rồi" nên đi lại từ số 0. Gần như bài nào cũng đã có người giải ở một ngành khác — không thấy thì phí cả pilot.

Quy tắc: **không có nguồn = giả định.** Mỗi cái AI/web nói ra, hỏi lại "lấy ở đâu?". Không chỉ được nguồn thì đánh dấu 🧮 (giả định để giảng), đừng xài như fact.

## Bước 0 — Bài này thực ra là dạng bài gì? (2 phút)

Bỏ context AI20k sang một bên. Mô tả Quick Win của nhóm như một bài toán chung — không có chữ "học viên / coach / Discord". Vài ví dụ cho dễ hình dung:

- "câu hỏi của user → câu trả lời kèm nguồn" → đây là bài Q&A có citation
- "một đống văn bản lộn xộn → data có cấu trúc" → bài extraction
- "bài nộp → nhận xét theo rubric" → bài rubric grading

Dạng bài (the pattern) đó gần như chắc chắn đã có người làm ở ngành khác. Tìm ra dạng bài → tìm ra người đã giải nó.

- **Quick Win của nhóm, viết lại thành 1 dạng bài chung (không có chữ domain)**: Từ một bộ tài liệu nguồn, tạo kiểm tra ngắn, đánh giá câu trả lời theo mục tiêu học, phân loại lỗi hiểu sai và trả về feedback có dẫn nguồn.
- **Input → output thực chất là gì**: Tài liệu nguồn + learning objective + câu trả lời người dùng → bộ câu hỏi, đáp án/giải thích, nhãn lỗi, gợi ý đọc lại kèm citation.
- **Ràng buộc không bỏ được (lấy từ `00-context.md`)**: Phải có citation; thiếu nguồn thì nói không đủ căn cứ; output chỉ dùng formative; cần human review cho câu hỏi/đáp án/tag lỗi; bảo vệ dữ liệu học viên; ngân sách nhỏ; pilot đủ nhỏ để chạy trong khóa hiện tại.

## Quy trình 8 phút

```text
2 phút  — Bước 0: gọi tên dạng bài
4 phút  — Phần A: deep research 4 tầng "ai giải dạng bài này rồi"
2 phút  — Phần B: rút về 2–3 hướng khả thi, đánh dấu nguồn
```

---

## Phần A — Deep research: ai giải dạng bài này rồi, giải sao?

Không phải gõ 1 câu vào AI rồi chép. Chạy 4 tầng, **tầng sau lấy kết quả tầng trước làm input**. Khung câu lệnh ở `prompts/04-find-solutions.md`.

Câu hỏi phụ (tự trả lời — viết ra cái nhóm *tìm thấy*, không phải cái nhóm *đoán*):

- Dạng bài này giống bài nào ở một ngành hoàn toàn khác?
- Hướng nào AI gợi ý mà nhóm **không kiểm được nguồn** — vậy có nên tin không?
- Một ca thất bại của người đi trước dạy nhóm tránh đúng điều gì?
- Nhóm "đi từ mức mấy" — kế thừa được gì để khỏi bắt đầu từ 0?

### Trả lời — điền theo 4 tầng

| Tầng | Hỏi AI/web câu gì | Tìm được gì | Nguồn / 🧮 nếu là giả định |
|---|---|---|---|
| 1 · Map | "Dạng bài tạo quiz + feedback có nguồn từ tài liệu thường giải bằng những hướng nào? 4–6 hướng, mỗi hướng khi nào nên dùng." | Có 4 hướng chính: dùng LMS quiz/question bank có feedback; dùng AI teacher tool để sinh câu hỏi; dùng RAG để bám tài liệu và citation; dùng AI-assisted grading để gom/chấm câu trả lời tương tự dưới sự review của người dạy. | Moodle Quiz docs: https://docs.moodle.org/en/Quiz; OpenAI RAG help: https://help.openai.com/en/articles/8868588-retrieval-augmented-generation-rag-and-semantic-search-for-gpts |
| 2 · Tiền lệ | "Đội nào đã làm bài quiz/feedback/grading ở quy mô lớp học? Họ làm cách nào?" | Moodle đã có quiz activity, question bank, reusable questions và feedback cho formative/self-assessment. Khanmigo có teacher tools như multiple choice assessment, exit ticket/rubric generator và recommend assignments. Gradescope dùng AI-assisted grading/answer groups để gom câu trả lời tương tự, sau đó instructor review và chấm theo nhóm. | Moodle Quiz docs: https://docs.moodle.org/en/Quiz; Khanmigo teacher tools: https://support.khanacademy.org/hc/en-us/articles/14799047733645-What-teacher-tools-are-available-on-Khanmigo; Gradescope guide: https://guides.gradescope.com/hc/en-us/articles/24838908062093-AI-assisted-grading-and-answer-groups |
| 3 · Phản chứng | "Ca nào làm dạng này thất bại? Nguyên nhân gốc là cách làm hay chuyện khác?" | Rủi ro thường không nằm ở việc tạo được câu hỏi, mà ở chất lượng/nguồn câu hỏi, adoption và human review. Nếu AI tạo feedback không bám nguồn, hallucination làm mất niềm tin; nếu dùng grading AI như điểm chính thức mà thiếu review/calibration thì rủi ro cao. Với công cụ học tập, người học có thể không dùng nếu flow quá rườm rà hoặc feedback không giúp sửa lỗi ngay. | RAG vẫn cần nguồn truy xuất phù hợp và grounding: https://help.openai.com/en/articles/8868588-retrieval-augmented-generation-rag-and-semantic-search-for-gpts; Gradescope vẫn đặt instructor vào vòng review answer groups: https://guides.gradescope.com/hc/en-us/articles/24838908062093-AI-assisted-grading-and-answer-groups; adoption là ràng buộc từ `00-context.md` |
| 4 · Thu hẹp | "Với ràng buộc budget nhỏ, có người review, cần citation, hướng nào khả thi cho pilot 6 tuần?" | Khả thi nhất là Boost: dùng model/API sẵn có + tài liệu khóa đã chunk/đánh section + form/quiz đơn giản để pilot. Không cần build LMS mới; có thể sinh quiz và feedback bằng prompt/RAG, lưu câu trả lời vào sheet/LMS, coach review trước khi phát hành và kiểm tra sample output sau khi chạy. | 🧮 Tổng hợp từ các nguồn trên và ràng buộc AI20k; đây là quyết định áp dụng cho lab, chưa phải benchmark thị trường. |

---

## Phần B — Rút về 2–3 hướng khả thi

Câu hỏi phụ:

- Hướng nào *kế thừa được nhiều nhất* từ người đã làm?
- Hướng nào nghe hay nhưng nhóm **không có nguồn** để tin?

### Trả lời

| Hướng giải khả thi | Ai làm rồi (gần bài mình nhất) | Nguồn / 🧮 | Hợp ràng buộc `00-context`? |
|---|---|---|---|
| Buy: dùng LMS quiz/question bank có feedback, nhập câu hỏi thủ công hoặc bán tự động | Moodle Quiz: quiz activity, question bank, reusable questions, feedback/self-assessment | https://docs.moodle.org/en/Quiz | Có một phần: ổn cho quiz và feedback, nhưng chưa tự động phát hiện misconception/gợi ý học lại theo tài liệu riêng nếu không bổ sung AI. |
| Boost: dùng model/API sẵn có + tài liệu khóa làm nguồn để sinh quiz, chấm formative, tag misconception và citation | RAG/document-grounded answer pattern; Khanmigo teacher tools cho tạo câu hỏi/assessment | https://help.openai.com/en/articles/8868588-retrieval-augmented-generation-rag-and-semantic-search-for-gpts; https://support.khanacademy.org/hc/en-us/articles/14799047733645-What-teacher-tools-are-available-on-Khanmigo | Có: budget nhỏ, dùng data riêng, dễ pilot nhỏ, giữ human review, citation rõ. |
| Partner/Buy: dùng tool grading có AI assistance cho bài trả lời tự luận | Gradescope AI-assisted grading/answer groups | https://guides.gradescope.com/hc/en-us/articles/24838908062093-AI-assisted-grading-and-answer-groups | Chưa hợp cho Quick Win đầu tiên: mạnh ở grading submission/answer groups, nhưng nặng hơn nhu cầu quiz formative sau bài học. |

**"Đi từ 5 lên" — nhóm kế thừa cụ thể cái gì** (1–2 câu):

```text
Nhóm không tự phát minh quiz engine từ đầu. Kế thừa pattern đã có: LMS quiz/question bank/feedback, RAG để grounding vào tài liệu có citation, và human-in-the-loop giống Gradescope khi output có rủi ro.
```

---

## Phát hiện ban đầu

Ghi nhanh 2–3 cái đáng chú ý nhất (chưa phải quyết định — quyết định ở file FINAL):

- Tạo quiz không phải phần khó nhất; phần cần kiểm soát là câu hỏi có bám learning objective, feedback có citation, và tag misconception có được coach tin không.
- Các hệ thống grading nghiêm túc đều giữ người dạy trong vòng review, nên pilot không nên để AI tự quyết đúng/sai như điểm chính thức.
- Hướng Boost hợp hơn Build vì AI20k có tài liệu riêng và cần pilot nhanh, không cần sở hữu một platform quiz đầy đủ ngay.

## Câu hỏi mở (mang sang bước chốt)

- Nên dùng form/sheet/LMS hiện có nào làm lớp giao diện đầu tiên để học viên không phải học thêm tool mới?
- Cần chuẩn hóa tài liệu khóa thành section/citation như thế nào để feedback "học lại phần nào" đủ rõ?

---

## Tổng kiểm tra trước khi sang `2-FINAL-solution.md`

| Hạng mục | Xong? |
|---|---|
| Gọi được dạng bài trong 1 câu, không còn chữ domain | x |
| Đủ 4 tầng deep research, tầng nào cũng có kết quả | x |
| Mỗi kết quả có nguồn, hoặc đánh dấu 🧮 nếu là giả định | x |
| Rút về 2–3 hướng + nói được "đi từ 5 lên" cái gì | x |

Hàng nào chưa xong → quay lại Phần A, đừng sang bước chốt vội.

Sau bước này, mở `2-FINAL-solution.md` — chốt Build/Buy/Boost/Partner + data & ai review + bản vẽ trực quan (đây là bản nộp của phase này).

*Liên quan: handbook §A5 · `prompts/04-find-solutions.md` · `00-context.md`*
