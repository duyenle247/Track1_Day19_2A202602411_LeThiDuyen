# Group Feedback Synthesis — Tổng hợp Phản hồi Toàn nhóm

- **Nhóm:** Nhóm [Số nhóm] · **Case:** AI Tutor (Nền tảng học trực tuyến VLearn)
- **Thành viên nhóm:** Lê Thị Duyên (2A202602411), [Thành viên 2], [Thành viên 3]
- **Link Artifact tổng hợp chung của nhóm (FigJam / Google Sheets):** [Link Tổng Hợp Feedback](https://www.figma.com/file/placeholder-day19-feedback-synthesis)

---

## 1. Bảng ma trận đối chiếu 3 Phiên Kiểm thử độc lập

| Tiêu chí | Feedback 1 (Tester 1 - Lê Thị Duyên facilitate) | Feedback 2 (Tester 2 - Thành viên 2 facilitate) | Feedback 3 (Tester 3 - Thành viên 3 facilitate) | Pattern hoặc Khác biệt chung |
| :--- | :--- | :--- | :--- | :--- |
| **Bối cảnh tester** | SV năm 3 CNTT, tự học trên Coursera / Udemy. | Người đi làm học thêm văn bằng 2 buổi tối, thời gian eo hẹp. | Học sinh cấp 3 đang tự ôn thi đại học trên nền tảng học trực tuyến. | Cả 3 đều gặp tình trạng hổng kiến thức toán/lý thuyết nền nhưng áp lực thời gian học khác nhau. |
| **First Action** | Click ngay nút *"Chẩn đoán điểm tắc"* ở Option A; lướt nhìn sơ đồ ở Option B. | Click thử Option B trước vì thấy sơ đồ bắt mắt, nhưng lập tức bị rối; chuyển sang A. | Thử Option C (bấm ghim bookmark) vì quen thói quen ghi chú khi nghe giảng. | **Pattern:** Tester có xu hướng tìm hành động tốn ít công sức nhất ngay khi nhìn thấy màn hình. |
| **Breakdown chính (Điểm gãy tương tác)** | Ở Option C: bối rối mất 3s vì bấm ghim xong không thấy giải thích gì ngay. | Ở Option B: phàn nàn sơ đồ quá nhiều node, làm che mất slide video và không biết node nào quan trọng. | Ở Option A: băn khoăn nếu AI chẩn đoán sai câu hỏi trắc nghiệm thì có mất thời gian không. | **Pattern:** Cả 3 tester đều rất nhạy cảm với việc bị che khuất slide bài giảng và việc AI nói quá dài. |
| **Cách lấy lại control** | Click nút [X] ở Option A; bấm thu gọn panel ở Option B. | Bấm nút mũi tên đóng panel Option B ngay sau 10 giây vì thấy vướng màn hình. | Bấm nút *"Xem ngay gợi ý"* ở Option C khi câu hỏi ôn tập quá khó. | **Pattern:** Cả 3 tester đều nhanh chóng tìm thấy các nút thoát hiểm ([X], [Đóng], [Bỏ qua]) mà không cần hỏi người hướng dẫn. |
| **Option được chọn** | **Option A** (A > C > B) | **Option A** (A > B > C) | **Option C** (C > A > B) | **Khác biệt:** 2/3 tester chọn Option A vì cần hiểu ngay; 1/3 tester chọn Option C vì ưu tiên nghe liền mạch không bị ngắt quãng. |
| **Trade-off chấp nhận** | Chấp nhận dừng video 45s để làm micro-quiz đổi lấy sự rõ ràng để học tiếp. | Chấp nhận thao tác thêm 1 click chọn vùng slide để AI không trả lời lan man. | Chấp nhận không hiểu ngay lập tức trong bài học để giữ mạch nghe trọn vẹn, dồn việc học sâu về cuối giờ. | **Pattern về Trade-off:** Không có giải pháp hoàn hảo; người học luôn phải đánh đổi giữa **mạch nghe liên tục (flow)** và **sự thấu hiểu tức thời (comprehension)**. |

---

## 2. Các Patterns & Khác biệt cốt lõi phát hiện được

### Pattern 1: Bản đồ khái niệm (Option B) bị từ chối trong phiên học trực tiếp
- **Bằng chứng:** Cả 3 tester đều nhận định Option B gây "ngợp" (overwhelmed) và cạnh tranh thị giác trực tiếp với slide bài giảng của giảng viên. Cả 3 đều bấm nút đóng/thu gọn panel này trong vòng 15 giây đầu tiên.
- **Ý nghĩa:** Việc AI tự động "show off" toàn bộ cấu trúc kiến thức giữa lúc học tạo ra gánh nặng nhận thức (cognitive overload) thay vì giúp ích.

### Pattern 2: Tâm lý cần phản hồi vi mô có kiểm soát (Micro-interaction with control)
- **Bằng chứng:** Ở Option A, khi AI đưa ra 1 câu hỏi trắc nghiệm chẩn đoán ngắn (thay vì tuôn ra 1 bài văn), 2/3 tester cảm thấy an tâm và thấy AI "thực sự hiểu mình".
- **Ý nghĩa:** Người dùng sẵn sàng đánh đổi 30–60 giây dừng video NẾU họ cảm thấy họ đang nắm quyền kiểm soát và thông tin nhận lại cực kỳ ngắn gọn, trúng đích.

### Khác biệt giữa nhóm người học: Tranh luận giữa "Giải quyết ngay" vs. "Bảo toàn mạch nghe"
- **Tester 1 & 2:** Muốn giải quyết ngay tại chỗ (Option A) vì sợ nghe tiếp cũng như "vịt nghe sấm".
- **Tester 3:** Sợ bị tụt lại so với tốc độ của lớp/video nên thà ghim lại (Option C) để cuối giờ giải quyết một thể.

---

## 3. Quyết định định hướng của nhóm (Group Next Change)

### 🎯 Quyết định Next Change duy nhất nhóm chốt:
> **Nhóm quyết định phát triển hướng kết hợp (Hybrid Solution) với cơ chế cốt lõi là Option A (In-Context Diagnostic), bổ sung cơ chế lưu vết tự động của Option C, đồng thời loại bỏ giao diện thường trực của Option B.**

- **Cụ thể tương tác mới:**
  1. Khi gặp điểm tắc, user click *"Chẩn đoán điểm tắc"* (Option A). AI chỉ hiển thị 1 câu hỏi trắc nghiệm 3 lựa chọn trong một popup nhỏ mờ (glassmorphism) không che slide.
  2. Sau khi user chọn, AI đưa ra đúng 2 dòng tóm tắt bản chất khái niệm hổng + 1 nút *"Đã hiểu, học tiếp"*.
  3. Khi bấm *"Đã hiểu, học tiếp"*, hệ thống **tự động âm thầm lưu điểm này vào sổ tay ôn tập cuối giờ** (kế thừa Option C) để sau khi kết thúc bài học, user có thể làm bài tập củng cố nếu muốn, mà không bắt user phải nhớ bấm nút ghim.

### 📋 Evidence dẫn tới quyết định này:
- 2/3 tester chọn Option A vì tính giải quyết tức thời nhưng đều lo ngại việc nếu gặp nhiều điểm tắc thì sẽ mất nhiều thời gian.
- Tester 3 và Tester 1 đều đánh giá cao giá trị sư phạm của bộ câu hỏi ôn tập cuối giờ của Option C.
- Option B hoàn toàn thất bại ở vai trò hỗ trợ trực tiếp trong bài giảng (cả 3 tester đều tắt).

---

## 4. Điều vẫn chưa được chứng minh (Still Unproven — GATE 5 PASS)

> ⚠️ **Tuyên bố minh bạch của nhóm:**  
> Kết quả từ 3 buổi kiểm thử micro-prototype cho nhóm thấy tín hiệu rõ ràng về hành vi tương tác và sự đánh đổi của người học, **nhưng KHÔNG đồng nghĩa với việc giải pháp đã được chứng minh thành công (NOT validated for product/market demand)**.

**Những điều nhóm vẫn chưa chứng minh được sau 3 feedback:**
1. **Tần suất chịu đựng gián đoạn:** Chưa đo lường được nếu trong một bài giảng dài 45 phút mà user phải dừng lại 4–5 lần để làm chẩn đoán Option A thì họ có bị ức chế và từ bỏ tính năng hay không.
2. **Tỷ lệ chuyển đổi ôn tập cuối giờ:** Chưa chứng minh được trong môi trường tự học thực tế không có người giám sát, người học có thực sự mở lại mục ôn tập cuối giờ hay họ sẽ tắt trình duyệt ngay khi video kết thúc.
3. **Độ chính xác của thuật toán chẩn đoán AI:** Prototype mới chỉ dùng canned data (dữ liệu soạn sẵn cho 1 slide chuẩn). Khi áp dụng vào các slide đa dạng khác, liệu AI có nhận diện chính xác khái niệm tiên quyết hay lại hallucinate đưa ra câu hỏi không liên quan?
