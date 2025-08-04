# User Story: Trang Đăng Nhập Hệ Thống Mua Hàng

## User Story ID: US-LOGIN-001

**Tiêu đề**: Đăng nhập vào hệ thống mua hàng

**Mô tả**:  
Với vai trò là **người dùng** (khách hàng đã đăng ký),  
Tôi muốn **đăng nhập vào hệ thống mua hàng bằng email và mật khẩu**,  
Để tôi có thể **truy cập tài khoản cá nhân, xem lịch sử mua hàng và thực hiện các giao dịch**.

**Tiêu chí chấp nhận**:  
- Người dùng nhập email và mật khẩu hợp lệ, sau đó được chuyển hướng đến trang chủ hoặc trang tài khoản.  
- Nếu email hoặc mật khẩu không đúng, hệ thống hiển thị thông báo lỗi rõ ràng (ví dụ: "Email hoặc mật khẩu không đúng").  
- Hệ thống hỗ trợ tùy chọn "Quên mật khẩu" để khôi phục tài khoản.  
- Giao diện đăng nhập phải thân thiện, hoạt động tốt trên cả desktop và mobile.  
- Thời gian phản hồi của hệ thống dưới 2 giây khi thông tin đăng nhập hợp lệ.  

**Độ ưu tiên**: Cao  
**Giá trị kinh doanh**: Cho phép người dùng truy cập an toàn vào tài khoản, đảm bảo trải nghiệm mua sắm liền mạch và tăng mức độ tương tác với hệ thống.

---

## Use Case ID: UC-LOGIN-001  
**Tên Use Case**: Đăng nhập bằng email và mật khẩu  

**Diễn viên**: Người dùng (khách hàng đã đăng ký)  
**Mô tả ngắn gọn**: Người dùng nhập email và mật khẩu để truy cập hệ thống mua hàng.  

**Điều kiện tiên quyết**:  
- Người dùng đã có tài khoản đăng ký trong hệ thống.  
- Hệ thống đang hoạt động bình thường.  

**Luồng chính**:  
1. Người dùng truy cập trang đăng nhập.  
2. Người dùng nhập email và mật khẩu vào các trường tương ứng.  
3. Người dùng nhấn nút "Đăng nhập".  
4. Hệ thống kiểm tra thông tin đăng nhập.  
5. Nếu thông tin hợp lệ, hệ thống chuyển hướng người dùng đến trang chủ hoặc trang tài khoản.  

**Luồng phụ**:  
- 4a. Nếu email hoặc mật khẩu không đúng:  
  - Hệ thống hiển thị thông báo lỗi: "Email hoặc mật khẩu không đúng".  
  - Người dùng được yêu cầu nhập lại thông tin.  
- 4b. Nếu người dùng nhấn "Quên mật khẩu":  
  - Hệ thống chuyển hướng đến trang khôi phục mật khẩu.  

**Điều kiện hậu quả**:  
- Người dùng đăng nhập thành công và truy cập được tài khoản.  
- Hoặc người dùng nhận thông báo lỗi và có cơ hội thử lại hoặc khôi phục mật khẩu.

---

## Use Case ID: UC-LOGIN-002  
**Tên Use Case**: Đăng nhập bằng tài khoản mạng xã hội  

**Diễn viên**: Người dùng (khách hàng đã đăng ký hoặc chưa đăng ký)  
**Mô tả ngắn gọn**: Người dùng sử dụng tài khoản mạng xã hội (Google, Facebook) để đăng nhập vào hệ thống.  

**Điều kiện tiên quyết**:  
- Người dùng có tài khoản Google hoặc Facebook.  
- Hệ thống đã tích hợp API đăng nhập mạng xã hội.  

**Luồng chính**:  
1. Người dùng truy cập trang đăng nhập.  
2. Người dùng chọn tùy chọn "Đăng nhập bằng Google" hoặc "Đăng nhập bằng Facebook".  
3. Hệ thống chuyển hướng đến trang xác thực của Google/Facebook.  
4. Người dùng xác nhận thông tin đăng nhập trên Google/Facebook.  
5. Hệ thống nhận thông tin từ Google/Facebook và đăng nhập người dùng.  
6. Nếu là người dùng mới, hệ thống tạo tài khoản mới dựa trên thông tin từ mạng xã hội.  
7. Người dùng được chuyển hướng đến trang chủ hoặc trang tài khoản.  

**Luồng phụ**:  
- 4a. Nếu xác thực mạng xã hội thất bại:  
  - Hệ thống hiển thị thông báo lỗi: "Không thể đăng nhập bằng tài khoản mạng xã hội".  
  - Người dùng được yêu cầu thử lại hoặc sử dụng email/mật khẩu.  

**Điều kiện hậu quả**:  
- Người dùng đăng nhập thành công hoặc được tạo tài khoản mới.  
- Hoặc người dùng nhận thông báo lỗi và có cơ hội thử lại.