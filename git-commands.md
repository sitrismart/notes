# Git Commands and Workflow

## Git Initialization and Setup
- `git init`: Tạo một repository Git mới trong một thư mục hiện có.

## Git Status and Staging
- `git status`: Kiểm tra trạng thái của repository.
- `git add`: Thêm các thay đổi vào staging area.
- `git reset`: Xoá các thay đổi đã được `git add` nhưng chưa commit.

## Git Commit and Log
- `git commit`: Thực hiện commit.
- `git commit -m "message"`: Commit với thông điệp mô tả. Mới bắt đầu dự án thường là `initial commit`.
- `git log`: Xem các commit và ID của commit.
- `git log --oneline`: Hiển thị các commit dưới dạng rút gọn.

## Git Checkout and Branching
- `git checkout {idcommit}`: Quay lại commit trước.
- `git checkout {branchname}`: Chuyển sang branch hiện tại hoặc branch khác.
- `git branch`: Hiển thị các branch hiện có.
- `git checkout -b {branchname}`: Tạo branch mới dựa trên branch hiện tại.

## Git Merge
- `git merge {branchname}`: Tổng hợp branch vào branch hiện tại.
- `git merge --continue --no-edit`: Sau khi giải quyết conflict, merge với tin nhắn mặc định của GitHub.
- `git merge --continue`: Sau đó, thực hiện `git commit -m ""` để commit với thông điệp như bình thường.

## Git Branch Management
- `git branch -d {branchname}`: Xoá branch.

## Git Push and Remote Repositories
- `git push {link} {branchname}`: Đẩy local lên remote khi mới tạo repository.
- `git remote add origin {link}`: Tạo tên đường dẫn tới repo là `origin` (dùng khi repo đã được tạo trước ở máy). Khi push chỉ cần dùng `git push origin {branchname}`.
- `git clone {link repo}`: Clone repo về máy.
- `git push -u origin {branchname}`: Đẩy một branch lên GitHub (chỉ cần sử dụng lần đầu).

## Fetch and Pull
- `git fetch origin`: Lấy về các thay đổi từ remote.
- `git checkout -b staging origin/staging`: Kéo branch `staging` về máy.
- `git fetch`: Tải về thay đổi từ remote nhưng không hợp nhất vào nhánh hiện tại.
- `git pull`: Kết hợp `git fetch` và `git merge` (tự động hợp nhất các thay đổi vào nhánh hiện tại).

## .gitignore File
Tạo ra file `.gitignore` để không commit những file không mong muốn.

```gitignore
# Bỏ qua tất cả các file `.log`
*.log

# Bỏ qua thư mục `node_modules`
node_modules/
