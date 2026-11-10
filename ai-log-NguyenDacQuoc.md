# AI log – TV1 – Nguyễn Đắc Quốc

> Mỗi thành viên một tệp trong `ai-logs/`. Ghi một mục ngay sau mỗi lần dùng AI có ảnh hưởng đến sản phẩm, commit cùng thay đổi liên quan. Cả đồ án tối thiểu 6 mục có nội dung thực chất. Mã mục tăng dần: AI-01, AI-02, ...

| Mục | Thông tin | 
| ----- | ----- | 
| Họ tên, MSSV | Nguyễn Đắc Quốc – 0306241236 | 
| Nhóm, đề tài | Nhóm 05 – Website Thương Mại Điện Tử (E-Commerce Platform) | 
| Vai trò | TV1 – LE (Leader) | 
| Công cụ AI dùng | ChatGPT (GPT-4o), Claude 3.5 Sonnet, GitHub Copilot | 

## Bảng tổng hợp

| Mã | Ngày | Giai đoạn | Nội dung | Commit / PR | 
| ----- | ----- | ----- | ----- | ----- | 
| AI-01 | 14/10 | Phân tích yêu cầu | Brainstorm chức năng và rủi ro của hệ thống TMĐT | Commit `3f8a1b2` / PR #1 | 
| AI-02 | 18/10 | Lập kế hoạch | Rà soát User Story và chia Sprint 1 cho dự án TMĐT | Commit `7e2d9c4` / PR #2 | 
| AI-03 | 24/10 | Thiết kế | Thiết kế Database Schema (Mongoose Model) cho web TMĐT | Commit `1a5b8c9` / PR #4 | 
| AI-04 | 29/10 | Lập trình | Xây dựng RESTful API Authentication & Phân quyền User/Admin | Commit `9d8c7b6` / PR #7 | 
| AI-05 | 03/11 | Lập trình | Xây dựng giao diện Dashboard Admin quản lý đơn hàng & sản phẩm | Commit `4f3e2d1` / PR #12 | 
| AI-06 | 08/11 | Kiểm thử | Viết Unit Test cho API Thanh toán/Giỏ hàng & Fix lỗi CORS | Commit `8c7b6a5` / PR #18 | 

### \[AI-01\] Brainstorm chức năng và rủi ro của hệ thống TMĐT

* Ngày / Người dùng: 2024-10-14 / Nguyễn Đắc Quốc

* Công cụ: ChatGPT (GPT-4o)

* Giai đoạn: Phân tích yêu cầu

* Task / Commit / PR: \[DOC\] Khảo sát & Đề cương chi tiết hệ thống TMĐT / `3f8a1b2` / PR #1

* Mục đích: Liệt kê danh sách các nhóm chức năng bắt buộc/tùy chọn và xác định các rủi ro vận hành/kỹ thuật khi làm sàn Thương mại điện tử trong 3 tuần với 5 người.

* Prompt chính (nguyên văn hoặc link chia sẻ hội thoại): "Nhóm 5 sinh viên làm website thương mại điện tử (E-Commerce) trong 3 tuần bằng ReactJS, Node.js (Express), MongoDB. Hãy liệt kê các chức năng cần có chia theo Khách hàng và Quản trị viên (phân loại bắt buộc vs tùy chọn), và 5 rủi ro lớn nhất kèm cách phòng tránh."

* Kết quả AI trả về (tóm tắt): AI đề xuất 18 chức năng (bao gồm tìm kiếm/lọc sản phẩm, giỏ hàng, thanh toán VNPAY/MOMO, theo dõi đơn hàng, voucher giảm giá, Chatbot CSKH, gợi ý sản phẩm AI) và 5 rủi ro về đồng bộ tồn kho, bảo mật thanh toán, quá tải DB.

* Đánh giá: Đúng 75%. AI đề xuất các tính năng nâng cao như Chatbot CSKH và Gợi ý sản phẩm thông minh vượt quá mốc thời gian 3 tuần. Thiếu rủi ro xung đột mã nguồn khi cả nhóm cùng thao tác trên dữ liệu giỏ hàng/đơn hàng.

* Đã chỉnh sửa gì: Loại bỏ Chatbot và Gợi ý AI khỏi danh sách MVP; bổ sung quy trình khóa tồn kho tạm thời khi đặt hàng và thống nhất Git Flow giải quyết xung đột code cho nhóm.

* Cách kiểm chứng: Đối chiếu với tài liệu mô tả yêu cầu môn học; họp nhóm thống nhất phạm vi chức năng cốt lõi (MVP) của website TMĐT với giảng viên.

* Tỷ lệ nội dung AI còn giữ lại (ước lượng): 70%

* Điều học được: Khi làm đề tài TMĐT, cần phải làm rõ phạm vi MVP (Minimum Viable Product) để tránh sa lầy vào các tính năng nâng cao của các sàn lớn như Shopee/Lazada.

### \[AI-02\] Rà soát User Story và chia Sprint 1 cho dự án TMĐT

* Ngày / Người dùng: 2024-10-18 / Nguyễn Đắc Quốc

* Công cụ: Claude 3.5 Sonnet

* Giai đoạn: Lập kế hoạch

* Task / Commit / PR: \[PLAN\] Sprint 1 Backlog & Story Estimation / `7e2d9c4` / PR #2

* Mục đích: Chuyển đổi yêu cầu nghiệp vụ sàn TMĐT thành danh sách User Story chuẩn Agile và lập kế hoạch Sprint 1 (1 tuần).

* Prompt chính (nguyên văn hoặc link chia sẻ hội thoại): "Tôi có danh sách chức năng hệ thống thương mại điện tử. Hãy chuyển đổi thành 12 User Story dạng 'As a... I want to... So that...' và gợi ý phân chia Sprint 1 tập trung vào luồng Mua hàng cơ bản cho nhóm 5 người (1 Leader, 2 Frontend, 2 Backend)."

* Kết quả AI trả về (tóm tắt): AI tạo 12 User Story hoàn chỉnh kèm ước lượng Story Point, đề xuất Sprint 1 gồm các công việc: Auth, Danh sách/Chi tiết sản phẩm và Giỏ hàng.

* Đánh giá: Đúng về chuẩn định dạng Agile. Tuy nhiên AI ước lượng thời gian cho luồng Giỏ hàng & Tính tổng tiền (kèm Mã giảm giá) quá thấp so với thực tế xử lý ở Backend.

* Đã chỉnh sửa gì: Tách Story Giỏ hàng thành 2 sub-task (Giỏ hàng cơ bản và Xử lý Voucher); tăng Story Point phần Giỏ hàng từ 3pt lên 5pt; gán task theo chuyên môn từng người.

* Cách kiểm chứng: Họp Sprint Planning với nhóm, review danh sách User Story và chốt backlog trên Trello Board.

* Tỷ lệ nội dung AI còn giữ lại (ước lượng): 85%

* Điều học được: Các bài toán nghiệp vụ TMĐT (như tính phí ship, voucher, tồn kho) có nhiều góc khuất logic mà AI khó ước lượng chính xác độ phức tạp nếu không mô tả chi tiết.

### \[AI-03\] Thiết kế Database Schema (Mongoose Model) cho web TMĐT

* Ngày / Người dùng: 2024-10-24 / Nguyễn Đắc Quốc

* Công cụ: ChatGPT (GPT-4o)

* Giai đoạn: Thiết kế

* Task / Commit / PR: \[DB\] Define E-Commerce Database Schemas / `1a5b8c9` / PR #4

* Mục đích: Thiết kế cấu trúc cơ sở dữ liệu MongoDB cho hệ thống TMĐT gồm các entity: User, Product, Category, Cart, Order, Review, Coupon.

* Prompt chính (nguyên văn hoặc link chia sẻ hội thoại): "Viết Mongoose schema cho các collection của website thương mại điện tử: User, Product (có biến thể size/màu, giá, tồn kho), Category, Cart, Order (địa chỉ giao hàng, trạng thái thanh toán, phương thức vnpay/cod), Coupon. Yêu cầu có validate dữ liệu và quan hệ ref giữa các model."

* Kết quả AI trả về (tóm tắt): AI sinh mã nguồn Mongoose Schema cho toàn bộ 7 collection với các ràng buộc validator chuẩn và index hỗ trợ tìm kiếm sản phẩm theo danh mục/giá.

* Đánh giá: Đúng 80%. Đã hỗ trợ mảng biến thể sản phẩm (variants), nhưng trong Order Schema lại thiếu lưu lịch sử giá tại thời điểm mua (dễ bị lỗi nếu giá sản phẩm gốc thay đổi sau này).

* Đã chỉnh sửa gì: Bổ sung trường `priceAtPurchase` trong `Order.items` để cố định giá tại thời điểm khách đặt hàng; thêm enum trạng thái đơn hàng (`Pending`, `Processing`, `Shipped`, `Delivered`, `Cancelled`).

* Cách kiểm chứng: Nạp dữ liệu mẫu (seed data) vào MongoDB, chạy thử các truy vấn tạo đơn hàng và kiểm tra tính toàn vẹn dữ liệu trên MongoDB Compass.

* Tỷ lệ nội dung AI còn giữ lại (ước lượng): 80%

* Điều học được: Thiết kế DB cho TMĐT cần đặc biệt chú ý đến tính nhất quán dữ liệu lịch sử (như giá bán, địa chỉ nhận hàng) để tránh thay đổi khi master data cập nhật.

### \[AI-04\] Xây dựng RESTful API Authentication & Phân quyền User/Admin

* Ngày / Người dùng: 2024-10-29 / Nguyễn Đắc Quốc

* Công cụ: GitHub Copilot

* Giai đoạn: Lập trình

* Task / Commit / PR: \[FEAT\] Auth & RBAC Middleware Implementation / `9d8c7b6` / PR #7

* Mục đích: Lập trình các API Đăng ký, Đăng nhập, Refresh Token, và các Middleware phân quyền người dùng (Customer / Admin) truy cập tài nguyên TMĐT.

* Prompt chính (nguyên văn hoặc link chia sẻ hội thoại): "// Create Express Auth controller for E-Commerce app: register, login, refresh token, bcrypt password, JWT verify middleware and checkAdminRole middleware"

* Kết quả AI trả về (tóm tắt): Copilot tự động hoàn thiện đoạn code Controller và Middleware phân quyền Role-Based Access Control (RBAC) chính xác.

* Đánh giá: Mã hóa Bcrypt và JWT đúng chuẩn. Tuy nhiên AI để lộ thông tin nhạy cảm (như mật khẩu đã hash) trong kết quả trả về của API Profile và hardcode `JWT_SECRET`.

* Đã chỉnh sửa gì: Sử dụng `.select('-password')` khi query thông tin User; chuyển các biến bí mật vào tệp `.env`; bổ sung rate-limiting để chống brute-force đăng nhập.

* Cách kiểm chứng: Dùng Postman test kịch bản: Customer cố tình truy cập API cập nhật sản phẩm của Admin (trả về 403 Forbidden) và Admin đăng nhập thành công (trả về 200 OK kèm Token).

* Tỷ lệ nội dung AI còn giữ lại (ước lượng): 75%

* Điều học được: Bảo mật trong ứng dụng TMĐT rất quan trọng, cần lọc bỏ các trường dữ liệu nhạy cảm trước khi trả kết quả API về client.

### \[AI-05\] Xây dựng giao diện Dashboard Admin quản lý đơn hàng & sản phẩm

* Ngày / Người dùng: 2024-11-03 / Nguyễn Đắc Quốc

* Công cụ: Claude 3.5 Sonnet

* Giai đoạn: Lập trình

* Task / Commit / PR: \[FEAT\] Admin E-Commerce Dashboard & Order Management UI / `4f3e2d1` / PR #12

* Mục đích: Xây dựng giao diện Quản trị viên TMĐT gồm các trang: Thống kê doanh thu cơ bản, Quản lý danh mục/sản phẩm và Xử lý trạng thái đơn hàng.

* Prompt chính (nguyên văn hoặc link chia sẻ hội thoại): "Tạo giao diện ReactJS với Tailwind CSS cho trang Admin E-Commerce Dashboard. Bao gồm: các thẻ KPI (doanh thu, đơn hàng, khách hàng), bảng danh sách đơn hàng có bộ lọc trạng thái (Chờ duyệt, Đang giao, Đã hủy) và Modal cập nhật trạng thái đơn."

* Kết quả AI trả về (tóm tắt): AI tạo một giao diện Dashboard hoàn chỉnh, thiết kế đẹp mắt với Tailwind CSS, tích hợp sẵn các biểu đồ và bảng dữ liệu mẫu.

* Đánh giá: Giao diện rất đẹp, đúng chuẩn Admin Thương mại điện tử. Hạn chế: Code bị dài (hơn 500 dòng trong một file), state giả lập chưa kết nối với API thực tế từ Server.

* Đã chỉnh sửa gì: Tách thành các component độc lập (`KpiCard.jsx`, `OrderTable.jsx`, `OrderStatusModal.jsx`); viết custom hook `useOrders` kết nối với API Backend Express.

* Cách kiểm chứng: Thao tác đổi trạng thái đơn hàng trên giao diện, kiểm tra tính tương thích responsive trên các màn hình và xác nhận DB được cập nhật đúng.

* Tỷ lệ nội dung AI còn giữ lại (ước lượng): 65%

* Điều học được: Giao diện Admin TMĐT cần trực quan và thao tác nhanh; việc tách nhỏ component giúp code dễ bảo trì khi quy mô dự án tăng lên.

### \[AI-06\] Viết Unit Test cho API Thanh toán/Giỏ hàng & Fix lỗi CORS

* Ngày / Người dùng: 2024-11-08 / Nguyễn Đắc Quốc

* Công cụ: ChatGPT (GPT-4o)

* Giai đoạn: Kiểm thử

* Task / Commit / PR: \[TEST\] Cart & Checkout API Unit Tests / `8c7b6a5` / PR #18

* Mục đích: Viết Unit Test kiểm thử các API thêm/sửa/xóa giỏ hàng, tính tổng tiền đơn hàng và xử lý cấu hình CORS cho phép ứng dụng Frontend gọi API.

* Prompt chính (nguyên văn hoặc link chia sẻ hội thoại): "Viết Jest test cases cho API POST /api/cart/add và POST /api/orders/checkout (kiểm tra tính đúng tổng tiền, giảm giá coupon, và lỗi khi vượt quá tồn kho). Đồng thời hướng dẫn cài đặt CORS middleware trong Express."

* Kết quả AI trả về (tóm tắt): AI cung cấp đoạn code test Jest/Supertest chi tiết kiểm tra các kịch bản tính toán tiền đơn hàng và file cấu hình CORS đầy đủ.

* Đánh giá: Cấu hình CORS chuẩn. Các test case logic tính tiền chính xác nhưng AI quên Mock kết nối Database, khiến khi chạy test bị ghi dữ liệu rác vào DB phát triển.

* Đã chỉnh sửa gì: Thêm thư viện `mongodb-memory-server` để giả lập Database tạm thời trong bộ nhớ khi chạy Unit Test, đảm bảo tính độc lập và sạch sẽ của dữ liệu.

* Cách kiểm chứng: Chạy lệnh `npm run test` trên terminal, tất cả 12 test cases của phần Cart & Checkout đều đạt (PASSED) với tỷ lệ phủ code 88%.

* Tỷ lệ nội dung AI còn giữ lại (ước lượng): 80%

* Điều học được: Luôn dùng Database giả lập (In-memory DB) hoặc Mock khi viết Unit Test cho luồng thanh toán TMĐT để tránh biến đổi dữ liệu thực.