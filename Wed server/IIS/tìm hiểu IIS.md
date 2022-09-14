![image](https://user-images.githubusercontent.com/111720261/190053551-366dec2a-4dc5-416a-bd98-029c21e08acd.png)

## 1. IIS là gì?
* Internet Information Services (IIS) - Dịch vụ thông tin Internet giống như Wed server đa năng dành cho Microsoft có nhiệm vụ tiếp nhận và phản hồi các yêu cầu của máy khách. Điều này giúp cho Web server dễ dàng chia sẻ và cung cấp thông tin trên mạng LAN/WAN hơn. Trong đó, các thông tin được cung cấp bởi các trang Wed tĩnh dự trên HTML hoặc bằng cách trao đổi tệp dưới dạng tải.
* Hiện nay các Web Server được trang bị  nhiều tính năng hiện đại có nhiều chức năng như làm cổng thông tin ứng dụng, thiện tương tác hoặc được tích hợp các ứng dụng trung gian như backend để tạo ra các hệ thống dành cho doanh nghiệp.
## 2. Cách thức hoạt động của IIS:
* IIS sử dụng các ngôn ngữ và giao thức tiêu chuẩn như HTML để tạo ra các ăn bản, nút, vị trí, tương tác,... Ngoài ra còn một số giao thức như: 

  HTTP giúp trao đổi thông tin giữa Web Server và người dùng.
  
  HTTPS sử dụng Transport Layer Security hoặc SSL để mã hoá giao tiếp và tăng cường bảo mật dữ liệu.
  
  FPT/FPTS hỗ trợ truyền tệp linh hoạt hơn.
  
  SMTP giúp gửi và nhận email hoặc các tin tức mạng trên USENET.
  
  ## 3. IIS làm việc với ASP.NET Core:
  * Phiên bản nâng cấp ASP.NET Core là một công cụ giúp tạo ra các trang wed tương tác dễ dàng hơn với quy trình.
  * Một yêu cầu bất kỳ gửi đến máy chủ IIS thông qua web sẽ được ASP.NET Core  xử lý và phản hồi lại cho khách hàng.
  * Webday có khả năng tạo và xuất bản nội dung cho các trang web IIS được các nhà phát triển sử dụng rộng rãi. Ngoài ra, còn có các công cụ phát triển tích hợp cũng được như Microsoft Visual Studio.
  ## 4. IIS Express để thử nghiệm:
  * IIS Express là một phiên bản thự nghiệm trang web độc quyền được phát triển bởi Microsoft. Với các chức năng giống như Web server IIS và một số tác vụ hỗ trợ hiện đại khác cho phép thực hiện các tác vụ không cần quyền quản trị.
  ## 5. An toàn bảo mật trong IIS:
  Bảo mật luôn là vấn đề được quan tâm đối với các trang web hoặc máy chủ, IIS cũng có một số tính năng bảo mật tích hợp thông qua các phương pháp:
  
        Hỗ trợ cập nhật các phiên bản bảo mật của hệ điều hành Windows.
        
      Tự động vô hiệu hoá các tính năng không hoạt động của IIS.
      
      Sử dụng tường lửa để phân biệt các gói tương thích với máy chủ.
      
      Kiểm soát địa chỉ IP và tên miền được phép truy cập vào Web Server.
      
      Sử dụng URL để uỷ quyền cho các yêu cầu.
      
      Lịch sử cho phép theo dõi người dùng truy cập vào Web Server.
      
      Các trang lỗi đảm bảo các thông tin cá nhân không bị lộ.
