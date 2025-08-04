# Soạn Requirement dưới dạng User Story

Dưới đây là phần soạn theo đúng cấu trúc bạn yêu cầu:

---

## 🧠 Giải thích khái niệm

---

### ✅ **User Story là gì?**

**User Story** là một mô tả ngắn gọn, dễ hiểu về nhu cầu của người dùng đối với hệ thống.

* Dạng phổ biến:

  > *Là một \[loại người dùng], tôi muốn \[mục tiêu] để \[lý do/lợi ích].*

* **Mục tiêu:** giúp team hiểu *ai cần gì và tại sao*, không đi sâu vào cách làm kỹ thuật.

* **Ví dụ:**

  > *Là một khách hàng, tôi muốn xem trạng thái đơn hàng để biết khi nào sản phẩm được giao.*

---

### ✅ **Use Case là gì?**

**Use Case** là tài liệu chi tiết mô tả **tương tác giữa người dùng và hệ thống** nhằm đạt được một mục tiêu cụ thể.

* Bao gồm:

  * Actor (người dùng tương tác)
  * Mục tiêu
  * Điều kiện đầu vào (precondition)
  * Luồng chính (main flow)
  * Luồng phụ (alternate flow)
  * Ngoại lệ (exception flow)

* **Mục tiêu:** giúp dev/test hiểu rõ luồng nghiệp vụ và viết code/test chính xác.

* **Ví dụ:**

  * **Use Case:** Thanh toán đơn hàng
  * **Luồng chính:** Chọn sản phẩm → nhập địa chỉ → chọn thanh toán → xác nhận → hoàn tất đơn

---

## ⭐ Best Practices


| Tóm tắt cách làm:                                                                         |
| ----------------------------------------------------------------------------------------- |
| 🔹 Viết **User Story** cho từng chức năng ở mức tổng quan, từ góc nhìn người dùng         |
| 🔹 Viết **Use Case** nếu chức năng đó có nhiều bước, có phân nhánh, hoặc cần teamwork sâu |
| 🔹 Đừng trộn kỹ thuật vào User Story – hãy để dev/task lo phần đó                         |


### ✅ **Khi nào dùng User Story:**

* Khi làm việc theo **Scrum / Agile**
* Khi cần quản lý **product backlog nhanh, linh hoạt**
* Khi ưu tiên **giá trị người dùng** và tránh đặc tả kỹ thuật sớm

---

### ✅ **Khi nào dùng Use Case:**

* Khi cần mô tả chi tiết **từng bước tương tác**
* Khi có **nhiều nhánh logic, lỗi, phân quyền**
* Khi dự án lớn, cần tài liệu rõ cho **dev / tester / BA**

---

### 📌 **Kết hợp tốt nhất:**

* Dùng **User Story** để định nghĩa yêu cầu từ góc nhìn người dùng.
* Dùng **Use Case** cho những chức năng phức tạp → hỗ trợ dev/test viết logic rõ ràng hơn.

---

### 🛠️ Mẹo thực tế:

| Tình huống                            | Nên dùng   |
| ------------------------------------- | ---------- |
| Form đăng nhập đơn giản               | User Story |
| Thanh toán có nhiều bước + xử lý lỗi  | Use Case   |
| Trang hiển thị danh sách              | User Story |
| Chức năng quản lý phân quyền phức tạp | Use Case   |

---

Nếu bạn muốn, mình có thể giúp bạn tạo file tài liệu dạng `.md`, `.pdf`, hoặc mẫu Notion dùng cho cả team. Bạn muốn định dạng nào?



## Ví dụ mẫu:

Dưới đây là ví dụ về cách **soạn lại chi tiết User Stories cho Trang chủ** hệ thống bán hàng, **có mã Story (Story ID)** theo mẫu quản lý backlog chuyên nghiệp. Mỗi mục gồm:

* Mã story
* Tiêu đề ngắn
* Mô tả user story
* Acceptance criteria
* Gợi ý backend API nếu có

---

- [Trang chủ](./home-story.md)
- [Trang Login](./login-story.md)