## 1. Bối cảnh AI20k (đọc, không sửa)

Khóa **AI Thực Chiến** có ~500 học viên (sinh viên năm cuối + người đi làm), đang chuẩn bị cho giai đoạn 6 tuần thực chiến sau Day 28. Lab này do track Product (~80 học viên, nhóm 3) làm. Hoạt động cả khóa nằm trên Discord, LMS, lớp live, lab, nộp bài, coaching — ở quy mô ~500 người.

Lãnh đạo chương trình muốn xây **AI20k Learning OS** — một hệ công cụ AI hỗ trợ học và vận hành khóa. Chính quy mô ~500 người là lý do **không build hết cùng lúc** được: mỗi nhóm nhận 1 track (1 công cụ lớn), tách nhỏ, chọn Quick Win, viết AI Pilot Plan để xin pilot.

Việc của nhóm hôm nay đúng là việc một PM/PO AI làm ngoài doanh nghiệp thật: stakeholder giao một "công cụ AI" quá lớn — bạn phải tách nhỏ, chọn đúng phần làm trước, và bảo vệ lựa chọn bằng lập luận chứ không bằng slide đẹp.

---

## 2. Track của nhóm (điền sau khi nhận track card)

- **Track số / tên**: 8 - Quiz & Auto-Grading Engine
- **Big Ask — chép nguyên văn câu yêu cầu trong track card**:

```text
Tạo quiz từ bài học, chấm formative, phát hiện misconception và gợi ý học lại 
```

- **Công cụ lớn này phục vụ ai** (học viên / coach / instructor / admin): học viên, coach, instructor
- **2 Red Flag đáng lo nhất (chép từ track card)**: 
1. Quiz không sát nội dung khóa, không phát hiện được misconception → học viên không sửa được misconception, coach/instructor không biết học viên đang hiểu sai chỗ nào.
2. Quiz có sát nội dung khóa, phát hiện được misconception → nhưng học viên không sửa được misconception, coach/instructor không biết học viên đang hiểu sai chỗ nào.


---

## 3. Ràng buộc mọi track phải tôn trọng (đọc, không sửa)

- **Privacy** — data học viên/submission/Discord nhạy cảm; trong lab dùng data mẫu/giả định, nói rõ dùng cái gì.
- **Human review** — output rủi ro cao phải có người review, AI không tự quyết việc quan trọng.
- **Citation** — trả lời dựa trên tài liệu khóa thì phải có nguồn; thiếu nguồn thì nói "không biết", không bịa.
- **Budget nhỏ** — ưu tiên tool/API có sẵn, prototype nhanh, không xây platform lớn.
- **Formative ≠ summative** — feedback/chấm bằng AI là formative, chưa phải điểm chính thức nếu chưa có người calibrate.
- **Adoption** — tool không ai dùng = $0 dù accuracy 99%.
- **Pilot đủ nhỏ** — chạy được trong bối cảnh khóa hiện tại.

---

## 4. Ghi chú thêm (tùy nhóm)
- Track này có thể dùng quiz để thu thập data misconception, nhưng không bắt buộc phải làm vậy.
- Có thể chọn làm quiz generation hoặc auto-grading, không nhất thiết phải làm cả hai.
