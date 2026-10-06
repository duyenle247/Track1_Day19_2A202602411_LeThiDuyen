# Three-Option Design Sheet

- **Họ và tên:** Lê Thị Duyên
- **Mã học viên:** 2A202602411
- **Nhóm:** Nhóm [Số nhóm] · **Case:** AI Tutor (Nền tảng học trực tuyến VLearn)
- **Link Board chung của nhóm (Figma / FigJam / Miro):** [Link Figma Board](https://www.figma.com/file/placeholder-day19-ai-tutor)

---

## Chặng 1 — Tổng hợp Evidence & Chốt Hypothesis Problem (Gate 1)

### 1. Evidence Snapshot từ Day 17 (3 Practice Notes)

| Practice Note | User đã thực sự làm / nói gì? (Fact-based) | Điều nhóm đang diễn giải (Interpretation) |
| :--- | :--- | :--- |
| **Note 1 (Lê Thị Duyên - P01)** | User đang xem slide khó hiểu trên VLearn, không biết bắt đầu từ đâu nên chụp màn hình gửi AI ngoài với câu: *"Tôi không hiểu chỗ này, cho tôi một lộ trình hiểu cái gì trước cái gì sau"*. Gặp lỗi bôi đen/vẽ tay không chuẩn nên bỏ dở, note lại để tối về tự mò vài tiếng. Quote: *"Thật ra em cũng không biết là nên bắt đầu từ đâu..."* | User không chỉ cần lời giải thích nội dung hiện tại, mà cái họ thực sự thiếu là khả năng tự chẩn đoán xem mình bị hổng kiến thức nền nào từ trước. Họ dùng AI ngoài như một công cụ lập bản đồ kiến thức. |
| **Note 2 (Thành viên 2 - P02)** | Khi gặp công thức toán/thuật toán phức tạp, user mở tab ChatGPT hỏi định nghĩa, nhưng nhận được một đoạn text rất dài. User đọc lướt 2 câu đầu rồi đóng tab, quay lại xem tiếp video với trạng thái lơ mơ để kịp tiến độ buổi học. | Việc AI giải thích quá dài (over-explaining) ngay giữa bài giảng làm đứt gãy mạch tập trung và tạo áp lực thời gian, khiến user thà bỏ qua còn hơn dừng lại đọc. |
| **Note 3 (Thành viên 3 - P03)** | User highlight từ khóa khó trên màn hình và click icon trợ giúp có sẵn của web, nhưng hệ thống chỉ hiển thị tooltip định nghĩa từ điển tĩnh (static dictionary). User tắt ngay tooltip vì *"nó không liên quan gì đến ngữ cảnh bài học này"*. | Định nghĩa tĩnh tách rời ngữ cảnh bài giảng không giải quyết được việc người học không hiểu mối liên hệ giữa khái niệm mới và bài giảng hiện tại. |

### 2. Thảo luận & Nhận định ban đầu
- **Behavior & Workaround lặp lại:** Chụp ảnh màn hình / copy từ khóa ném sang chatbot bên ngoài; nản lòng khi gặp giải thích quá dài; chấp nhận bỏ qua để không lỡ luồng học và để dành về nhà tự giải quyết (tốn từ 1–3 tiếng).
- **Evidence gây bất ngờ:** User không xin "đáp án" hay "tóm tắt", mà xin một **"lộ trình phải hiểu cái gì trước, cái gì sau"** (chẩn đoán lỗ hổng tiên quyết).
- **Điều vẫn chỉ là suy đoán của nhóm:** Liệu khi đưa lộ trình chẩn đoán ngay trong màn hình học, user có thực sự tương tác từng bước hay họ vẫn cảm thấy bị gián đoạn và muốn lưu lại để học sau?

### 3. Chốt Hypothesis Problem (GATE 1 PASS)
> **Hypothesis Problem:**  
> Khi **đang theo dõi bài giảng trực tuyến có nhiều khái niệm phức tạp liên đới**, **học viên trực tuyến** gặp khó khăn trong việc **tiếp thu bài học liên tục** vì **không tự chẩn đoán được mình đang bị hổng kiến thức tiên quyết nào để tra cứu đúng trọng tâm**, dẫn đến **bị đứt gãy luồng học, tốn 1–3 tiếng tự mò mẫm sau giờ học hoặc bỏ dở nội dung**.

- **Evidence ban đầu hỗ trợ giả thuyết:** Hành vi của P01 chụp ảnh màn hình hỏi AI ngoài về "lộ trình hiểu cái gì trước cái gì sau", và P02 bỏ cuộc vì AI giải thích quá dài không đúng lỗ hổng.
- **Điều vẫn chưa được chứng minh:** Mức độ can thiệp (intervention level) nào của AI là vừa vặn: Can thiệp chủ động ngay trên slide, hỗ trợ chẩn đoán khi được gọi, hay chỉ ghi nhận điểm tắc để xử lý sau buổi học?

---

## Chặng 2 — Ba Solution Options & Comparison Contract (Gate 2)

### 1. Bảng quy ước chung (Những thứ giữ nguyên 100%)
- **Target user:** Học viên học trực tuyến trên nền tảng web/desktop.
- **Situation:** Đang xem slide bài giảng bài học phức tạp (Ví dụ: Slide về *Thuật toán Gradient Descent trong Machine Learning*).
- **Task giao cho tester:** *"Khi gặp đoạn kiến thức khó hiểu trên slide này, hãy dùng công cụ để vượt qua điểm tắc và tiếp tục bài học."*
- **Desired outcome:** Nắm được khái niệm tiên quyết cần bù đắp trong dưới 2 phút mà không làm mất hoàn toàn luồng học chính.
- **Content / Data fixture:** Cùng 1 slide bài giảng về *Gradient Descent*, chứa đồ thị hàm mất mát, công thức đạo hàm riêng và learning rate.

---

### 2. So sánh cơ chế 3 Options (Comparison Contract)

| Thành phần | Option A: In-Context Prerequisite Diagnosis (User-Initiated) | Option B: Knowledge Graph & Concept Breakdown (AI-Initiated) | Option C: Smart Bookmark & Socratic Sync (Deferred Review) |
| :--- | :--- | :--- | :--- |
| **Solution Mechanism** | **Chẩn đoán hội thoại vi mô tại chỗ:** User khoanh vùng đoạn không hiểu -> AI phân tích ngữ cảnh slide và đưa ra cây 2–3 câu hỏi trắc nghiệm chẩn đoán nhanh để xác định lỗ hổng. | **Bản đồ khái niệm tương tác thời gian thực:** AI tự động quét slide và render sẵn một mini concept map bên lề; highlight các khái niệm tiên quyết (prerequisites). | **Ghi chú thông minh & Luyện tập truy hồi ngắt quãng:** User bấm 1 phím tắt/nút "Đang kẹt"; AI âm thầm chụp ngữ cảnh và tạo bộ câu hỏi gợi mở (Socratic cards) để giải quyết sau khi hết video. |
| **User làm gì?** | Chủ động click nút "Chẩn đoán điểm tắc", chọn đoạn slide khó hiểu, trả lời 1–2 câu hỏi trắc nghiệm ngắn. | Quan sát panel concept map bên cạnh slide, click vào nút khái niệm mình chưa vững để xem giải thích súc tích 3 dòng. | Bấm nút "Ghim điểm kẹt" (Bookmark friction) rồi tiếp tục nghe giảng; mở panel ôn tập sau khi bài học kết thúc. |
| **AI làm gì?** | Phân tích ảnh/text vùng chọn -> phát hiện khái niệm tiên quyết -> tạo micro-quiz chẩn đoán -> đưa tóm tắt ngắn đúng phần hổng. | Phân tích toàn bộ slide -> trích xuất cấu trúc kiến thức -> hiển thị thanh tiến trình độ khó và cây khái niệm liên quan. | Lưu timestamp và ngữ cảnh slide -> sinh các câu hỏi phản tư kiểu Socratic -> nhắc nhở học viên ôn lại ở cuối bài. |
| **Trigger** | User chủ động kích hoạt (Click button/Selection). | Hệ thống tự động kích hoạt khi slide chuyển trang. | User chủ động ghim nhanh (1-click), AI kích hoạt xử lý sâu ở cuối phiên học. |
| **Trade-off chính** | **Độ sâu vs. Đứt gãy luồng:** Giải quyết đúng bệnh nhưng bắt user dừng lại 1–2 phút để tương tác trắc nghiệm giữa bài giảng. | **Tiện lợi vs. Cognitive Overload:** Không làm gián đoạn bài giảng nhưng màn hình có thêm nhiều thông tin (map/tags) dễ gây phân tâm. | **Bảo toàn mạch học vs. Độ trễ giải quyết:** Giữ nguyên 100% luồng nghe giảng nhưng học viên phải chấp nhận mang "nỗi băn khoăn" tới cuối buổi mới giải tỏa. |

---

### 3. Distance Check (Kiểm tra độ khác biệt có ý nghĩa)
- **A khác B vì:** A yêu cầu user chủ động kích hoạt và cùng AI tương tác qua lại để tìm ra lỗ hổng (Co-diagnostic), trong khi B là AI tự động chuẩn bị sẵn toàn bộ bản đồ kiến thức để user tự do tham khảo thụ động (Passive Reference).
- **B khác C vì:** B cố gắng giải quyết sự thấu hiểu ngay lập tức trong lúc đang học (In-the-moment comprehension), còn C cố ý trì hoãn việc giải quyết đến cuối buổi học để bảo toàn tuyệt đối mạch tập trung của bài giảng (Deferred deep review).
- **A khác C vì:** A can thiệp sâu vào thời gian thực bằng hội thoại chẩn đoán vi mô (High intervention, instant feedback), trong khi C chỉ ghi nhận tín hiệu tối thiểu và không làm gián đoạn luồng nghe giảng (Zero interruption, post-session retrieval).

---

## Chặng 3 — Human–AI Design Pass (Gate 3)

### Human–AI Decision Table

| Human–AI Decision | Option A (In-Context Diagnostic) | Option B (Concept Map Navigator) | Option C (Smart Bookmark & Socratic) |
| :--- | :--- | :--- | :--- |
| **User làm gì? AI làm gì?** | **User:** Khoanh vùng điểm kẹt, chọn câu trả lời chẩn đoán.<br>**AI:** Đọc slide, sinh 2 câu hỏi test nhanh, đưa thẻ kiến thức bù đắp. | **User:** Lướt xem sơ đồ, click node khái niệm cần xem.<br>**AI:** Tự động parse slide, dựng visual graph các node tiên quyết. | **User:** Bấm 1 nút ghim điểm tắc; cuối giờ làm bài tập phản tư.<br>**AI:** Đóng gói context slide, soạn flashcard Socratic. |
| **AI Act / Ask / Don't Act? Vì sao?** | **Ask:** AI không tự tiện nhảy ra màn hình mà đợi user gọi; sau đó hỏi xác nhận mức độ hiểu trước khi đưa giải thích. Vì chẩn đoán sai sẽ làm hỏng trải nghiệm học. | **Act with Low Prominence:** AI tự động hiển thị sơ đồ ở panel phụ bên phải, không chiếm màn hình chính, không che video. | **Don't Act immediately, Act upon Session End:** Trong lúc học AI im lặng; chỉ hành động gửi thông báo tổng hợp khi video kết thúc. |
| **User hiểu capability & limit bằng gì?** | Nhãn hướng dẫn rõ: *"AI chẩn đoán kiến thức nền tảng trong 60 giây — Không giải bài tập hộ"*. Progress bar hiển thị *"Bước 1/2 chẩn đoán"*. | Badge ghi chú: *"Bản đồ khái niệm trích xuất tự động từ giáo trình — Bấm vào node để xem tóm tắt 3 dòng"*. | Thông báo xác nhận ngắn (toast 1s): *"Đã lưu slide 12 vào sổ ôn tập cuối giờ. Bạn cứ yên tâm nghe tiếp"*. |
| **Evidence & Uncertainty được thể hiện thế nào?** | AI trích dẫn: *"Dựa trên công thức đạo hàm ở phút 04:15, có thể bạn đang vướng ở 'Quy tắc chuỗi (Chain Rule)'"*. Nếu độ tin cậy thấp, AI hỏi: *"Bạn có muốn xem lại khái niệm này không?"*. | Các node khái niệm có màu phân biệt: Xanh (Đã học ở bài trước), Vàng (Khái niệm mới của bài này), Nét đứt (Khái niệm nâng cao bổ trợ). | Thẻ ôn tập ghi rõ: *"Câu hỏi tạo từ slide 12 lúc bạn bấm ghim"*. Cho phép user đánh giá thẻ có trúng chỗ mình không hiểu hay không. |
| **User kiểm soát & Recovery thế nào?** | - Nút **"Bỏ qua / Đóng" (X)** luôn ở góc trên bên phải.<br>- Nút **"Không phải chỗ này"** để chọn lại vùng slide.<br>- Nút **"Xem thẳng giải thích ngắn"** nếu không muốn làm trắc nghiệm. | - Nút **Thu gọn (Collapse)** panel bản đồ để xem toàn màn hình slide.<br>- Nút **"Báo khái niệm không chuẩn"** để ẩn node rác. | - Nút **"Hủy ghim"** ngay lập tức nếu bấm nhầm.<br>- Nút **"Đánh dấu đã hiểu, xóa khỏi danh sách"** trong lúc làm bài ôn tập cuối giờ. |

---

## Chặng 4 — Prototype Blueprint & Annotations (Gate 4)

### Common Frame Structure (70% dùng chung):
- Màn hình player bài giảng VLearn tỉ lệ 16:9.
- Phía trên: Tiêu đề bài học *"Bài 4: Tối ưu hóa với Gradient Descent"*.
- Trung tâm: Slide bài giảng có đồ thị hàm mất mát cong parabol, công thức đạo hàm và learning rate $\alpha$.
- Phía dưới: Thanh điều khiển video (Play, Pause, Progress bar tại phút 08:30).

### Prototype Annotations (Nội bộ nhóm quan sát):
- **OPTION A Annotation:**
  - *We expect the tester to:* Bấm vào nút "Hỏi AI điểm tắc", khoanh vùng công thức đạo hàm, trả lời câu hỏi trắc nghiệm chẩn đoán.
  - *Watch for:* Tester có ngại làm quiz không? Có hiểu vì sao AI lại hỏi ngược lại mình không?
  - *Do not explain:* Không chỉ cho tester nút trắc nghiệm hoặc giải thích câu hỏi hộ tester.
- **OPTION B Annotation:**
  - *We expect the tester to:* Liếc nhìn panel bên phải, nhận diện được node màu vàng "Đạo hàm riêng", click vào để xem tóm tắt.
  - *Watch for:* Tester có bị phân tâm khỏi video không? Sơ đồ có quá tải thông tin không?
  - *Do not explain:* Không giải thích ý nghĩa các màu sắc trên sơ đồ.
- **OPTION C Annotation:**
  - *We expect the tester to:* Bấm nút bookmark "Ghim điểm kẹt", tiếp tục xem hết đoạn video ngắn, sau đó mở tab "Ôn tập cuối giờ".
  - *Watch for:* Cảm xúc của tester khi phải chờ đến cuối giờ mới được giải tỏa thắc mắc.
  - *Do not explain:* Không giục tester bấm nút kết thúc bài học.
