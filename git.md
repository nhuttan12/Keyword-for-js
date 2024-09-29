# Những thứ liên quan tới git 
## Lưu ý: tùy vào mỗi công ty sẽ có quy chuẩn làm việc riêng, nên phần nầy chỉ mang tính tham khảo.
## 1. Cách commit - Tham khảo từ J2Team
### **Cấu trúc chung của một commit message**
```<type>:<description> [body]```
Trong đó: 
- **type** và **description** là phần bắt buộc 
- **body** là phần **TÙY CHỌN**, có thể có hoặc không
ví dụ: 
```feat: add email notification on new messages refers to JIRA-1234```
1. **\<type\>**
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
2. **\<description\>**
    - **Mô tả ngắn gọn** về nội dung commit
    - **Không dài quá 50 ký tự** để có thể dễ dàng đọc trên github, cũng như các git tool khác 
    - Sử dụng **câu mệnh lệnh** ở **thì hiện tại**.<br>
Ví dụ **"change" thay cho "changed..."**
    - **Không viết hoa chữ cái đầu tiên.**
    - **Không xử dụng dấu chấm ở cuối câu.**
    - Nếu có **liên quan tới 1 issue** nhứt định nào đó thì phải thêm **#issue** đó ở đằng sau.
3. **Ví dụ:**
    - ```feat: thêm tính năng tìm kiếm #123```
    - ```refactor: tối ưu hóa hàm xử lý dữ liệu #2```
    - ```docs: cập nhật hướng dẫn cài đặt #1```
    - ```ci: cập nhật cấu hình CI #55```

## 2. Cách đặt tên nhánh
1. **Thêm tiền tố ở tên nhánh là một cách thức phổ biến và hệu quả để phân loại nhánh dựa trên kế hoạch được lập nên**
   - **feature/**: nhánh đó được xử dụng để phát triển 1 chức năng nhất định.
   - **bugfix/**: nhánh đó được xử dụng để sửa lỗi của một tính năng nào đó.
   - **bugfix/**: nhánh đó đang được xử dụng để sửa lỗi khẩn cấp.
   - **bugfix/**: nhánh đó được xử dụng để phát hành một tính năng mới.
   - **test/**: kiểm thử chức năng đó có lỗi gì không
2. **Hậu tố**
   - **Nên viết tách riêng** ra bằng dấu ```-``` hoặc là dấu ```/``` để tăng khả năng đọc tên nhánh <br>
     ví dụ: ```create-welcome-page``` hoặc ```create/welcome/page```
   - **Thêm id của issue** để dễ dàng phân biệt được task và theo dõi quá trình phát triển<br>
     ví dụ: ```ui-1-create-welcome-page```<br>
     có nghĩa là tạo trang mở đầu thuộc phần giao diện và đang là issue 1
   - **Tránh đánh số tên nhánh**: việc đánh số sẽ dễ gây rắc rối và tăng thêm khả năng bị lẫn lộn trong quá trình đặt tên nhánh
   - **Tránh đặt tên nhánh quá dài**: mặc dù tên nhánh phải càng rõ ràng càng tốt, nhưng nó cũng phải ngắn gọn và xúc tích, nếu như đặt tên nhánh quá dài có thể ảnh hưởng tới khả năng đọc và tính hiệu quả của nó
   - **Tính nhứt quán**: sau khi đã thống nhất quy ước thì phải xử dụng nó xuyên suốt việc phát triển phần mềm
  
Dẫn chứng từ:
- [Best Practices for Naming Git Branches   - Tilburg Science Hub](https://tilburgsciencehub.com/topics/automation/version-control/advanced-git/naming-git-branches/)
- [Best practices for naming Git branches](https://graphite.dev/guides/git-branch-naming-conventions)
