# Kế hoạch kiểm thử Celine Closet — 79 ca

Trần Ngọc Diễm Huyền (TS03223), Nguyễn Quang Khải (TS03226) · SD21307. Lịch và phân công đề xuất cho bản cập nhật Tuần 1 và 2.

| Nhân lực | Thời hạn | Ngày bắt đầu | Ngày bàn giao | Phương thức | Phạm vi & nhiệm vụ chi tiết |
|---|---|---|---|---|---|
| Huyền và Khải | 1 ngày | 15/11/2026 | 15/11/2026 | Đối chiếu đặc tả và mã | Rà soát luồng đăng ký, đăng nhập, phân quyền và CRUD danh mục. Chuẩn bị dữ liệu thử. |
| Trần Ngọc Diễm Huyền | 1 ngày | 15/11/2026 | 15/11/2026 | JUnit, Mockito, kiểm tra web | 51 ca UT_001–UT_051 cho tài khoản. Kiểm tra thêm 6 ca UI_001–UI_006 và cập nhật kết quả. |
| Nguyễn Quang Khải | 1 ngày | 15/11/2026 | 15/11/2026 | JUnit, Mockito, kiểm tra web | 16 ca UT_052–UT_067 cho quyền và quản lý danh mục. Kiểm tra thêm 6 ca UI_007–UI_012 và cập nhật kết quả. |
| Huyền và Khải | Sau khi kiểm tra | 15/11/2026 | 15/11/2026 | Maven và GitHub | Mỗi bạn chạy đủ 67 ca trên máy, lưu kết quả và đăng mã kiểm thử cùng tài liệu vào repo cá nhân. |

## Phương pháp và phạm vi

| Phân hệ | Dữ liệu và kỹ thuật | Kiểm tra |
|---|---|---|
| Đăng ký | Phân vùng hợp lệ, thiếu, sai định dạng, trùng, xác nhận sai. Biên mật khẩu 7/8/9 và 31/32/33, điện thoại 9/10/11 chữ số. | Lỗi form hoặc chuyển trang đăng nhập, xác minh DAO và mật khẩu băm. |
| Đăng nhập, đăng xuất | Email tồn tại hoặc chưa tồn tại, thông tin không khớp, 4 vai trò, next=wishlist. | Đối chiếu session, phản hồi và đường dẫn. |
| Quản lý danh mục | Quyền ADMIN, CRUD, ẩn/hiện, ID sai và DAO lỗi. | Đối chiếu dữ liệu chuyển DAO, chuyển trang, phân quyền và ngoại lệ. |
| UI và SQL | 12 ca chạy tay trên trình duyệt với DB thử. | Ghi kết quả thực tế, đối chiếu dữ liệu sau tải lại, chụp ảnh khi có sai khác. |

Môi trường JUnit dùng JDK 17 hoặc 21, Maven, JUnit 5 và Mockito. Web thử dùng Eclipse, Tomcat 11 và SQL Server CelineClossetDB. Đặt email và tên danh mục riêng cho mỗi bạn. Phạm vi của gói tập trung vào tài khoản và danh mục.

| Điều kiện | Tiêu chí |
|---|---|
| Bắt đầu | Mở được project Maven, có JDK phù hợp. Ca UI cần Tomcat, DB thử, tài khoản khách và ADMIN. |
| Tạm dừng | Ghi nhận lỗi môi trường, thiếu dữ liệu thử hoặc lỗi triển khai trước khi đánh giá ca nghiệp vụ. |
| Chạy lại | Khắc phục nguyên nhân, chạy lại ca bị ảnh hưởng và ghi bằng chứng. |
| Hoàn thành JUnit | 67 lượt, 0 failures, 0 errors, 0 skipped. Giữ báo cáo Surefire. |
| Hoàn thành UI | 12 ca có kết quả thực tế. Khi phát hiện lỗi, ghi ID, bước tái hiện, kết quả mong đợi, thực tế và bằng chứng. |
