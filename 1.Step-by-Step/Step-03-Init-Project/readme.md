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

### 💛 A3. Dự án NodeJS and ExpressJS


