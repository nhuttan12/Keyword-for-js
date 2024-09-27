# Những thứ liên quan tới git
## 1. Cách commit 
### **Cấu trúc chung của một commit message**
```<type>:<description> [body]```
Trong đó: 
- **type** và **description** là phần bắt buộc 
- **body** là phần **TÙY CHỌN**, có thể có hoặc không
ví dụ: 
```feat: add email notification on new messages refers to JIRA-1234```
### **\<type\>**
- **feat (feature)**: Thêm tính năng mới.
- **fix**: Sửa lỗi.
- **refactor**: Tái cấu trúc mã mà không thay đổi chức năng bên ngoài.
- **style**: Thay đổi về định dạng, code style (không liên quan đến logic như khoảng trắng, dấu chấm phẩy, format code).
- **test**: Thêm hoặc chỉnh sửa các bài kiểm thử (test).
- **chore**: Các công việc lặt vặt, không ảnh hưởng đến mã nguồn hoặc tính năng (ví dụ: cập nhật thư viện, build lại mã).
- **docs (documentation)**: Thay đổi hoặc thêm tài liệu (docs).
- **perf (performance)**: Cải thiện hiệu năng.
- **ci (Continuous Integration)**: Thay đổi các cấu hình CI/CD (Continuous Integration/Continuous Deployment).
- **build**: Thay đổi về quá trình build (ví dụ như thay đổi các cấu hình build, dependencies, scripts).
- **revert**: Hoàn tác một commit trước đó.
- **ci (Continuous Integration)**: Các thay đổi liên quan đến hệ thống CI/CD.
- **hotfix**: Sửa lỗi gấp phát sinh trong môi trường production.
- **wip (work in progess)**: đang trong quá trình phát triển
### **\<description\>**
- **Mô tả ngắn gọn** về nội dung commit
- **Không dài quá 50 ký tự** để có thể dễ dàng đọc trên github, cũng như các git tool khác 
- Sử dụng **câu mệnh lệnh** ở **thì hiện tại**.
Ví dụ **"change" thay cho "changed..."**
- **Không viết hoa chữ cái đầu tiên.**
- **Không xử dụng dấu chấm ở cuối câu.**
- Nếu có **liên quan tới 1 issue** nhứt định nào đó thì phải thêm **#issue** đó ở đằng sau.
#### **Ví dụ:**
- ```feat: thêm tính năng tìm kiếm```
- ```refactor: tối ưu hóa hàm xử lý dữ liệu```
- ```docs: cập nhật hướng dẫn cài đặt```
- ```ci: cập nhật cấu hình CI```

## 2. Cách đặt tên issue và tạo tên nhánh dựa trên issue đó