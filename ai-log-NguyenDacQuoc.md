# AI log – TV1 – Nguyễn Đắc Quốc

> Mỗi thành viên một tệp trong `ai-logs/`. Ghi một mục ngay sau mỗi lần dùng AI có ảnh hưởng đến sản phẩm, commit cùng thay đổi liên quan. Cả đồ án tối thiểu 6 mục có nội dung thực chất. Mã mục tăng dần: AI-01, AI-02, ...

| Mục | Thông tin |
| --- | --- |
| Họ tên, MSSV | Nguyễn Đắc Quốc – 0306241236 |
| Nhóm, đề tài | Nhóm 03 – Website Bán Thiết Bị Điện Tử & Phụ Kiện (TechStore) |
| Vai trò | TV1 – LE (Leader) |
| Công cụ AI dùng | ChatGPT (GPT-4o), Claude 3.5 Sonnet, GitHub Copilot |

## Bảng tổng hợp

| Mã | Ngày | Giai đoạn | Nội dung | Commit / PR |
| --- | --- | --- | --- | --- |
| AI-01 | 14/10 | Phân tích yêu cầu | Brainstorm chức năng và rủi ro của đề tài | Commit `3f8a1b2` / PR #1 |
| AI-02 | 18/10 | Lập kế hoạch | Rà soát User Story và chia Sprint 1 | Commit `7e2d9c4` / PR #2 |
| AI-03 | 24/10 | Thiết kế | Thiết kế Database Schema (Mongoose Model) | Commit `1a5b8c9` / PR #4 |
| AI-04 | 29/10 | Lập trình | Xây dựng RESTful API Authentication (JWT & Bcrypt) | Commit `9d8c7b6` / PR #7 |
| AI-05 | 03/11 | Lập trình | Xây dựng giao diện Dashboard Admin & Bảng sản phẩm | Commit `4f3e2d1` / PR #12 |
| AI-06 | 08/11 | Kiểm thử | Viết Unit Test cho API Auth & Xử lý lỗi CORS | Commit `8c7b6a5` / PR #18 |

---

### [AI-01] Brainstorm chức năng và rủi ro của đề tài
- Ngày / Người dùng: 2024-10-14 / Nguyễn Đắc Quốc
- Công cụ: ChatGPT (GPT-4o)
- Giai đoạn: Phân tích yêu cầu
- Task / Commit / PR: [DOC] Khảo sát & Đề cương chi tiết / `3f8a1b2` / PR #1
- Mục đích: Liệt kê danh sách chức năng phân loại theo nhóm người dùng và xác định các rủi ro kỹ thuật/vận hành khi làm đề tài TechStore trong 3 tuần với 5 người.
- Prompt chính (nguyên văn hoặc link chia sẻ hội thoại): "Nhóm 5 sinh viên làm website bán thiết bị điện tử TechStore trong 3 tuần bằng ReactJS, Node.js (Express), MongoDB. Hãy liệt kê các chức năng cần có chia theo Khách hàng và Quản trị viên (phân loại bắt buộc vs tùy chọn), và 5 rủi ro lớn nhất kèm cách phòng tránh."
- Kết quả AI trả về (tóm tắt): AI đề xuất 16 chức năng (bao gồm tìm kiếm, giỏ hàng, thanh toán VNPAY, đánh giá, Chatbot tư vấn, gợi ý sản phẩm thông minh) và 5 rủi ro về thời gian, quá tải DB, bảo mật.
- Đánh giá: Đúng 75%. AI đề xuất thêm tính năng Chatbot AI và Gợi ý sản phẩm quá phức tạp so với thời gian 3 tuần của nhóm. Thiếu rủi ro về xung đột Git khi phân chia công việc.
- Đã chỉnh sửa gì: Loại bỏ tính năng Chatbot AI và Gợi ý sản phẩm khỏi mảng bắt buộc; bổ sung rủi ro Merge Conflict khi đẩy code chung và thống nhất quy trình Git Flow cho nhóm.
- Cách kiểm chứng: Đối chiếu danh sách chức năng với yêu cầu đề cương môn học; họp nhóm thống nhất phạm vi sản phẩm với giảng viên hướng dẫn.
- Tỷ lệ nội dung AI còn giữ lại (ước lượng): 70%
- Điều học được: Cần giới hạn rõ ràng thời gian thực hiện và quy mô nhân sự trong prompt để AI không đưa ra các tính năng vượt quá nguồn lực thực tế.

### [AI-02] Rà soát User Story và chia Sprint 1
- Ngày / Người dùng: 2024-10-18 / Nguyễn Đắc Quốc
- Công cụ: Claude 3.5 Sonnet
- Giai đoạn: Lập kế hoạch
- Task / Commit / PR: [PLAN] Sprint 1 Backlog & Story Estimation / `7e2d9c4` / PR #2
- Mục đích: Viết danh sách User Story chuẩn định dạng Agile và đề xuất phân chia công việc cho Sprint 1 (1 tuần).
- Prompt chính (nguyên văn hoặc link chia sẻ hội thoại): "Tôi có danh sách chức năng website bán đồ điện tử. Hãy chuyển đổi thành 10 User Story dạng 'As a... I want to... So that...' và gợi ý phân chia Sprint 1 cho nhóm 5 người (trong đó 1 Leader, 2 Frontend, 2 Backend)."
- Kết quả AI trả về (tóm tắt): AI tạo 10 User Story hoàn chỉnh kèm theo ước lượng Story Point và đề xuất Sprint 1 tập trung vào Auth, Xem sản phẩm và Giỏ hàng cơ bản.
- Đánh giá: Đúng về cấu trúc chuẩn User Story. Tuy nhiên thời gian ước lượng (Story Point) cho phần Authentication và Giỏ hàng quá thấp so với năng lực thực tế của nhóm.
- Modifications / Đã chỉnh sửa gì: Điều chỉnh Story Point tăng gấp đôi cho phần Auth (từ 3pt -> 5pt); gán tên cụ thể các thành viên phụ trách từng task dựa theo năng lực cá nhân.
- Cách kiểm chứng: Họp Sprint Planning với nhóm, review và chốt công việc trên Trello Board.
- Tỷ lệ nội dung AI còn giữ lại (ước lượng): 85%
- Điều học được: AI không nắm được trình độ thực tế của từng thành viên, vì vậy việc ước lượng độ khó (Story Points) luôn cần được nhóm điều chỉnh lại.

### [AI-03] Thiết kế Database Schema (Mongoose Model)
- Ngày / Người dùng: 2024-10-24 / Nguyễn Đắc Quốc
- Công cụ: ChatGPT (GPT-4o)
- Giai đoạn: Thiết kế
- Task / Commit / PR: [DB] Define Database Schemas & Models / `1a5b8c9` / PR #4
- Mục đích: Tạo cấu trúc các Collection trong MongoDB (User, Product, Category, Order, Cart) bằng Mongoose ODM.
- Prompt chính (nguyên văn hoặc link chia sẻ hội thoại): "Viết Mongoose schema cho các entity: User, Product, Category, Order, Cart trong dự án bán hàng điện tử Node.js. Cần có validate dữ liệu (email, phone, price > 0) và định nghĩa mối quan hệ (ref) giữa các collection."
- Kết quả AI trả về (tóm tắt): AI sinh toàn bộ code Mongoose schema cho các model kèm theo Indexing cho các trường tìm kiếm thường xuyên như `product.name` và `user.email`.
- Đánh giá: Đúng 80%. Cấu trúc chuẩn, tuy nhiên thiếu trường `status` (Đã xác nhận, Đang giao, Đã hủy...) trong Order Schema và thiếu thuộc tính `discountPrice` trong Product Schema.
- Đã chỉnh sửa gì: Bổ sung enum `status` cho Order, thêm `discountPrice`, `stockQuantity` cho Product và sửa lại Regex validation số điện thoại theo định dạng Việt Nam.
- Cách kiểm chứng: Chạy script khởi tạo dữ liệu mẫu (seed data) và kiểm tra hiển thị schema trên MongoDB Compass mà không phát sinh lỗi validation.
- Tỷ lệ nội dung AI còn giữ lại (ước lượng): 80%
- Điều học được: AI tạo khung Schema rất nhanh nhưng dễ bỏ sót các trường dữ liệu nghiệp vụ đặc thù, cần rà soát kỹ đối chiếu với luồng nghiệp vụ.

### [AI-04] Xây dựng RESTful API Authentication (JWT & Bcrypt)
- Ngày / Người dùng: 2024-10-29 / Nguyễn Đắc Quốc
- Công cụ: GitHub Copilot
- Giai đoạn: Lập trình
- Task / Commit / PR: [FEAT] Express Auth Controller & Middleware / `9d8c7b6` / PR #7
- Mục đích: Lập trình các API Đăng ký, Đăng nhập, Mã hóa mật khẩu bằng Bcrypt và Tạo/Xác thực Token JWT.
- Prompt chính (nguyên văn hoặc link chia sẻ hội thoại): "// Create Express authentication controller with register, login, bcrypt password hashing, JWT token generation, and auth Middleware"
- Kết quả AI trả về (tóm tắt): Copilot tự động gợi ý code chi tiết cho router `POST /api/auth/register`, `POST /api/auth/login` và middleware `verifyToken`, `requireAdmin`.
- Đánh giá: Đúng logic mã hóa và kiểm tra token. Hạn chế: AI hardcode giá trị `JWT_SECRET` trực tiếp trong file code thay vì đọc từ biến môi trường (`process.env`).
- Đã chỉnh sửa gì: Di chuyển `JWT_SECRET` và `EXPIRES_IN` vào tệp `.env`; bổ sung khối `try-catch` và middleware xử lý lỗi tập trung (error handling middleware) để tránh treo server.
- Cách kiểm chứng: Sử dụng Postman gửi request Đăng ký/Đăng nhập, kiểm tra Token trả về và dùng Token đó gọi các API bảo vệ thành công.
- Tỷ lệ nội dung AI còn giữ lại (ước lượng): 75%
- Điều học được: Luôn rà soát các vấn đề an toàn thông tin (hardcoded secret, validate input) khi sử dụng code gợi ý từ AI autocomplete.

### [AI-05] Xây dựng giao diện Dashboard Admin & Bảng sản phẩm
- Ngày / Người dùng: 2024-11-03 / Nguyễn Đắc Quốc
- Công cụ: Claude 3.5 Sonnet
- Giai đoạn: Lập trình
- Task / Commit / PR: [FEAT] Admin Product Management UI / `4f3e2d1` / PR #12
- Mục đích: Tạo giao diện trang quản lý sản phẩm dành cho Admin với các tính năng: danh sách sản phẩm, bộ lọc, tìm kiếm, phân trang và modal Thêm/Sửa sản phẩm.
- Prompt chính (nguyên văn hoặc link chia sẻ hội thoại): "Tạo React component bằng Tailwind CSS cho trang Admin Manage Products. Yêu cầu responsive, có thanh tìm kiếm, bộ lọc danh mục, bảng dữ liệu phân trang và Modal Dialog thêm/sửa sản phẩm."
- Kết quả AI trả về (tóm tắt): Claude trả về một file JSX đầy đủ giao diện chỉn chu, sử dụng Tailwind CSS và Lucide Icons đẹp mắt, tích hợp sẵn state giả định.
- Đánh giá: Giao diện sinh ra rất đẹp và đáp ứng đúng responsive. Tuy nhiên toàn bộ UI và logic state nằm chung trong 1 file duy nhất (hơn 400 dòng code), chưa tách component nhỏ và chưa kết nối với API backend.
- Đã chỉnh sửa gì: Refactor lại code, chia nhỏ thành các sub-component: `ProductTable.jsx`, `ProductModal.jsx`, `ProductFilter.jsx`; tích hợp thư viện `axios` để kết nối API từ Backend.
- Cách kiểm chứng: Kiểm tra hiển thị giao diện trên trình duyệt trên cả Desktop và Mobile; thực hiện thao tác Thêm/Sửa/Xóa sản phẩm và kiểm tra dữ liệu thay đổi trong DB.
- Tỷ lệ nội dung AI còn giữ lại (ước lượng): 60%
- Điều học được: AI có xu hướng gom toàn bộ code vào một file để tiện hiển thị. Người lập trình cần chủ động tách nhỏ component để đảm bảo tính tái sử dụng và dễ bảo trì.

### [AI-06] Viết Unit Test cho API Auth & Xử lý lỗi CORS
- Ngày / Người dùng: 2024-11-08 / Nguyễn Đắc Quốc
- Công cụ: ChatGPT (GPT-4o)
- Giai đoạn: Kiểm thử
- Task / Commit / PR: [TEST] Auth Unit Testing & Fix CORS Policy / `8c7b6a5` / PR #18
- Mục đích: Viết các bản kiểm thử tự động (Unit Test) cho API Đăng nhập và cấu hình CORS policy cho phép Frontend giao tiếp với Backend.
- Prompt chính (nguyên văn hoặc link chia sẻ hội thoại): "Viết Jest test cases dùng Supertest cho API POST /api/auth/login (cho các trường hợp: đăng nhập thành công, sai mật khẩu, thiếu email) và hướng dẫn cấu hình CORS middleware trong Express hỗ trợ credentials."
- Kết quả AI trả về (tóm tắt): AI cung cấp đoạn mã cấu hình CORS chuẩn và bộ test case Jest/Supertest bao phủ đủ các kịch bản kiểm thử.
- Đánh giá: Phần cấu hình CORS chính xác. Bộ test case viết tốt nhưng thiếu việc Mock dữ liệu database (khiến test suite kết nối thẳng vào DB thật khi chạy).
- Đã chỉnh sửa gì: Thêm `jest.mock()` cho Mongoose User Model để cô lập môi trường test, tránh phụ thuộc và tác động đến dữ liệu thật trong Database.
- Cách kiểm chứng: Chạy lệnh `npm run test` trong console; tất cả test case đều PASSED với tỷ lệ bao phủ code (code coverage) đạt trên 85%.
- Tỷ lệ nội dung AI còn giữ lại (ước lượng): 85%
- Điều học được: Cần yêu cầu AI sử dụng Mock Object/Stub khi viết Unit Test cho API để đảm bảo kiểm thử chạy nhanh và độc lập.

<!-- Mẫu mục mới: chép khối dưới, đổi mã AI-xx

### [AI-xx] Tiêu đề ngắn
- Ngày / Người dùng:
- Công cụ:
- Giai đoạn: Phân tích yêu cầu | Lập kế hoạch | Thiết kế | Lập trình | Kiểm thử | Tài liệu
- Task / Commit / PR:
- Mục đích:
- Prompt chính (nguyên văn hoặc link chia sẻ hội thoại):
- Kết quả AI trả về (tóm tắt):
- Đánh giá: Đúng / Sai / Thiếu – vì sao
- Đã chỉnh sửa gì:
- Cách kiểm chứng:
- Tỷ lệ mã AI còn giữ lại (ước lượng): ...%
- Điều học được:
-->