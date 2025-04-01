# Step 03 Init Project

Sau khi Team hoàn tất Step 1-2 thì tiến hành bắt tay vào cấu hình dự án (Init Project)

>Nguyên tắc cái gì sử dụng CHUNG thì LÀM TRƯỚC

## 💛 A. Cấu trúc dự án

### A1. Dự án HTML Css

Cấu trúc cơ bản một dự án HTML có sử dụng js, css, và hình ảnh

```html
root/
├─ js/
│  ├─ main.js
├─ images/
│  ├─ image-1.png
│  ├─ image-2.jpg
├─ css/
│  ├─ global.css
│  ├─ index.css
│
├─ download.html
├─ contact-us.html
├─ index.html

```

Nếu sử dụng thêm các thư viện bổ trợ khác như Font Awesome, Owl Carousel thì đặt thư viện đó vào folder tên là plugins

- Css dùng chung: đặt trong file css/global.css
- Css của trang nào thì tạo riêng file css cho trang đó ví dụ css/index.css

Tương tự như vậy

- Js dùng chung: đặt trong file js/global.js
- Js dùng riêng cho trang nào thì tạo file riêng js cho trang đó js/index.js

**Lưu ý quan trọng**

Tổ chức tên file, tên thư mục, tên class css làm sao để khi RAP (Merge) code lại không xảy ra hiện tượng bị trùng tên, xung đột class.

### 💛 A2. Dự án ReactJs

Cấu trúc phổ biến

```html
react-ecommerce/
├─ node_modules/
├─ public/
├─ src/
│  ├─ components/
│       ├─ ui
│       ├─ layout
│       ├─ shared
│  ├─ constants/
│  ├─ hooks/
│  ├─ libs/
│  ├─ utils/
│  ├─ stores/
│  ├─ pages/
│       ├─ HomePage
│       ├─ ProductPage
│       ├─ ProductDetailPage
│       ├─ CartPage
│       ├─ CheckOutPage
│       ├─ CheckOutDonePage
│       ├─ LoginPage
│       ├─ RegisterPage
│       ├─ CustomerPage
│       ├─ CustomerOrderPage
│       ├─ CustomerProfilePage
│       ├─ NoPage
│  ├─ App.tsx
│  ├─ App.css
│  ├─ index.css
│  ├─ main.tsx
├─ .env
├─ index.html
├─ .gitignore
├─ package.json
├─ README.md
├─ tsconfig.json
├─ vite.config.ts

```

### 💛 A3. Dự án NodeJS and ExpressJS

Cấu trúc backend api với NodeJS and ExpressJS đơn giản

```html
project-restful-apis/
├── node_modules/
├── public/             # Tệp tĩnh như hình ảnh, CSS, JavaScript, v.v.
├── src/
│   ├── controllers/    # Xử lý các request và gọi các service tương ứng
│   ├── middleware/     # Các middleware như xác thực, logging, v.v.
│   ├── models/         # Các model đại diện cho dữ liệu (ORM/ODM models)
│   ├── services/       # Business logic chính của ứng dụng
│   ├── helpers/        # Các hàm tiện ích được dùng trong nhiều nơi
│   ├── validations/    # Xác thực dữ liệu request
│   ├── configs/        # Các file cấu hình (config.js, database.js, v.v.)
│   ├── routes/         # Định nghĩa các route của API
│   │   ├── v1/         # API v1 routes
│   │   ├── v2/         # API v2 routes (nếu có)
│   ├── app.ts          # Cấu hình Express và middleware chính
│   ├── server.ts       # Tệp khởi động server (kết nối DB và chạy server)
├── .env                # Biến môi trường cho project
├── .gitignore          # Các tệp và thư mục không cần đưa vào git
├── package.json        # Thông tin dự án và các dependencies
├── README.md           # Tài liệu hướng dẫn về dự án
```


## 💛 B. Tài nguyên dùng chung

- Bạn phụ trách init project thực hiện code các tính năng dùng chung và push lên git để thành viên team `clone` về triển khai task chi tiết.
- Thống nhất quy trình triển khai code