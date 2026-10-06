# AI Support Log — Nhật ký Sử dụng AI & Kiểm chứng Cá nhân

- **Họ và tên:** Lê Thị Duyên
- **Mã học viên:** 2A202602411
- **Bài tập:** Track 1 — Day 19 (Three Solution Options & Prototype Testing)

---

## 1. Tuyên bố tuân thủ nguyên tắc sử dụng AI

Tôi cam kết tuân thủ nghiêm ngặt các quy tắc học thuật của môn học:
- **Phạm vi sử dụng:** Dùng AI để hỗ trợ gợi ý cơ chế tương tác (Chặng 2), soạn thảo dữ liệu mẫu / canned AI output cho prototype (Chặng 4), và rà soát câu hỏi dẫn dắt trong kịch bản kiểm thử (Chặng 5).
- **Phạm vi KHÔNG sử dụng:** Toàn bộ các quan sát hành vi (observations), câu nói nguyên văn (quotes) và phản hồi từ tester T01 trong file `prototype-feedback-note.md` đều là dữ liệu thực tế thu thập từ phiên kiểm thử do chính tôi trực tiếp facilitate, tuyệt đối không dùng AI để sinh dữ liệu người dùng giả mạo.
- **Tự chịu trách nhiệm:** Mọi đánh giá, phán đoán, phân tích 4 lớp và kết luận Next Change đều do tôi và nhóm trực tiếp thảo luận và quyết định.

---

## 2. Bảng phân định công việc & Đánh giá chất lượng hỗ trợ của AI

| Công việc trong bài Lab | AI làm hay bạn làm? | AI đã giúp gì? | AI làm sai / hời hợt ở đâu? | Bạn đã kiểm chứng, điều chỉnh và quyết định lại thế nào? |
| :--- | :--- | :--- | :--- | :--- |
| **Chặng 1: Tổng hợp Evidence & Hypothesis Problem** | **Cả hai cùng làm** (Bạn chủ trì) | Giúp định dạng lại câu Hypothesis Problem theo cấu trúc chuẩn: *Khi [situation], [user] gặp khó khăn...* | AI ban đầu đưa ra một Hypothesis Problem quá chung chung mang tính "muốn học nhanh hơn", bỏ quên mất chi tiết cốt lõi từ Day 17 là user bị hổng kiến thức tiên quyết và phải chụp màn hình. | Tôi đã ép lại câu giả thuyết dựa trên đúng quote gốc của P01: *"không biết bắt đầu từ đâu, phải hiểu cái gì trước cái gì sau"* để giữ trọn vẹn mạch bằng chứng từ Day 17. |
| **Chặng 2: Brainstorm 3 Solution Options** | **AI gợi ý, Bạn chọn & chuẩn hóa** | Đề xuất các cơ chế phân chia vai trò User - AI khác nhau theo phổ tương tác (Initiative spectrum). | AI gợi ý một phương án là "Chatbot sidebar trả lời tự do". Đây thực chất là tính năng ChatGPT bọc lại (wrapper), vi phạm quy tắc tạo 3 cơ chế thực sự khác biệt. | Tôi loại bỏ gợi ý chatbot tự do, thay thế bằng cơ chế **Option A (In-context Diagnostic micro-quiz)** và **Option C (Deferred Socratic review)** để tạo ra sự đánh đổi thực sự giữa việc giải quyết ngay lập tức vs. bảo toàn luồng học. |
| **Chặng 3: Human–AI Design Pass** | **Bạn làm chính, AI hỗ trợ template** | Cung cấp cấu trúc 4 quyết định: Expectation, Role & Agency, Evidence & Uncertainty, Control & Recovery. | AI thường quên thiết kế đường thoát hiểm (Recovery path) khi AI đoán sai hoặc chẩn đoán trượt lỗ hổng kiến thức. | Tôi bổ sung rõ ràng các nút thoát hiểm: Nút [X], nút [Chọn lại vùng slide], và nút [Bỏ qua làm quiz, xem thẳng giải thích ngắn] để đảm bảo người dùng luôn giữ quyền kiểm soát tối thượng. |
| **Chặng 4: Tạo Canned Data cho Prototype** | **AI hỗ trợ chính** | Sinh văn bản bài học mẫu về *Gradient Descent*, công thức đạo hàm riêng và các câu hỏi trắc nghiệm chẩn đoán giả lập để đưa vào Figma. | Câu hỏi trắc nghiệm do AI tự tạo ban đầu quá dài và nặng tính lý thuyết hàn lâm, không phù hợp với ngữ cảnh micro-interaction dưới 60 giây. | Tôi rút gọn toàn bộ câu hỏi chẩn đoán xuống còn 1 câu duy nhất với 3 lựa chọn súc tích để tester đọc và bấm được ngay trong 10 giây. |
| **Chặng 5: Soạn Kịch bản Kiểm thử & Test Script** | **Bạn làm, AI rà soát lỗi dẫn dắt** | Đóng vai trò phản biện, quét qua các câu hỏi phỏng vấn để phát hiện câu hỏi mang tính định hướng. | AI ban đầu đề xuất câu hỏi: *"Bạn có thấy tính năng chẩn đoán này hữu ích hơn chatbot cũ không?"* — Đây là câu hỏi mang tính pitch giải pháp và dẫn dắt lộ liễu. | Tôi sửa lại hoàn toàn theo nguyên tắc kiểm thử khách quan: Dùng Outcome Task (*"Hãy tìm cách vượt qua điểm khó hiểu trên slide"*) và các câu hỏi trung lập (*"Bạn sẽ làm gì tiếp theo?", "Theo bạn nó nên hoạt động ra sao?"*). |
| **Chặng 6: Ghi chép & Phân tích 4 lớp Feedback** | **Bạn làm 100%** | Không dùng AI để can thiệp vào ghi chép hay bịa đặt phản hồi. | Nếu để AI tổng hợp, AI có xu hướng kết luận thiên vị kiểu *"Tester rất thích giải pháp A và sản phẩm đã sẵn sàng phát triển"*. | Tôi tự tay viết toàn bộ mục *Observed, Interpreted, Decided, Still Unproven*, giữ nguyên những lời phàn nàn của tester (như Option B gây ngợp, Option C gây hụt hẫng) để rút ra bài học thật. |

---

## 3. Bài học cá nhân về việc cộng tác với AI trong Product Design

1. **AI rất giỏi sinh ý tưởng nhưng rất tệ trong việc nhận thức bối cảnh thực tế (situational awareness):** AI dễ dàng vẽ ra các tính năng hoành tráng nhưng không lường trước được người học trực tuyến đang chịu áp lực thời gian ra sao khi một video bài giảng vẫn đang chạy.
2. **Vai trò của PM là người gác cổng (Gatekeeper) cho tính chân thực của dữ liệu:** Không bao giờ được để AI tóm tắt hoặc "làm đẹp" các phản hồi tiêu cực của người dùng. Chính những chỗ người dùng lúng túng, chê bai hoặc bấm nhầm mới là mỏ vàng để định hình vòng lặp sản phẩm tiếp theo.
