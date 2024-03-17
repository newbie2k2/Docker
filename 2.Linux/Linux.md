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

### 2.6: Manipulating Files and Directories (Thao tác tập tin và thư mục)
Di chuyển File System
```
+ mkdir: Making Directory - Tạo thư mục

+ mv [source] [destination]: Di chuyển hoặc đổi tên một tập tin hoặc thư mục
=> mv old_file.txt new_file.txt: đổi tên thư mục
=> mv file.txt /path/to/directory: di chuyển một tập tin vào một thư mục

+ cp [source] [destination]: Sao chép một tập tin hoặc thư mục
=> cp file.txt file_copy.txt: Sao chép tập tin
=> cp file.txt /path/to/directory: Sao chép một tập tin vào một thư mục

+ rm [file_name]: xoá tập tin hoặc thư mục
+ rm -r directory_name: xóa một thư mục và nội dung của nó

+ touch {file path/file name.x}: Tạo 1 file mới, hoặc nhiều file
=> touch colen.txt colen1.txt
```

### 2.7: Edit and View file (Chỉnh sửa và hiển thị file)
```
+ nano {filename.x}: View và Edit nội dung của file
+ cat {filename.x}: Xem nội dung file (toàn bộ content)
+ more {filename.x}: Xem content theo từng page (press space để load thêm, q to quit)
+ less {filename.x} (install using apt): xem content theo từng page (press up/down để load thêm, press q to quit)
+ head -n {number line} {path}: View từ số dòng đầu tiên của file
+ tail -n {number line} {path}: View từ số dòng đầu tiên của file
```

Chỉnh sửa tập tin
```
+ nano [file_name]: Sử dụng trình soạn thảo văn bản nano
+ vi [file_name]: Sử dụng trình soạn thảo văn bản vi hoặc vim
+ vim [file_name]: Sử dụng trình soạn thảo văn bản vi hoặc vim
vi và vim là hai trình soạn thảo văn bản mạnh mẽ nhưng phức tạp hơn nano. Để sử dụng, bạn cần biết một số lệnh và phím tắt cơ bản. 
Để lưu và thoát, bạn thường sử dụng Esc rồi :wq cho vi hoặc vim

+ emacs [file_name]: Sử dụng trình soạn thảo văn bản emacs
emacs là một trình soạn thảo văn bản mạnh mẽ với nhiều tính năng phức tạp. Nó có một hệ thống phím tắt riêng, nhưng cũng cung cấp một giao diện người dùng đồ họa nếu bạn cài đặt.

```

### Bài 2.8: Redirection (Chuyển hướng)
```
+ command > file.txt : ( > ) Ghi đè (overwrite) nội dung ra tập tin.
=> cat hello-docker > file-docker.txt : Chuyển nội dung của file hello-docker sang file-docker.txt
=> echo Hello Docker > file-docker.txt

+ command >> file.txt : Ghi thêm nội dung vào cuối file mà không làm mất nội dung của file

+ command 2> error.txt
=> command: Đây là lệnh bạn muốn thực thi
=> 2>: Đây là phần của lệnh redirection, chuyển hướng đầu ra lỗi chuẩn (stderr).
=> error.txt: Đây là tên của tập tin mà đầu ra lỗi chuẩn sẽ được ghi vào
=>  Lệnh này sẽ chạy "command" và chuyển hướng bất kỳ lỗi nào xuất hiện trong quá trình thực thi của nó vào tập tin "error.txt"

+ command &> output.txt
=> command: đây là lệnh bạn muốn thực thi
=> &>: Đây là phần lệnh redirection chuyển hướng cả đầu ra chuẩn (stdout) và lỗi chuẩn (stderr)
=> output.txt: Đây là tập tin mà đầu ra chuẩn và lỗi chuẩn sẽ được ghi vào
=> Lệnh này sẽ chạy command và chuyển hướng cả đầu ra chuẩn và đầu ra lỗi chuẩn vào tập tin output.txt. Điều này có nghĩa là cả kết quả đúng và lỗi sẽ được ghi vào cùng một tập tin

+ command < input.txt: Lệnh này sử dụng nội dung của tập tin input.txt làm đầu vào cho command

+ command1 | command2: Pipes (|) cho phép bạn kết hợp đầu ra của một lệnh với đầu vào của một lệnh khác. Điều này hữu ích khi bạn muốn chuyển dữ liệu trực tiếp từ một lệnh sang lệnh khác
=> ls | grep "hello-docker"
=> ls là lệnh để liệt kê các tệp tin trong thư mục hiện tại.
=> grep "example" là lệnh để tìm kiếm chuỗi "example" trong đầu vào được cung cấp cho nó.
=> Kết quả của lệnh "ls" sẽ chuyển đến lệnh 'grep', và 'grep' sẽ hiện thị ca dòng có chứa từ khoá "example". Điều này giúp bạn tìm kiếm các tệp tin có tên chứa từ khoá "hello-docker" trong thư mục hiện tại

```

### Bài 2.9: Searching (Tìm kiếm)
```
+ grep: là một công cụ tìm kiếm mạnh mẽ để tìm kiếm các dòng trong tệp tin hoặc đầu vào chuẩn (stdin) mà khớp với một biểu thức chính quy (regular expression)
=> grep hello hello-docker.txt
=> grep -i hello hello-docker.txt: (-i) không phân biệt chữ hoa thường
=> grep -i hello hello-docker*
=> grep -i root /etc/passwd
=> grep -i -r hello .: (.) thư mục hiện tại
```




