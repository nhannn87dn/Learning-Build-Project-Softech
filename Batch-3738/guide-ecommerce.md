# Hướng dẫn làm đề tài E-Commerce

## EndUser 

### Trang chủ

- Slide Banner chính: tạo một Model mới với ads có các trường


```js
{
    src: 'link hinh',
    alt: 'noi dung cho alt',
    link: 'link khi click vao hinh'
}
```
- SP khuyến mãi (nếu có): lấy theo promoPrice, startDatePromo, endDatePromo, isHome =true

- SP Bán chạy (Nếu có): isBest = true, isHome = true

- SP theo từng loại danh mục: Lấy số lượng hiển thị ra một cách linh động (limit=4) , isHome=true

- Tin mới lên: Model Article: title, description, content, author, createdAt, thumbnail

### Danh mục sản phẩm

- Hiển thị danh sách sản phẩm theo `slug`
- Lọc sản phẩm theo danh mục (nếu có)
- Sắp giá tăng dần, giảm dần (bắt buộc)
- Lọc theo thuộc tính nếu có. ví dụ: ram 16gb, cpu i3 (nếu có)
- Phân trang (bắt buộc)

### Chi tiết sản phẩm

- Hình ảnh sản phẩm (bắt buộc)
- Gallery hình: là một mảng (Nếu có)

```js
photos: [
    {
        id,
        src,
        alt
    }
]
```

- Thông số kỹ thuật (nếu có)

```js
params: [
    {
        id: 1
        key: 'He dieu hanh'
        value: 'Android 11'
    },
]
```

- Bài viết mô tả sản phẩm (bắt buộc)
- Nút đặt hàng, chọn số lượng cần đặt


### Giỏ hàng

Lấy sản phẩm từ localStorage lên để hiển thị, Dùng zustand.


### CheckOut

- Điền thông tin người mua
- Phương thức thanh toán

---

### Quản lý đăng nhập (nếu có)

- Login
- Register
- Quên mật khẩu
- Trang Dashboard của khách hàng: profile, lịch đơn hàng đã đặt



## Dashboard

Phân quyền nếu có. dựa vào thuộc tính `role`  của user đang login  từ model `staff`

### Quản lý đơn hàng

- Hiển thị danh sách đơn hàng
- Bộ lọc: mã đơn hàng (LIKE), theo số đt (LIKE), trạng thái đơn, ngày đặt (BETWEEN)
- Cập nhật được trạng thái đơn hàng: pending --> đã xử lý, đã thanh toán
- Có thể bỏ bớt, thêm sản phẩm vào đơn hàng (Nếu làm đc)


### Quản lý sản phẩm

- Gắng làm cho được cái Upload hình ảnh sản phẩm
- Tìm hiểu cách để tích hợp CKeditor React để soạn bài viết mô tả cho sản phẩm


### Các mục còn lại

- Thêm, edit, delete, danh sách
