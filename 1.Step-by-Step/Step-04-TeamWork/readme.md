# Step 04 TeamWork

Bạn học được kỹ năng mềm làm việc NHÓM

- Quy trình làm việc nhóm
- Phân công Task cho thành viên nhóm
- Phối hợp xử lý Task trong nhóm


>Nguyên tắc cái gì sử dụng CHUNG thì LÀM TRƯỚC

## 💛 Sử Dụng GitHub khi làm việc NHÓM

Team thảo luận và tiến hành xử lí các Task dùng chung cho dự án TRƯỚC để đẩy lên Github.

Cử một bạn làm nhóm trưởng, thành tạo Github một chút, để đảm nhận công việc Merge code.

### 💥Quy trình đưa dự án lên Github

**1️⃣ Giai đoạn 1:**

1. Tạo repository dự án
2. Add repository vào dự án

```bash
git remote add origin [link-repo]
```
3. Code và đưa những thành phần sử dụng chung lên nhánh main / master

```bash
git add .
git commit -m "init project"
git push -u origin main
```

Lưu ý quan trọng:

- Phần code dùng chung này chỉ duy nhất 1 bạn nào đó được phân công chỉnh sửa ví dụ như Leader. 
- Các thành viên còn lại không được sửa để tránh xung đột (conflict )

**2️⃣ Giai đoạn 2:**

Các thành viên trong nhóm nhận Task và làm việc với Github.

>Nguyên tắc: Không được đụng tới phần code của người khác.

Ví dụ bạn Nguyễn Văn Dũng nhận tasks và thực hiện

Bước 1: Clone repo về

```bash
git clone https://github.com
```

Bước 2: Clone nhánh main sang một nhánh mới và thực hiện các Tasks của mình trên nhánh này.

```bash
git branch -b dung main
```

Lệnh trên có nghĩa là bạn Dũng đang tạo mới nhánh tên là `dung` và sao chép toàn bộ code từ nhánh `main` qua. Đồng thời chuyển đến nhánh `dung`.

Bạn có thể sử dụng lệnh sau để chuyển đến nhánh bạn muốn:

```bash
git checkout [branch name]
```

[branch name] là tên của nhánh cần nhảy đến.

Bước 3: Bạn Dũng tiến hành phần Task được giao trên nhánh `dung`

Bước 4: Bạn Dũng làm xong Tasks tiến hành commit Tasks

```bash
git add .
git commit -m 'do Tasks abc'
```

Đồng bộ nhánh `dung` lên remote

```bash
git push --set-upstream origin dung
```

**3️⃣ Giai đoạn 3:**

Leader thực hiện merge code của tất cả các thành viên sau khi đã push lên nhánh của mình vào nhánh `main`

Cách thực hiện:


-  Lead xem Pull and requests trên Github.
- Chọn Base là `main`. để đưa thay đổi này vào merge `main`
- comment pull: Comment nội dung gì đó khi tạo Create Pull requests
- Merge `dung` vào `main`

Mỗi thành viên sẽ sinh ra một pull request nên Leader thực hiện chu trình này cho tất cả thành viên.

**4️⃣ Giai đoạn 4:**

Chạy thử code ở nhánh `main`

Team thực hiện pull nhánh `main` về sau khi merge

```bash
git checkout main
git pull origin main
```

Nhánh `main` ở local sẽ được cập nhật những thay đổi mới từ remote.

Chạy thử dự án xem có phát sinh lỗi gì không ?

- Nếu có lỗi: lỗi ở đâu, thuộc phần code của thành viên nào thì thực hiện lại từ Bước 3 của Giao đoạn 2.
- Nếu không lỗi ==> Hoàn thành