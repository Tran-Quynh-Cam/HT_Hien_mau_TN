# Hệ Thống Quản Lý Hiến Máu Tình Nguyện

## Giới thiệu
Đây là tài liệu tổng quan cho tiểu dự án **Quản lý hệ thống hiến máu tình nguyện**.
Mục tiêu là hỗ trợ số hóa quy trình hiến máu từ đăng ký, đặt lịch, xác nhận hiến máu đến quản lý kho máu và thống kê.

## Mục tiêu hệ thống
- Tạo nền tảng cho người hiến máu đăng ký tài khoản và đăng ký lịch hiến máu.
- Hỗ trợ nhân viên y tế/quản trị viên quản lý kho máu hiệu quả.
- Tự động gửi thông báo nhắc lịch hiến máu và thông báo khẩn khi cần nhóm máu hiếm.
- Cung cấp báo cáo, thống kê theo thời gian, địa điểm, nhóm máu.
- Nâng cao khả năng theo dõi lịch sử hiến máu của từng người dùng.

## Đối tượng sử dụng
- Người hiến máu.
- Nhân viên y tế.
- Quản trị viên hệ thống.

## Chức năng chính

### 1. Dành cho người hiến máu
- Đăng ký tài khoản (xác thực OTP).
- Đăng nhập.
- Cập nhật thông tin cá nhân.
- Đăng ký lịch hiến máu theo địa điểm/thời gian phù hợp.
- Hủy lịch hiến máu theo quy định.
- Xem lịch sử hiến máu.

### 2. Dành cho nhân viên y tế
- Đăng nhập.
- Quản lý kho máu (nhóm máu, số lượng, hạn sử dụng, trạng thái).
- Xác nhận lịch hiến máu.
- Xem báo cáo/thống kê số lượng máu theo nhiều tiêu chí.

### 3. Dành cho quản trị viên
- Đăng nhập quản trị.
- Quản lý kho máu.
- Gửi thông báo đến người hiến máu.

### 4. Tự động từ hệ thống
- Tự động xác nhận hiến máu thành công.
- Tự động gửi thông báo xác nhận đăng ký, nhắc lịch hiến máu.
- Hỗ trợ thông báo khẩn qua email/SMS/giao diện hệ thống khi cần máu đặc biệt.

## Quy trình nghiệp vụ cốt lõi

### Quy trình tiếp nhận người hiến máu
1. Đăng ký thông tin.
2. Kiểm tra sức khỏe.
3. Thực hiện hiến máu.
4. Theo dõi sau hiến máu.

### Quy trình đăng ký tài khoản (UC-01)
1. Người dùng nhập thông tin cá nhân.
2. Hệ thống kiểm tra hợp lệ.
3. Hệ thống gửi OTP qua email/số điện thoại.
4. Người dùng nhập OTP để xác thực.
5. Tạo tài khoản thành công và chuyển tới đăng nhập.

Luồng ngoại lệ:
- Thông tin không hợp lệ: yêu cầu nhập lại.
- OTP không hợp lệ: yêu cầu nhập lại hoặc gửi lại OTP.

### Quy trình đăng nhập (UC-02)
1. Người dùng nhập tên đăng nhập và mật khẩu.
2. Hệ thống kiểm tra thông tin.
3. Nếu hợp lệ: chuyển vào trang chức năng.
4. Nếu không hợp lệ: hiển thị thông báo lỗi.

## Yêu cầu phi chức năng nổi bật
- Bảo mật dữ liệu người hiến máu (phân quyền truy cập, mã hóa dữ liệu).
- Độ chính xác và nhất quán dữ liệu kho máu.
- Khả năng mở rộng để tích hợp nền tảng mobile trong tương lai.
- Hỗ trợ báo cáo phục vụ phân tích (ví dụ tích hợp Excel/Power BI).

## Khó khăn và hướng cải tiến

### Khó khăn hiện tại
- Thiếu nguồn máu hiếm.
- Khó khăn trong bảo quản và đồng bộ dữ liệu.

### Hướng phát triển
- Gợi ý địa điểm hiến máu tối ưu theo vị trí người dùng.
- Nâng cấp trải nghiệm thông báo khẩn đa kênh.
- Mở rộng hệ thống trên nền tảng di động.

## Trạng thái tài liệu
README này được viết lại từ nội dung báo cáo khảo sát/phân tích nghiệp vụ trong file `report.docx` (ngày 25/03/2025).