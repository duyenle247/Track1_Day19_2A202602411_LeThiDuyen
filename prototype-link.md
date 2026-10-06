# Prototype Links & Testing Kit

- **Họ và tên:** Lê Thị Duyên
- **Mã học viên:** 2A202602411
- **Nhóm:** Nhóm [Số nhóm] · **Case:** AI Tutor (Nền tảng học trực tuyến VLearn)

---

## 1. Danh sách Link Prototype (Test-Ready)

| Phương án | Tên cơ chế | Link Interactive Prototype | Định dạng & Công cụ dựng | Người chịu trách nhiệm chính |
| :--- | :--- | :--- | :--- | :--- |
| **Option A** | In-Context Prerequisite Diagnosis | [Mở Interactive Prototype (Chạy trực tiếp)](./prototype.html) / [Figma Prototype](https://www.figma.com/proto/placeholder-day19/Option-A-Diagnosis) | HTML/CSS Interactive + Figma Clickable | **Lê Thị Duyên** |
| **Option B** | Knowledge Graph & Concept Breakdown | [Mở Interactive Prototype (Chạy trực tiếp)](./prototype.html) / [Figma Prototype](https://www.figma.com/proto/placeholder-day19/Option-B-ConceptMap) | HTML/CSS Interactive + Figma Clickable | [Thành viên 2] |
| **Option C** | Smart Bookmark & Socratic Sync | [Mở Interactive Prototype (Chạy trực tiếp)](./prototype.html) / [Figma Prototype](https://www.figma.com/proto/placeholder-day19/Option-C-Bookmark) | HTML/CSS Interactive + Figma Clickable | [Thành viên 3] |

> 💡 **Cách mở nhanh Prototype tương tác:**  
> File micro-prototype HTML tương tác đã được tích hợp sẵn ngay trong repo tại [`prototype.html`](./prototype.html). Bạn có thể mở trực tiếp bằng bất kỳ trình duyệt nào (Chrome, Edge, Safari) để chuyển đổi qua lại giữa A / B / C và thử nghiệm tương tác mượt mà như app thật!

---

## 2. Dữ liệu chuẩn & 70% Common Context dùng chung

- **Context Screen:** Màn hình video player bài giảng giao diện web VLearn.
- **Tiêu đề bài học:** *"Khóa học Machine Learning cơ bản — Bài 4: Tối ưu hóa mô hình với Gradient Descent"*.
- **Content Fixture:**
  - Slide hiển thị tại phút 08:30:
    - Tiêu đề slide: *"Cập nhật trọng số với Đạo hàm riêng và Learning Rate"*.
    - Công thức: $\theta_j := \theta_j - \alpha \frac{\partial}{\partial \theta_j} J(\theta)$.
    - Đồ thị cong minh họa hướng dốc đi xuống cực tiểu cục bộ.
- **Điểm gây tắc nghẽn (Intended Bottleneck):** Người học không hiểu ký hiệu đạo hàm riêng $\frac{\partial}{\partial \theta_j}$ và tại sao phải trừ đi thay vì cộng vào.

---

## 3. Kịch bản & Nhiệm vụ giao cho Tester (Test Script & Outcome Task)

### A. Mở đầu (Opening — 0 đến 2 phút)
> *"Cảm ơn bạn đã tham gia buổi trải nghiệm hôm nay. Mình đang cùng nhóm thử nghiệm ba cách thiết kế giao diện hỗ trợ học tập khác nhau, hoàn toàn không phải bài kiểm tra kiến thức của bạn. Trong suốt quá trình, không có thao tác nào là đúng hay sai.*  
> *Bạn hãy tự do click, khám phá trên màn hình và vui lòng **nói to suy nghĩ thành tiếng (think-aloud)** về những gì bạn thấy và dự định làm. Mình sẽ ngồi quan sát và hạn chế tối đa việc giải thích để đảm bảo tính khách quan."*

### B. Câu hỏi bối cảnh ngắn (Relevant Context Check)
> *"Gần đây khi học bài hoặc đọc tài liệu trên mạng, bạn có hay gặp phải trường hợp đọc một slide/đoạn văn mà thấy toàn từ chuyên ngành khó hiểu, không biết mình đang bị hổng kiến thức từ đâu không? Những lúc đó bạn thường làm gì?"*

### C. Nhiệm vụ cốt lõi (Outcome Task — Dùng chung cho cả A/B/C)
> *"Giả sử bạn đang học bài giảng này và đang bị kẹt, không hiểu công thức đạo hàm trên slide.*  
> **Hãy dùng từng phương án giao diện trên màn hình để làm sao bạn vượt qua được chỗ khó hiểu này và có thể tự tin học tiếp.**"  
> *(Tuyệt đối không chỉ dẫn: 'Bạn bấm vào nút AI này đi', 'Bạn xem cái cây bên phải đi').*

### D. So sánh & Đánh đổi sau khi trải nghiệm xong cả 3 options (Compare — 14 đến 18 phút)
1. *"Trong tình huống học thực tế của bạn, bạn sẽ chọn phương án A, B hay C? Vì sao?"*
2. *"Ở phương án bạn chọn, bạn muốn tự mình làm phần nào và muốn AI tự động làm phần nào?"*
3. *"Điều gì ở phương án bạn vừa chọn khiến bạn vẫn cảm thấy lấn cấn hoặc chưa thực sự thoải mái?"*

---

## 4. Definition of Testable Checklist (Gate 4 Verification)

- [x] Cả 3 prototype đều chia sẻ cùng bài giảng, cùng slide và cùng công thức toán học.
- [x] Tester tự click và điều hướng được mà không cần người bên cạnh bấm hộ.
- [x] Mỗi phương án đều có điểm hiển thị rõ ràng: Expectation, Evidence/Uncertainty, và nút Control/Recovery (X, Hủy, Quay lại).
- [x] Có nút Reset rõ ràng để tester thử lần lượt cả 3 option.
