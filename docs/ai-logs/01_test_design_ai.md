# Nhật ký thiết kế kiểm thử với AI
Đầu vào: SPECIFICATIONS.md và mã AuthController, ValidationUtil, AdminCategoryController, CategoryDAO cùng form danh mục.

Yêu cầu thiết kế: Dựa trên đặc tả Celine Closet, lập kế hoạch và bảng ca kiểm thử cho controller và UI đăng ký, đăng nhập, quản lý danh mục. Dùng phân vùng tương đương và giá trị biên. Ghi dữ liệu, thao tác và kết quả mong đợi.

Đối chiếu mã: đăng nhập bằng email, mật khẩu giới hạn cả hai đầu 8–32, số điện thoại bắt đầu bằng 0, quyền CRUD danh mục thuộc ADMIN và xóa là xóa mềm. Ca chưa thực thi ghi Chưa chạy.


## Cập nhật gói dùng chung
Yêu cầu cập nhật là trình bày Test Plan và Test Cases theo bảng có phân công, tiền điều kiện, bước chạy, dữ liệu, mong đợi và trạng thái. Đối chiếu 67 lượt JUnit thật của Celine Closet và 12 ca web/SQL.
