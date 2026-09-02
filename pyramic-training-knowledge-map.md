# PYRAMIC Training System — Knowledge Map (SID Decomposition)

Nguồn: [A] Science and Development of Muscle Hypertrophy (Brad Schoenfeld)
       [B] The Muscle and Strength Training Pyramid: Nutrition 2.0 (Eric Helms)

---

## 1. FRAMING BRIEF (SID L1)

| Thành phần | Giá trị |
|---|---|
| Topic | Tập luyện phì đại cơ bắp (hypertrophy) + dinh dưỡng nền cho người tập gym tự nhiên |
| Nguồn kiến thức | [A] Schoenfeld (chương 1–9) + [B] Helms (Level 1–5 + Adjustment) |
| Audience | Người tập gym, beginner → intermediate, mục tiêu tăng cơ/giảm mỡ bền vững |
| In scope | Khoa học hypertrophy, thiết kế chương trình, dinh dưỡng nền, đo lường tiến độ, điều chỉnh |
| Out of scope | Chẩn đoán y tế, điều trị chấn thương, doping, khung giờ ăn chuyên biệt cho VĐV đỉnh cao |
| Output artifacts | Kế hoạch 12 tuần, thẻ động tác, công thức dinh dưỡng, check-in, review tuần |

---

## 2. CONCEPTUAL DECOMPOSITION (SID L3)

```text
PYRAMIC Training System
├── 1. Cơ chế sinh học của hypertrophy
│   ├── 1.1. Mechanical Tension [A-Ch2]
│   ├── 1.2. Metabolic Stress [A-Ch2]
│   ├── 1.3. Muscle Damage [A-Ch2]
│   ├── 1.4. Sarcoplasmic vs Myofibrillar Hypertrophy [A-Ch3]
│   └── 1.5. Epigenetic Memory / Satellite Cells [A-Ch7]
├── 2. Biến số tập luyện (Training Variables)
│   ├── 2.1. Volume — sets/muscle/week [A-Ch4, p78-91]
│   ├── 2.2. Frequency — lần/tuần [A-Ch4, p86-91]
│   ├── 2.3. Load — %1RM / rep range [A-Ch4, p92-99]
│   ├── 2.4. Exercise Selection — chọn bài [A-Ch4, p100-103]
│   ├── 2.5. Rest Interval — nghỉ giữa set [A-Ch4, p111-114]
│   ├── 2.6. Repetition Duration — tốc độ rep [A-Ch4, p115-122]
│   ├── 2.7. Exercise Order — thứ tự bài [A-Ch4, p123-125]
│   ├── 2.8. Range of Motion — biên độ [A-Ch4, p126-128]
│   └── 2.9. Intensity of Effort — RIR/RPE [A-Ch4, p129-135]
├── 3. Thiết kế chương trình
│   ├── 3.1. Biomechanics & Exercise Selection Strategies [A-Ch8, p178-189]
│   ├── 3.2. Periodization [A-Ch8, p190-210]
│   ├── 3.3. Split routine vs Full-body [A-Ch4]
│   ├── 3.4. Double progression system [A-Ch4, synthesis]
│   └── 3.5. Advanced techniques (drop set, superset, ecc overload) [A-Ch5]
├── 4. Dinh dưỡng nền (Nutrition Pyramid)
│   ├── 4.1. Energy Balance — tìm maintenance, deficit/surplus [B-L1, p42-73]
│   ├── 4.2. Protein — g/lb theo giai đoạn [B-L2, p77-82]
│   ├── 4.3. Carbs & Fat — phân bổ % calo [B-L2, p82-91]
│   ├── 4.4. Fiber & Micronutrients [B-L2/3, p96-113]
│   ├── 4.5. Nutrient Timing & Meal Frequency [B-L4, p117-141]
│   └── 4.6. Supplementation [B-L5, p142-164]
├── 5. Đo lường và theo dõi
│   ├── 5.1. Methods: Circumference, US, CT, MRI, Biopsy [A-Ch3, p57-77]
│   ├── 5.2. Cân nặng — trend 7-14 ngày [B-Adjustment, p180-183]
│   ├── 5.3. Waist/body circumference [B-Adjustment, p188-191]
│   ├── 5.4. Visual assessment [B-Adjustment, p184-185]
│   └── 5.5. Performance assessment [B-Adjustment, p186-187]
├── 6. Điều chỉnh và thích ứng
│   ├── 6.1. Rate of weight loss/gain [B-L1, p54-66]
│   ├── 6.2. Diet Breaks & Refeeds [B-L4, p118-127]
│   ├── 6.3. Recovery Diet / Reverse Diet [B-Recovery, p226-231]
│   ├── 6.4. Fatigue management & Deload [A-Ch4 + A-Ch8]
│   └── 6.5. Plateau troubleshooting [A-Ch7 + B-Adjustment]
└── 7. Yếu tố cá nhân
    ├── 7.1. Genetics — responders vs non-responders [A-Ch7, p166-169]
    ├── 7.2. Age — sarcopenia [A-Ch7, p170-171]
    ├── 7.3. Sex differences [A-Ch7, p173-174]
    └── 7.4. Training Status [A-Ch7, p175-177]
```

---

## 3. FUNCTIONAL DECOMPOSITION (Quy trình từ input → output)

```text
User profile + goals
→ Assessment (Level 1: Energy Balance [B-L1])
→ Level 2: Macro setup [B-L2]
→ Program Design (Training Variables [A-Ch4])
→ Exercise Selection [A-Ch8]
→ Weekly Schedule A/B/C
→ Daily Check-in + adjustment
→ Weekly Review + one-variable change
→ Periodization block (4-12 weeks)
→ Recovery / Deload / Diet Break [B-L4]
→ Next block
```

---

## 4. RULE LIBRARY (có Rule ID + Nguồn)

### 4.1. Volume (số set mỗi nhóm cơ mỗi tuần)

| Rule ID | Quy tắc | Nguồn | Loại | Ngoại lệ |
|---------|--------|-------|------|----------|
| VOL-01 | Khuyến nghị chung: 10–20 sets/nhóm cơ/tuần để tối đa hypertrophy | [A-Ch4, p84] | Fact | Beginner có thể đáp ứng với 5–10 sets; advanced có thể cần 20+ |
| VOL-02 | Trên ~10 sets/buổi cho một nhóm cơ, lợi ích thêm giảm dần | [A-Ch4, p84-85] | Fact | Nếu tập total-body, volume có thể cao hơn trước khi bão hoà |
| VOL-03 | Lagging muscle groups: có thể tăng volume trên mức trung bình trong một chu kỳ | [A-Ch4, p85] | Recommendation | Chỉ ưu tiên một nhóm cơ mỗi chu kỳ; xoay vòng |
| VOL-04 | Periodize volume: tăng dần qua chu kỳ, cài tuần giảm volume để phục hồi | [A-Ch4, p84] | Recommendation | Không khuyến khích volume cao kéo dài không nghỉ |

### 4.2. Frequency (số lần tập mỗi nhóm cơ mỗi tuần)

| Rule ID | Quy tắc | Nguồn | Loại | Ngoại lệ |
|---------|--------|-------|------|----------|
| FREQ-01 | Volume-equated: hypertrophy tương tự giữa tần suất cao và thấp | [A-Ch4, p87] | Fact | Khi tổng volume cố định, tần suất không ảnh hưởng nhiều |
| FREQ-02 | Khi volume cao (≥20 sets/nhóm cơ/tuần), cần frequency ≥2 để tránh vượt ngưỡng per-session | [A-Ch4, p87] | Recommendation | Nếu tập 1 buổi/tuần với 20 sets, chất lượng set cuối xuống |
| FREQ-03 | Cách tối thiểu 48h giữa các buổi cho cùng nhóm cơ | [A-Ch4, p86] | Recommendation | Có thể 72h nếu volume cao hoặc recovery kém |

### 4.3. Load (cường độ tạ)

| Rule ID | Quy tắc | Nguồn | Loại | Ngoại lệ |
|---------|--------|-------|------|----------|
| LOAD-01 | Hypertrophy đạt được ở nhiều khoảng rep: 6–15RM là phổ biến | [A-Ch4, p92-99] | Fact | Có thể dùng 15–30RM cho Type I fibers; 3–5RM cho neural adaptation |
| LOAD-02 | Kết hợp nhiều khoảng tải có lợi cho hypertrophy toàn diện | [A-Ch4, synthesis] | Recommendation | Không cần thiết trong mọi buổi; periodize theo block |
| LOAD-03 | Double progression: tăng reps → đạt đầu trên rep range → tăng tạ → quay lại đầu dưới | [A-Ch4, synthesis] | Recommendation | Không tăng tạ nếu form hỏng hoặc recovery kém |

### 4.4. Exercise Selection

| Rule ID | Quy tắc | Nguồn | Loại |
|---------|--------|-------|------|
| EX-01 | Chọn bài theo movement pattern: squat, hinge, horizontal push/pull, vertical push/pull, core | [A-Ch4, p100-103] | Recommendation |
| EX-02 | Ưu tiên bài ổn định, có thể tăng tải dần, cho phép đo lường tiến bộ | [A-Ch4, p100] | Recommendation |
| EX-03 | Có bài thay thế cho mỗi movement pattern (dễ hơn và khó hơn) | [A-Ch4, synthesis] | Recommendation |

### 4.5. Nutrition — Energy Balance

| Rule ID | Quy tắc | Nguồn | Loại |
|---------|--------|-------|------|
| NB-01 | Tìm maintenance: 2 tuần cân + track calo, tính trung bình 7 ngày | [B-L1, p44-46] | Recommendation |
| NB-02 | Công thức ước lượng: [cân nặng(lb) × 10] × activity multiplier (1.3–2.2) | [B-L1, p47-48] | Assumption |
| NB-03 | Fat loss: 0.5–1% body weight/tuần để giữ cơ và performance | [B-L1, p54-55] | Recommendation |
| NB-04 | Muscle gain: 0.25–0.5% body weight/tuần (nam), 0.125–0.25% (nữ) | [B-L1, p59-60] | Recommendation |
| NB-05 | "3500 calorie rule": 1 lb (~0.5 kg) mỡ ≈ 3500 calo — dùng để ước lượng, không tuyệt đối | [B-L1, p46] | Assumption |

### 4.6. Nutrition — Protein

| Rule ID | Quy tắc | Nguồn | Loại |
|---------|--------|-------|------|
| PRO-01 | Cutting: 1.0–1.2 g/lb (2.2–2.6 g/kg) body weight | [B-L2, p81] | Recommendation |
| PRO-02 | Gaining/Maintenance: 0.8–1.0 g/lb (1.6–2.2 g/kg) | [B-L2, p78-84] | Recommendation |
| PRO-03 | Người béo phì: dùng chiều cao (cm) làm target protein (g) | [B-L2, p82] | Recommendation |
| PRO-04 | Protein tính trên total body weight, không lean mass (trừ khi có số liệu chính xác) | [B-L2, p81-82] | Recommendation |

### 4.7. Nutrition — Carbs & Fat

| Rule ID | Quy tắc | Nguồn | Loại |
|---------|--------|-------|------|
| MAC-01 | Sau khi đặt protein, phân bổ calo còn lại: fat tối thiểu 0.45 g/lb (1 g/kg), phần còn lại là carbs | [B-L2, p82-84] | Recommendation |
| MAC-02 | Fat tối thiểu: 15–20% tổng calo để duy trì hormone | [B-L2, p84] | Fact |
| MAC-03 | Carbs: ưu tiên quanh buổi tập để hỗ trợ performance | [B-L4, p132-136] | Recommendation |

### 4.8. Progression & Adjustment

| Rule ID | Quy tắc | Nguồn | Loại |
|---------|--------|-------|------|
| ADJ-01 | Chỉ thay đổi một biến sau 10–14 ngày dữ liệu đủ | [B-Adjustment] | Recommendation |
| ADJ-02 | Nếu cân nặng trend + waist + performance đều ổn định: giảm 100–150 kcal/ngày hoặc tăng 1500–2000 bước/ngày | [B-Adjustment] | Recommendation |
| ADJ-03 | Nếu giảm cân quá nhanh + fatigue/strength giảm: không thắt chặt, tăng nhẹ calo hoặc giảm volume | [B-Adjustment, p54-55] | Recommendation |
| ADJ-04 | Diet break: 1–2 tuần ăn maintenance sau 8–12 tuần diet liên tục | [B-L4, p118-121] | Recommendation |
| ADJ-05 | Deload: giảm 30–50% volume, giữ nguyên tạ, trong 1 tuần khi có dấu hiệu fatigue tích luỹ | [A-Ch4 synthesis] | Recommendation |

### 4.9. Safety

| Rule ID | Quy tắc | Nguồn | Loại |
|---------|--------|-------|------|
| SFT-01 | Đau ngực, ngất, khó thở bất thường, tim đập nhanh: dừng, tìm đánh giá y tế | [A-Ch1-9] | Fact |
| SFT-02 | Đau nhói, sưng, mất khả năng chịu lực, mất chức năng: dừng, tìm chuyên môn | [A-Ch1-9] | Fact |
| SFT-03 | Bệnh nền/thuốc ảnh hưởng tập ăn: không tự đặt mục tiêu, yêu cầu clearance chuyên môn | [B-Introduction] | Fact |
| SFT-04 | Không khuyến nghị dưới BMR hoặc quá 1% body weight/tuần | [B-L1, p54-55] | Fact |
| SFT-05 | Không khuyên nhịn bù, tập phạt, detox, steroid | [A-Ch9 + B-L1] | Fact |

---

## 5. PRACTICAL APPLICATION RULES (tổng hợp từ 2 sách)

### 5.1. Khi thiết kế kế hoạch cho beginner

- Bắt đầu với 5–10 sets/nhóm cơ/tuần [VOL-01]
- Tần suất: 2–3 lần/tuần/nhóm cơ [FREQ-01]
- Khoảng rep: 8–15, RIR 2–4 [LOAD-01]
- Chọn bài compound + máy, ít biến thể [EX-01]
- Protein: 1.0 g/lb (2.2 g/kg) [PRO-01]
- Calo: maintenance hoặc deficit nhẹ (200–300 calo) [NB-03]

### 5.2. Khi thiết kế kế hoạch cho intermediate

- 10–20 sets/nhóm cơ/tuần [VOL-01]
- Tần suất: 2 lần/tuần/nhóm cơ [FREQ-02]
- Khoảng rep: 6–15, RIR 1–3 [LOAD-01, LOAD-03]
- Periodize volume: foundation → build → consolidate [VOL-04]
- Protein: 1.0–1.2 g/lb (cutting) / 0.8–1.0 g/lb (gaining) [PRO-01, PRO-02]
- Diet break mỗi 8–12 tuần nếu đang cut [ADJ-04]

### 5.3. Khi review tiến độ

- Trend 7–14 ngày, không snapshot [NB-01]
- Co-signals: cân nặng, vòng eo, performance, adherence, sleep, hunger, energy [B-Adjustment]
- Chỉ thay đổi một biến [ADJ-01]
- Gắn nhãn Fact/Assumption/Hypothesis [SID L7]

---

## 6. CONVERSATION STARTER (dùng để gửi chatbot)

```
Mình là người mới, chưa biết tập các động tác này thế nào. Hãy dùng toàn bộ PYRAMIC Training Knowledge Map (Rule ID VOL-01 đến SFT-05, từ sách Schoenfeld và Helms) trong Knowledge để thiết kế kế hoạch tập luyện cho mình.

Trước khi trả lời, truy xuất Rule ID phù hợp theo thứ tự: Frame → Training Variables → Program Design → Exercise Selection → Nutrition → Progression → Safety → Review.

Với TỪNG động tác, tạo Thẻ Động Tác gồm:
1. Setup (đặt tay/chân/ghế/tải ở đâu)
2. 3–4 cue thực hiện, kèm nhịp thở
3. Cảm giác đúng — mình nên thấy căng ở đâu
4. Lỗi người mới thường gặp + cách sửa
5. Khi nào phải dừng
6. PROMPT TẠO ẢNH: prompt tiếng Anh, góc quay 3/4, có mũi tên hướng chuyển động, có chú thích khớp cần thấy rõ
7. TỪ KHOA VIDEO: 1 cụm tiếng Anh + 1 tiếng Việt để tìm video đúng kỹ thuật

Kế hoạch 12 tuần gồm: Foundation (4 tuần) → Build (4 tuần) → Consolidate (4 tuần). Mỗi tuần: lịch A/B/C, sets × reps, RIR, nghỉ, bài thay thế. Giải thích Double Progression. Quy tắc bỏ buổi, deload, fatigue. Dinh dưỡng nền: maintenance → deficit nhẹ. Check-in hằng ngày, Review tuần, chỉ thay đổi một biến sau 10–14 ngày.

Phân tách Fact từ sách/Assumption/Hypothesis/Recommendation + Confidence. Ghi [Rule ID] và [Nguồn] cho mọi quy tắc quan trọng. Xưng hô mình–bạn, tiếng Việt đời thường, cổ vũ thực tế, không hứa kết quả, ưu tiên Safety Gate.
```

---

## 7. DEPLOYMENT NOTES

### 7.1 Vai trò của file này

File này là **bản đồ điều hướng và Rule Index**, không phải toàn văn hai cuốn sách. Nó giúp GPT tìm đúng chủ đề, Rule ID và nhánh kiến thức trước khi trả lời. Khi chưa có PDF sách gốc, các con trỏ chương/trang trong file chỉ được xem là **citation chưa xác minh độc lập**.

### 7.2 Hai PDF sách nguồn — thêm vào Knowledge khi có file

Hai nguồn gốc của bản đồ này:

| Ký hiệu | Sách | Tên file nên đặt khi upload |
|---|---|---|
| `[A]` | Brad Schoenfeld — *Science and Development of Muscle Hypertrophy* | `source-a-schoenfeld-hypertrophy.pdf` |
| `[B]` | Eric Helms — *The Muscle and Strength Training Pyramid v2.0: Nutrition* | `source-b-helms-nutrition-pyramid-v2.pdf` |

Đổi tên file trước khi upload. Tên gốc tải về thường có hậu tố nhà phân phối và ký tự lạ, làm GPT trích dẫn lộn xộn và khó viết `[A-Ch4]` / `[B-L2]` cho đúng.

Lưu ý chất lượng file: nếu PDF là bản scan ảnh không có lớp text, GPT sẽ không tra được đoạn/trang cụ thể. Trước khi coi PDF là nguồn truy xuất được, hãy thử một câu kiểm tra như "tra trong file `[B]` phần Level 2 nói gì về protein" và xem GPT có dẫn được nội dung thật hay không. Nếu không, giữ nguyên trạng thái S1 ở `v3-03` và dùng bản đồ này làm nguồn chính.

Hiện thư mục dự án mới có **1 PDF kế hoạch 12 tuần**, chưa có hai PDF sách nguồn. Không đổi tên hoặc tạo PDF giả để lấp chỗ. Chỉ thêm hai file khi bạn có bản PDF đọc được.

### 7.3 Luật nâng độ tin cậy khi PDF đã được thêm

- Trước khi có PDF sách: Rule map là T1 ở mức **Rule ID nội bộ**, còn dẫn chương/trang là T2 — chưa xác minh toàn văn.
- Sau khi PDF sách đã upload: khi GPT truy xuất được đúng đoạn, có thể ghi nguồn dạng `[A-Ch4, trang x]` hoặc `[B-L2, trang y]`.
- Nếu GPT không truy xuất được trang/đoạn cụ thể: vẫn dùng T2, không nói "sách viết" như đã đối chiếu.
- Không trộn hai sách thành một nguồn. `[A]` là Schoenfeld; `[B]` là Helms.
- Khi hai nguồn hoặc hai file V2 mâu thuẫn, áp dụng `v3-03-retrieval-and-citation-contract.md` và SSOT V3; ghi nhận mâu thuẫn thay vì tự che đi.

### 7.4 Quy tắc upload

Upload **file này trước hai PDF sách**, để GPT có bản đồ Rule ID và biết PDF nào là nguồn A/B. Sau đó upload PDF A và PDF B. Không upload bản scan mờ nếu mục tiêu là trích trang/câu chữ; nếu chỉ có bản scan, cần kiểm tra khả năng OCR của GPT trước khi coi là nguồn truy xuất được.

### 7.5 Không upload PDF kế hoạch mẫu như nguồn nền

`TẬP LUYỆN ĐỀ XUẤT/ke-hoach-12-tuan-88kg (1).pdf` là tài liệu chương trình đầu vào, không phải sách nguồn. Chỉ upload khi muốn audit/adapt theo `one-request-full-pdf-validation-instruction.md`; không dùng nó làm bằng chứng cho mọi khuyến nghị.

- `custom-gpt-compact-instruction.md` cần cập nhật: thêm file này vào danh sách ưu tiên, ngay sau `master-instruction.md` hoặc trước `training-journey-specification.md`.
- `master-instruction.md` cần cập nhật: thêm dòng yêu cầu truy xuất Rule ID từ PYRAMIC Knowledge Map.
- Khi có sách dạng PDF, nên trích xuất thêm các trang cụ thể cho từng Rule ID và dẫn nguồn chính xác.

---

**Confidence:**
- High: Volume, Frequency, Load, Exercise Selection, Rest Interval, Protein, Energy Balance, Adjustment Rules — các quy tắc này có nguồn peer-reviewed và đồng thuận cao.
- Medium: Advanced techniques (drop set, superset), individual response, optimal rep ranges for specific fiber types — còn phụ thuộc cá nhân và chưa có đồng thuận tuyệt đối.