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

Câu hỏi phụ (tự trả lời):

- Nếu tóm vấn đề không gọn trong 1 câu → nhóm chưa hiểu vấn đề.
- Exit criteria của nhóm có ai DÁM thực thi khi sếp vẫn thích pilot không?
- Adoption: ai dùng đầu tiên — không phải "cả khóa ~500 người"?

### Trả lời

1. **Tóm vấn đề** (1 câu, từ Problem Framing): Học viên track Product cần biết mình hiểu sai phần nào ngay sau bài học, nhưng hiện coach/instructor chỉ phát hiện misconception muộn qua Discord, lab hoặc submission.
2. **Cách làm + lý do** (từ 02-solution, 1 câu): Chọn hướng Boost: dùng model/API sẵn có + Google Forms/Sheets hoặc LMS + tài liệu AI20k có citation, vì cần pilot nhanh và không nên build quiz platform từ số 0.
3. **Scope pilot**: phục vụ ai · bao nhiêu người · bao lâu · mấy phase: Pilot cho khoảng 80 học viên track Product, chạy trên 1-2 bài học có learning objective rõ, trong 3 tuần. Phase 1 chuẩn bị và review quiz; Phase 2 chạy với học viên; Phase 3 đo kết quả và quyết định mở rộng/dừng.
4. **Người**: nhóm làm · ai review output rủi ro cao · ai có quyền quyết approve/dừng: Nhóm lab thiết kế flow, prompt, bảng đo và mockup. Coach/instructor track Product review 100% câu hỏi, đáp án, citation trước khi phát hành và review mẫu câu trả lời sau khi chạy. Pilot owner giả định là instructor/program lead track Product, có quyền approve, yêu cầu sửa hoặc dừng pilot.
5. **Data**: dùng data gì (mẫu/giả định) · cơ chế privacy/citation: Dùng tài liệu bài học đã chia section, learning objective, rubric formative 3 mức, misconception dự kiến và câu trả lời quiz của học viên. Trong lab dùng data mẫu/giả định; khi pilot thật, câu trả lời được tối thiểu hóa thông tin cá nhân, phân tích ẩn danh, không đưa log Discord riêng tư vào prompt nếu chưa được phép. Mọi feedback học lại phải trỏ về section tài liệu; thiếu nguồn thì nói "không đủ căn cứ từ tài liệu hiện có".
6. **Budget** (tách hạng mục): API/tool: Google Forms/Sheets hoặc LMS hiện có + chi phí API LLM theo lượt quiz, giới hạn 1-2 bài học và 5-7 câu/bài. Thời gian người: 2-3 giờ chuẩn hóa tài liệu, 2 giờ tạo/review quiz, 1-2 giờ review sample sau khi chạy, 1 giờ tổng hợp metric. Hạng mục ẩn: hướng dẫn học viên cách dùng quiz, support khi lỗi form/API, bảo trì citation khi tài liệu bài học đổi.
7. **Timeline + cổng giữa phase**: Phase 1 (tuần 1) chọn bài học, chia section, tạo draft quiz, coach review → cổng: ≥80% câu hỏi/citation pass ở lần review đầu. Phase 2 (tuần 2) phát quiz cho học viên track Product sau bài học, thu câu trả lời và feedback → cổng: adoption ≥60% học viên được mời. Phase 3 (tuần 3) coach review sample, đo misconception và quyết định mở rộng/dừng → cổng: ≥80% tag misconception trong mẫu được coach xác nhận đúng và không có feedback bịa nguồn.
8. **Metrics** (SMART + baseline + ngưỡng + ai đo):

| Metric | Đo bằng gì · ai đo | Baseline | Ngưỡng đạt |
|---|---|---|---|
| Adoption quiz | Số học viên hoàn thành quiz / số học viên được mời; nhóm lab đo từ Forms/LMS | 0% vì chưa có quiz formative AI sau bài học | ≥60% học viên pilot hoàn thành quiz trong 48 giờ |
| Chất lượng citation | Coach review mẫu feedback và kiểm tra section được dẫn | Chưa có citation tự động; baseline = chưa đo | 0 feedback bịa nguồn; ≥80% citation được coach xác nhận đúng/đủ |
| Độ đúng của tag misconception | Coach review tối thiểu 20-30 câu trả lời hoặc toàn bộ câu bị AI gắn misconception | Chưa có tag misconception; baseline = chưa đo | ≥80% tag trong mẫu được coach xác nhận đúng |
| Hiệu quả sửa hiểu sai | Tỉ lệ câu sai/gần đúng được học viên làm lại đúng sau gợi ý; nhóm lab đo từ quiz retry hoặc câu follow-up | Giả định hiện chưa đo được; cần lấy baseline từ lần làm đầu | ≥50% câu sai/gần đúng được sửa đúng ở lần thử lại |
| Giảm tải câu hỏi lặp | So sánh số câu hỏi misconception lặp lại trên Discord/coaching sau bài pilot; coach ghi nhận | Giả định hiện có khoảng 8 câu hỏi/bài từ 01-frame | Giảm ≥25% câu hỏi lặp về cùng misconception trong bài pilot |

   Leading indicator (biết kết quả sớm trong 1–2 tuần): Tỉ lệ hoàn thành quiz trong 48 giờ và tỉ lệ câu hỏi/citation được coach duyệt trước khi phát hành.

9. **Exit criteria** (định trước, ≥2 mức):

| Mức | Điều kiện | Hành động | Ai có quyền dừng |
|---|---|---|---|
| Cảnh báo | Adoption <60% hoặc coach phải sửa >20% citation/câu hỏi trước khi phát hành | Tối ưu flow, rút ngắn quiz, sửa prompt/citation, chạy lại trên 1 bài học nhỏ hơn | Instructor/coach yêu cầu sửa trước khi chạy tiếp |
| Nghiêm trọng | Có feedback bịa nguồn, tag misconception đúng <70%, hoặc học viên hiểu nhầm kết quả là điểm chính thức | Dừng pilot, không mở rộng; chỉ dùng lại sau khi sửa review gate và wording formative | Pilot owner/instructor track Product |
| Dừng mở rộng | Sau 3 tuần không đạt ≥2 metric chính: adoption, citation, tag misconception, sửa hiểu sai | Không scale sang toàn khóa; ghi learning và quay lại scope khác | Program lead/instructor |

   *Liên hệ 2 Red Flag ở `00-context.md`: exit criteria có chặn được chúng không?*

10. **Adoption** (tool không ai dùng = $0): Người dùng đầu tiên là học viên track Product ngay sau 1-2 bài học được chọn, không triển khai cho cả 500 học viên. Workflow đổi ở chỗ sau bài học, học viên nhận link quiz 5-7 câu trong LMS/Discord, làm trong 48 giờ và nhận feedback học lại có citation. Coach/instructor giới thiệu rõ đây là formative, không tính điểm; nhóm lab support lỗi form/API và tổng hợp kết quả. Nếu adoption thấp, không ép mở rộng; nhóm phỏng vấn nhanh 5-7 học viên để biết vướng ở thời điểm, độ dài quiz hay chất lượng feedback rồi quyết định sửa hoặc dừng.

---

## Tự phản biện

- Budget thiếu hạng mục ẩn nào không?
- Exit criteria đủ mạnh để THẬT SỰ dừng, hay chỉ trên giấy?
- Giả định quan trọng nhất sai → plan gì?

Trả lời thử:

- Budget dễ thiếu thời gian chuẩn hóa citation và thời gian coach review sau khi có câu trả lời thật; đã tách riêng hai phần này để tránh coi API là chi phí duy nhất.
- Exit criteria có người dừng rõ: instructor/pilot owner được quyền dừng nếu feedback bịa nguồn, tag misconception thấp hoặc học viên hiểu nhầm là điểm chính thức.
- Giả định quan trọng nhất là học viên sẽ làm quiz sau bài học. Nếu sai, nhóm không scale; trước tiên giảm quiz xuống 3-5 câu, gắn quiz vào workflow LMS/live recap, hoặc chuyển Quick Win sang công cụ cho coach tạo câu hỏi thay vì học viên tự dùng.

---

## Tổng kiểm tra trước khi sang `2-FINAL-pitch.md`

| Hạng mục | Xong? |
|---|---|
| Tóm vấn đề trong 1 câu | x |
| Budget tách hạng mục, không "miscellaneous" | x |
| Metric có baseline + ngưỡng + ai đo | x |
| Exit criteria có người có quyền thực thi (≥2 mức) | x |
| Adoption: chỉ rõ ai dùng đầu tiên (không "cả khóa") | x |

⚑ Coach kiểm tra ở Mốc 4: *"Xin gì? Hứa gì? Đo gì? Dừng khi nào?"*

Sau bước này, mở `2-FINAL-pitch.md` — dồn tất cả thành 5-slide pitch + AI Support Log.

*Liên quan: handbook §A7+§A8 · `templates/ai-pilot-plan-core.md` · `prompts/06-pilot-plan-challenge.md`*
