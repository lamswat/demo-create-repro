# Lệnh liên quan đến hệ thống 
- exit: thoát khỏi cửa sổ dòng lệnh.
- logout: tương tự exit.
- reboot: khởi động lại hệ thống.
- halt: tắt máy.
- start:khởi động chế độ xwindows từ cửa sổ terminal.
- mount: gắn hệ thống tập tin từ một thiết bị lưu trữ vào cây thư mục chính.
- unmount: ngược với lệnh mount.
# lệnh thao tác trên tập tin
- ls -lah: hiện các danh sách ẩn.

![image](https://user-images.githubusercontent.com/111720261/187820247-3a905ae8-cb57-479d-b9ce-66949b8ef99b.png)


- ls: lấy danh sách tất cả các file và thư mục trong thư mục hiện hành.

![image](https://user-images.githubusercontent.com/111720261/187820647-67c044ce-8fbd-466d-a5a1-a0606f53d81a.png)

- pwd: xuất đường dẫn của thư mục làm việc.

![image](https://user-images.githubusercontent.com/111720261/187821014-87b736a6-3d32-41e5-b25f-9b9febfa99ef.png)

- cd: thay đổi thư mục làm việc đến một thư mục mới.
- mkdir: tạo thư mục mới.

![image](https://user-images.githubusercontent.com/111720261/187821774-1d333538-5567-4b1c-8d5b-ed74abb1179d.png)

- rmdir: xoá thư mục rỗng.

![image](https://user-images.githubusercontent.com/111720261/187822105-8cdf7404-8706-4313-b303-0aa885263873.png)

- cp:copy một hay nhiều tập tin đến thư mục mới.
- mv: đổi tên hay di chuyển tập tin, thư mục.
- rm: xoá tập tin.
- wc: đếm số dòng, số kí tự... trong tập tin.
- touch:tạo 1 tập tin.
- cat: xem nội dung tập tin.
- vi: khởi động trình soạn thảo văn bản vi.

![image](https://user-images.githubusercontent.com/111720261/187822396-5589813c-b76c-4709-9c95-43ae9c156bd6.png)

- df: kiểm tra dung lượng đĩa.

![image](https://user-images.githubusercontent.com/111720261/187822780-bdf3a1a1-146b-47ed-9d2e-8d1421891615.png)
- du: xem dung lượng đĩa đã dùng cho một số tập tin nhất định.

![image](https://user-images.githubusercontent.com/111720261/187823265-2009cec5-1376-4544-bdf2-ae2a5e543324.png)

- nano:khởi động trình soạn thảo văn bản nano.

![image](https://user-images.githubusercontent.com/111720261/187823402-8b11df90-da71-4f89-949d-f30d9303794d.png)
- less:Xem tập tin theo dòng lệnh.
- tail:xem nội dung tập tin( mặc định xem 10 dòng cuối, muốn xem 100 dòng cuối thì dùng lệnh sau : tail 100 tenfile)
- more: xem nội dung tập tin theo trang.
- head: xem nội dung tập tin (mặc định xem 10 dòng đầu, muốn xem 100 dòng đầu thì dùng lệnh sau : head 100 tenfile)
# lệnh khi làm việc trên terminal
- clear: xoá trắng cửa sổ dòng lệnh.
- date: xem ngày, giờ hệ thống.

![image](https://user-images.githubusercontent.com/111720261/187824923-9957eb88-eb92-4d99-8d36-549b7cf827af.png)
- cal: xem lịch hệ thống.
# Lệnh quản lí hệ thống
- rpm: kiểm tra gói đã cài đặt hay chưa, hoặc cài đặt một gói, hoặc sử dụng để gỡ bỏ một gói
- ps: kiểm tra hệ thống tiến trình đang chạy.
- kill: dừng tiến trình khi tiến trình bị treo. Chỉ có người dùng supper-user mới có thể dừng tất cả các tiến trình còn người dùng bình thường chỉ  có thể dừng tuieens trình mà mình tạo ra.
- top: hiển thị sự hoạt động của các tiến trình, đặc biệt là thông tin về tài nguyên hệ thống vè việc sử dụng các tài nguyên đó của từng tiến trình .

![image](https://user-images.githubusercontent.com/111720261/187825829-1db490e5-d675-44bd-8e1c-e3710c202aa2.png)

- pstree: hiển thị tất cả các tiến trình dưới dạng cây.

![image](https://user-images.githubusercontent.com/111720261/187826472-147770f9-55cd-4412-9b0a-550c5a2d9d8e.png)

- sleep: cho hệ thống dừng hoạt động trong 1 khoảng thời gian.
- useradd: tạo 1 người dùng mới. 
- groupadd: tạo 1 nhóm người dùng mới.
- passwd: thay đổi password cho người dùng .
- userdel:xoá người dùng đã tạo.
- groupdel: xoá nhóm người dùng đã tạo.
- gpasswd: thay đổi password của 1 nhóm người dùng.
- su: cho phép đăng nhập với tư cách của người dùng khác.
- groups: hiển thị nhóm của user hiện tại.
- who: cho biết ai đang đăng nhập hệ thống.

![image](https://user-images.githubusercontent.com/111720261/187827687-23fc7a55-3b2c-4fa9-b97c-cfb6a1d53c9b.png)

- w:tương tự như lệnh who.

![image](https://user-images.githubusercontent.com/111720261/187828083-0a2a24f5-4c79-4fee-8120-73ef9e252fd1.png)

- man man:xem hướng dẫn về dòng lệnh như cú pháp, các tham số.

![image](https://user-images.githubusercontent.com/111720261/187828422-c63547e6-b743-47c4-8eee-4a09689e9549.png)

# Các câu lệnh kiểm tra thông tin hệ thống ( system information)
| Lệnh Linux | Mô tả |
|----------------|------------|
| cat/proc/cpuinfo | Kiểm tra thông tin CPU(số core) |
| cat/proc/meminfo | Kiểm tra thông tin về RAM đang sử dụng |
| cat/porc/version | Kiểm tra phiên bản của Kernel Linux |
| cat/porc/ioports | Kiểm tra thông tin port I/O | 
| cat/ect/redhat-release | Kiểm tra phiên bản Centos |
| uname -a | Kiểm tra các thông tin về Kernel |
| free -m | Kiểm tra dung lượng RAM còn trống |
| init 0 | Tắt máy (tương đương lệnh shutdown -h now hoặc telinit 0) |
| df -h| Hiển thị thông tin những file hệ thống, nơi file được lưu hoặc tất cả những file mặc định. Lệnh này có thể xem được dung lượng ổ cứng đã sử dụng và còn trống. |
| du -sh| Kiểm tra dung lượng thư mục hiện tại |
| du  -ah| Hiển thị dung lượng của thư mục con và các file trong thư mục hiện tại |
| du -h -max-depth=1 | Hiển thị dung lượng các thư mục con ở cấp 1 (ngay trong thư mục hiện tại) |
| df | 	Kiểm tra dung lượng đĩa cứng, các phân vùng đĩa |
| lspci | Xem thông tin mainboard   /sbin/ifconfig Xem các địa chỉ IP của máy |
| hostname | Xem tên máy (hostname) |
| finger user@sever | Thu thập thông tin chi tiết về người dùng hiện đang dùng hệ thống |
|arch | 	Kiểm tra kiến trúc của máy (architech) |
|cat/proc/swaps | 	Kiểm tra thông tin SWAP của máy (tương tự như virtual RAM của Windows) |
| last reboot | 	Xem lịch sử reboot máy |

# Các lệnh shutdown, restart ... trong Linux
| lệnh Linux | Mô tả |
|--------------|------|
|Logout | Kết thúc session (phiên làm việc) hiện tại|
|reboot | 	Khởi động lại máy |
|shutdown -r now | Khởi động lại máy (tương đương với lệnh reboot) |
|shutdown -h now | 	Tắt máy (ngay lập tức) |
|shutdown -h 9:30| 	Hẹn giờ tắt máy (schedule) vào lúc 9h30 (tính theo khung 24h) |
|shutdown -c | 	Hủy bỏ tất cả các lệnh tắt máy trước đó (các lệnh tắt máy theo schedule) |
|telinit 0 | Tắt máy (tương đương lệnh shutdown -h now) |
|init 0 | Tắt máy (tương đương lệnh shutdown -h now hoặc telinit 0) |
|exit |  Thoát khỏi terminal |
|halt | Tắt máy (tương tự shutdown) |
|sleep | Cho hệ thống ngừng hoạt động trong một thời gian (ngủ – tương tự Windows) |
 
# Các lệnh quản lí user 
| lệnh Linux | Mô tả |
|--------------|------|
| passwd |	Đổi mật khẩu (standard user có thể đổi pass của họ còn user root thì thay đổi được password của mọi user)|
| useradd | Kiểm tra syntax và định dạng của dữ liệu user/password (/etc/passwd) |
| userdel | Tạo user mới, ví dụ: useradd -c “test user 1” -g group1|
| userdel | Xóa User |
| usermod | Thay đổi thông tin user (group, name…)|
| groupadd |	Tạo một nhóm user mới |
| groupdel |Xóa nhóm user |
| groupmod |	Thay đổi thông tin group, ví dụ, groupmod -n “old group name”  “new name”|
| who /w |	Hiển thị những user đang đăng nhập hệ thống |
| uname | Hiển thị tên của hệ thống (host) | 
| id | 	Hiển thị user ID (Chỉ danh của user) |
| logname | Hiển thị tên user đang login |
| su | Cho phép đăng nhập với tên user khác (tương tự secondary logon của Windows) |
| groups | Hiển thị nhóm của user hiện tại |
| #vi /ect/passwd |	Xem danh sách user |
| #vi /ect/group  |	Xem danh sách nhóm (group) |
| chmod [tên file=""][/tên] | Thay đổi quyền cho file/thư mục (chỉ user sở hữu file mới thực hiện được) |
| chown user [tên file=""][/tên] |Thay đổi chủ sở hữu file/thư mục |
| chgrp group [file][/file] |Thay đổi group sở hữu file/thư mục |

# Các lệnh Quản lý services và process:
| lệnh Linux | Mô tả |
|--------------|------|
| top |	Lệnh top khá giống như Task Manager trong Windows. Nó đưa ra thông tin về tất cả tài nguyên hệ thống, các process đang chạy, tốc độ load trung bình… Lệnh top -d thiết lập khoảng thời gian làm mới lại hệ thống  |
| ps -u username|	Kiểm tra những process được thực hiện bởi một user nhất định|
| ps -U root | 	Kiểm tra mọi process ngoại trừ những process hệ thống |
| ps -A |	Kiểm tra mọi process trong hệ thống|
| Ss | Kiểm tra socket đang kết nối |
| ss -I |	Hiển thị các cổng đang mở |
| w username | 	Kiểm tra user đăng nhập, lịch sử đăng nhập, các process user đó đang chạy |
|  vmstat3 | 	Kiểm soát hành vi hệ thống, phần cứng và thông tin hệ thống trong Linux |
| ps       |	Hiển thị các chương trình hiện đang chạy|
| uptime | Hiển thị thời gian đã vận hành của hệ thống trong bao lâu |
| rmp | 	Kiểm tra, gỡ bỏ hoặc cài đặt 1 gói .rpm |
| yum | 	Cài đặt các ứng dụng đóng gói (giống rpm)  |
| wget |	Tải các ứng dụng từ một website về |
| sh | 	Chạy một ứng dụng có đuôi .sh |
| Startx|	Khởi động chế độ xwindows từ cửa sổ terminal |
| yum update -y| 	Update Linux (CentOS)|
| stop/start/restart| 	Dừng/ khởi động/khởi động lại một service hoặc ứng dụng, ví dụ: service mysql stop hoặc /etc/init.d/mysqld start |
| kill |	Dừng proccess (thường dùng khi process bị treo). Chỉ có super-user mới có thể dừng tất cả các process còn user khác chỉ có thể dừng proccess mà user đó tạo ra |
| kill PID hoặc %job | Ngừng một process bằng số PID (Process Identification Number) hoặc số công việc |
| pstree | Hiển thị tất cả các process dưới dạng cây |
| service -status-all |	Kiểm tra tất cả các service và tình trạng của nó|
| whereis mysql |Hiển thị nơi các file dịch vụ được cài đặt|
| service -status-all │ grep abc |	Xem tình trạng của process abc | 
| kill -9 PID |	Bắt buộc đóng một process ID|
| kill -1 PID |Bắt buộc đóng một process ID và load lại cấu hình mặc định của process đó |

# Một số lệnh hữu ích khác
| lệnh Linux | Mô tả |
|--------------|------|
| clear | Xoá trắng cửa sổ dòng lệnh |
| hwclock | Fix lịch của BIOS |
| cal | Xem lịch hệ thống |
| date | Xem lịch ngày giờ hệ thống |
| date –s “1 JAN 2018 15:29:00” | Đặt ngày giờ hệ thống theo string |
| date +%Y%m%d -s “20180101″ | Đặt ngày hệ thống (không thay đổi giờ) |
| date +%T -s “00:29:00″ | Đặt giờ hệ thống, không thay đổi ngày |

# Các câu lệnh xem thông tin file và thư mục
| lệnh Linux | Mô tả |
|--------------|------|
| ls | Lấy danh sách tất cả các file và folder trong thư mục hiện hành |
| ls tenthumuc | Liệt kê nội dung bên trong một thư mục |
| ls -l | Như trên, nhưng liệt kê cả kích thước file, ngày cập nhật.|
| ls -a | Liệt kê tất cả các file ẩn |
| pwd | Xuất đường dẫn của folder đang làm việc |
| cd  | Thay đổi folder làm việc đến một folder mới (tương tự như trong DOS ) |
| df  | Kiểm tra disk space |

# Lệnh nén và giải nén
| lệnh Linux | Mô tả |
|--------------|------|
| tar -cvf	| Nén file/thư mục sang định dạng .tar|
| tar -xvf	| Giải nén file tar |
| gzip	| Chuyển file .tar sang .tar.gz |
| gunzip	| Chuyển file .tar.gz về .tar |
| tar -xzf	| Giải nén file .tar.gz, ví dụ:  tar -xvf archive.tar |
| tar -zxvf	| Giải nén file .tar.bz2 |
| tar -jxvf	| Giải nén file .tar.gz2 |
| unzip	| Giải nén file zip | 

# Lệnh sao lưu và phục hồi database
| lệnh Linux | Mô tả |
|--------------|------|
| mysqldump -u root -p[dbpass] [databasename] > [database.sql]	| Sao lưu database ra file .sql |
| mysqldump -u root -p[dbpass] [databasename] │ gzip -9 > [backupfile].sql.gz	| Sao lưu database và nén lại dưới dạng .gz |
| mysql -u username -p[dbpass] [databasename] < [database].sql | Khôi phục database |


