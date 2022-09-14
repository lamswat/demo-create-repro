#  cài PHP.

- Phiên bản PHP có sẵn CentOS 7 là các bản cũ và đã lỗi thời và vì lý do đó, các bạn nên cài đặt kho lưu trữ gói của bên thứ ba để có thể sử dụng các phiên bản PHP mới nhất . Và Remi là kho lưu trữ gói phổ biến cung cấp các bản phát hành PHP mới nhất cho các máy chủ CentOS.

## Bước 1: Để cài đặt kho Remi các bạn chạy lệnh sau

          yum install -y yum-utils https://rpms.remirepo.net/enterprise/remi-release-7.rpm

![image](https://user-images.githubusercontent.com/111720261/188839876-7350332f-7623-40af-939f-2dbeb98a3a2c.png)

## Bước 2: Sau khi cài đặt gói Remi xong, các bạn cần chọn phiên bản PHP mà mình cần cài đặt và kích hoạt gói chứa phiên bản PHP đó. Ở hướng dẫn này mình sẽ cài đặt PHP 8.0 nên sẽ kích hoạt gói bằng lệnh sau

          yum-config-manager --enable remi-php80
  
  ![image](https://user-images.githubusercontent.com/111720261/189019568-c82d27b7-5b9e-464f-8178-7b1930b3579e.png)

## Bước 3: Khi module remi-80 của PHP đã được bật, bạn có thể tiến hành cài đặt PHP và các PHP Extension cần thiết bằng lệnh bên dưới:

          yum install -y php php-ldap php-zip php-embedded php-cli php-mysql php-common php-gd php-xml php-mbstring php-mcrypt php-pdo php-soap php-json php-simplexml php-process php-curl php-bcmath php-snmp php-pspell php-gmp php-intl php-imap perl-LWP-Protocol-https php-pear-Net-SMTP php-enchant php-pear php-devel php-zlib php-xmlrpc php-tidy php-opcache php-cli php-pecl-zip unzip gcc

![image](https://user-images.githubusercontent.com/111720261/189019275-e37993dc-487f-4b13-835f-6a5b24fe67fe.png)

## Bước 4: hiên bản PHP vừa cài đặt bằng cách

            php -v
            
![image](https://user-images.githubusercontent.com/111720261/189019809-4b94d0b9-4158-43ed-9e67-792b78a357d8.png)

# 4. kiểm tra việc apache kiểm soát php.

- Thư mục gốc web mặc định là /var/www/html. Ta tạo một tệp PHP (info.php) trong thư mục này để kiểm tra Apache xử lý PHP.

## File info.php sẽ hiển thị thông tin chi tiết phiên bản PHP mà chúng ta cài đặt

          nano /var/www/html/info.php

- Dán nội dung sau vào file:

                <?php
                phpinfo();
                ?>

![image](https://user-images.githubusercontent.com/111720261/189065582-0266c0e8-8dd7-4cff-9288-556ece294624.png)

- Sau đó tiến hành “Lưu lại” ấn tổ hợp phím Ctrl + o 

## Bây giờ các bạn mở trình duyệt lên và gõ địa chỉ:http://192.168.23.132/info.php, nếu kết quả hiển thị như hình dưới là việc cài đặt của chúng ta đã thành công

![image](https://user-images.githubusercontent.com/111720261/189020239-480a65ab-9225-4df2-9ea0-306098c29148.png)

# 5. Cài đặt PhpAdmin(tùy chọn).

- pMyadmin là một trình quản lý Mysql server trên giao diện web, giúp chúng ta dễ dàng thao tác với Database hơn

- phpMyAdmin có trong repository EPEL (Gói bổ sung cho Enterprise Linux). Để truy cập EPEL, bạn cần install gói đặc biệt – epel-release.

## bước 1: Sử dụng lệnh sau để install epel-release CentOS:

        yum install epel-release
               
## Bước 2: Cài đặt phpMyadmin

        yum install phpmyadmin

## Bước 3: Cấu hình phpmyadmin, bạn vào file phpmyadmin.conf để thiết lập

        nano /etc/httpd/conf.d/phpMyAdmin.conf

- đây bạn sẽ thấy 4 chuỗi ip yêu cầu khác nhau, khớp với chuỗi IP dài. Giá trị mặc định là 127.0.0.1 . Thay thế giá trị đó bằng IP máy bạn sẽ sử dụng để truy cập phpMyAdmin

![image](https://user-images.githubusercontent.com/111720261/188841714-6f14bc0f-8cb8-4b7c-84b6-5629103b1d4a.png)


 ## Bước 4: Khởi động lại Apache web server

          systemctl restart httpd

#  trình duyệt, vào đường dẫn sau để truy cập vào phpMyadmin: https://127.0.0.1/phpmyadmin

![image](https://user-images.githubusercontent.com/111720261/189021917-bb602bad-5e88-4c34-9e8d-bc0b813b59f4.png)

# đăng nhập vào bằng tài khoản root để kiểm tra:

![image](https://user-images.githubusercontent.com/111720261/189022109-15f486be-7b15-4c2e-b242-0107b4efd6ae.png)

![image](https://user-images.githubusercontent.com/95491130/183231975-763ed3be-3b5c-4dfe-9625-e4ecd0efd9a0.png)

