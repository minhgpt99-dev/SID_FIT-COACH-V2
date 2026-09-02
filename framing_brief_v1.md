# Framing Brief — Chatbot Tập Luyện & Ăn Uống Cá Nhân


---

## 1. Chủ đề (Topic)

Xây dựng Custom GPT hỗ trợ tập luyện thể hình và lên lịch ăn uống cho người mới tập.

## 2. Bài toán (Problem)

Là người mới tập, chưa có nền tảng về phân chia bài tập theo nhóm cơ, nguyên tắc progressive overload, hay tính macro theo mục tiêu. Cần chatbot giúp:

- Thiết kế lịch tập theo tuần phù hợp với thời gian và trang thiết bị sẵn có
- Lên thực đơn theo mục tiêu calo/macro cụ thể
- Giải thích lý do đằng sau mỗi lựa chọn (để mình hiểu, không chỉ làm theo)
- Tạo file PDF tổng hợp lịch tập + meal plan, có mã QR link video bài tập
- Có Hình ảnh cụ thể ( giải phẫu từng nhóm cơ trong quá trình tập luyện )

**Mục đích cuối:** Hiểu được cách tự thiết kế lịch tập và bữa ăn, không chỉ nhận kết quả xong rồi quên.

**Task types chính:** design, explain

## 3. Audience

- **Ai dùng:** Bản thân  ; Mở rộng : Các Coaching sử dụng AI Để lên lịch cho người mới 
- **Trình độ:** Người mới tập 0–6 tháng, biết tập tạ cơ bản
- **Có thể làm if-else nếu tăng trình độ**, nhưng chưa biết cách tự thiết kế lịch tập/meal plan ( Validation khúc sau )
- **Nơi tập:** Mega Gym — An Dương Vương, TP.HCM (có đầy đủ: tạ đòn, máy, dây kháng lực, tạ tay, ghế tập)
- **Mục tiêu:** Hiểu đúng nguyên tắc, tránh chấn thương, tiến bộ đều, và có thể tự thiết kế lịch tập/meal plan sau khi được hướng dẫn
- **Thời gian:** 4–5 buổi/tuần, mỗi buổi 45–60 phút
- **Body stats:** 88kg | 1m68 | 27 tuổi | Mục tiêu: **recomposition** (tăng cơ + giảm mỡ cùng lúc)
- **TDEE ước tính:** ~2,775 kcal/ngày (moderate exercise)
- **Protein mục tiêu:** 140–194g/ngày (1.6–2.2g/kg)
- **Ẩm thực:** Việt Nam
- **Yêu cầu kỹ thuật:** Chatbot cần có **memory** (ghi nhớ cuộc hội thoại) và tự tính lại calo/macro khi user cập nhật dữ liệu mới

## 4. Scope (In-scope / Out-of-scope)

### In-scope

- Lịch tập theo tuần theo nhóm cơ
- Hướng dẫn kỹ thuật cơ bản
- Meal plan theo mục tiêu calo/macro
- Giải thích nguyên tắc dinh dưỡng cơ bản (protein, carb, fat, caloric surplus/deficit)

### Out-of-scope

- Lời khuyên y tế / chẩn đoán chấn thương
- Phác đồ tập cho vận động viên thi đấu
- Supplément nâng cao không có bằng chứng khoa học
- Chế độ ăn kiêng cực đoan

## 5. Output & Task Type

### Chatbot Functions

| Task | Mô tả |
|------|-------|
| **Design** | Thiết kế lịch tập theo tuần (split, bài tập, sets/reps) |
| **Design** | Lên thực đơn theo calo/macro mục tiêu |
| **Design** | Tạo file PDF tổng hợp lịch tập + thực đơn, có video  những bài tập liên quan kèm theo trong lúc tập|
| **Explain** | Giải thích lý do lựa chọn (tại sao tập bài này trước, tại sao cần X gram protein) |

### Output Format

- Lịch tập tuần (table/outline)
- Bảng thực đơn hàng ngày
- File PDF tổng hợp (có mã  link video bài tập)

## 6. Rủi ro nếu framing sai

| Rủi ro | Hệ quả |
|--------|--------|
| Không define rõ "người mới tập" | Chatbot gợi ý bài quá nặng hoặc quá nhẹ |
| Thiếu dietary constraints ( Những hạn chế trong chế độ ăn ) | Meal plan không khả thi (thức ăn không có sẵn, quá nhiều thời gian nấu) |
| Chỉ "trả lời câu hỏi" không có cấu trúc | Chatbot giỏi liệt kê nhưng không giúp người dùng hành động |
| Không xác định rõ mục tiêu tập | Lịch tập và meal plan không khớp với kết quả mong muốn |

## 7. Open Questions — ĐÃ TRẢ LỜI ✅

| Câu hỏi | Trả lời |
|---------|----------|
| Mục tiêu tập? | **Cả hai** — recomposition (tăng cơ + giảm mỡ) |
| Body stats? | 88kg, 1m68, 27 tuổi, TDEE ~2,775 kcal |
| Ẩm thực? | **Việt Nam** — ưu tiên món Việt, nguyên liệu dễ mua |
| Tính năng tính toán? | Cần tự tính calo/macro + **memory** ghi nhớ cuộc hội thoại |

---

## 8. Yêu cầu kỹ thuật (Technical Requirements)

| Yêu cầu | Chi tiết |
|---------|----------|
| **Memory** | Lưu lại: cân nặng, mục tiêu, lịch sử bữa ăn, lịch sử tập, phản hồi về难度 |
| **Tự tính toán** | Tính lại TDEE, calo, macro khi user cập nhật cân nặng hoặc mức độ hoạt động |
| **Personalization** | Điều chỉnh lịch tập theo equipment sẵn có, thời gian rảnh,.feedback về difficulty |
| **PDF export** | Tạo file PDF tổng hợp lịch tập + meal plan, có mã QR video bài tập |
| **Language** | Trả lời bằng tiếng Việt, ngôn ngữ đời thường, dễ hiểu |

---
