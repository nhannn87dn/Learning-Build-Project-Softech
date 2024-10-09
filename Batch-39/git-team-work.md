# Cách sử dụng Git Cơ bản

## Kịch bản:

Có folder code trên máy tính ==> cần chia sẽ cho mọi người cùng làm việc

## Điều kiện

- Cần: 1 Acc github, cài đặt GIT CLI vào máy tính
- Đủ: kết nối git local, git remote.

## Kết nối Local với Remote

### Bước 1: Làm 1 lần

Mở thư mục bạn cần đưa code lên trong terminal. Sau đó nhập lệnh

```bash
git init
# khởi tạo git local
# tạo ra thư mục .git ẩn
```

Tiếp theo bạn cần tạo kết nối giữa repo local với repo remote.

```bash
git remote add origin https://github.com/nhannn87dn/project-react-demo-git.git
```

Giải thích:

- https://github.com/nhannn87dn/project-react-demo-git.git: là link repo remote của bạn

Sau khi nhập lệnh trên, kiểm tra lại xem đã thành công chưa

```bash
git remote -v
```

nếu ra được như dưới là OK

```bash
origin  https://github.com/nhannn87dn/project-react-demo-git.git (fetch)
origin  https://github.com/nhannn87dn/project-react-demo-git.git (push)   
```

### Bước 2: Đồng bộ code từ local lên remote

Bước này gồm bộ 3 lệnh thực hiện liên tiếp nhau:

```bash
# để thêm all các thay đổi vào index
git add .
# Để chốt thay đổi
git commit -m "ghi chu thay doi"
# Thiết lập nhánh main làm mặc định
git branch -M main # làm 1 lần đầu tiên
# Đẩy code từ local lên remote
git push -u origin main # đẩy code lên nhánh main
```


### Bước 3: Teamwork với Git

- Mỗi nhiệm của mỗi người làm thì các bạn sẽ tạo ra một nhánh (branch)

```bash
# Sau khi clone main về, tạo nhánh riêng cho từng task
git checkout -b thang_component_header main
# tạo nhánh tên là thang_component_header sao chép code từ nhánh main qua
# các bạn phải đứng trên nhánh của mình để code
```

Sau code  xong tính năng thì đẩy lên nhánh của mình

```bash
git add .
git commit -m "add feature"
git push -u origin thang_component_header
```

### Bước 4: Merge code vào main

Làm tuần tự

```bash
# chuyển sang nhánh main
git checkout main
# cập nhật thay đổi mới cho main
git pull
# Merge các nhánh khác hoàn thiện vào main
git merge thang_component_header
```

Sau khi merge thì code nó mới chỉ có trên local thôi. Bạn cần đồng bộ lên remote.

```bash
git push -u origin main
```