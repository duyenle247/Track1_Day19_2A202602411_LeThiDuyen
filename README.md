# Track 1 — Day 19: Prototype & User Feedback Testing

## 1. Thông tin Cá nhân & Nhóm
- **Họ và tên:** Lê Thị Duyên
- **Mã học viên:** 2A202602411
- **Tên nhóm:** Matcha
- **Các thành viên trong nhóm:**
  1. **Lê Thị Duyên** (2A202602411) — Chịu trách nhiệm chính: Option A
  2. **Trần Thị Thúy** — Chịu trách nhiệm chính: Option B
  3. **Nguyễn Thùy Linh** — Chịu trách nhiệm chính: Option C
- **Case nghiên cứu:** **AI Tutor — Nền tảng học trực tuyến VLearn**

---

## 2. Hypothesis Problem của Nhóm
> **Khi đang theo dõi bài giảng trực tuyến có nhiều khái niệm phức tạp liên đới, học viên trực tuyến gặp khó khăn trong việc tiếp thu bài học liên tục vì không tự chẩn đoán được mình đang bị hổng kiến thức tiên quyết nào để tra cứu đúng trọng tâm, dẫn đến bị đứt gãy luồng học, tốn 1–3 tiếng tự mò mẫm sau giờ học hoặc bỏ dở nội dung.**

- **Bằng chứng từ Day 17 (Evidence Continuity):** 
  - Hành vi của P01 (Lê Thị Duyên phỏng vấn): Phải chụp màn hình gửi AI ngoài với prompt: *"Tôi không hiểu chỗ này, cho tôi một lộ trình hiểu cái gì trước cái gì sau"*.
  - Quote đắt giá: *"Thật ra em cũng không biết là nên bắt đầu từ đâu..."*
- **Điều vẫn chưa biết / chưa được chứng minh:** Liệu người học có sẵn sàng dừng video 30–60 giây để tương tác chẩn đoán với AI ngay trong bài giảng hay họ chỉ muốn lưu lại để xem sau khi hết video?

---

## 3. Ba Solution Options & Link Micro-Prototypes

| Phương án | Tên giải pháp & Cơ chế chính | Link Prototype | Trade-off cốt lõi |
| :--- | :--- | :--- | :--- |
| **Option A** | **In-Context Prerequisite Diagnosis** *(User-initiated)*: User khoanh vùng đoạn không hiểu -> AI phân tích slide và đưa ra câu hỏi trắc nghiệm chẩn đoán nhanh để tìm lỗ hổng kiến thức nền tảng. | [Chạy Prototype HTML](./prototype.html) / [Figma Prototype](https://www.figma.com/proto/placeholder-day19/Option-A-Diagnosis) | **Độ sâu vs. Đứt gãy luồng:** Bắt đúng bệnh nhưng tạm dừng video 45s để làm trắc nghiệm. |
| **Option B** | **Knowledge Graph & Concept Breakdown** *(AI-initiated)*: AI tự động parse slide và render một mini concept map bên lề; làm nổi bật các khái niệm tiên quyết cần biết. | [Chạy Prototype HTML](./prototype.html) / [Figma Prototype](https://www.figma.com/proto/placeholder-day19/Option-B-ConceptMap) | **Tiện lợi vs. Cognitive Overload:** Không dừng bài giảng nhưng tạo gánh nặng thị giác lớn. |
| **Option C** | **Smart Bookmark & Socratic Sync** *(Deferred review)*: User bấm 1-click ghim điểm tắc; AI âm thầm lưu context và tạo bài tập phản tư gợi mở (Socratic) để giải quyết sau khi hết video. | [Chạy Prototype HTML](./prototype.html) / [Figma Prototype](https://www.figma.com/proto/placeholder-day19/Option-C-Bookmark) | **Bảo toàn luồng học vs. Độ trễ:** Giữ nguyên 100% mạch học nhưng phải chờ đến cuối giờ mới giải tỏa. |

> 💻 **Micro-Prototype tương tác sẵn dùng:** Xem trực tiếp tại file [`prototype.html`](./prototype.html) trong repo để test cả 3 phương án A/B/C với giao diện VLearn thật.

---

## 4. Đóng góp của Tôi trong Nhóm (Personal Contributions)
- **Thiết kế giải pháp & Micro-prototype:** 
  - Trực tiếp phụ trách thiết kế và xây dựng **Option A (In-Context Prerequisite Diagnosis)** trên code interactive HTML (`prototype.html`) và Figma.
  - Đồng thiết kế khung **70% Common Context** (màn hình slide viewer bài giảng VLearn Day 18+19, slide 7 *"Cùng một pain có thể dẫn tới nhiều cách giải"*) để đảm bảo cả 3 option có tính so sánh chuẩn xác.
- **Human–AI Design:** Xác định 4 quyết định thiết kế cho Option A (Expectation, Role & Agency [Ask], Evidence & Uncertainty, và đặc biệt là hệ thống nút thoát hiểm Recovery Control: [✕ Đóng], [Thử lại], [Bỏ qua quiz]).
- **Facilitation & Testing:** Trực tiếp đóng vai trò Facilitator, điều phối phiên kiểm thử toàn bộ 3 phương án A/B/C với Tester 1 (T01 - Sinh viên CNTT ngoài nhóm) theo đúng nguyên tắc không dẫn dắt.
- **Tổng hợp & Phân tích:** Độc lập thực hiện phân tích 4 lớp (*Observed, Interpreted, Decided, Still Unproven*) cho Feedback 1; đồng thời cùng nhóm thảo luận, đối chiếu ma trận kết quả 3 phiên và chốt định hướng Group Next Change.

---

## 5. Prototype Feedback & Group Next Change

### A. Tóm tắt quan sát từ phiên cá nhân facilitate (Tester 1)
- Tester chọn ngay nút chẩn đoán ở Option A và phản ứng rất tích cực khi AI chỉ hỏi 1 câu trắc nghiệm ngắn thay vì tuôn văn bản dài: *"Nó hỏi đúng chỗ mình lấn cấn chứ không tuôn ra một đống chữ bắt mình đọc"*.
- Tester bấm tắt Option B ngay sau 10 giây vì thấy sơ đồ chằng chịt gây phân tâm khỏi bài giảng.
- Ở Option C, tester bối rối mất vài giây vì không nhận được giải thích ngay, nhưng đánh giá cao giá trị ghi nhớ khi làm bài ôn tập cuối giờ.

### B. Ba-Feedback Synthesis (Tổng hợp toàn nhóm)
- **Pattern chung:** 2/3 tester chọn Option A; 1/3 chọn Option C. Cả 3 tester đều từ chối Option B vì gây quá tải nhận thức giữa giờ học.
- **Sự đánh đổi:** Người học luôn phải chọn giữa **hiểu ngay tại chỗ** (chấp nhận dừng luồng) và **bảo toàn mạch nghe giảng** (chấp nhận mang nỗi băn khoăn về cuối buổi).

### C. Group Next Change (Quyết định vòng lặp tiếp theo của nhóm)
- **Chốt giải pháp kết hợp (Hybrid):** Lấy **Option A làm tương tác cốt lõi** trong lúc học (1-question diagnostic popup nhẹ, không che slide), đồng thời **tự động lưu vết sang sổ ôn tập của Option C** để luyện tập củng cố sau giờ học mà không bắt user phải nhớ thao tác bấm ghim. Loại bỏ hoàn toàn bản đồ thường trực của Option B.

### D. Điều vẫn chưa được chứng minh (Still Unproven)
- Chưa chứng minh được liệu khi gặp 4–5 điểm tắc liên tục trong 1 bài giảng, người học có còn kiên nhẫn làm trắc nghiệm Option A hay không.
- Chưa chứng minh được tỷ lệ người học thực tế tự giác mở lại tab ôn tập cuối giờ khi học ở nhà không có người giám sát.

---

## 6. AI Support Log (Tóm tắt Nhật ký Sử dụng AI)
- **AI đã giúp gì:** Gợi ý các cơ chế tương tác trên phổ Initiative Spectrum; sinh canned dummy data về slide *Gradient Descent*; rà soát và loại bỏ các câu hỏi mang tính dẫn dắt / pitch giải pháp trong test script.
- **AI làm sai / hời hợt ở đâu:** AI ban đầu đề xuất chatbot tự do (vốn chỉ là wrapper của ChatGPT, không giải quyết được pain point); AI đề xuất các câu hỏi kiểm thử mang tính thiên vị người dùng ("Bạn có thích tính năng này không?"); AI quên thiết kế đường phục hồi (Recovery) khi AI đoán sai.
- **Tôi đã tự sửa gì:** Loại bỏ gợi ý chatbot tự do; tự tay xây dựng kịch bản Outcome Task khách quan; thiết kế các nút thoát hiểm [X] và [Chọn lại]; cam kết 100% dữ liệu quan sát và quotes từ tester là sự thật và tự tay viết toàn bộ reflection cá nhân.

---

## Danh mục tài liệu chi tiết đính kèm:
- [three-option-design-sheet.md](./three-option-design-sheet.md) — Chi tiết 3 phương án thiết kế & Human–AI Decision Table
- [prototype-link.md](./prototype-link.md) — Link micro-prototype tương tác & Kịch bản kiểm thử
- [prototype-feedback-note.md](./prototype-feedback-note.md) — Ghi chép chi tiết phiên kiểm thử cá nhân facilitate (4 lớp)
- [group-feedback-synthesis.md](./group-feedback-synthesis.md) — Tổng hợp kết quả 3 phiên, Pattern & Group Next Change
- [ai-support-log.md](./ai-support-log.md) — Nhật ký chi tiết phân định vai trò và kiểm chứng giữa người và AI
