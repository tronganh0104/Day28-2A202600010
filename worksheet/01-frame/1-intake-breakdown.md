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

Đừng chép lại đề. Cả nhóm nói lại "công cụ lớn stakeholder muốn" bằng lời mình. Nếu 3 người nói 3 kiểu khác nhau → chưa hiểu giống nhau, bàn thêm.

Câu hỏi phụ (tự trả lời):

- Stakeholder nói họ muốn gì, và họ thực sự *cần* gì — có khác nhau không?
- "Tại sao bây giờ?" — ở quy mô ~500 người, cái gì đang đau khiến phải làm công cụ này lúc này?
- Ai là người dùng đầu tiên thật sự, không phải "cả khóa"?

### Trả lời

- **Big Ask, viết lại bằng lời nhóm (2–3 câu)**: Stakeholder muốn một công cụ AI giúp biến nội dung bài học thành các bài quiz ngắn, dùng để kiểm tra hiểu bài liên tục chứ không phải thi chính thức. Công cụ cần chỉ ra học viên đang hiểu sai khái niệm nào và gợi ý đúng phần tài liệu cần học lại, đồng thời giúp coach/instructor nhìn thấy các misconception phổ biến để can thiệp sớm.
- **Tại sao bây giờ**: Khóa đang vận hành ở quy mô khoảng 500 học viên, trong đó track Product có khoảng 80 học viên chia nhóm 3. Nếu chờ đến submission cuối hoặc lớp live mới phát hiện học viên hiểu sai thì coach/instructor không đủ thời gian sửa từng người; cần một cơ chế formative nhẹ, chạy thường xuyên, tạo tín hiệu sớm trước giai đoạn thực chiến 6 tuần.
- **Người dùng đầu tiên cụ thể**: Học viên track Product sau mỗi bài/lab, và coach phụ trách track Product cần xem nhanh nhóm nào đang hiểu sai phần nào.

## Phần B — Tách công cụ lớn thành 5–8 use case

Nhìn mục **Big Vision Modules** trong track card. Mỗi dòng = 1 use case làm được riêng, viết dạng *"AI làm X cho ai để họ Y"* — không phải tính năng mơ hồ. Cần 5–8 dòng (ít hơn 5 = chưa tách đủ; nhiều hơn 8 = đang liệt kê vụn).

| # | Use case (AI làm gì · cho ai · để họ làm được gì) | Người dùng | Làm được độc lập? |
|---|---|---|---|
| 1 | AI tạo quiz formative 5-7 câu từ tài liệu bài học cho học viên để họ tự kiểm tra hiểu bài ngay sau khi học. | Học viên | Có |
| 2 | AI chấm câu trả lời quiz ngắn cho học viên để họ biết câu nào sai và vì sao, không dùng làm điểm chính thức. | Học viên | Có |
| 3 | AI phát hiện misconception theo từng câu trả lời cho coach để coach biết học viên đang hiểu sai khái niệm nào. | Coach | Có |
| 4 | AI gợi ý đoạn bài học/tài liệu cần học lại kèm citation cho học viên để họ sửa đúng phần hổng kiến thức. | Học viên | Có |
| 5 | AI tổng hợp dashboard misconception theo lớp/nhóm cho instructor để ưu tiên nội dung cần nhắc lại trong buổi live. | Instructor | Có — cần dữ liệu quiz đã chạy |
| 6 | AI tạo bộ câu hỏi biến thể theo cùng learning objective cho instructor để giảm lặp đề và tăng độ phủ nội dung. | Instructor | Có |
| 7 | AI gắn tag learning objective và độ khó cho câu hỏi quiz để instructor/coach rà soát chất lượng ngân hàng câu hỏi. | Instructor/coach | Có |
| 8 | AI cảnh báo câu hỏi có khả năng lệch tài liệu hoặc đáp án mơ hồ cho người review để tránh quiz gây hiểu sai thêm. | Instructor/coach | Có |

Cần ít nhất **4 use case thật sự độc lập** (làm được mà không cần cái khác xong trước). Nếu nhiều cái phụ thuộc nhau → gộp hoặc viết lại cho tách bạch.

---

## Phát hiện ban đầu

- Không nên bắt đầu bằng "auto-grading toàn bộ bài nộp" vì rủi ro cao: dễ bị hiểu là điểm chính thức, cần rubric/calibration, và có thể ảnh hưởng niềm tin của học viên.
- Lát cắt quiz formative sau bài học có dữ liệu đầu vào rõ hơn: tài liệu bài học, learning objective, câu trả lời quiz, và feedback học lại đều có thể giới hạn trong phạm vi nhỏ.

## Câu hỏi mở (mang sang bước chọn Quick Win)

- Pilot nên chạy trên mấy bài học đầu tiên để vừa có đủ nội dung, vừa không quá rộng?
- Ngưỡng nào được xem là "phát hiện misconception thành công": tỉ lệ học viên sửa được câu sai, hay coach xác nhận tag misconception đúng?

---

## Tổng kiểm tra trước khi sang `2-quick-win.md`

| Hạng mục | Xong? |
|---|---|
| Cả nhóm phát biểu lại Big Ask giống nhau, không cần nhìn card | x |
| Có 5–8 use case dạng "AI làm X cho ai để Y" | x |
| Có ≥4 use case thật sự độc lập | x |
| Nhóm KHÔNG còn ý định pitch "build cả platform" | x |

Sau bước này, mở `2-quick-win.md` — chấm điểm chọn 1 lát cắt làm trước.

*Liên quan: handbook §A1+§A2 · `prompts/01-breakdown.md` · `00-context.md`*
