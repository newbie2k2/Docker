### 2.2 Chạy Linux với Docker
- Các câu lệnh của Linux phân biệt hoa thường
```
Docker pull {image name}:
Docker run {image name}: run image, nếu không có tự động dowload

docker ps: xem các container đang chạy
docker ps -a: xem tất cả các docker

docker run -it ubuntu: vào ubuntu tương tác
```

```
+ docker run -it ubuntu: vào ubuntu tương tác
=> root@4d0a1b37f575:/# 
=> root: mình đang đăng nhập vào ubuntu với cái username là root
=> 4d0a1b37f575: ID của container hiện đang chạy
=> /: mình đang đứng ở thư mục gốc
=> #: quyền user cao nhât, $ user bình thường

+ echo {message}: dùng để hiển thị nội dung ra màn hình
+ echo $0: hiển thị tên của shell (môi trường dòng lệnh) hiện đang được sử dụng, vị trí đang chạy các câu lệnh 
+ whoami: hiển thị tên người dùng đang đăng nhập vào hệ thống hiện tại
+ pwd: hiển thị thư mục hiện tại bạn đang đứng

+ ls: lấy ra tất cả các file, folder của thư mục hiện tại
+ ls -a: lấy tất cả + các file đang ẩn (hidden)
+ history: danh sách các câu lệnh đã chạy (!2: chạy lại câu lệnh thứ 2)

+ clear: clear màn hình (Ctrl + L trên Window, Ctrl + L trên Linux)
```

### 2.3 Linux Package Management

Advanced Package Tool là một công cụ quản lý gói (package management tool) trong các hệ thống dựa trên Debian Linux như Ubuntu. Nó được sử dụng để quản lý việc cài đặt, cập nhật và gỡ bỏ các gói phần mềm trên hệ thống
```
* Để sử dụng các lệnh apt, bạn cần có quyền quản trị hệ thống và thường phải sử dụng sudo trước mỗi lệnh để đảm bảo có đủ quyền hạn.
+ apt: help
+ apt list: Danh sách package đã có trên máy 
+ apt install [package]: Cài đặt một gói phần mềm mới.
+ apt remove [package]: Gỡ bỏ một gói phần mềm đã cài đặt.
+ apt update: Cập nhật danh sách các gói phần mềm từ các nguồn (repositories) đã cấu hình trên hệ thống.
+ apt upgrade: Cập nhật tất cả các gói phần mềm đã cài đặt lên phiên bản mới nhất.
+ apt search [keyword]: Tìm kiếm các gói phần mềm có chứa từ khóa được chỉ định.
+ apt show [package]: Hiển thị thông tin chi tiết về một gói phần mềm cụ thể.
+ apt autoremove: Gỡ bỏ các gói phần mềm không còn phụ thuộc vào bất kỳ gói phần mềm nào khác trên hệ thống.
```

### 2.4 Linux file system
![2.4 Linux file system](../Images/linux-filesystem.png)
+ Trong Linux, tất cả đều là file
+ root (/) là cao nhất trong cây thư mục/hệ thống Linux
+ bin: binary or execute programs (nơi chứa các chương trình dưới dạng thực thi)
+ boot: booting process (một trong những thư mục quan trọng trong hệ thống tệp tin. Nó chứa các tập tin và dữ liệu liên quan đến quá trình khởi động (booting) của hệ thống)
+ dev: devices (chứa các tập tin đại diện cho các thiết bị (devices) vật lý và ảo trong hệ thống)
+ etc: các file cấu hình cho hệ thống
+ home: Nơi người dùng lưu trữ dữ liệu cá nhân

### 2.5: Navigating File System
Điều hệ thống tệp là cách tổ chức và quản lý các tập tin và thư mục trong hệ điều hành của bạn. Điều này cho phép bạn lưu trữ và tổ chức dữ liệu của mình theo cách phù hợp.

```
+ pwd: Print Working Directory - Hiện thị thư mục hiện tại đang làm việc

+ ls: List - Liệt kê danh sách các file
+ ls -1: ls + in ra từng dòng
+ ls -l: hiển thị chi tiết ....
+ ls -a: lấy ra tất cả các file, cả file ẩn

+ cd: Change directory - Thay đổi thư mục làm việc
+ cd -: quay lại đến thư mục trước đó
+ cd ~: Di chuyển đến thư mục home của người dùng hiện tại
+ cd ~[username]: Di chuyển đến thư mục home của người dùng cụ thể

+ mkdir [directory_name]: Tạo thư mục mới


+ mv [source] [destination]: Di chuyển hoặc đổi tên tập tin hoặc thư mục
=> mv file1.txt /path/to/new_directory

+ cp [source] [destination]: Sao chép tập tin hoặc thư mục
=> cp file1.txt /path/to/new_directory

+ rm [file_name]: Xoá tập tin hoặc thư mục
+ rm -r [directory_name]: xóa thư mục và nội dung của nó:
```
