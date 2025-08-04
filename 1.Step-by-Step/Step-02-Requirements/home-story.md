
# 🧾 User Stories – Trang Chủ E-Commerce

---

### 🟦 **Story ID:** `HP-001`

### 🏷 **Tiêu đề:** Hiển thị banner trên trang chủ

### 📄 **User Story:**

> Là một khách truy cập, tôi muốn xem các banner quảng cáo nổi bật trên trang chủ để biết những chương trình khuyến mãi hoặc sản phẩm đang được chú ý.

### ✅ **Acceptance Criteria:**

* Hiển thị banner ở đầu trang chủ dưới dạng slider (carousel).
* Mỗi banner hiển thị hình ảnh, tiêu đề ngắn và nút CTA "Xem ngay".
* Click vào banner dẫn tới landing page hoặc trang sản phẩm.
* Banner phải responsive trên desktop và mobile.
* Quản trị viên có thể quản lý (tạo, sửa, xoá) banner từ dashboard.

### 🔌 **Backend gợi ý:**

* `GET /banners`
* `POST /banners`, `PUT /banners/:id`, `DELETE /banners/:id`

---

### 🟦 **Story ID:** `HP-002`

### 🏷 **Tiêu đề:** Hiển thị sản phẩm theo danh mục nổi bật

### 📄 **User Story:**

> Là một khách truy cập, tôi muốn thấy một số sản phẩm tiêu biểu của mỗi danh mục chính ngay trên trang chủ để dễ dàng tiếp cận sản phẩm phù hợp với nhu cầu.

### ✅ **Acceptance Criteria:**

* Hiển thị tối đa 5 sản phẩm cho mỗi danh mục nổi bật (ví dụ: Áo thun, Giày, Phụ kiện...).
* Mỗi sản phẩm hiển thị: ảnh đại diện, tên sản phẩm, giá bán.
* Click vào sản phẩm → chuyển đến trang chi tiết sản phẩm.
* Tên danh mục là heading, có liên kết đến trang danh sách danh mục đầy đủ.
* Danh mục nổi bật được chọn từ backend (flag `isFeatured: true`).

### 🔌 **Backend gợi ý:**

* `GET /homepage/featured-categories-products`
  → Trả về danh sách danh mục và 5 sản phẩm mỗi danh mục.

---

### 🟦 **Story ID:** `HP-003`

### 🏷 **Tiêu đề:** Hiển thị danh sách sản phẩm khuyến mãi

### 📄 **User Story:**

> Là một khách hàng, tôi muốn thấy các sản phẩm đang giảm giá trên trang chủ để dễ dàng nhận biết ưu đãi hấp dẫn và mua nhanh.

### ✅ **Acceptance Criteria:**

* Hiển thị 5 sản phẩm đang khuyến mãi (giá giảm).
* Mỗi sản phẩm hiển thị: ảnh, tên, giá gốc, giá khuyến mãi, phần trăm giảm giá.
* Có nhãn "SALE" hoặc “Giảm giá” trên sản phẩm.
* Sản phẩm có thể click để xem chi tiết.

### 🔌 **Backend gợi ý:**

* `GET /products?isDiscounted=true&limit=5`

---

### 🟦 **Story ID:** `HP-004`

### 🏷 **Tiêu đề:** Hiển thị tin tức mới nhất trên trang chủ

### 📄 **User Story:**

> Là một khách hàng, tôi muốn đọc nhanh các bài viết hoặc tin tức mới nhất từ trang chủ để cập nhật xu hướng, mẹo hay hoặc thông tin hữu ích liên quan đến sản phẩm.

### ✅ **Acceptance Criteria:**

* Hiển thị tối đa 5 bài viết mới nhất từ blog hoặc mục tin tức.
* Mỗi bài viết hiển thị: ảnh thumbnail, tiêu đề, ngày đăng, đoạn mô tả ngắn (\~100 ký tự).
* Click vào ảnh hoặc tiêu đề → chuyển đến trang chi tiết bài viết.
* Thứ tự bài viết theo ngày đăng (mới nhất trước).

### 🔌 **Backend gợi ý:**

* `GET /posts?limit=5`

---
