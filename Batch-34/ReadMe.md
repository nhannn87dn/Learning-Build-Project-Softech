# Chia nhom

## Team 1

Thành viên: Thanh Bình, Kim Ánh, Hoàng Anh, Chí Năm

Đề tài: E-Commerce - 

## Team 2

Thành viên:  Hiếu, Nam Hoàng, Xuân Trọng, Ngọc Anh

Đề tài: E-Commerce - Đồ công nghệ


## Chủ đề E-Commerce

### Giao diện EndUser (Khách hàng dùng)

Ưu tiên dùng NextJS, còn không thì react

```text
e-commerce/
├─ Trang chủ (* Bắt buộc)
├─ Trang Danh Mục Sản phẩm (*)
├─ Trang Chi tiết Sản phẩm (*)
├─ Trang Liên hệ (*)
├─ Trang Giỏ hàng (*) - Danh sách sản phẩm, tăng giảm SL, xóa bớt SP, Tổng tiền
├─ Trang Checkout (*) - Đơn hàng, Thông tin giao hàng, phương thức thanh toán

├─ Trang Login - Nếu quyết định tạo trang khách hàng thì làm
├─ Trang Register 
├─ Trang Customer Profile - Thông tin khách hàng (Thay đổi thông tin Customer, thay đổi mật khẩu)
├─ Trang Customer Orders - Lịch sử đặt hàng

├─ Trang Thông báo Đặt hàng thành công (*)
├─ Trang Danh mục Tin tức
├─ Trang Chi tiết Một bài Tin tức
```

==> **Chi tiết từng trang cần làm gì ?**

- https://ecshopvietnam.com/ecshopmi/
- https://ecshopvietnam.com/ecshopapple/
- https://ecshopvietnam.com/ecshopfashion/
- https://ngocnguyen.vn/
- https://themeforest.net/category/ecommerce?term=technology


### Giao diện Dashboard (Chủ cửa hàng)

```text
e-commerce-Dashboard/
├─ Dashboard (* Bắt buộc)
├─ Trang QL Danh Mục Sản phẩm (*)
├─ Trang QL Sản phẩm (*)
├─ Trang QL Liên hệ (*)
├─ Trang QL Đơn hàng (*)
├─ Trang QL Nhân viên (Employees) - Nếu quyết định tạo trang khách hàng thì làm
├─ Trang QL Shipper (Để giao đơn hàng cho ai đi ship)
├─ Trang QL Danh mục Tin (nếu có làm)
├─ Trang QL Tin (nếu có làm)

```



### API Backend

Code API cho các tính năng trên

- Tham khảo Models: https://github.com/nhannn87dn/NodeJs-ExpressJs-MongooDB-Course/tree/main/02.Examples/express-mongoose-backend-api/src/models



## Init Project - Cấu hình chung

Team sẽ cử ra một bạn, tạo tài khoản github để up code, add thành viên của mình vào quản lí soucre cùng.

### Đối với FrontEnd

- Cài đặt App, các packages dự kiến sử dụng
- Code các component sử dụng chung: Như Layout, Header, Footer, Buttons, Inputs, Font chữ, Size chữ....Style chung

### Đối với Backend

- Tạo Database sử dụng MoongoDB Atlas (cloud)
- Share thông số kết nối cho all thành viên được phân làm Backend
- Khởi tạo dự án API: ExpressJS, Mongoose
- Tạo Các collection độc lập trước, sau đó tạo các collections có quan hệ sau.
- Tạo models, Tạo service, Tạo Controller, Tạo Routes, Tạo Validation
- Tạo Authentication, Authorizarion
