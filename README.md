# Moveek Website - Pages Documentation
## Trang chủ (Home)
- **Đường dẫn:** `/`
- **Chức năng:**
  - Hiển thị giới thiệu tổng quan về website.
  - Gợi ý các nội dung nổi bật hoặc mới nhất.
  - Nút điều hướng đến các trang chính.

![Home](https://drive.google.com/file/d/1Om-EXMCFgmlv3Lvfm4yIegJkSwsJ2VIb/view?usp=drive_link)
---

## Trang đăng nhập (Login)
- **Đường dẫn:** `/login` và `/admin/login`

- **Chức năng:**
  - Cho phép người dùng đăng nhập vào hệ thống.
  - Tích hợp xác thực (authentication).
  - Phân quyền người dùng nếu có (Admin/User).

- **Yêu cầu:**
  - Chưa có token user nào trong cookies
  - Đảm bảo xác thực quyền qua Api

![Login](https://drive.google.com/file/d/1fNqtcZ62tp-9AfDfrXP6nmm4uPAAqAuf/view?usp=drive_link)
![Login Admin](https://drive.google.com/file/d/1fNqtcZ62tp-9AfDfrXP6nmm4uPAAqAuf/view?usp=drive_link)
---

## Trang tổng quan quản trị(Dashboard Admin)

- **Đường dẫn:** `/admin/dashboard`

- **Chức năng:**
  -Cho phép quản trị viên có xem nội dung tổng quan của website(Số lượng phim, số lượng người dùng, số lượng rạp, số lượng đặt vé).

- **Yêu cầu:**
  - Đảm bảo dữ liệu được tải từ API hoặc database.

![Admin Dashboard](https://drive.google.com/file/d/1xBaynqAQON-O4PRXM9kfvFaN9lhnWThq/view?usp=drive_link)

---

## Trang danh sách phim (Movies)

- **Đường dẫn:** `/admin/movies`
- **Chức năng:**
  - Danh sách phim đang chiếu, sắp chiếu.
  - Lọc phim theo thể loại, định dạng...
  - CRUD

- **Yêu cầu:**
  - Đảm bảo dữ liệu được tải từ API hoặc database.

![Movies List](https://drive.google.com/file/d/1MvYpnM8qQRyOgJx8IPH4fsqkdC-hd8fZ/view?usp=drive_link)

---

## Trang danh sách rạp (Theaters)

- **Đường dẫn:** `/admin/theaters`
- **Chức năng:**
  - Danh sách rạp phim.
  - Lọc rạp theo địa điểm, loại rạp...
  - CRUD

- **Yêu cầu:**
  - Đảm bảo dữ liệu được tải từ API hoặc database.

![Theaters List](https://drive.google.com/file/d/1ZGLXw5FiDRUrYsDZ4AGU64ia5VW6R1di/view?usp=drive_link)

---

## Trang danh sách suất chiếu (Showtimes)

- **Đường dẫn:** `/admin/showtimes`
- **Chức năng:**
  - Danh sách suất chiếu phim.
  - Lọc suất chiếu theo ngày giờ, phim, rạp...
  - CRUD

- **Yêu cầu:**
  - Đảm bảo dữ liệu được tải từ API hoặc database.

![Showtimes List](https://drive.google.com/file/d/1fv8NnU6xAq2mMtHH2U-iTA0R3xc5rpO5/view?usp=drive_link)

---

## Trang danh sách người dùng (Users)

- **Đường dẫn:** `/admin/users`
- **Chức năng:**
  - Danh sách người dùng.
  - Lọc người dùng theo vai trò, trạng thái...

- **Yêu cầu:**
  - Đảm bảo dữ liệu được tải từ API hoặc database.

![Users List](https://drive.google.com/file/d/1Kir0Ynz4ltIDrAskWeSQ-AbJHHpIA-ze/view?usp=drive_link)
  
---
## Trang danh sách vé (Bookings)

- **Đường dẫn:** `/admin/bookings`
- **Chức năng:**
  - Danh sách vé đã đặt.
  - Lọc vé theo ngày giờ, phim, rạp...

- **Yêu cầu:**
  - Đảm bảo dữ liệu được tải từ API hoặc database.

![Bookings List](https://drive.google.com/file/d/13pQzRZgFT7O2C40-la3NrlgM62jirpF5/view?usp=drive_link)

---

## ⏰ Trang chọn suất chiếu phim (Showtime Selection)

- **Đường dẫn:** `/lich-chieu/[movieCode]`
- **Chức năng:**
  - Hiển thị danh sách các suất chiếu của một bộ phim đã chọn.
  - Người dùng có thể lọc theo:
    - Ngày chiếu (calendar picker).
    - Rạp chiếu (theater).
  - Khi chọn suất chiếu, người dùng sẽ được chuyển sang bước chọn ghế.

- **Yêu cầu:**
  - Đã chọn phim trước đó.
  - Đảm bảo suất chiếu được tải từ API hoặc database.

![Showtime Selection](https://drive.google.com/file/d/1DvMEaujVW_UCdz3c2AqpBdoPFyV-jJpX/view?usp=drive_link)

---

## Trang chọn ghế (Seat Selection)

- **Đường dẫn:** `/dat-ve/[showtimeId] (chế độ 1 của trang)
- **Chức năng:**
  - Hiển thị thông tin của suất chiếu.
  - Hiển thị sơ đồ ghế của phòng.
  - Khi chọn xong ghế, người dùng sẽ được chuyển sang bước nhập thông tin thanh toán.

- **Yêu cầu:**
  - Đã chọn suất chiếu trước đó.
  - Đảm bảo ghế được tải từ API hoặc database.

![Seat Selection](https://drive.google.com/file/d/1lW7wne3E9KzdfeQ4Ao5oIOC9YBqMPgIa/view?usp=drive_link)

---

## Trang nhập thông tin thanh toán (Payment Method)

- **Đường dẫn:** `/dat-ve/[showtimeId]` (Chế độ 2 của trang)
- **Chức năng:**
  - Hiển thị thông tin vé và các ghế đã chọn.
  - Cho phép nhập thông tin thanh toán.
  - Tích hợp cổng thanh toán VNPay.
  - Tự động chuyển hướng người dùng đến trang cổng VNPAY để thanh toán.
  - Nhận callback từ VNPAY (sau khi người dùng thanh toán thành công/thất bại).
  - Hiển thị kết quả thanh toán cho người dùng.
- **Yêu cầu:**
  - Đơn hàng đã được khởi tạo và lưu tạm (pending).
  - Dữ liệu gửi đi đúng format của VNPAY (mã hóa, checksum, redirect URL,...).
  - Server/backend xử lý được response từ VNPAY và cập nhật trạng thái đơn hàng.
  - Đảm bảo bảo mật thông tin giao dịch.

![Payment Method](https://drive.google.com/file/d/1SGHwVxhh4fqGxtxFbThehQ2qCPdDmj92/view?usp=drive_link)
![Payment Method](https://drive.google.com/file/d/1ajT5uSHWWFOxSLbJIFtLtGuRF0k3uu7a/view?usp=drive_link)
![Payment Method](https://drive.google.com/file/d/1BkIz0gmV2jSzvcY_Mb5YIzD355sBKShl/view?usp=drive_link)

---

## Trang thông tin vé (Ticket Confirmation)

- **Đường dẫn:** `/thong-tin-ve/[bookingCode]`
- **Chức năng:**
  - Hiển thị thông tin vé và các ghế đã chọn.
  - Cho phép người dùng in vé hoặc tải về.
- **Yêu cầu:** Đơn hàng đã được thanh toán thành công.
- **Lưu ý:** Đảm bảo bảo mật thông tin giao dịch.

![Ticket Confirmation](https://drive.google.com/file/d/1sKWBWc5XvXkComjJ72H476wqjYMzOiKT/view?usp=drive_link)

---

## Trang thông tin người dùng (User Profile)

- **Đường dẫn:** `/user/profile`
- **Chức năng:**
  - Hiển thị thông tin người dùng.
  - Cho phép người dùng cập nhật thông tin cá nhân.
  - Hiển thị lịch sử đặt vé của người dùng

- **Yêu cầu:** Người dùng đã đăng nhập.
- **Lưu ý:** Đảm bảo bảo mật thông tin cá nhân.

![User Profile](https://drive.google.com/file/d/176TOHT1ZgNAs6uLr57U24LsWp8Kuu--E/view?usp=drive_link)