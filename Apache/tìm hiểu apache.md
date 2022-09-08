# Kiến thức Apache và hướng dẫn cài đặt chi tiết nhất
![image](https://user-images.githubusercontent.com/111720261/188768897-42c4a6d7-8ccb-48ec-9303-ec2508f20d4d.png)

# apache là gì ?
# 1. Thông tin về apache Wed server

Tên chính thức của Apache là HTTP Server. Được điều hành và phát triển bởi Apache Software Foundation.

Nó giúp chủ website đưa nội dung lên web – vì vậy có tên gọi là “web server”. Apache là một trong số những web server lâu đời và đáng tin cậy nhất, phiên bản đầu tiên đã được ra mắt từ hơn 20 năm trước, tận những năm 1995.
Khi một người truy cập vào website của bạn, họ sẽ điền tên miền vào thanh địa chỉ. Sau đó, web server sẽ chuyển những files được yêu cầu xuống như là một nhân viên chuyển hàng ảo.
![image](https://user-images.githubusercontent.com/111720261/188771136-b85aa49d-5bdb-4ee6-a095-a132d48fc88b.png)

# 2. Công việc của Apache là gì?

Dù gọi Apache là web server, nhưng nó lại không phải là server vật lý. Apache là một phần mềm chạy trên server đó.

# * Công việc chính của Apache:

Thiết lập kết nối giữa server và trình duyệt người dùng (Firefox, Google Chrome, Safari…)

Chuyển file tới và lui giữa chúng (cấu trúc 2 chiều dạng client-server).

# * Quá trình hoạt động diễn ra như thế nào?

Khi một khách truy cập tải một trang trên website của bạn, trình duyệt người dùng sẽ gửi yêu cầu tải trang web đó lên server. Sau đó, Apache sẽ trả kết quả với tất cả đầy đủ các file cấu thành nên trang đó (hình ảnh, chữ,…).

Apache sử dụng một tập tin .htaccess để ghi lại URL. Giao thức HTTP/HTTPs là kênh giao tiếp giữa Server và client. Apache chịu trách nhiệm cho việc đảm bảo tiến trình này diễn ra nhanh và bảo mật giữa 2 máy.

# Tìm hiểu về Web Server

# 1. Web Server là gì?

File servers, database servers, mail servers, và web servers sử dụng nhiều phần mềm server khác nhau. Từng ứng dụng sẽ truy cập files riêng lưu trên server vật lý và dùng chung cho các mục đích khác nhau.

Nhiệm vụ của web server là đưa website lên internet. Để làm được điều đó, nó hoạt động giống như là một người đứng giữa server và máy khách (client). Nó sẽ kéo nội dung từ server về cho mỗi một truy vấn xuất phát từ máy khách để hiển thị kết quả tương ứng dưới hình thức là một website.

![image](https://user-images.githubusercontent.com/111720261/188771997-ce6116fe-cf4e-47bd-b53f-194948314dc2.png)

Điểm khó khăn lớn nhất của một web server là kéo dữ liệu cho nhiều người dùng cùng một lúc – vì mỗi một người lại cũng đang truy vấn tới các trang web khác nhau. Web server xử lý các file này dưới ngôn ngữ lập trình như là PHP, Python, Java, vâng vâng.

Những ngôn ngữ này biến chúng thành file HTML và file trên trình duyệt cho người dùng web thấy được. Khi bạn nghe tới cụm từ “web server”, hãy hiểu rằng nó là công cụ chịu trách nhiệm giao tiếp giữa server-client.

# 2. Apache Web Server hoạt động như thế nào?

Mặc dù chúng ta gọi Apache là web server, nhưng nó lại không phải là server vật lý. Nó là một phần mềm chạy trên server đó. Công việc của nó là thiết lập kết nối giữa server và trình duyệt người dùng (Firefox, Google Chrome, Safari…). Rồi chuyển file tới và lui giữa chúng (cấu trúc 2 chiều dạng client-server). Apache là một phần mềm đa nền tảng. Nó hoạt động tốt với cả server Unix và Windows.

Khi một khách truy cập tải một trang web trên website của bạn. Ví dụ, trang chủ “About Us”, trình duyệt người dùng sẽ gửi yêu cầu tải trang web đó lên server và sẽ trả kết quả với tất cả đầy đủ các file cấu thành nên trang About Us (hình ảnh, chữ…). Server và client giao tiếp với nhau qua giao thức HTTP và Apache chịu trách nhiệm cho việc đảm bảo tiến trình này diễn ra mượt mà và bảo mật giữa 2 máy.

Apache là một nền tảng module có độ tùy biến rất cao. Moduels cho phép quản trị server tắt hoặc thêm chức năng. Apache có modules cho bảo mật caching, URL rewriting, chứng thực mật khẩu, vâng vâng. bạn cũng có thể thiết lập cấu hình server riêng qua file gọi là .htaccess, vốn là file cấu hình Apache  được hỗ trợ hoàn toàn bởi mọi gói hosting của Hostinger.

Apache vs Những Web Servers khác
Bên cạnh Apache, cũng có nhiều web server khác nữa. Mỗi một ứng dụng web server lại có mục tiêu khác nhau. Apache được sử dụng nhiều nhất nhưng các đối thủ cũng có thể mạnh riêng.

![image](https://user-images.githubusercontent.com/111720261/188772353-25bdb3a1-b3cf-44b5-ad8f-d71b626bb72d.png)

# 1. Apache vs NGINX

Nginx, phát âm là Engine-X, là một ứng dụng web server được phát hành năm 2004. Ngày nay, nó đã phổ biến rất nhiều trong giới lập trình web. Nginx được tạo để xử lý các vấn đề được gọi là c10k problem (10,000 connections). Có nghĩa là web server sử dụng threads để xử lý truy vấn của khách không thể thực hiện được hơn 10,000 kết nối cùng lúc.

Vì Apache sử dụng cấu trúc dạng thread, chủ sở hữu các website nặng có traffic lớn sẽ gặp phải vấn đề hiệu xuất. Nginx là một trong các web server có thể xử lý vấn đề c10k và có lẽ là phần mềm thành công nhất làm việc này.

Nginx có kiến trúc xử lý dạng “sự kiện” (event) không phải tạo process mới cho mỗi truy vấn. Thay vào đó, nó xử lý truy vấn trong một thread duy nhất. Master process sẽ quản lý nhiều worker processes mà thực sự quản lý việc xử lý truy vấn. Dạng quản lý sự kiện như vậy của Nginx phân tán truy vấn một cách hiệu quả để đạt hiệu quả quản lý tốt hơn.

Nếu bạn có một website có traffic lớn, Nginx là lựa chọn tối ưu, vì nó có thể xử lý nhiều tiến trình với tài nguyên thấp nhất có thể. Không phải ngẫu nhiên mà nhiều website lớn như Netflix, Hulu Pinterest, Airbnb đều đang sử dụng nó.

Tuy nhiên, đối với những doanh nghiệp vừa và nhỏ, Apache tỏ ra hiệu quả hơn Nginx, vì nó dễ cấu hình hơn, nhiều modules hơnv à là một môi trường thân thiện cho người mới bắt đầu hơn.

# 2. Apache vs Tomcat

Tomcat là một web server cũng được phát triển bởi Apache Software Foundation, vì vậy tên chính thức của nó là Apache Tomcat. Nó cũng là một server HTTP, tuy nhiên, nó hỗ trợ mạnh cho ứng dụng Java thay vì website tĩnh. Tomcat có thể chạy nhiều bản Java chuyên biệt như Java Servlet, JavaServer Pages (JSP), Java EL, và WebSocket.

Tomcat được tạo đặc biệt riêng cho Java apps, mặc dù Apache là vẫn là một server HTTP. Bạn có thể sử dụng Apache với nhiều ngôn ngữ lập trình khác (PHP, Python, Perl, vâng vâng.) với sự giúp đỡ của module Apache phù hợp (mod_php, mod_python, mod_perl, etc.).

Mặc dù bạn có thể sử dụng Tomcat server để phục vụ trang web tĩnh, nhưng nó không hiệu quả như là khi sử dụng Apache. Ví dụ, Tomcat sẽ tải máy ảo Java lên trước và những thư viện Java liên quan khác, mà website thông thường thì không cần thiết.

Tomcat cũng khó cấu hình hơn các web server khác. Ví dụ, để chạy WordPress, hãy dùng các server dành cho HTTP như là Apache hoặc NGINX.

# Apache có những ưu điểm gì? 

# 1. Hỗ trợ rộng rãi hoàn toàn miễn phí
Với đặc điểm là mã nguồn mở, bạn có thể sử dụng Apache hoàn toàn miễn phí, kể cả cho mục đích thương mại. Đồng thời, với lượng lớn người dùng, nếu bạn có rắc rối nào thì cộng đồng người dùng lớn sẵn sàng hỗ trợ.

# 2. Ổn định, tin cậy
Apache là phần mềm đáng tin cậy, ổn định. Song song đó, bạn hoàn toàn có thể yên tâm được sử dụng phiên bản tốt nhất. Mã nguồn mở giúp

Apache được cập nhật thường xuyên, nhiều bản vá lỗi bảo mật liên tục.

# 3. Linh hoạt, thân thiện với người dùng
Sở hữu cấu trúc module, khiến người dùng hài lòng vì tính linh hoạt của nó.

Apache cũng dễ cấu hình, thân thiện với người dùng, nhất là người mới bắt đầu sử dụng.

![image](https://user-images.githubusercontent.com/111720261/188772773-dd983b8c-fa2a-41a9-a1f6-01f8e533e8d0.png)

# 4. Hoạt động hiệu quả đa nền tảng
Apache hoạt động đa nền tảng (hoạt động được cả với server Unix và Windows).

Đặc biệt, hoạt động cực kỳ hiệu quả với WordPress sites.

Dễ dàng thiết lập một website an toàn

Không cần bất cứ tùy chỉnh nào, bạn có thể chủ động cài đặt WordPress website trên Apache web server.

Đặc biệt, Apache server hoạt động tốt với các hệ thống quản trị nội dung lớn trên thế giới (Joomla, Drupal, …), web frameworks (Django, Laravel, …) và các ngôn ngữ lập trình khác. Nhờ ưu điểm đặc biệt này, Apache có thể giữ vững vị trí số một trong số các nền tảng web hosting, đặc biệt là đối với VPS hoặc shared hosting.

# Hạn chế của Apache
Chiếm khá nhiều bộ nhớ mỗi khi xử lý bất kỳ dữ liệu nào, dù nó là tĩnh hay động.

Gặp vấn đề hiệu năng (kém linh hoạt, xử lý hơi chậm ,…) nếu website có lượng truy cập cực lớn.

Quá nhiều lựa chọn thiết lập có thể gây ra các điểm yếu bảo mật.

Apache có rất nhiều đối thủ không ngừng cải thiện những hạn chế của Apache. Điển hình như NginX tải file tĩnh tốt hơn và ngốn rất ít tài nguyên. Hay LightSpeed nhẹ và có bộ cache tuyệt vời…

# Những điều cần biết về Apache và hướng dẫn cài đặt chi tiết
# 1. Ứng dụng Apache
Apache là một web server phổ biến nhất thế giới cho phép bạn thiết lập một website an toàn mà không tốn nhiều công sức. Nó thường được chọn bởi những người kinh doanh tự thân và một doanh nghiệp nhỏ, để tạo thương hiệu trên mạng.

Bạn có thể cài đặt WordPress website trên Apache web server mà không phải tùy chỉnh gì hết. Hơn nữa, Apache server hoạt động tốt với các hệ thống quản trị nội dung lớn trên thế giới (Joomla, Drupal, vâng vâng.), web frameworks (Django, Laravel, etc.), và các ngôn ngữ lập trình khác. Việc này giúp nó giữ vững vị trí số một trong số các nền tảng web hosting, đặc biệt là đối với VPS hoặc shared hosting.

# 2. Hướng dẫn cài đặt
Để cài đặt thành công Apache app về máy đòi hỏi người sử dụng phải khá am hiểu về công nghệ thông tin và có những kiến thức nhất định trên lĩnh vực này. Quy trình cài đặt này trải qua 3 bước và dưới đây là quy trình cụ thể để cài đặt  từ source phù hợp từng loại cấu hình máy.

# Bước 1: Download
Nhiều người dùng sẽ thắc mắc đặt câu hỏi download Apache ở đâu? Và câu trả lời chính là download Apache từ Apache Lounge phiên bản 64 bytes hoặc 32 bytes. Và file download chính là httpd – 2.4.33 – win64 – VC15. zip.

Bản Apache VC15 được cấu thành trên  Visual C Redistributable for Visual Studio 2017. Chính vì vậy, bạn phải cài đặt nó trên Win của mình hoặc nếu là Win XP thì một lời khuyên đó là nên dùng bản Apache VC10.

# Bước 2: Cài đặt chi tiết
Sau khi bạn tiến hành download rồi thì việc cần làm tiếp theo là giải nén thư mục Apache 24 rồi gắn vào ổ C và tiến hành đổi tên thành Apache 24 theo mặc định. Như vậy quá trình cài đã hoàn tất.

Để khởi động lợi phần mềm Apache bạn click vào thư mực C:\Apache24\bin và chạy file httpd.exe. Rồi sau đó bạn hoàn toàn có thể truy cập vào đường link http://localhost để kiểm tra và nếu hiện dòng chữ “ it works” là chứng tỏ bạn đã cài đặt thành công app.

Nhưng đôi khi đang chạy phần mềm bạn sẽ thấy thông báo httpd.exe: AH00558: httpd.exe: Could not reliably determine the server’s fully qualified domain name, using fe80::b93e:e93c:a570:f94a. Set the ‘ServerName’ directive globally to suppress this message.

Khi gặp lỗi này, người dùng không cần quá lo lắng vì đây chỉ là cảnh báo đơn thuần, không phải lỗi. Để sửa, bạn chỉ cần gán giá trị cho mục Server Nam trong ổ C như sau:

– #ServerName www.example.com:80

– Bỏ dấu “#” và thay đổi thành “localhost” hoặc domain của bạn.

– ServerName localhost

Sau đó, bạn tắt cửa sổ httpd.exe và tiến hành chạy lại file này để khởi động lại phần mềm: Bật mod_rewrite trong Apache trên localhost

– Để sử dụng được WordPress Permalink bạn bật mod_rewrite trên localhost. Để bật mod_rewrite trong Apache mở file

– C:\Apache24\conf\httpd.conf và tìm đoạn sau:

– #LoadModule rewrite_module modules/mod_rewrite.so

– Xóa dấu “#” ở trước để bật module này nhé.

# Bước 3: Cài đặt service
Người dùng còn chưa biết tính năng đặc biệt đó là bạn có thể cài đặt để khởi động hệ thống, dừng Apache thông qua một số ứng dụng service của Windows bằng cách mở Command Prompt hoặc Run as Administrator và sử dụng một đoạn lệnh sau:

– cd C:\Apache24\bin

– httpd -k install

Tiếp đó, bạn di chuyển đến thư mục bin của Apache và sử dụng lệnh httpd – k install để cài đặt. Khi thành công, sẽ hiện thông báo:

– Installing the ‘Apache2.4’ service

– The ‘Apache2.4’ service is successfully installed.

– Testing httpd.conf….

– Errors reported here must be corrected before the service can be started.

Bạn có thể bắt đầu, kết thúc hoặc chạy lại app trên Windows bằng cách start, stop hoặc restart service ở Control Panel > Administrative Tools > Services.

Đôi khi cũng có thể sử dụng lệnh bằng cách mở Command Prompt hoặc Run as Administrator và các lệnh như:

– # start

– net start Apache2.4

– # stop

– net stop Apache2.4.

– Đó chính là quy trình tỉ mỉ về cách cài đặt Apache trên Windows của bạn.
