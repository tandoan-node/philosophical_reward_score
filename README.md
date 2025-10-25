# Mô Phỏng Mô Hình Thưởng (Reward Model) - RLHF

*Đây là dự án mô phỏng chức năng cốt lõi của Mô hình Thưởng (Reward Model), một thành phần quan trọng trong quá trình huấn luyện AI bằng phản hồi từ con người (RLHF - Reinforcement Learning from Human Feedback) hoặc Tối ưu hóa Ưu tiên Trực tiếp (DPO).*

**Sử dụng Gemini 2.5 Flash API để mô phỏng khả năng chấm điểm ưu tiên của người dùng, thay vì huấn luyện một mô hình phân loại cục bộ.**

## 🌟 Mục tiêu Dự án

**Minh họa Chức năng RM:** Chứng minh cách một mô hình AI có thể học được và đánh giá "ý kiến" hoặc "ưu tiên" chủ quan của con người (trong trường hợp này là mức độ Triết học/Sâu sắc của câu trả lời).

**Giải pháp Ổn định:** Cung cấp một giải pháp hoạt động 100% bằng cách tận dụng sức mạnh của Large Language Model (LLM) để chấm điểm theo cấu trúc JSON (đầu ra của một Reward Model).

## 🧠 Kiến trúc Hoạt động

*Dự án này là một ứng dụng web đơn giản (HTML/JavaScript) sử dụng API để thực hiện tác vụ phức tạp:*

### Thành phần

* Vai trò trong RLHF/DPO
* Công cụ/Kỹ thuật
* Giao diện người dùng
* Nơi người dùng nhập câu trả lời của Policy Model.
* HTML/Tailwind CSS
* Hàm chấm điểm
* Gửi yêu cầu chấm điểm đến RM.
* JavaScript (fetch API)
* Mô hình Thưởng (RM)
* Nhận đầu vào và trả về điểm số ưu tiên.
* Gemini 2.5 Flash API

### Tiêu chí ưu tiên

* Định nghĩa "ý kiến" người dùng (Triết học, Sâu sắc, Đa chiều).
* System Instruction của Gemini
* Đầu ra
* Điểm số từ 0.0 đến 1.0 và giải thích.
* JSON Schema (Structured Output)

### 🛠 Hướng dẫn Sử dụng (Chạy Ứng dụng)

**Yêu cầu:** Ứng dụng này chỉ yêu cầu một trình duyệt web.

* Khởi chạy: Mở file reward_model_gemini_api.html trong môi trường hỗ trợ Canvas hoặc trình duyệt của bạn.
* Thử nghiệm:
    - Nhập văn bản Triết học (Điểm cao mong đợi): "Ý thức là gì? Nó có thể được định nghĩa bằng thuật toán hay không? Đây là câu hỏi triết học sâu sắc nhất mà AI đặt ra."

    - Nhập văn bản Nông (Điểm thấp mong đợi): "AI rất hữu ích. Nó giúp tôi làm việc nhanh hơn và chơi game tốt hơn. AI là công cụ tốt."

    - Kết quả: Ứng dụng sẽ hiển thị Reward Score (Điểm Thưởng) và giải thích, minh họa cách Reward Model đánh giá các phản hồi.
