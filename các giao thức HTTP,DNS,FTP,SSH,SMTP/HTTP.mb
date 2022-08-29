# VLAN là gì?

VLAN là viết tắt của Virtual Local Area Network hoặc Virtual LAN, có nghĩa là Mạng cục bộ ảo” hoặc “Mạng LAN ảo”. VLAN là một mạng tùy chỉnh được tạo từ một hoặc nhiều mạng LAN hiện có. Nó cho phép các nhóm thiết bị từ nhiều mạng (cả có dây và không dây ) được kết hợp thành một mạng logic duy nhất. Kết quả là một mạng LAN ảo có thể được quản lý giống như một mạng cục bộ vật lý. Việc tạo lập nhiều mạng LAN ảo trong cùng một mạng cục bộ ( giữa các khoa trong một trường học, giữa các cục trong một công ty,...) giúp giảm thiểu vùng quảng bá (broadcast domain) cũng như tạo thuận lợi cho việc quản lý một mạng cục bộ rộng lớn.

Với mạng LAN thông thường, các máy tính trong cùng một địa điểm (cùng phòng,..) có thể được kết nối với nhau thành một mạng LAN., chỉ sử dụng một thiết bị tập trung như hub hay switch. Có nhiều mạng LAN khác nhau cần rất nhiều bộ hub, swtich. Tuy nhiên thực tế số lượng máy tính trong một LAN thường không nhiều, ngoài ra nhiều máy tính cùng một địa điểm (cùng phòng) có thể thuộc nhiều LAN khác nhau vì vậy càng tốn nhiều bộ hub, switch khác nhau. Do đó vừa tốn tài nguyên số lượng hub, switch và lãng phí số lượng port Ethernet.

Với nhu cầu tiết kiệm tài nguyên đồng thời đáp ứng nhu cầu sử dụng nhiều LAN trong cùng một địa điểm, giải pháp đưa ra là nhóm các máy tính thuộc các LAN khác nhau vào cùng một bộ tập trung switch. Giải pháp này gọi là mạng LAN ảo hay VLAN.

![image](https://user-images.githubusercontent.com/48250210/157635234-009f04a5-1d14-4d94-8084-f55beb043638.png)

Hiện nay, VLAN đóng một vai trò rất quan trọng trong công nghệ mạng LAN. Để thấy rõ được lợi ích của VLAN, chúng ta hãy xét trường hợp sau:

Giả sử, một công ty có 3 bộ phận là: Engineering, Marketing, Accounting, mỗi bộ phận trên lại trải ra trên 3 tầng. Để kết nối các máy tính trong một bộ phận với nhau thì ta có thể lắp đặt cho mỗi tầng một switch. Điều đó có nghĩa là mỗi tầng phải dùng 3 switch cho 3 bộ phận, nên để kết nối 3 tầng trong công ty cần phải sử dụng 9 switch => rất tốn kém và không thể tận dụng hết số port vốn có của 1 switch. Vì vậy, giải pháp VLAN ra đời nhằm giải quyết vấn đề trên một cách đơn giản và vẫn tiết kiệm được tài nguyên.

![image](https://user-images.githubusercontent.com/48250210/157639138-8e653ae5-8ef3-4d65-be42-82f865e67383.png)

Như hình vẽ ta thấy, mỗi tầng của công ty chỉ cần dùng 1 switch, và switch này được chia VLAN. Các máy tính ở bộ phận Engineering thì sẽ được gán vào VLAN Engineering, các PC ở bộ phận khác cũng được gán vào các VLAN tương ứng là Marketing và Accounting. Cách làm trên giúp ta có thể tiết kiệm tối đa số switch phải sử dụng đồng thời tận dụng được hết số cổng sẵn có của switch.

# Phân loại

Có 3 loại VLAN, bao gồm:
* VLAN dựa trên cổng (port based VLAN): mỗi cổng (ethernet hoặc Fast ethernet) được gắn vợi một VLAN xác định. Do đó mỗi máy tính/thiết bị host kết nối với một cổng của switch đều thuộc một VLAN nào đó. Đây là cách cấu hình VLAN đơn giản và phổ biến nhất.
* VLAN dựa trên địa chỉ vật lý MAC (MAC address based VLAN): mỗi địa chỉ MAC được gắn tới một VLAN nhất định. Cách cấu hình này rất phức tạp và khó quản lý. 
* VLAN dựa trên giao thức (protocol based VLAN): tương tự với VLAN dựa trên địa chỉ MAC nhưng sử dụng địa chỉ IP thay cho địa chỉ MAC. Cách cấu hình này không được thông dụng

# Ưu điểm của VLAN

* Tiết kiệm băng thông của hệ thống mạng: VLAN chia mạng LAN thành nhiều đoạn (segment) nhỏ, mỗi đoạn đó là một vùng quảng bá (broadcast domain). Khi có gói tin quảng bá (broadcast), nó sẽ được truyền duy nhất trong VLAN tương ứng. Do đó việc chia VLAN giúp tiết kiệm băng thông của hệ thống.
* Tăng khả năng bảo mật: do các thiết bị ở các VLAN khác nhau không thể truy nhập vào nhau (trừ khi sử dụng router nối giữa các VLAN). Như trong ví dụ trên, các máy tính trong VLAN Accounting chỉ có thể liên lạc được với nhau. máy ở VLAN Accounting không thể kết nối được với máy tính ở VLAN Engineering.
* Dễ dàng thêm/bớt máy tính vào VLAN: việc thêm một máy tính vào  VLAN rất đơn giản, chỉ cần cấu hình cổng cho máy đó vào VLAN mong muốn
* Giúp mạng có tính linh động cao: VLAN có thể dễ dàng di chuyển thiết bị. Giả sử trong ví dụ trên, sau một thời gian sử dụng, công ty quyết định để mỗi bộ phận một tầng riêng biệt. Với VLAN, ta chỉ cần cấu hình lại các cổng switch rồi đặt chúng vào VLAN theo yêu cầu. 
VLAN có thể được cấu hình tĩnh hay động. Trong cấu hình tĩnh, người quản trị mạng phải cấu hình cho từng cổng của mỗi switch. Sau đó, gán cho nó vào một VLAN nào đó. Trong cấu hình động, mỗi cổng của switch có thể tự cấu hình VLAN cho mình dựa trên địa chỉ MAC của thiết bị đã kết nối vào.

# Cấu trúc hoạt động của VLAN

Cấu trúc của một mạng các VLAN gồm 3 tầng thiết bị như sau
* Tầng 1: là router làm nhiệm vụ định tuyến giữa các VLAN
* Tầng 2: là các switch. trên các cổng của mỗi switch chia thành các VLAN
* Tầng 3: là các workstation

Ký hiệu T: là đường Trunk

![image](https://user-images.githubusercontent.com/48250210/157784138-93b8f570-38e3-4c4e-a226-d0c4432aee1a.png)

# Cách thức tạo lập VLAN

Mỗi một cổng trên switch có thể chia cho một VLAN. Những cổng được chia sẻ cho cùng một VLAN thì chia sẻ broadcast. Cổng nào không thuộc VLAN thì sẽ không chia sẻ broadcast. Những cải tiến của VLAN là làm giảm bớt broadcast và sự lãng phí băng thông.

Có 2 phương thức để tạo lập VLAN:

- Static VLAN

Phương thức này được ám chỉ như là port-base membership. Việc gán các cổng switch vào một VLAN là đã tạo một static VLAN. Giống như một thiết bị được kết nối  vào mạng, nó tự động thừa nhận VLAN của cổng đó. Nếu user thay đổi các cổng và cần truy cập vào cùng một VLAN thì người quản trị mạng cần phải khai báo cổng tới VLAN cho kết nối tới.

- Dynamic VLAN

VLAN được tạo thông qua việc sử dụng các phần mềm như Ciscowork 2000. Với một VMMPS (VLAN Management Policy Server) có thể đăng ký các cổng của switch vào các VLAN một cách tự động dựa trên địa chỉ MAC nguồn của thiết bị được nối vào cổng. Dynamic VLAN hiện thời tính đến thành viên của nó dựa trên địa chỉ MAC của thiết bị. Như một thiết bị trong mạng, nó truy vấn một cơ sở dữ liệu trên VMPS của các VLAN thành viên.

Trên switch cổng được gán cho một VLAN cụ thể thì độc lập với user hoặc hệ thống gắn với cổng đó. CÓ nghĩa là tất cả các user nằm trên các cổng nên là thành viên của cùng 1 VLAN. Một workstation hay một hub có thể kết nối vào một cổng VLAN. người quản trị mạng thực hiện gán các VLAN. Cổng mà được cấu hình là static thì không thể thay đổi  một cách tự động tới VLAN khác khu mà cấu hình lại switch.

Khi các user gắn với cùng một phân đoạn mạng chia sẻ, tất cả các user đó cùng chia sẻ băng thông của phân đoạn mạng. Mỗi một user được gắn vào môi trường chia sẻ, tất cả các user đó cùng chia sẻ băng thông của phân đoạn mạng. Mỗi một user được gắn vào môi trường chia sẻ, thì sẽ có ít băng thông sẵn có cho mỗi user, bởi tất cả các user đều nằm trên một miền xung đột. Nếu chia sẻ trở nên quá lớn, xung đột có thể xảy rả quá mức và các trình ứng dụng có thể bị mất chất lượng.

Các switch làm giảm xung đột bằng cách cung cấp băng thông giữa các thiết bị sử dụng Micro segmentation (vi phân đoạn), tuy nhiên các switch chỉ chuyển các gói tịn dạng ARP ( Address Resolution Protocol - Giao thức độ phân giải địa chỉ). VLAN đưa ra nhiều băng thông hơn cho user trong một mạng chia sẻ bằng cách hạn chế miền quảng bá cụ thể.

VLAN mặc định cho tất cả các cổng trên switch là VLAN1 hoặc management VLAN. VLAN mặc định không thể xóa, tuy nhiên các VLAN thêm vào có thể tạo ra và các cổng có thể gán lại tới các VLAN xen kẽ. Mỗi một cổng giao diện trên switch giống như cổng của bridge và switch đơn giản là một bridge nhiều cổng. Các bridge lọc tải mạng mà không cần quan tâm đến phân đoạn mạng nguồn mà chỉ cần quan tâm đến phân đoạn mạng đích. Nếu một frame cần chuyển qua bridge, và địa chỉ MAC đích là biết được, thì bridge sẽ chuyển frame tới cổng giao diện chính xác. Nếu bridge hoặc switch không biết đích đến, nó sẽ chuyển gói tin qua tất cả các cổng trong vùng quảng bá (VLAN) trừ cổng nguồn. Mỗi một VLAN nên có một địa chỉ lớp 3 duy nhất hoặc địa chỉ subnet được đăng ký. Điều đó giúp router chuyển mạch gói giữa các VLAN. Các VLAN có thể tồn tại như các mạng end-to-end

# End-to-End VLAN (VLAN đầu cuối)

Các End-to-End VLAN cho phép các thiết bị trong một nhóm sử dụng chung tài nguyên. Bao gồm các thông số như server lưu trữ, nhóm dự án và các phòng ban. Mục đích của các End-to-End VLAN là duy trì 80% thông lượng trên VLAN hiện thời. Một End-to-End VLAN có các đặc điểm sau:
* Các user được nhóm vào các VLAN độc lập về vị trí vật lý nhưng lại phụ thuộc vào nhóm chức năng hoặc đặc thù công việc.
* Tất cả các user trong một VLAN nên có cùng kiểu truyền dữ liệu 80/20 (80% băng thông cho VLAN và 20% băng thông cho các truy cập từ xa).
* Như một user di chuyển trong một khuôn viên mạng, VLAN dành cho user đó không nên thay đổi.
* Mỗi VLAN có những bảo mật riêng cho từng thành viên. 

Như vật, trong End-to-End VLAN, các user sẽ được nhóm vào thành những nhóm dựa trên chức năng, theo nhóm dự án hoặc theo cách mà những người dùng đó sử dụng tài nguyên mạng

# Geographic VLANs ( các VLAN cục bộ)

Nhiều hệ thống mạng mà cần có sự di chuyển tới những nơi tập trung tài nguyên, End-to-End VLAN trở nên khó duy trì. Những user yêu cầu sử dụng nhiều nguồn tài nguyên khác nhau, nhiều trong số đó không còn ở trong VLAN của chúng nữa. Bởi sự thay đổi về địa điểm và cách sử dụng tài nguyên. Các VLAN được tạo ra xung quanh các giới hạn địa lý hơn là giới hạn thông thường.

Vị trí địa lý có thể rộng như toàn bộ một tòa nhà, hoặc cũng có thể nhỏ như một switch trong một wiring closet (tủ dây điện). Trong một số cấu trúc VLAN cục bộ, đó là một cách để tìm ra nguyên tắc 20/80 trong hiệu quả với 80% của thông lượng truy cập từ xa và 20% thông lượng hiện thời tới user. Điều này trái ngược với End-to-End VLAN. Mặc dù hình thái mạng này user phải đi qua thiết bị lớp 3 để đạt được 80% tài nguyên khai thác. Thiết kế này cho phép cung cấp cho một dự định, một phương thức chắc chắn của việc xác nhận tài nguyên.

# Nhận dạng VLAN Frame

![image](https://user-images.githubusercontent.com/48250210/157790183-0d08cdc8-3a92-455d-b1ef-e0efe1e68822.png)

Với các VLAN sử dụng nhiều switch, frame header được đóng gói hoặc sử dụng lại để phản hồi một VLAN Id trước khi Frame được gửi đi vào nốt kết giữa các switch. Trước khi chuyển gói tin đến điểm cuối, Frame header được thay đổi trở lại với định dạng ban đầu. VLAN nhận dạng bằng cách: gói tin nào thì thuộc VLAN đó. Phương thức đa mạch nối (Multiple trunking) tồn tại, bao gồm IEEE 802.1q, ISL, 802.10 và LANE.

**1. IEEE 802.1q: Frame tagging**

Giao thức này như là một phương thức chuẩn của IEEE để dành cho việc nhận dạng các VLAN bằng cách thêm vào Frame header đặc điểm của một VLAN. Phương thức này còn được gọi là gắn thẻ cho Frame (Frame tagging).

![image](https://user-images.githubusercontent.com/48250210/157791043-2eb28dc8-d728-4470-ac8a-104614621633.png)

Trong hình minh họa một định dạng Frame 802.1q với VLAN Id. mỗi một cổng 802.1q được gán cho một đường trunk và tất cả các cổng trên đường trunk để ở trong một Native VLAN. Mỗi cổng 802.1q được gán một giá trị nhận dạng đó là native VLAN Id (mặc định là VLAN 1). Tất cả các frame không được gắn thẻ được gán vào trong LAN cái mà theo lý thuyết là nằm trong tham số Id. Một đường trunk 802.1q được kết hợp các cổng trunk có một giá trị Native VLAN. Tuy nhiên các trạm làm việc thông thường có thể đọc được các Native Frame không gắn thẻ nhưng lại đọc được các Frame được gắn thẻ. IEEE 802.1q Frame tagging đã đưa ra một phương truyền thông VLAN giữa các switch.

**2. Inter-Switch Link Protocol**

ISL là một giao thức đóng gói của Cisco. Giao thức này dùng để đa liên kết các hệ thống đa switch, nó được hỗ trợ, tương thích trên switch cũng tốt như router.

![image](https://user-images.githubusercontent.com/48250210/157794971-6927cd95-ce87-4dce-b591-70d2a6378dcb.png)

Dòng switch Castalyst sử dụng ISL frame tagging là một kỹ thuật có độ trễ thấp, dùng cho việc dồn kênh từ nhiều VLAN trên một đường dây vật lý. ISL được thực thi cho kết nối giữa switch, router và NIC sử dụng trên các node như server. Để hỗ trợ chức năng ISL, các thiết bị kết nối phải được cấu hình ISL.

# Các kiểu VLAN

* VLAN 1

Mặc định, các thiết bị lớp 2 sẽ sử dụng một VLAN mặc định để đưa tất cả các cổng của thiết bị đó vào. Thêm vào nữa là có rất nhiều giao thức lớp 2 như CDP, PAgP, và VTP cần phải được gửi tới một VLAN xác định trên các đường trunk. Chính vì các mục đích đó mà VLAN mặc định được chọn là VLAN 1.

CDP, PagP, VTP, và DTP luôn luôn được truyền qua VLAN 1 và mặc định này không thể thay đổi được. Các khuyến cáo của Cisco chỉ ra rằng VLAN 1 chỉ nên dành cho các giao thức kể trên.

* Default VLAN

VLAN 1 còn được gọi là default VLAN. Chính vì vậy, mặc định, native VLAN, management VLAN và user VLAN sẽ là thành viên của VLAN 1.

Tất cả các giao diện Ethernet trên switch Catalyst mặc định thuộc VLAN 1. Các thiết bị gắn với các giao diện đó sẽ là thành viên của VLAN 1, trừ khi các giao diện đó được cấu hình sang các VLAN khác.

* User VLANs

Hiểu đơn giản User VLAN là một VLAN được tạo ra nhằm tạo ra một nhóm người sử dụng mà không phụ thuộc vào vị trí địa lý hay logic và tách biệt với phần còn lại của mạng ban đầu. Câu lệnh switchport access vlan được dùng để chỉ định các giao diện vào các VLAN khác nhau.

* Native VLAN

Một chủ đề hay gây nhầm lẫn là Native VLAN. Native VLAN là một VLAN có các cổng được cấu hình trunk. Khi một cổng của switch được cấu hình trunk, trong phần tag của frame đi qua cổng đó sẽ được thêm một số hiệu VLAN thích hợp. Tất cả các frames thuộc các VLAN khi đi qua đường trunk sẽ được gắn thêm các tag của giao thức 802.1q và ISL, ngoại trừ các frame của VLAN 1. Như vậy, theo mặc định các frames của VLAN 1 khi đi qua đường trunk sẽ không được gắn tag.
Khả năng này cho phép các cổng hiểu 802.1Q giao tiếp được với các cổng cũ không hiểu 802.1Q bằng cách gửi và nhận trực tiếp các luồng dữ liệu không được gắn tag. Tuy nhiên, trong tất cả các trường hợp khác, điều này lại gây bất lợi, bởi vì các gói tin liên quan đến native VLAN sẽ bị mất tag.

Native VLAN được chuyển thành VLAN khác bằng câu lệnh: **Switch(config-if)#switchport trunk native vlan vlan-id**

* Management VLAN

Hiện nay, đa số các thiết bị như router, switch có thể truy cập từ xa bằng cách telnet đến địa chỉ IP của thiết bị. Đối với các thiết bị mà cho phép truy cập từ xa thì chúng ta nên đặt vào trong một VLAN, được gọi là Management VLAN. VLAN này độc lập với các VLAN khác như user VLAN, native VLAN. Do đó khi mạng có vấn đề như : hội tụ với STP, broadcast storms, thì một Management VLAN cho phép nhà quản trị vẫn có thể truy cập được vào các thiết bị và giải quyết các vấn đề đó.

Một yếu tố khác để tạo ra một Management VLAN độc lập với user VLAN là việc tách các thiết bị đáng tin cậy với các thiết bị không tin cậy. Do đó làm giảm đi khả năng các user khác đạt được quyền truy cập vào các thiết bị đó.

# Cách cấu hình VLAN

**1. Tạo VLAN**

**Bước 1.** Đăng nhập vào tiện ích trên web và chọn đến phần VLAN Management > VLAN Settings.

**Bước 2.** Trong khu vực VLAN Table, bấm chuột vào Add để tạo một VLAN mới. Một cửa sổ sẽ xuất hiện.

**Bước 3.** VLAN có thể được thực hiện thêm vào theo hai phương thức khác nhau như được hiển thị bởi những tùy chọn bên dưới. Sau đó bạn hãy lựa chọn phương thức mong muốn.

**Bước 4.** Nếu bạn đã chọn VLAN ở bước 3 thì hãy nhập VLAN ID vào trường VLAN ID. Chú ý, phạm vi phải nằm trong khoảng từ 2 đến 4094.

**Bước 5.** Trong trường VLAN Name, bạn cần phải nhập tên cho VLAN. Ví dụ như: VLAN Name sẽ là Accounting, có tối đa 32 ký tự có thể được sử dụng.

**Bước 6.** Bạn tiếp tục chọn hộp kiểm VLAN Interface State để thực hiện kích hoạt trạng thái interface VLAN. Nó đã được tự động lựa chọn theo mặc định. Nếu không, mạng VLAN sẽ bị tắt và không có gì có thể được truyền hay nhận thông qua VLAN.

**Bước 7.** Tích chuột vào hộp kiểm Link Status SNMP Traps nếu như bạn muốn kích hoạt việc tạo SNMP trap.

**Bước 8.** Nếu bạn chọn Range ở trong bước 3, hãy nhập phạm vi cho các VLAN ở trong trường VLAN Range. Phạm vi đã có sẵn là 2 – 4094. Trong ví dụ này, VLAN Range sẽ là từ 3 đến 52.

**Lưu ý:** Có thể tạo được tối đa 100 VLAN cùng một lúc.

**Bước 9.** Bạn nhấn vào Apply để hoàn tất.

**2. Chỉnh sửa VLAN**

**Bước 1.** Đăng nhập vào tiện ích dựa trên trình duyệt web và lựa chọn VLAN Management > VLAN. Bạn hãy tìm đến trang VLAN thì mục Settings sẽ mở ra.

**Bước 2.** Chọn hộp kiểm bên cạnh VLAN nơi mà bạn muốn chỉnh sửa.

**Bước 3.** Nhấn Edit để thực hiện chỉnh sửa VLAN đã chọn. Cửa sổ Edit VLAN được xuất hiện.

**Bước 4.** Bạn có thể thay đổi VLAN hiện tại bằng cách dùng danh sách drop-down VLAN ID. Điều này được sử dụng để có thể nhanh chóng chuyển đổi giữa các VLAN bạn muốn cấu hình, mà không phải thực hiện quay lại trang VLAN Settings.

**Bước 5.** Chỉnh sửa tên của VLAN vào trong trường VLAN Name. Tên này sẽ không ảnh hưởng đến hiệu suất của VLAN và còn được sử dụng để nhận dạng dễ dàng.

**Bước 6.** Đánh dấu vào phần hộp kiểm VLAN Interface State để có thể kích hoạt trạng thái interface của VLAN. Nếu không thì VLAN sẽ bị tắt và không có gì có thể được truyền hoặc thực hiện nhận thông qua VLAN.

**Bước 7.** Tích chuột vào hộp kiểm Enable Link Status SNMP Traps để cho phép tạo SNMP trap với thông tin ở trạng thái liên kết. Hộp này sẽ được chọn theo mặc định.

**Bước 8.** Nhấn vào Apply để hoàn tất.

**5.3. Xóa cấu hình mạng VLAN**

**Bước 1.** Bạn hãy đăng nhập vào tiện ích dựa trên web và lựa chọn VLAN Management > VLAN Settings.

**Bước 2.** Chọn hộp kiểm bên cạnh VLAN mà bạn muốn xóa.

**Bước 3.** Nhấn Delete để thực hiện xóa VLAN đã chọn.

# Các giao thức trong VLAN

**1. VLAN Trunking Protocol – Giao thức mạch nối các VLAN**

VTP (Vlan Trunking Protocol) là giao thức hoạt động ở tầng liên kết dữ liệu trong mô hình OSI. VTP giúp cho việc cấu hình VLAN luôn đồng nhất khi thêm, xóa, sửa thông tin về VLAN trong hệ thống mạng.

VTP gửi thông điệp quảng bá qua “VTP domain” mỗi 5 phút một lần, hoặc khi có sự thay đổi xảy ra trong quá trình cấu hình VLAN. Một thông điệp VTP bao gồm “rivision-number”, tên VLAN (VLAN name), số hiệu VLAN. Bằng sự cấu hình VTP Server và việc quảng bá thông tin VTP tất cả các switch đều đồng bộ về tên VLAN và số liệu VLAN của tất cả các VLAN.

Một trong những thành phần quan trọng trong các thông tin quảng bá VTP là tham số “revision-number”.  Mỗi thành phần VTP server điều chỉnh thông tin VLAN, nó tăng “revision-number” lên 1, rồi sau đó VTP Server mới gửi thông tin quảng bá VTP đi. Khi một switch nhận một thông điệp VTP với “revision-number” lớn hơn, nó sẽ cập nhật cấu hình VLAN.

![image](https://user-images.githubusercontent.com/48250210/157797779-ebe31d42-6176-4305-a7bd-91e4f2d39c0d.png)

VTP hoạt động ở một trong 3 cơ chế sau:
* Server
* Client
* Transparent

![image](https://user-images.githubusercontent.com/48250210/157797871-381a7917-8cd2-49fc-8c95-c671d5e3f8af.png)

Switch ở chế độ VTP Server có thể tạo, chỉnh sử và xóa VLAN. VTP server lưu cấu hình VLAN trong NVRAM của nó. VTP Server gửi thông điệp ra tất cả các cổng” trunk”.

Switch ở chế độ VTP client không tạo, sửa và xóa thông tin VLAN. VTP Client có chức năng đáp ứng theo mọi sự thay đổi của VLAN từ Server và gửi thông điệp ra tất cả các cổng “trunk” của nó. VTP Client đồng bộ cấu hình VLAN trong hệ thống.

Switch ở chế độ transparent sẽ nhận và chuyển tiếp các thông điệp quảng bá VTP do các switch khác gửi đến mà không quan tâm đến nội dung của các thông điệp này. Nếu “transparent switch” nhận thông tin cập nhật VTP nó cũng không cập nhật vào cơ sở dữ liệu của nó; đồng thời nếu cấu hình VLAN của nó có gì thay đổi, nó cũng không gửi thông tin cập nhật cho các switch khác. Trên “transparent switch” chỉ có một việc duy nhất là chuyển tiếp thông điệp VTP. Switch hoạt động ở “transparent-mode” chỉ có thể tạo ra các VLAN cục bộ. Các VLAN này sẽ không được quảng bá đến các switch khác.

**2. Inter VLAN Routing**

- Inter-VLAN

Mỗi mạng có nhu cầu riêng của nó, tuy nhiên cho dù đó là một mạng lưới rộng lớn hay nhỏ, định tuyến nội bộ, trong hầu hết các trường hợp, là điều cần thiết. Khả năng để phân chia mạng bằng cách tạo ra VLANs, do đó giảm broadcasts mạng và tính bảo mật ngày càng tăng. Các thiết lập phổ biến bao gồm một broadcast domain riêng biệt cho các dịch vụ quan trọng ngày càng nhiều.

Vấn đề ở đây là làm thế nào có thể từ một trong những người sử dụng VLAN ( thuộc về 1 broadcast domain), sử dụng được các dịch vụ được cung cấp bởi một VLAN khác? Do vậy giải pháp định tuyến trên VLAN đã được đề cập đến.

Inter-VLAN là phương pháp được thiết lập có hiệu quả nhất bằng cách cung cấp một liên kết trunk duy nhất giữa Switch và Router mà có thể mang lưu lượng truy cập của nhiều VLAN và trong đó các lưu lượng ấy lần lượt có thể được định tuyến bởi Router.

Với Inter-VLAN Routing, Router nhận frame từ Switch với gói tin xuất phát từ một VLAN đã được tag. Nó liên kết các frame với các subinterface thích hợp và sau đó giải mã nội dung của frame (phần IP packet). Router sau đó thực hiện chức năng của Layer 3 dựa trên địa chỉ mạng đích có trong gói tin IP để xác định subinterface cần chuyển tiếp gói IP. Các IP packet bây giờ được đóng gói thành frame theo chuẩn dot1Q (hoặc ISL) để nhận dạng VLAN của subinterface chuyển tiếp và truyền đi trên đường trunk vào Switch.

- Cấu hình Inter-VLAN

a. Trên Switch

SW0(config)#vlan 10

SW0(config-vlan)#name IT

SW0(config-vlan)#vlan 20

SW0(config-vlan)#name sale

SW0(config-vlan)#exit

SW0(config)#interface range f0/1-10

SW0(config-if-range)#switchport access vlan 10

SW0(config-if-range)#exit

SW0(config)#interface range f0/11-20

SW0(config-if-range)#switchport access vlan 20

SW0(config-if-range)#exit

SW0(config)#interface range g1/1-2

SW0(config-if-range)#switchport mode trunk

SW0(config)#interface vlan 1

SW0(config)#no shutdown

SW0(config-if)#ip add 10.0.0.101 255.255.255.0

SW0(config-if)#end

SW0#write

b. Cấu hình định tuyến VLAN trên Router

R1(config)#int f0/0

R1(config-if)#no shut

R1(config)#int f0/0.10

R1(config-subif)#encapsulation dot1Q 10

R1(config-subif)#ip add 192.168.1.1 255.255.255.0

R1(config-subif)#exit

R1(config)#int f0/0.20

R1(config-subif)#encapsulation dot1Q 20

R1(config-subif)#ip add 192.168.2.1 255.255.255.0

R1(config-subif)#exit
# 1. NAT là gì?

NAT (Network Address Translation) là một kỹ thuật cho phép chuyển đổi từ một địa chỉ IP này thành một địa chỉ IP khác. Thông thường, NAT được dùng phổ biến trong mạng sử dụng địa chỉ cục bộ, cần truy cập đến mạng công cộng (Internet). Vị trí thực hiện NAT là router biên kết nối giữa hai mạng.

# 2. Cơ chế hoạt động của NAT

NAT sử dụng IP của chính nó làm IP công cộng cho mỗi máy con (client) với IP riêng. Khi một máy con thực hiện kết nối hoặc gửi dữ liệu tới một máy tính nào đó trên internet, dữ liệu sẽ được gửi tới NAT, sau đó NAT sẽ thay thế địa chỉ IP gốc của máy con đó rồi gửi gói dữ liệu đi với địa chỉ IP của NAT. Máy tính từ xa hoặc máy tính nào đó trên internet khi nhận được tín hiệu sẽ gửi gói tin trở về cho NAT computer bởi vì chúng nghĩ rằng NAT computer là máy đã gửi những gói dữ liệu đi. NAT ghi lại bảng thông tin của những máy tính đã gửi những gói tin đi ra ngoài trên mỗi cổng dịch vụ và gửi những gói tin nhận được về đúng máy tính đó (client).

# 3. Các loại NAT

**Static NAT(NAT tĩnh)**

NAT tĩnh hay còn gọi là Static NAT là phương thức NAT một đổi một. Nghĩa là một địa chỉ IP cố định trong LAN sẽ được ánh xạ ra một địa chỉ IP Public cố định trước khi gói tin đi ra Internet. Phương pháp này không nhằm tiết kiệm địa chỉ IP mà chỉ có mục đích ánh xạ một IP trong LAN ra một IP Public để ẩn IP nguồn trước khi đi ra Internet làm giảm nguy cơ bị tấn công trên mạng.

***Cấu hình Static NAT***

- Thiết lập mối quan hệ chuyển đổi giữa địa chỉ nội bộ bên trong và địa chỉ đại điện bên ngoài.

  `Router (config) # ip nat inside source static [local ip] [global ip]`

- Xác định các cổng kết nối vào mạng bên trong và thực hiện lệnh.

  `Router (config-if) # ip nat inside`

-Xác định các cổng kết nối ra mạng công cộng bên ngoài thực hiện lệnh.

  `Router (config-if) # ip nat outside.`

**Dynamic NAT(NAT động)**

Nat động (Dynamic NAT) là một giải pháp tiết kiệm IP Public cho NAT tĩnh. Thay vì ánh xạ từng IP cố định trong LAN ra từng IP Public cố định. LAN động cho phép NAT cả dải IP trong LAN ra một dải IP Public cố định ra bên ngoài.

***Cấu hình Dynamic NAT***

- Xác định dải địa chỉ đại diện bên ngoài (public):các địa chỉ NAT.

  `Router (config) # ip nat pool [name start ip] [name end ip] netmask [netmask]/prefix-lenght [prefix-lenght]`

- Thiết lập ACL cho phép những địa chỉ nội bộ bên trong nào được chuyển đổi: các địa chỉ được NAT.

  `Router (config) # access-list [access-list-number-permit] source [source-wildcard]`

- Thiết lập mối quan hệ giữa địa chỉ nguồn đã được xác định trong ACL với dải địa chỉ đại diện ra bên ngoài.

  `Router (config) # ip nat inside source list <acl-number> pool <name>`

- Xác định các cổng kết nối vào mạng nội bộ.

  `Router (config-if) # ip nat inside`

- Xác định các cổng kết nối ra bên ngoài.

  `Router (config-if) # ip nat outside`

**NAT Overload**

NAT Overload là một dạng của Dynamic NAT, nó thực hiện ánh xạ nhiều địa chỉ IP thành một địa chỉ (many – to – one) và sử dụng các địa chỉ số cổng khác nhau để phân biệt cho từng chuyển đổi. NAT Overload còn có tên gọi là PAT (Port Address Translation). Chỉ số cổng được mã hóa 16 bit, do đó có tới 65536 địa chỉ nội bộ có thể được chuyển đổi sang một địa chỉ công cộng.

***Cấu hình Overload***

- Xác định dãy địa chỉ bên trong cần chuyển dịch ra ngoài (private ip addresses range)

  `Router (config) # access-list <ACL-number> permit <source> <wildcard>`

- Cấu hình chuyển đổi địa chỉ IP sang cổng nối ra ngoài

  `Router (config) # ip nat inside source list <ACL-number> interface <interface> overload`

- Xác định các cổng nối vào mạng bên trong và nối ra mạng bên ngoài

Đối với các cổng nối vào mạng bên trong:
  
  `Router (config-if) # ip nat inside`

Đối với nối ra mạng bên ngoài:

  `Router (config-if) # ip nat outside`
  
# 4. Chức năng của NAT

- Ban đầu, NAT được đưa ra nhằm giải quyết vấn đề thiếu hụt địa chỉ của IPv4 .
- NAT giúp chia sẻ kết nối Internet (hay 1 mạng khác) với nhiều máy trong LAN chỉ với 1 IP duy nhất.
- NAT che giấu IP bên trong LAN
- NAT giúp quản trị mạng lọc các gói tin được gửi đến hay gửi từ một địa chỉ IP và cho phép hay cấm truy cập đến một port cụ thể.

# 5. Các vấn đề an ninh và quản trị mạng

Dynamic NAT (NAT động) tự động tạo ra một bức tường lửa giữa mạng nội bộ và mạng bên ngoài, hoặc giữa các mạng nội bộ của bạn và Internet. NAT chỉ cho phép các kết nối có nguồn gốc bên trong Stub Domain. Về cơ bản, điều này có nghĩa là một máy tính nằm ở mạng ngoài không thể kết nối với máy tính của bạn, trừ khi máy tính của bạn đã kết nối với máy tính đó trước. Bạn có thể duyệt Internet và kết nối đến một trang web, hoặc thậm chí là download một file tin; nhưng người khác không thể sử dụng các địa chỉ IP của bạn để kết nối tới một Port (cổng) trên máy tính của bạn.

Trong những trường hợp cụ thể, Static NAT (NAT tĩnh) cũng cho phép các thiết bị bên ngoài khởi tạo kết nối đến các máy tính trên Stub Domain. Một số NAT Router cung cấp bộ lọc và traffic logging. Bộ lọc cho phép công ty của bạn kiểm soát những trang mà nhân viên truy cập vào trên trang Web để ngăn chặn họ xem được những tài liệu quan trọng. Bạn có thể sử dụng traffic logging để tạo ra một tập tin nhật ký những trang web được truy cập và tạo ra các báo cáo khác nhau.

NAT đôi khi bị nhầm lẫn với các máy chủ proxy, nhưng giữa NAT và máy chủ proxy có sự khác biệt nhất định. NAT không thể nhầm lẫn được với các máy tính nguồn và máy tính đích, NAT giống như một thiết bị thứ ba. Còn một máy chủ proxy có thể bị nhầm lẫn. Máy tính nguồn biết rằng nó thực hiện một yêu cầu đến máy chủ proxy và phải được cấu hình để thực hiện yêu cầu đó. Máy tính đích sẽ hiểu rằng các máy chủ proxy là máy tính nguồn, và giao dịch với nó trực tiếp.

Ngoài ra, máy chủ proxy thường làm việc ở tầng 4 (Transport) trong mô hình OSI Reference Model hoặc cao hơn, trong khi NAT làm việc ở tầng 3 giao thức liên mạng (Network protocol). Khi làm việc tại một tầng cao hơn khiến các máy chủ proxy hoạt động chậm hơn so với các thiết bị NAT. Lợi ích lớn nhất của NAT đó là quản trị mạng (Network Administation) một cách rõ ràng. Ví dụ, bạn có thể di chuyển máy chủ Web của bạn hoặc máy chủ FTP tới máy tính chủ khác mà không cần phải lo lắng các liên kết bị hỏng. Đơn giản chỉ cần thay đổi, sử dụng Inbound Route Map để phản hồi máy chủ mới. Bạn cũng có thể thay đổi mạng nội bộ (Internal Network) một cách dễ dàng, bởi vì chỉ có địa chỉ IP bên ngoài hoặc địa chỉ IP của Router hoặc địa chỉ IP trong nhóm địa chỉ Global Address.

NAT và DHCP (dynamic host configuration protocol - giao thức cấu hình Host động). Bạn có thể chọn một loạt các địa chỉ IP Private trên Stub Domain và có máy chủ DHCP phát những địa chỉ IP này khi cần thiết.
# 1. Mô hình OSI

Mô hình OSI hay Open Systems Interconnection có nhiệm vụ thiết lập kết nối giữa các thiết bị giao tiếp trên toàn cầu. OSI được coi là mã nguồn mở vì khả năng phù hợp với mọi hệ thống mạng của nó. Mô hình cung cấp một tiêu chuẩn dưới dạng kiến trúc phân tầng cho phép các hệ thống khác nhau có thể giao tiếp được với nhau, trong đó gồm có 7 tầng với những cấu trúc và chức năng riêng đã được định nghĩa sẵn. Mỗi tầng có một chức năng riêng và chỉ giao tiếp với các tầng tiếp giáp với nó, mọi sự thay đổi về vị trí các tầng trong kiến trúc trên đều không được chấp nhận:

+ Tầng ứng dụng (Application Layer) 

Là tầng duy nhất tương tác trực tiếp với tiến trình ứng dụng, có trách nhiệm cung cấp giao diện cũng như các thao tác dữ liệu giúp người dùng và phần mềm ứng dụng tương tác với nhau. Một số giao thức có trong tầng ứng dụng như: HTTP, FTP, POP, DHCP,…

+ Tầng trình diễn (Presentation Layer)

Là tầng ngay dưới tầng ứng dụng, nó đáp ứng các nhu cầu của tầng ứng dụng như phiên dịch, mã hóa, giải mã, nén dữ liệu. Phiên dịch dữ liệu theo cú pháp mà ứng dụng có thể hiểu, mã hóa dữ liệu gửi đi cũng như giải mã dữ liệu nhận, nén dữ liệu trước khi truyền xuống tầng phiên

+ Tầng phiên (Session Layer) 

Là tầng ngay dưới tầng trình diễn, cung cấp các nhu cầu dịch vụ cho tầng trình diễn. Tầng phiên chịu trách nhiệm đóng và mở luồng giao tiếp giữa hai thiết bị, thời gian giữa mở và đóng được gọi là phiên. Nó đảm bảo phiên mở đủ lâu để dữ liệu có thể gửi đi và đóng đủ nhanh để tránh lãng phí tài nguyên. Ngoài ra, tầng phiên cung cấp dịch vụ đánh dấu điểm hoàn thành. Ví dụ khi bạn truyền một file dung lượng 10 GB, cứ sau mỗi 1GB lại đánh dấu điểm hoàn thành 1 lần thì khi bị mất kết nối hoặc tạm ngừng ở điểm 6GB rồi truyền lại thì chỉ cần truyền 4GB phần dữ liệu còn lại chưa được truyền

+ Tầng giao vận (Transport Layer) 

Là tầng ngay dưới tầng phiên, nó đáp ứng các nhu cầu của tầng phiên. Tầng giao vận chịu trách nhiệm thiết lập kết nối giữa hai thiết bị, nó nhận dữ liệu từ tầng phiên rồi xử lý để gửi xuống tầng dưới cũng như nhận dữ liệu từ tầng dưới xử lý để chuyển lên tầng phiên. Tầng giao vận có thể cung cấp dịch vụ kiểm soát luồng và kiểm soát lỗi để đảm bảo dữ liệu được chuyển đi được chính xác và không quá tải bên nhận

+ Tầng mạng (Network Layer) 

Đáp ứng các nhu cầu của tầng giao vận, chịu trách nhiệm giúp dữ liệu có thể truyền giữa các thiết bị ở các mạng khác nhau, nếu 2 thiết bị cùng trong một mạng thì ta không cần thiết phải có tầng này. Tầng mạng còn cung cấp các thuật toán dò đường cho các bộ định tuyến để xác định đường truyền vật lý tốt nhất cho dữ liệu

+ Tầng liên kết dữ liệu (Data Link Layer) 

Đáp ứng các nhu cầu của tầng mạng, về cơ bản tầng này giống với tầng mạng nhưng nó hỗ trợ dữ liệu có thể được truyền đi giữa các thiết bị trong cùng một mạng

+ Tầng vật lý (Physical Layer) 

Bao gồm các thiết bị phần cứng giúp truyền tải dữ liệu như cáp, bộ định tuyến,…. Ở tầng này dữ liệu được truyền tải dưới dạng bit 0 và 1

**Ưu điểm của mô hình OSI** 

+ Mỗi tầng có 1 cấu trúc và chức năng riêng nên dễ dàng xây dựng và sửa chữa

+ Có thể tích hợp trong nhiều mạng lưới khác nhau

+ Hỗ trợ kết nối có liên kết và kết nối phi liên kết

**Nhược điểm của mô hình OSI**

+ Tầng phiên và tầng trình diễn thường không được sử dụng nhiều so với các tầng khác vì chức năng hạn hẹp của nó

+ Không hỗ trợ các giao thức, không định nghĩa bất kì giao thức nào

+ Nhiều dịch vụ trùng lặp tại các tầng, ví dụ tầng mạng và tầng liên kết dữ liệu

+ Các tầng không thể hoạt động song song, tầng dưới phải chờ dữ liệu từ tầng trên

# 2. Mô hình TCP/IP

TCP/IP là viết tắt của Transmission Control Protocol/Internet Protocol. Đây là một bộ các giao thức truyền thông được sử dụng để kết nối các thiết bị mạng với nhau trên Internet. TCP/IP cũng có thể được sử dụng như một giao thức truyền thông trong mạng máy tính riêng (mạng nội bộ). Trong đó, bộ Giao thức internet - một tập hợp các quy tắc và thủ tục - thường gọi là TCP/IP. Trong đó, TCP và IP là hai giao thức chính bên cạnh những giao thức khác trong bộ. Bộ giao thức TCP/IP hoạt động như một lớp trừu tượng giữa các ứng dụng internet và hạ tầng router/switch. Cũng vậy, TCP/IP chỉ định cách dữ liệu được trao đổi qua internet. Nó thực hiện bằng cách cung cấp thông tin liên lạc đầu cuối. Từ đó xác định cách nó được chia thành các packet, xác định địa chỉ, truyền dẫn, định tuyến và nhận dữ liệu. TCP/IP được thiết kế để đảm bảo độ tin cậy, nó có khả năng khôi phục tự động khi gặp sự cố trong quá trình truyền dữ liệu.

Giao thức TCP/IP được chia thành 4 tầng mạng:

+ Tầng ứng dụng

Đảm nhận vai trò giao tiếp dữ liệu giữa 2 máy khác nhau thông qua các dịch vụ mạng khác nhau (duyệt web, chay hay các giao thức trao đổi dữ liệu SMTP, SSH, FTP…). Dữ liệu khi đến được tầng này sẽ được định dạng để kết nối theo kiểu Byte nối Byte. Các thông tin định tuyến tại đây sẽ giúp xác định đường đi đúng của một gói tin

+ Tầng mạng

Đảm nhận việc truyền tải dữ liệu một cách hợp lý. Nhiệm vụ của tầng Internet là xử lý các gói tin, sau đó kết nối với các mạng độc lập để vận chuyển các gói dữ liệu đã được mã hóa qua các ranh giới mạng. Tầng Internet cũng bao gồm nhiều giao thức như giao thức IP, ICMP

+ Tầng giao vận 

Tầng dữ liệu hoạt động thông qua hai giao thức chính là TCP (Transmission Control Protocol) và UDP (User Datagram Protocol). Nhiệm vụ của tầng giao vận là duy trì liên lạc đầu cuối trên toàn mạng. Ở tầng này, TCP và UDP sẽ hỗ trợ nhau phân luồng dữ liệu. Trong nhiều trường hợp giao thức UDP sẽ được thay thế TCP

+ Tầng vật lý 

Tầng vật lý (còn được gọi là tầng liên kết dữ liệu) là tầng thấp nhất trong mô hình TCP/IP. Tầng này chịu trách nhiệm truyền dữ liệu giữa hai thiết bị trong cùng một mạng. Tại đây, các gói dữ liệu được đóng vào khung (gọi là Frame) và được định tuyến đi đến đích đã được chỉ định ban đầu

**Ưu điểm của mô hình TCP/IP**

+ Thiết lập kết nối giữa các loại máy tính khác nhau

+ Hoạt động độc lập với hệ điều hành

+ Hỗ trợ nhiều giao thức định tuyến

+ Kiến trúc client - server, khả năng mở rộng cao

+ Có thể hoạt động độc lập

+ Hỗ trợ nhiều giao thức định tuyến

+ Nhẹ, không gây nhiều áp lực với máy tính hay mạng

**Nhược điểm của mô hình TCP/IP**

+ Việc cài đặt khá phức tạp, khó để quản lý

+ Tầng transport không đảm bảo việc phân phối các gói tin

+ Các giao thức trong TCP/IP không dễ để có thể thay thế

+ Không tách biệt rõ ràng các khái niệm về dịch vụ, giao diện và giao thức. Do đó nó không hiệu quả để mô tả các công nghệ mới trong mạng mới

+ Dễ bị tấn công SYN  - một kiểu tấn công từ chối dịch vụ

# 3. So sánh 2 mô hình OSI và CTP/IP

**Điểm tương đồng giữa mô hình OSI và TCP/IP**

+ Chia sẻ kiến trúc chung

Cả 2 mô hình đều là mô hình logic và có kiến trúc tương tự vì cả 2 mô hình đều được xây dựng dựa trên các lớp

+ Xác định tiêu chuẩn 

Cả 2 lớp đều có các tiêu chuẩn xác định và chúng cũng cung cấp khuôn khổ được sử dụng để thực hiện các tiêu chuẩn và thiết bị

+ Quy trình khắc phục sự cố được đơn giản hóa

Cả 2 mô hình đã đơn giản hóa quá trình khắc phục sự cố bằng cách chia nhỏ chức năng phức tạp thành các thành phần đơn giản hơn

+ Các tiêu chuẩn được xác định trước

Các tiêu chuẩn và giao thức đã được xác định trước, những mô hình này không xác định lại chúng, chỉ tham khảo hoặc sử dụng lại chúng. Ví dụ, các tiêu chuẩn Ethernet đã được IEEE xác định trước khi phát triển các mô hình 

+ Cả 2 đều có chức năng tương tự của các lớp Transport và Network

Chức năng được thực hiện giữa lớp Presentation và lớp Network tương tự như chức năng được thực hiện ở lớp Transport

# Sự khác biệt giữa mô hình OSI và TCP/IP

+ Mô hình TCP/IP được nhiều người tin cậy và được sử dụng phổ biến trên toàn cầu hơn mô hình OSI
+ Mô hình OSI tiếp cận theo chiều dọc còn mô hình TCP/IP thì tiếp cận theo chiều ngang
+ Mô hình TCP/IP có sự kết hợp giữa tầng trình diễn và tầng phiên ở trong tầng ứng dụng còn mô hình OSI thì không có sự kết hợp nào
+ Mô hình OSI thì mô hình được thiết kế trước sau đó sẽ phát triển giao thức còn mô hình TCP/IP thì ngược lại
+ Mô hình OSI có 7 tầng còn mô hình TCP/IP chỉ có 4 tầng
+ Mô hình TCP/IP chỉ hỗ trợ truyền thông không kết nối từ tầng mạng còn mô hình OSI thì hỗ trợ cả kết nối định tuyến và không dây
+ Mô hình OSI thì có giao thức độc lập còn mô hình TCP/IP lại phụ thuộc vào giao thức

# 4. Kết luận

Chúng ta có thể kết luận rằng mô hình TCP/IP đáng tin cậy đối với mô hình OSI, TCP/IP được sử dụng cho kết nối đầu cuối để truyền dữ liệu qua Internet. TCP/IP mạnh mẽ, linh hoạt, hữu hình và cũng gợi ý cách dữ liệu nên được gửi qua web. Lớp vận chuyển của Mô hình TCP/IP kiểm tra xem dữ liệu đã đến theo thứ tự chưa, nó có lỗi hay không, các gói bị mất có được gửi hay không, xác nhận có được nhận hay không, v.v…
# Định tuyến là gì?

Định tuyến là quá trình xác định đường đi tốt nhất trên một mạng máy tính để gói tin tới được đích theo một số thủ tục nhất định nào đó thông qua các nút trung gian là các bộ định tuyến router. Thông tin về những con đường này có thể được cập nhật tự động từ các router khác hoặc là do người quản trị mạng chỉ định cho router. Sau khi Router nhận gói tin, thì Router sẽ gỡ bỏ phần header lớp 2 để tìm địa chỉ đích thuộc lớp 3. Sau khi đọc xong địa chỉ đích lớp 3 nó tìm kiếm trong Routing Table cho mạng chứa địa chỉ đích. Để truyền được gói tin đến đích thì các router cần phải được cấu hình một bảng định tuyến (Routing Table) và giao thức định tuyến (Routing Protocol). Bảng định tuyến là bảng chứa tất cả những đường đi tốt nhất đến một đích nào đó tính từ router. Khi cần chuyển tiếp một gói tin, router sẽ xem địa chỉ đích của gói tin, sau đó tra bảng định tuyến và chuyển gói tin đi theo đường tốt nhất tìm được trong bảng. Trong bảng định tuyến có thể bao gồm một tuyến mặc định, được biểu diễn bằng địa chỉ 0.0.0.0 0.0.0.0.

Bảng định tuyến của mỗi giao thức định tuyến là khác nhau, nhưng có thể bao gồm những thông tin sau:

- Địa chỉ đích của mạng, mạng con hoặc hệ thống.

- Địa chỉ IP của router chặng kế tiếp phải đến.

- Giao tiếp vật lí phải sử dụng để đi đến Router kế tiếp.

- Subnet mask của địa chỉ đích.

- Khoảng cách đến đích (ví dụ: số lượng chặng để đến đích).

- Thời gian (tính theo giây) từ khi Router cập nhật lần cuối.

Giao thức định tuyến là ngôn ngữ giao tiếp giữa các router. Một giao thức định tuyến cho phép các router chia sẻ thông tin về các network, router sử dụng các thông tin này để xây dựng và duy trì bảng định tuyến.

# Phân loại định tuyến

Có nhiều tiêu chí để phân loại các giao thức định tuyến khác nhau. Định tuyến được phân chia thành 2 loại cơ bản:

- Định tuyến tĩnh: Việc xây dựng bảng định tuyến của router được thực hiện bằng tay bởi người quản trị.

- Định tuyến động: Việc xây dựng và duy trì trạng thái của bảng định tuyến được thực hiện tự động bởi router.

Việc chọn đường đi được tuân thủ theo 2 thuật toán cơ bản:

+ Distance vector: Chọn đường đi theo hướng và khoảng cách tới đích.

+ Link State: Chọn đường đi ngắn nhất dựa vào cấu trúc của toàn bộ mạng theo trạng thái của các đường liên kết mạng.

![image](https://user-images.githubusercontent.com/55913475/157820356-e28d7b1e-82cc-48c1-9cfc-111782e21081.png)

Khi chọn lựa một giao thức định tuyến động cần cân nhắc một số yếu tố như: độ lớn của hệ thống mạng, băng thông các đường truyền, khả năng của router, loại router và phiên bản router, các giao thức đang chạy trong hệ thống mạng.

# Các giao thức định tuyến

**RIP (Routing Information Protocol)**
- RIP là một giao thức IGP để phân phối thông tin định tuyến giữa các router bên trong một AS
- RIP là một giao thức định tuyến vecto khoảng cách
- Mỗi router khởi tạo bảng định tuyến với một danh sách các kết nối trực tiếp với các router gần nhất.
- Mỗi router sẽ flood bảng định tuyến của nó trên toàn AS
- Khi một router nhận được một thông tin từ router khác, nó sẽ update bảng định tuyến của mình để cuối cùng nó đảm bảo rằng có thể biết được tất cả các router khác.
- Trong bảng định tuyến của router, mỗi đích đến có một thuộc tính gọi là metric cost, đó là khoảng cách vecto từ router đến đích.
- Nếu một router có thể chọn nhiều hop để gửi data tới đích, nó sẽ quyết định chọn một hop dựa vào so sánh các metric phải trả khi gửi data.

**IGRP (Interior Gateway Routing Protocol)**
IGRP là giao thức định tuyến dạng classful, nghĩa là không chứa subnet mask trong các thông tin cập nhật định tuyến (routing update). Do không có khả năng mang các thông tin update nên dẫn đến có một vài hạn chế trong các thiết kế mạng dùng giao thức này. Các giao thức nhóm classful gồm RIPv1 và IGRP. Các đặc điểm của một giao thức classful gồm
- Thực hiện quá trình summary ở ranh giới các mạng
- Các routes được trao đổi giữa các mạng được summary theo địa chỉ của IANA.
- Bên trong một network, các lớp mạng con trao đổi với nhau bởi router mà không cần giá trị mask. Do đó giá trị subnet mask phải có cùng giá trị cho tất cả các interface trong cùng mạng.
Nếu có một entry trong bảng định tuyến cho một subnet cụ thể, gói IP sẽ được chuyển về địa chỉ đích đó. Nếu địa chỉ đích là không biết, datagram sẽ bị drop. Nếu ta có cấu hình default-network cho router, default network sẽ được dùng. Tuy nhiên default-network chỉ được dùng trong classful routing nếu router không có kiến thức về mạng đíc ở bất kỳ mức nào. Như vậy nếu major network là biết, gói IP sẽ bị drop cho dù có một mạng default network.
Ở chế độ mặc định, IGRP tính toán metric dựa trên các thông số băng thông (bandwidth) và độ trễ (delay). IGRP có thời gian cập nhật dài hơn RIP, có khả năng hỗ trợ cân bằng tải với metric không bằng nhau. IGRP không hỗ trợ discontiguous network, VLSM.

**EIGRP (Enhanced Interior Gateway Routing Protocol)**
EIGRP là giao thức định tuyến dạng lai giữa distance vector và link state. EIGRP là một phát triển riêng của Cisco nhằm khắc phục các nhược điểm của RIP/IGRP và có những ưu điểm như dễ cấu hình, độ hội tụ nhanh, tiết kiệm tài nguyên mạng khi trao đổi thông tin, sử dụng địa chỉ multicast để liên lạc, khả năng sử dụng hiệu quả băng thông, hỗ trợ VLSM và vấn đề mạng không liên tục (discontiguous network).
Các giao thức định tuyến nhóm classless được thiết kế để khắc phục các hạn chế của định tuyến classful, trong đó bao gồm các đặc điểm sau:
- Không gian địa chỉ được sử dụng hiệu quả
- Hỗ trợ VLSM. Các cổng của router trong cùng một network có thể có các giá trị subnet mask khác nhau
- Hỗ trợ cho việc sử dụng CIDR
- Các route có thể được summary.
EIGRP và IGRP có cùng cách tính metric, tuy nhiên metric của EIGRP bằng metric của IGRP nhân với 256 do IGRP có trường metric là 24 bit trong khi EIGRP có trường metric là 32 bit:
EIGRP Metric = IGRP Metric * 256

**OSPF (Open Shortest Path First)**
- OSPF là giao thức IGP để phân phối các thông tin định tuyến bên trong một mạng AS. OSPF là một giao thức định tuyến trạng thái liên kết.
- Thông tin của topo mạng sẽ được các router tính toán chọn đường đi tốt nhất để gửi data đến đích, thường dựa vào thuật toán Dijkstra.
- Thuận lợi chính của giao thức trạng thái liên kết là các router biết được các thông tin về topo mạng, nên nó có thể tính toán được đường đi tốt nhất mà thõa mãn các yêu cầu đặc biệt.
- Bất lợi của nó là nếu có thêm các router của mạng thì sẽ làm tăng lên số lượng và tần số của bảng tin update và cũng kéo dài thời gian tính toán chọn đường.

**BGP (Border Gateway Protocol)**
- BGP là một giao thức EGP được thiết kết để phân phối thông tin định tuyến giữa các AS.
- BGP là một giao thức định tuyến vecto khoảng cách.
- Bảng định tuyến chứa tất cả các đích mà router biết và địa chỉ hop tiếp theo mà router phải gửi để đến đích cũng như metric cost của con đường đó.
- Nếu một router có thể chọn nhiều hop để gửi data tới đích, nó sẽ quyết định chọn một hop dựa vào so sánh các metric phải trả khi gửi data.

# Lệnh cấu hình các giao thức định tuyến cơ bản

**1. RIP v2**

`router(config)#router rip`

 `router (config-router)#ver 2`
 
 `router (config-router)#net ip-add (major network)`
 
 `router (config-router)#no auto-summary`
 
 **2.OSPF**
 
 Note: Tất cả những router có cùng area phải cấu hình giống nhau tất cả các thông số thì khu vực đó mới hoạt động đúng chức năng được.

- Cấu hình cơ bản

`Router(config)#router ospf process ID (difference)`

`Router(config-router)#network ip-add Wildcard-mask area-ID`

- Cấu hình priority ở các interface để bầu DR và BDR

Priority càng lớn thì khả năng được bầu làm DR càng cao, ngược với bầu Root brige của Switch, càng nhỏ thì lại càng được bầu.

`Router(config)#interface fastethernet 0/0`

`Router(config-if)#ip ospf priority 55`

Sau khi cấu hình xong priority có thể kiểm tra bằng lệnh.

`Router# show ip ospf interface f0/0`

- Chỉnh sửa lại OSPF cost metric trong mỗi interface

Cost càng nhỏ thì tuyến đó càng được coi là best path

`Router(config-if)#ip ospf cost 1`

- Các lệnh show dùng để kiểm tra cấu hình OSPF

`show ip protocol`

`show ip route`

`show ip ospf`

`show ip ospf interface`

`show ip ospf database`

`show ip ospf neighbor detail`

`clear ip route *`

`debug ip ospf events`

`debug ip ospf ad`

**3. EIGRP**

- Cấu hình cơ bản.

`Router(config)#router eigrp As_id`

`Router(config-router)#network network number`

`Router(config-router)#no auto-summary`

- Thay đổi băng thông và tự tổng hợp tuyến trong interface

`Router(config-if)#bandwidth kilobits`

`Router(config-if)#ip summary-address protocol AS network number subnet mask`

- Cân bằng tải trong EIGRP

`Router(config-router)#variance number`

- Quảng bá default route

Cách 1:

`Router(config)#ip route 0.0.0.0 0.0.0.0 [interface/nexthop]`

`Router(config)#redistribute static`

Cách 2:

`Router(config)#ip default-network network number`

Cách 3:

`Router(config-if)#ip summary-network eigrp AS number 0.0.0.0 0.0.0.0`

- Quảng bá các tuyến khác trong EIGRP (không phải là default)

`Router(config-router)#redistribute protocol process ID metrics k1 k2 k3 k4 k5`

Ex: `Router(config-router)#redistribute ospf metrics 100 100 100 100 100`

- Chia sẻ traffic trong EIGRP

`Router(config-router)#traffic share {balanced/min}`

- Các lệnh kiểm tra cấu hình EIGRP

`show ip eigrp neighbor`

`show ip eigrp interface`

`show ip eigrp topology`

`show ip eigrp traffic`

`debug eigrp packet`
# Địa chỉ Ipv4 là gì?

Ipv4 viết tắt cho Internet Protocol Version 4, dịch ra có nghĩa là giao thức Internet phiên bản thứ 4. Ipv4 đã được bộ quốc phòng Hoa Kỳ chuẩn hóa trong bản MIL-STD-1777. Giao thức Internet IP đã trải qua nhiều phiên bản khác nhau và phiên bản Ipv4 là phiên bản đầu tiên được sử dụng rộng rãi trên toàn thế giới và hiện vẫn còn đang là nòng cốt của Internet trên toàn thế giới. Ipv4 là giao thức mang tính hướng dữ liệu và được sử dụng cho hệ thống chuyển mạch gói. Ipv4 không quan tâm đến thứ tự truyền gói tin, cũng không đảm bảo gói tin sẽ đến đích hay là có xảy ra tình trạng lặp gói tin ở đích đến hay không. Nó chỉ có cơ chế đảm bảo tính toàn vẹn dữ liệu bằng việc sử dụng những gói kiểm tra được thiết lập đi kèm với nó. Địa chỉ Ipv4 là 1 địa chỉ đơn nhất đang được sử dụng bởi các thiết bị điện tử hiện nay để nhận diện và liên lạc với nhau trên Internet. Để đánh địa chỉ, Ipv4 sử dụng 32bit và chia ra làm 4 octet (mỗi octet có 8 bit = 1 byte). Dấu chấm được sử dụng để ngăn các octet với nhau.

# Các lớp của địa chỉ IPv4

Ban đầu, 1 địa chỉ Ipv4 được chia ra làm 2 phần là địa chỉ của mạng (Network ID) và địa chỉ của máy (Host ID). Địa chỉ của mạng (Network ID) được xác lập bởi octet đầu tiên và địa chỉ của máy (Host ID) được xác lập cho 3 octet còn lại. Với cách chia này thì địa chỉ của network bị giới hạn ở con số 256. Đây là con số quá ít so với nhu cầu sử dụng thực tế. Vì vậy người ta đã định nghĩa phân lớp mạng để vượt qua giới hạn này và tập hợp thành 1 lớp mạng đầy đủ còn được gọi là classful.

Địa chỉ IP được phân ra thành 5 lớp khác nhau: lớp A, lớp B, lớp C, lớp D,lớp E. Với cách phân loại này sẽ tạo được vô số địa chỉ IPv4 khác nhau.
- Lớp A: Như đã đề cập ở phần trên, địa chỉ Ipv4 được chia ra làm 4 octet. Lớp A của địa chỉ Ipv4 sử dụng octet đầu làm network và 3 Octet sau làm host. Bit đầu tiên của địa chỉ lớp A luôn được chọn là 0. Dải địa chỉ mạng lớp A chạy từ 1.0.0.0 đến 126.0.0.0. Vì vậy lớp A sẽ có tổng cộng 126 mạng. Trong khi đó mạng Loopback là 127.0.0.0. Phần host của lớp A có tất cả 24 bit. Do đó, mỗi lớp A có (224 – 2) host.
![image](https://user-images.githubusercontent.com/55913475/157800373-fc18a3e1-2379-44e4-8a32-ddab71931d23.png)
- Lớp B: Lớp B của địa chỉ Ipv4 sử dụng 2 obtet đầu làm phần mạng và 2 obtet sau làm phần host. Hai bit đầu tiên của lớp B luôn là 1 và 0. Dải địa chỉ mạng lớp B chạy từ 128.0.0.0 đến 191.255.0.0. Như vậy lớp B sẽ có tổng cộng 214 mạng. Vì phần host dài 16 bit nên mạng lớp B có (216 – 2) host.
![image](https://user-images.githubusercontent.com/55913475/157800438-822aaaee-413d-442a-a268-45ea524c1e3c.png)
- Lớp C: Lớp C của địa chỉ Ipv4 dùng 3 octet đầu làm phần mạng và 1 octet sau làm phần host. Địa chỉ lớp C luôn có 3 bit đầu là 1 1 0. Dải mạng lớp C chạy từ 192.0.0.0 -> 223.255.255.0. Như vậy sẽ có 221 mạng trong lớp C. Đối với phần host gồm 1 octet sau cùng nên dài 8 bit và sẽ có (28 – 2) host trong lớp C.
![image](https://user-images.githubusercontent.com/55913475/157800512-52e31f85-bf1c-43da-8e86-a2d8d5740d6c.png)
- Lớp D: Lớp D được sử dụng làm các địa chỉ multicast và dải địa chỉ lớp D từ 224.0.0.0 -> 239.255.255.255.
- Lớp E: Lớp E gồm các giải số từ 240.0.0.0 trở đi và được sử dụng cho mục đích dự phòng.

# Lưu ý của IPv4

- Các địa chỉ của lớp A, lớp B, lớp C của Ipv4 thường được dùng để đặt cho các host.
- Nên quan sát octet đầu tiên của địa chỉ Ipv4 để xác định địa chỉ IP thuộc lớp nào. Nếu octet đầu tiên từ 1 đến 126 thì địa chỉ thuộc lớp A. Nếu octet đầu tiên từ 128 đến 191 thì địa chỉ thuộc lớp B. Nếu octet đầu tiên từ 192 đến 223 thì địa chỉ thuộc lớp C. Nếu octet đầu tiên từ 224 đến 239 thì địa chỉ thuộc lớp D. Cuối cùng, nếu octet đầu tiên từ 240 đến 255 thì địa chỉ thuộc lớp E.

# Hạn chế của IPv4

Hạn chế lớn nhất của Ipv4 là cấu trúc thiết kế của nó không có bất cứ cách thức bảo mật nào cả. Ipv4 cũng hoàn toàn không có phương tiện mã hóa dữ liệu. Vì vậy, lưu lượng truyền tải dữ liệu giữa các host với nhau sẽ không được bảo mật, chỉ được bảo mật phổ biến ở mức ứng dụng mà thôi. Nếu áp dụng phương thức bảo mật phổ biến IPSec tại tầng IP thì mô hình bảo mật chủ yếu là bảo mật lưu lượng giữa các mạng còn việc bảo mật đầu cuối thường sử dụng rất hạn chế. Việc thiếu hụt không gian địa chỉ cũng là 1 trong những hạn chế rất lớn của Ipv4. Để đánh địa chỉ, phiên bản Ipv4 chỉ sử dụng 32bit, do đó không gian của nó chỉ có khoảng 236 địa chỉ. Sự bùng nổ Internet đến thời điểm hiện tại khiến cho tài nguyên Ipv4 được sử dụng gần như là cạn kiện. Vì thế phiên bản này không đủ đáp ứng so với nhu cầu hiện nay. 
# Địa chỉ IPv6 là gì?

IPv6 (Internet Protocol version 6) là phiên bản mới nhất của Giao thức Internet (IP), giao thức truyền thông cung cấp một hệ thống định vị vị trí cho các máy tính trên mạng và định tuyến lưu lượng trên Internet. Trong thời đại Internet bùng nổ và trở nên phổ biến, lượng địa chỉ IPv4 ngày càng cạn kiệt, bộc lộ các hạn chế đối với việc phát triển các loại hình dịch vụ hiện đại trên Internet, không đáp ứng đủ nhu cầu người dùng. Được IETF tạo ra để thay thế và khắc phục những lỗi của IPv4,  IPv6  ra đời.

# Phân loại địa chỉ IPv6

Một địa chỉ IPv6 có thể được phân thành 1 trong 3 loại như sau:
- Unicast
Một địa chỉ unicast được định nghĩa duy nhất trên một cổng của một node IPv6. Một gói tin được gởi đến một địa chỉ unicast được đưa đến cổng được định nghĩa bởi địa chỉ đó.
- Multicast
Một địa chỉ multicast định nghĩa một nhóm các cổng IPv6. Một gói tin gởi đến địa chỉ multicast được xử lý bởi tất cả những thành viên của nhóm multicast.
- Anycast
Một địa chỉ anycast được đăng kí cho nhiều cổng (trên nhiều node). Một gói tin được gởi đến một địa chỉ anycast là được chuyển đến chỉ một trong số các cổng này.

# Cấu trúc của địa chỉ IPv6

Vẫn giữ đặc trưng là một chuỗi tập hợp của các con số có giới hạn, được sắp xếp thành 1 dãy số có quy luật, địa chỉ IPv6  có chiều dài ấn tượng:128bit. Địa chỉ IPv6 được biểu diễn dưới dạng các cụm số hexa được ngăn thành 8 phần, mỗi phần có chiều dài 16bit và được ngăn bởi dấu “:”. Với 128 bit chiều dài, không gian địa chỉ IPv6 gồm 2128 địa chỉ, cung cấp một lượng địa chỉ khổng lồ cho hoạt động Internet.

# Ưu điểm của địa chỉ IPv6

- Không gian địa chỉ lớn hơn và dễ dàng quản lý hơn: Tăng từ 32bit lên 128bit.
- Header của giao thức được cải tiến: Cải thiện hiệu suất chuyển tiếp gói tin.. Khôi phục lại nguyên lý kết nối đầu cuối-đầu cuối của Internet và loại bỏ hoàn toàn công nghệ NAT
- Quản trị TCP/IP dễ dàng hơn:  IPv6 được thiết kế với khả năng tự động cấu hình mà không cần sử dụng máy chủ DHCP, hỗ trợ nhiều trong việc giảm cấu hình thủ công.
- Cấu trúc định tuyến tốt hơn: Định tuyến IPv6 được thiết kế hoàn toàn phân cấp. Khả năng QoS (Quality of service) giúp đánh dấu QoS cho các gói tin và dán nhãn để giúp xác định những traffic cần được ưu tiên.
- Hỗ trợ tốt hơn Multicast: Tăng cường sử dụng truyền thông một chiều hiệu quả.
- Hỗ trợ bảo mật tốt hơn: Mã hóa và xác thực truyền thông.
- Tính di động: Dễ dàng hơn khi xử lý với thiết bị di động hay chuyển vùng
- Jumbograms: Hỗ trợ các packet payload cực lớn cho hiệu quả cao hơn.
- Anycast: Dịch vụ dự phòng sử dụng những địa chỉ không có cấu trúc đặc biệt.

# Sự khác biệt giữa địa chỉ IPv4 và địa chỉ IPv6

- IPv6 có triển khai IP Security (IPSec) để tăng bảo mật. Nhưng công nghệ này cũng có triển khai và tích hợp hoàn toàn vào IPv4 tùy thuộc vào đơn vị IPS.
- Về địa chỉ: IPv4 32Bit trong khi IPv6 có đến 128Bit.
- Địa chỉ IPv4 chỉ đánh số, trong khi đó, IPv6 có cả chữ và số
- IPv4 tách nhị phân bằng dấu chấm (.), IPv6 lại tách bằng dấu 2 chấm (:)
- Header của IPv4 là 12 trường còn của IPv6 chỉ 8 trường
- IPv4 sử dụng ARP (Address Resolution Protocol) để ánh xạ đến địa chỉ MAC, trong khi IPv6 sử dụng NDP (Neighbour Discovery Protocol) để ánh xạ đến MAC.
# 1. ARP là gì?

– ARP là phương thức phân giải địa chỉ động giữa địa chỉ lớp network và địa chỉ lớp datalink. Quá trình thực hiện bằng cách: một thiết bị IP trong mạng gửi một gói tin local broadcast đến toàn mạng yêu cầu thiết bị khác gửi trả lại địa chỉ phần cứng ( địa chỉ lớp datalink ) hay còn gọi là Mac Address của mình.

– ARP là giao thức lớp 2 – Data link layer trong mô hình OSI và là giao thức lớp Link layer trong mô hình TCP/IP.

– Ban đầu ARP chỉ được sử dụng trong mạng Ethernet để phân giải địa chỉ IP và địa chỉ MAC. Nhưng ngày nay ARP đã được ứng dụng rộng rãi và dùng trong các công nghệ khác dựa trên lớp hai.

# 2. Hoạt động của ARP trong mạng LAN

   - Bước 1: Máy gửi kiểm tra cache của mình. Nếu đã có thông tin về sự ánh xạ giữa địa chỉ IP và địa chỉ MAC thì chuyển sang Bước 7.

   - Bước 2: Máy gửi khởi tạo gói tin ARP request với địa chỉ SHA và SPA là địa chỉ của nó, và địa chỉ TPA là địa chỉ IP của máy cần biết MAC. (Trường THA để giá trị toàn 0 để biểu hiện là chưa tìm được địa chỉ MAC)

   - Bước 3: Gửi quảng bá gói tin ARP trên toàn mạng (Địa chỉ MAC đích của gói tin Ethernet II là địa chỉ MAC quảng bá ff:ff:ff:ff:ff:ff).

   - Bước 4: Các thiết bị trong mạng đều nhận được gói tin ARP request. Gói tin được xử lý bằng cách các thiết bị đều nhìn vào trường địa chỉ Target Protocol Address.

  Thiết bị với IP trùng với IP trong trường Target Protocol Address sẽ bắt đầu quá trình khởi tạo gói tin ARP Reply bằng cách lấy các trường Sender Hardware Address và Sender Protocol Address trong gói tin ARP nhận được đưa vào làm Target trong gói tin gửi đi. Đồng thời thiết bị sẽ lấy địa chỉ MAC của mình để đưa vào trường Sender Hardware Address. Đồng thời cập nhất giá trị ánh xạ địa chỉ IP và MAC của máy gửi vào bảng ARP cache của mình để giảm thời gian xử lý cho các lần sau.

  - Bước 5: Thiết bị đích bắt đầu gửi gói tin Reply đã được khởi tạo đến thiết bị nguồn vừa gửi bản tin ARP request. Gói tin reply là gói tin gửi unicast.

  - Bước 6: Thiết bị nguồn nhận được gói tin reply và xử lý bằng cách lưu trường Sender Hardware Address trong gói reply như địa chỉ phần cứng của thiết bị đích cần tìm.

  - Bước 7: Thiết bị nguồn update vào ARP cache của mình giá trị tương ứng giữa địa chỉ IP và địa chỉ MAC của thiết bị đích. Lần sau sẽ không còn cần tới ARP request.

# 3. Hoạt động của ARP trong môi trường liên mạng

  Hoạt động của ARP trong một môi trường phức tạp hơn đó là hai hệ thống mạng gắn với nhau thông qua một Router.

Do các broadcast lớp MAC không thể truyền qua Router nên khi đó máy A sẽ xem Router C như một cầu nối hay một trung gian (Agent) để truyền dữ liệu. Trước đó, máy A sẽ biết được địa chỉ IP của Router C (địa chỉ Gateway) và biết được rằng để truyền gói tin tới B phải đi qua C.

Để tới được router C thì máy A phải gửi gói tin tới port X của router C (là gateway trong LAN A). Quy trình truyền dữ liệu được mô tả như sau:
   
   Máy A gửi ARP request để tìm MAC của port X.

   Router C trả lời, cung cấp cho A địa chỉ MAC của port X.

   Máy A truyền gói tin tới port X của router C (với địa chỉ MAC đích là MAC của port X, IP đích là IP máy B).

   Router C nhận được gói tin của A, forward ra port Y. Trong gói tin có chứa địa chỉ IP máy B, router C sẽ gửi ARP request để tìm MAC của máy B.

  Trên thực tế ngoài dạng bảng định tuyến này người ta còn dùng phương pháp proxy ARP (sẽ tìm hiểu phần sau), trong đó có một thiết bị đảm nhận nhiệm vụ phân giải địa chỉ cho tất cả các thiết bị khác. Theo đó các máy trạm không cần giữ bảng định tuyến nữa Router C sẽ có nhiệm vụ thực hiện, trả lời tất cả các ARP request của tất cả các máy.

# 4. Các bản tin ARP
    
   - ARP probe: Đây là loại bản tin ARP dùng để máy thăm dò xem địa chỉ mà máy được cấp phát (cấu hình manual hoặc DHCP, …) có bị trùng với địa chỉ IP của máy nào trong cùng mạng hay không. Khi mới ban đầu, các máy đều thực hiện broadcast bản tin ARP này.

   - Bản tin này có cấu trúc địa chi IP của máy gửi là 0.0.0.0 (thể hiện máy gửi bản tin này chưa xác định IP, đồng thời cũng là để các máy khác trong mạng không cập nhật MAC của máy vào ARP caching – vì nó chưa được gán IP cụ thể nào)

   - Địa chỉ MAC đích là 00:00:00:00:00:00

   - Địa chỉ IP đích là địa chỉ IP mà máy gửi được cấp phát.

   - Thông thường bản tin ARP request này sẽ không có reply.

   - ARP announcements: ARP cũng sử dụng một cách đơn giản để thông báo tới các máy trong mạng khi địa chỉ IP hoặc địa chỉ MAC của nó thay đổi. Đó chính là bản tin gratuitous ARP

   - Bản tin Gratuitous ARP được gửi broadcast request trong mạng với địa chỉ MAC và IP máy gửi là địa chỉ sau khi thay đổi.

   - Địa chỉ MAC đích là 00.00.00.00.00.00. Địa chỉ IP đích là chính nó. Điều này đảm bảo các máy trong mạng khi nhận được bản tin này sẽ chỉ cập nhật địa chỉ MAC và IP của máy gửi vào trong ARP caching của mình => không có bản tin reply cho bản tin này.

   - ARP request: Là bản tin ARP request mà máy gửi gửi broadcast để tìm địa chỉ MAC của máy nhận.

   - Địa chỉ MAC và IP gửi là địa chỉ của máy gửi.

   - Địa chỉ MAC nhận được set là 0 hết.

   - Địa chỉ IP nhận là địa chỉ IP của máy cần tìm.

   - ARP reply: Là bản tin mà máy nhận sau khi nhận được ARP request sẽ đóng gói lại MAC của mình và gửi bản tin reply về cho máy gửi.

   - Nó sẽ đóng gói là địa chỉ IP và MAC của mình vào địa chỉ SHA và PHA.

   - Địa chỉ mà máy gửi gửi tới nó sẽ được đóng gói và phần địa chỉ THA và TPA.

   - Gửi bản tin unicast.
    
 # 5. ARP Caching
  
  ARP là một giao thức phân giải địa chỉ động. Quá trình gửi gói tin Request và Reply sẽ tiêu tốn băng thông mạng. Chính vì vậy càng hạn chế tối đa việc gửi gói tin Request và Reply sẽ càng góp phần làm tăng khả năng họat động của mạng. Từ đó sinh ra nhu cầu của ARP Caching. ARP Cache có dạng giống như một bảng tương ứng giữa địa chỉ hardware và địa chỉ IP.
(Trong Window: dùng câu lệnh arp -a trong Command Prompt để show ra ARP cache trong máy)
# 1. DHCP là gì?

DHCP (Dynamic Host Configuration Protocol hay Giao thức cấu hình host động) là một giao thức được sử dụng để cung cấp quản lý nhanh chóng, tự động và tập trung cho việc phân phối địa chỉ IP trong mạng. DHCP cũng được sử dụng để cấu hình đúng subnet mask, cổng mặc định và thông tin về DNS server trên thiết bị.

# 2. Các thành phần của DHCP

Khi làm việc với DHCP, bạn cần hiểu tất cả thành phần của nó. Dưới đây là danh sách các thành phần của DHCP.

   - DHCP server: Một thiết bị mạng chạy dịch vụ DHCP chứa địa chỉ IP và thông tin cấu hình liên quan. Đây thường là máy chủ hoặc router nhưng có thể là bất cứ thứ gì hoạt động như máy chủ chẳng hạn như thiết bị SD-WAN.
   - DHCP client: Thiết bị nhận thông tin cấu hình từ máy chủ DHCP. Đây có thể máy tính, thiết bị di động, thiết bị IoT (Internet of Things) hoặc bất cứ thiết bị gì khác yêu cầu kết nối mạng. Hầu hết các thiết bị này được cấu hình để nhận thông tin DHCP theo mặc định.
   - IP address pool: Dãy địa chỉ có sẵn cho client DHCP. Những địa chỉ này thường được truyền tuần tự từ thấp nhất đến cao nhất.
   - Subnet: Mạng IP có thể được phân thành các phân đoạn được gọi là subnet (mạng con). Mạng con giúp mạng được quản lý dễ dàng hơn.
   - Lease: Khoảng thời gian client DHCP giữ thông tin địa chỉ IP. Khi khoảng thời gian này hết hạn, client phải làm mới nó.
   - DHCP relay: Router hoặc máy chủ nghe tin nhắn được phát trên mạng đó và sau đó chuyển chúng đến một máy chủ được cấu hình. Máy chủ này sau đó phản hồi lại relay agent để truyền chúng đến client. Nó được sử dụng để tập trung máy chủ DHCP thay vì để máy chủ trên mỗi mạng con.

# 3. Nguyên lý hoạt động của DHCP

Thành phần chính của DHCP bao gồm 4 bản tin:

   - DISCOVERY
   - OFFER
   - REQUEST
   - ACK
    
Quá trình cấp phát địa chỉ IP trong giao thức DHCP bao gồm các bước sau:

![image](https://user-images.githubusercontent.com/55913475/157590268-35b0df36-748b-40e8-b9d3-e87639d35b3f.png)

Kịch bản client xin cấp DHCP từ modem

   - Bước 1: Khi muốn có địa chỉ IP để truy cập vào internet thì client sẽ tạo ra bản tin DISCOVERY để yêu cầu cấp phát địa chỉ IP
   - Bước 2: Client chưa biết địa chỉ chính xác của Server cấp phát địa chỉ cho mình do đó nó sẽ gửi bản tin này dưới dạng broadcast.
   - Bước 3: Server sẽ nhận bản tin DISCOVERY của client. Sau khi biết client muốn được cấp địa chỉ IP nó sẽ kiểm tra xem địa chỉ IP nào phù hợp để cấp cho client sử dụng
   - Bước 4: Server tạo bản tin OFFER. Gói tin này sẽ lưu trữ thông tin về IP và các thông số cấu hình khác mà client yêu cầu để có thể sử dụng để truy cập internet
   - Bước 5: Tất cả các server sẽ gửi bản OFFER dưới dạng broadcast
   - Bước 6: Client nhận gói OFFER và nó sẽ chọn ra bản OFFER đầu tiên mà nó nhận được. Nếu không nhận được OFFER nào trong một khoảng thời gian nào đó thì nó sẽ gửi lại DISCOVERY một lần nữa
   - Bước 7: Client tạo ra gói REQUEST. Và gửi dưới dạng broadcast tới tất cả các server. Server nào được nhận OFFER sẽ mang ý nghĩa là nó đồng ý nhận IP. Server nào không được nhận OFFER thì thông báo là không nhận OFFER đó
   - Bước 8: Server nhận bản tin REQEST. Các server không được nhận OFFER sẽ bỏ qua gói tin này. Gói tin nào được nhận OFFER sẽ nhận và xử lý nó. Nó sẽ kiểm tra sem IP này còn sử dụng được hay không. Nếu còn sử dụng được thì nó sẽ ghi lại thông tin và gửi lại gói tin PACK cho client. Còn nếu không thì nó sẽ gửi lại PNAK để quay lại bước 1.
    
 # 4. Ưu điểm khi sử dụng DHCP

   - Tập trung quản trị thông tin cấu hình host
   - Cấu hình động các máy
   - Cấu hình IP cho các máy một cách liền mạch.
   - Sự linh hoạt
   - Đơn giản hóa vài trò quản trị của việc cauas hình địa chỉ IP của client.
   - Sự linh hoạt
    
 # 5. Rủi ro bảo mật của DHCP
 
 Giao thức DHCP không yêu cầu xác thực để bất kỳ client nào cũng có thể tham gia mạng một cách nhanh chóng. Do đó, nó có nhiều vấn đề về bảo mật như máy chủ trái phép đưa thông tin xấu cho client, client trái phép được cấp địa chỉ IP, v.v… Bởi vì client không có cách nào để xác thực tính hợp lệ của máy chủ DHCP, do đó máy chủ có thể cung cấp thông tin mạng không chính xác. Điều này có thể gây ra các cuộc tấn công từ chối dịch vụ (denial-of-service attack) hoặc tấn công man-in-the-middle sử dụng máy chủ giả để chặn dữ liệu có thể được sử dụng với mục đích xấu. Ngược lại, bởi vì máy chủ DHCP không xác thực client, do đó nó sẽ phát thông tin địa chỉ IP đến bất cứ thiết bị nào yêu cầu. Ai đó có thể cấu hình client để liên tục thay đổi thông tin đăng nhập và nhanh chóng làm cạn kiệt địa chỉ IP có sẵn trong phạm vi, ngăn các thiết bị truy cập vào mạng. Thông số DHCP có thể giải quyết được một số vấn đề kể trên. Tùy chọn Relay Agent Information Option cho phép kỹ sư mạng gắn thẻ thông điệp DHCP khi chúng đến mạng. Thẻ này được sử dụng để kiểm soát truy cập mạng. Ngoài ra, còn có một điều khoản để xác thực thông điệp DHCP. Việc sử dụng xác thực 802.1x còn được gọi là kiểm soát truy cập mạng (NAC) được sử dụng để bảo mật DHCP. Hầu hết các nhà cung cấp mạng hàng đầu đều hỗ trợ NAC.
 # 1. DNS là gì?

DNS viết tắt của Domain Name System có nghĩa là hệ thống phân giải tên miền. DNS là hệ thống cho phép thiết lập tương ứng giữa địa chỉ IP và tên miền trên Internet. DNS được phát minh vào năm 1984 cho Internet và đây là một trong số các chuẩn công nghiệp của các cổng bao gồm cả TCP/IP. Hệ thống phân giải tên miền chính là chìa khóa chủ chốt của nhiều dịch vụ mạng hiện nay như Internet, Mail server, Web server… Mỗi máy tính khi kết nối vào Internet sẽ được gán cho 1 địa chỉ IP riêng biệt và không trùng lẫn với bất kỳ máy tính nào khác trên thế giới. Cũng giống như vậy đối với website cũng có địa chỉ IP riêng biệt của website đó. Nói cách khác, DNS cũng giống như một danh bạ điện thoại dành riêng cho Internet. Nếu bạn biết tên của một người nhưng không biết số điện thoại hay ngược lại, bạn có thể tham khảo trong sổ danh bạ dễ dàng.

# 2. Cách thức hoạt động của DNS

DNS hoạt động theo từng bước theo cấu trúc của DNS. Bước đầu tiên gọi là DNS query, một truy vấn để lấy thông tin. Sử dụng tình huống tìm kiếm website bằng cách gõ tên miền vào trong web browser (ví dụ, www.google.com). Đầu tiên, DNS server sẽ tìm thông tin phân giải trong filehosts – một file text trong hệ điều hành chịu trách nhiệm chuyển hostname thành địa chỉ IP. Nếu không thấy thông tin, nó sẽ tìm trọng cache – bộ nhớ tạm của phần cứng hay phần mềm. Nơi phổ biến nhất lưu thông tin cache này là  bộ nhớ tạm của trình duyệt và bộ nhớ tạm của Internet Service Providers (ISP). Nếu không nhận được thông tin, bạn sẽ thấy mã lỗi hiện lên. Tổng cộng có khoảng 4 loại server tham gia vào trong hệ thống phân giải tên miền:
  # DNS Recursor
DNS recursor là server đóng vai trò liên lạc với các server khác để thay nó làm nhiệm vụ phản hồi cho client (trình duyệt người dùng). Nó như một nhân viên cần mẫn nhận nhiệm vụ lấy và trả thông tin cho client (trình duyệt) để tìm đúng thông tin chúng cần. Để lấy được thông tin, DNS recursor có thể sẽ cần gọi đến Root DNS Server để trợ giúp.
  # Root Nameserver
Root DNS Server, cũng thường được gọi là nameserver, là server quan trọng nhất trong hệ thống cấp bậc của DNS. Nó không có tên cụ thể. Bạn có thể hiểu nó là một thư viện để định hướng tìm kiếm giúp bạn. Trên thực tế, DNS recursive resolver sẽ chuyển yêu cầu tới Root Nameserver. Sau đó, server này sẽ phản hồi rằng nó cần tìm trong các top-level domain name servers (TLD nameserver) cụ thể nào.
  # TLD Nameserver
Khi bạn muốn truy cập Google hay Facebook, thường phần mở rộng của bạn sẽ dùng là .com. Nó là một trong các top-level domain. Server cho loại top-level domain này gọi là TLD nameserver. Nó chịu trách nhiệm quản lý toàn bộ thông tin của một phần mở rộng tên miền chung. Ví dụ như khi bạn gõ www.google.com trên trình duyệt, TLD .com sẽ phản hồi từ một DNS resolver để giới thiệu cho nó một Authoritative DNS server. Authoritative Name Server là nơi chính thức chứa nguồn dữ liệu của tên miền đó.
  # Authoritative Nameserver
Khi một DNS resolver tìm thấy một authoritative nameserver, đây là việc phân giải tên miền diễn ra. Authoritative nameserver có chứa thông tin tên miền gắn với địa chỉ nào. Nó sẽ đưa cho recursive resolver địa chỉ IP cần thiết tìm thấy trong danh mục các bản ghi của nó.

# 3. Các loại DNS bản ghi DNS thường sử dụng
 
 - CNAME Record: Là một bản ghi tên quy chuẩn (Canonical Name Record). Đây là một dạng bản ghi tài nguyên trong hệ thống tên miền.
 - A Record: Dùng để trỏ tên miền website tới một địa chỉ IP cụ thể. Đây được xem là bản ghi DNS đơn giản nhất.
 - MX Record: Bản ghi này bạn có thể sử dụng để trỏ tên miền đến mail server. MX Record chỉ định server nào quản lý các dịch vụ Email của tên miền đó.
 - AAAA Record: Dùng để trỏ tên miền đến địa chỉ IPv6 và cho phép thêm host mới, TTL và IPv6.
 - TXT Record: Ngoài ra, có thể thêm giá trị TXT, Host mới, TTL và Point To để chứa các thông tin định dạng văn bản domain.
 - SRV Record: Đây là bản ghi DNS đặc biệt, dùng để xác định chính xác dịch vụ nào đang chạy Port nào. Và thông qua bản ghi này bạn có thể thêm Priority, Port, Weight, TTL, Point to.
 - NS Record: Bản ghi này có thể chỉ định Name Server cho từng tên miền phụ và bên cạnh đó có thể tạo tên Name Server, TTL hay host mới.

# 4. Các loại DNS Server
  
  - Root Name Server
Root Name Server là một dịch vụ phân giải tên miền gốc và trên thế giới có khoảng 12 DNS root Server. DNS root Server quản lý tất cả các tên miền Top-level. Khi có yêu cầu phân giải một Domain Name thành một địa chỉ IP, client sẽ gửi yêu cầu đến DNS gần nhất (DNS ISP). DNS ISP sẽ kết nối tới DNS root Server để hỏi địa chỉ của Domain Name. DNS root Server sẽ căn cứ và dựa vào các Top Level của tên miền và từ đó có những tài liệu hướng dẫn phù hợp để chuyển hướng cho khách hàng đến đúng địa chỉ cần truy vấn.
 - Local Name Server
DNS Server này dùng để chứa thông tin để truy xuất và tìm kiếm máy chủ tên miền. Và thường được duy trì và phát triển bởi các doanh nghiệp hay các nhà cung cấp dịch vụ Internet.

# 5. Các loại truy vấn DNS

Trong một truy vấn DNS thông thường, ba loại truy vấn xảy ra. Bằng cách sử dụng kết hợp các truy vấn này. Một quy trình được tối ưu hóa cho quá trình phân giải DNS có thể giúp giảm khoảng cách di chuyển. Trong một tình huống lý tưởng, dữ liệu bản ghi được lưu trong bộ nhớ cache sẽ khả dụng, cho phép máy chủ định danh DNS trả về truy vấn không đệ quy.

3 loại truy vấn DNS:

  - Recursive query: DNS client yêu cầu máy chủ DNS (thường là recursive DNS resolver). Sẽ trả lời máy khách bằng bản ghi tài nguyên được yêu cầu. Hoặc thông báo lỗi nếu resolver không thể tìm thấy bản ghi.
  - Iterative query: Trong tình huống này, DNS client sẽ cho phép máy chủ DNS trả về câu trả lời tốt nhất có thể. Nếu máy chủ DNS được truy vấn không có kết quả trùng khớp với tên truy vấn. Nó sẽ trả về một giới thiệu đến máy chủ DNS có thẩm quyền cho mức thấp hơn. DNS client sau đó sẽ thực hiện một truy vấn đến địa chỉ được giới thiệu. Quá trình này tiếp tục với các máy chủ DNS bổ sung trong chuỗi truy vấn cho đến khi xảy ra lỗi hoặc hết thời gian.
  - Non-recursive query: Thông thường điều này sẽ xảy ra khi DNS resolver client truy vấn máy chủ DNS một record mà server có quyền truy cập hoặc bản ghi tồn tại bên trong bộ đệm của server. Thông thường, một máy chủ DNS sẽ lưu các bản ghi DNS để ngăn chặn việc tiêu thụ thêm băng thông và giảm tải cho các máy chủ DNS khác.

# 6. Nguyên nhân DNS dễ bị tấn công?

Vì hệ thống tên miền khá phức tạp và người tấn công có thể tận dụng điểm yếu trong DNS để tấn công với nhiều phương thức khác nhau. Đa số các cuộc tấn công đều tập trung vào việc lạm dụng DNS để ngăn người dùng không thể truy cập vào Internet. Bên cạnh đó, DNS cũng có thể bị tấn công bằng phướng pháp tận dụng giao thức DNS để chuyển hướng người dùng truy cập vào các trang web độc hại nhằm đánh cắp dữ liệu nhạy cảm của cá nhân, doanh nghiệp. Ngoài ra, việc sử dụng server đệ quy sẽ lưu phản hồi vào bộ nhớ tạm để tăng tốc độ của các truy vấn tiếp theo. Nhằm giảm số lượng request thông tin, nhưng khá nguy hiểm và dễ bị tấn công bởi Man-In-The-Middle. Những kẻ tấn công có thể truy cập vào Over IP (VoIP) để đánh cắp thông tin, mạo danh, trích xuất dữ liệu, thông tin,….
# 1. Tổng quan về FTP
  - FTP(viết tắt của File Transfer Protocol) là một giao thức truyền tải tập tin từ máy tính này đến máy tính khác thông qua một mạng TCP hoặc qua mạng Internet. Nhờ vào giao thức này nên người sử dụng có thể tải dữ liệu như hình ảnh, văn bản, các tập tin nhạc, video... từ máy tính của mình lên máy chủ đang đặt ở một nơi khác hoặc tải các tập tin đã có trên máy chủ về máy tính cá nhân của mình một cách dễ dàng. FTP cũng là giao thức dùng để truyền tải dữ liệu web lên máy chủ web cho dù máy chủ đặt rất xa.
  - Được sử dụng để trao đổi tập tin qua mạng lưới truyền thông sử dụng TCP/IP (internet, mạng nội bộ, …). Sử dụng để tải xuống máy tính các file từ máy chủ. Mặc dù việc truyền file từ hệ thống này sang hệ thống khác rất đơn giản và dễ hiểu, nhưng đôi khi xảy ra những vấn đề khác nhau. Ví dụ, 2 hệ thống có thể có các quy ước tập tin khác nhau, 2 hệ thống có các cách khác nhau để thể hiện văn bản và dữ liệu hay 2 hệ thống có cấu trúc thư mục khác nhau, … Giao thức FTP khắc phục những vấn đề này bằng cách thiết lập 2 kết nối giữa các máy chủ. Một kết nối để sử dụng truyền dữ liệu, 1 kết nối còn lại được sử dụng để điều khiển kết nối.

# 2. Mô hình của FTP

  - Mô hình và nguyên lí hoạt động của FTP:
 
 ![image](https://user-images.githubusercontent.com/55913475/157581009-ac968f2a-c8ca-4271-b04c-6ad7f4a4b12c.png)
 
 Giống như hầu hết các giao thức TCP/IP, FTP dựa trên mô hình Client – Server. Tuy nhiên, khác với các ứng dụng khác chạy trên nền TCP/IP, FTP cần tới 2 kết nối TCP:

  + Control connection (sử dụng port 21 – trên server): Đây là kết nối TCP logic chính được tạo ra khi phiên làm việc được thiết lập. Nó được thực hiện giữa các quá trình điều khiển. Nó được duy trì trong suốt phiên làm việc và chỉ cho các thông tin điều khiển đi qua như lệnh hay response(phản hồi)
  + Data connection (sử dụng port 20 – trên server): Kết nối này sử dụng các quy tắc rất phức tạp vì các loại dữ liệu có thể khác nhau. Nó được thực hiện giữa các quá trình truyền dữ liệu. Kết nối này mở khi có lệnh chuyển tệp và đóng khi tệp truyền xong.

  - Mô hình FTP

Sơ đồ minh họa:

![image](https://user-images.githubusercontent.com/55913475/157581186-f55ae2dc-5bc0-446f-88f5-0cf200a313a3.png)

Do chức năng điều khiển và dữ liệu được truyền tải bằng cách sử dụng các kênh riêng biệt nên mô hình FTP chia mỗi thiết bị thành 2 phần giao thức logic chịu trách nhiệm cho mỗi kết nối ở trên:

   + Protocol interpreter (PI): Là thành phần quản lý kênh điều khiển, phát và nhận lệnh và trả lời.
   + Data transfer process (DTP): chịu trách nhiệm gửi và nhận dữ liệu giữa client và server.

 # 3. Chức năng từng phần trong mô hình FTP
 
 Phía Server

  - Server Protocol Interpreter (Server-PI) : Chịu trách nhiệm quản lí Control Connection trên Server. Nó lắng nghe yêu cầu kết nối hướng từ User trên cổng 21. Khi kết nối được thiết lập, nó nhận lệnh từ User-PI, gửi phản hồi và quản lí tiến trình truyền dữ liệu trên Server.
  - Server Data Transfer Process (Server-DTP) : chịu trách nhiệm nhận và gửi file từ User-DTP. Server-DTP vừa làm nhiệm vụ thiết lập Data Connection và lắng nghe Data Connection của User thông qua cổng 20. Nó tương tác với Server File System trên hệ thống cục bộ để đọc và chép file.

Phía Client

  - User Interface: Đây là chương trình được chạy trên máy tính, nó cung cấp giao diện xử lí cho người dùng, chỉ có trên phía Client. Nó cho phép người dùng sử dụng những lệnh đơn giản để điều khiển các session FTP, từ đó có thể theo dõi được các thông tin và kết quả xảy ra trong quá trình.
  - User Protocol Interpreter (User-PI): Chịu trách nhiệm quản lí Control Connection phía Client. Nó khởi tạo phiên kết nối FTP bằng việc phát hiện ra Request tới Server-PI. Sau khi kết nối được thiết lập, nó xử lí các lệnh nhận được trên User Interface, gửi chúng tới Server-PI rồi đợi nhận Response trở lại. Nó cũng quản lí các tiến trình trên Client.
  - User Data Transfer Process (User-DTP): Có nhiệm vụ gửi hoặc nhận dữ liệu từ Server-DTP. User-DTP có thể thiết lập hoặc lắng nghe DataConnection từ Server thông qua cổng 20. Nó tương tác với Client File System trên Client để lưu trữ file.

# 4. Nguyên lí hoạt động của FTP

Cần có 2 kết nối TCP trong phiên làm việc của FTP: TCP Data connection trên cổng 20, TCP Control connection trên cổng 21.

  - Control connection : luôn được mở ở mọi thời điểm khi dữ liệu hoặc lệnh được gửi.
  - Data connection : chỉ được mở khi có trao đổi dữ liệu thực.

Trình tự chung của FTP hoạt động như sau:

  1. FTP Client mở Control connection đến FTP server (trên port 21) và chỉ định 1 cổng trên Client để Server gửi lại phản hồi. Đường kết nối này dùng để truyền lệnh và không phải là dữ liệu. Control connection sẽ mở trong suốt thời gian của phiên làm việc (telnet giữa 2 hệ thống)
  2. Client chuyển tiếp thông tin như username, password tới Server để thực hiện xác thực (authentication). Server sẽ trả lời bằng mã chấp nhận hay từ chối của các request.
  3. Client gửi thêm các lệnh với tên tệp, kiểu dữ liệu, … để vận chuyển, thêm luồng dữ liệu(tức là chuyển tập tin từ máy khách đến máy chủ hoặc ngược lại). Server sẽ phản hồi với mã (reply code) chấp nhận hoặc từ chối.
  4. Khi dữ liệu đã sẵn sàng, 2 bên sẽ mở kết nối TCP trên cổng 20.
  5. Dữ liệu có thể được vận chuyển giữa Client và Server trên cổng 20. Dữ liệu vận chuyển được mã hóa theo 1 số định dạng bao gồm NVT-ASCII hoặc nhị phân(binary)
  6. Khi quá trình vận chuyển dữ liệu được hoàn thành, phiên làm việc của FTP Server sẽ đóng lại Data Connection trên cổng 20. Nhưng vẫn giữ Control Connection trên công 21.
  7. Control connection có thể được sử dụng để thiết lập truyền dữ liệu khác hoặc đóng liên kết.

# 5. FTP reply
Mỗi lần User-PI gửi lệnh đến Server-PI qua Control connection, server sẽ gửi lại phản hồi dưới dạng các code. Code reply nhằm các mục đích sau:

  - Xác nhận máy chủ đã nhận được lệnh.
  - Cho biết lệnh từ phía người dùng có được chấp nhận hay không, nếu xảy ra lỗi thì đó là lỗi gì.
  - Cho biết nhiều thông tin khác nhau cho người dùng về phiên, ví dụ như là: tình trạng truyền file, …

# 6. Tính bảo mật của FTP

Giống như phần lớn các giao thức cũ, phương pháp đăng nhập đơn giản của FTP là một sự kế thừa từ những giao thức ở thời kì đầu của Internet. Ngày nay, nó không còn đảm bảo tính an toàn cần thiết trên môi trường Internet toàn cầu vì username và password được gửi qua kênh kết nối điều khiển dưới dạng clear text(không mã hóa). Điều này làm cho bảo mật FTP đã định ra thêm nhiều tùy chọn chứng thực và mã hóa phức tạp cho những ai muốn tăng thêm mức độ an toàn vào trong phần mềm FTP của họ.

# 7. Kênh dữ liệu trong FTP
Kênh điều khiển được tạo ra giữa Server-PI và User-PI, sử dụng quá trình thiết lập kết nối và chứng thực được duy trì trong suốt phiên kết nối FTP. Các lệnh và các hồi đáp được trao đổi giữa bộ phận PI (Protocol Interpreter) qua kênh điều khiển, những dữ liệu thì không. Mỗi khi cần phải truyền dữ liệu giữa các server và client, một kênh dữ liệu cần phải được tạo ra. Kênh dữ liệu kết nối bộ phận User-DTP và Server-DTP. Kết nối này cần thiết cho cả hoạt động truyền file trực tiếp (gửi hoặc nhận một file) cũng như đối với việc truyền dữ liệu ngầm, như là yêu cầu một danh sách file trong thư mục nào đó trên server. Để tạo ra kênh dữ liệu, FTP sử dụng 2 phương thức khác nhau: Normal (Active) Data Connections (mặc định) và Passive Data Connections. Khác biệt giữa 2 phương thức này là phía Client hay bên Server đưa ra yêu cầu khởi tạo kết nối.
  - Normal (Active) Data Connections
Phương thức tạo kết nối dữ liệu bình thường hay còn gọi là Kết nối kênh dữ liệu ở dạng chủ động. Phía Server-DTP tạo kênh dữ liệu bằng cách mở một cổng kết nối tới User-DTP. Server sử dụng cổng đặc biệt được dành riêng cho kết nối dữ liệu là cổng số 20. Trên máy Client, cổng mặc định được sử dụng chính là cổng được sử dụng để kết nối điều khiển, nhưng Server sẽ thường chọn mỗi cổng khác nhau cho mỗi chuyển giao.
  - Passive Data Connections
Phương thức tạo kết nối bị động. Server sẽ chấp nhận 1 yêu cầu kết nối dữ liệu được khởi tạo từ Client. Server sẽ trả lời lại phía Client với địa chỉ IP cũng như địa chỉ cổng mà Server sẽ sử dụng. Sau đó phía Server-DTP lắng nghe trên cổng này một kết nối TCP đến từ User-DTP. Theo mặc định, phía Client sẽ sử dụng cùng cổng mà nó sử dụng cho Control Connection như trong trường hợp chủ động. Tuy nhiên, trong phương pháp này, Client cũng có thể chọn sử dụng một cổng khác cho Data Connection nếu cần thiết.

# 8. Các phương thức truyền dữ liệu trong FTP

Khi Client-DTP và Server-DTP thiết lập xong kênh dữ liệu, dữ liệu sẽ được truyền trực tiếp từ phía Client tới phía Server, hoặc ngược lại, tùy theo các lệnh được sử dụng. Do thông tin điều khiển được gửi đi trên kênh điều khiển, nên toàn bộ kênh dữ liệu có thể được sử dụng để truyền dữ liệu. FTP có ba phương thức truyền dữ liệu, đó là: stream mode, block mode, và compressed mode.
  - Stream mode
      Dữ liệu truyền đi liên tiếp dưới dạng các byte không cấu trúc.
  
      Thiết bị gửi chỉ đơn thuần đẩy luồng dữ liệu qua kết nối TCP tới phía nhận.
  
      Không có trường tiêu đề nhất định
  
      Không có cấu trúc dạng Header, nên việc báo hiệu kết thúc file sẽ đơn giản được thực hiện khi thiết bị gửi ngắt kênh kết nối dữ liệu khi đã truyền dữ liệu xong.
  
  Được sử dụng nhiều nhất trong 3 phương thức trong triển khai FTP thực tế. Do: Là phương thức mặc định và đơn giản nhất; là phương thức phổ biến nhất, vì nó xử lí các file chỉ đơn thuần là xử lí dòng byte, mà không cần để ý tới nội dung; Không tốn 1 lượng byte “overload” nào để thông báo Header.
   - Block mode
     Phương thức truyền dữ liệu mang tính quy chuẩn hơn.
  
     Dữ liệu được chia thành nhiều khối nhỏ và đóng gói thành các FTP block.
  
     Mỗi block có 1 trường Header 3 byte: báo hiệu độ dài, và chứa thông tin về các khối dữ liệu đang được gửi.
  
     Một thuật toán đặc biệt được sử dụng để kiểm tra các dữ liệu đã truyền đi. Và để phát hiện, khởi tạo lại đối với 1 phiên truyền dữ liệu đã bị ngắt kết nối.
  
  - Compressed mode (Chế độ nén)
       Phương thức truyền dữ liệu sử dụng 1 kỹ thuật nén đơn giản, là “run-lenght encoding (mã hóa chiều dài)” – có tác dụng phát hiện và xử lí các đoạn lặp trong dữ liệu được truyền đi để giảm chiều dài của toàn bộ thông điệp.
    
       Thông tin sau khi được nén, sẽ được xử lí như Block mode, với trường Header.
    
       Trong thực tế, việc nén dữ liệu thường được thực hiện ở chỗ khác, làm cho phương thức Compressed mode trở nên không cần thiết.
    
 # 9. Dữ liệu trong FTP

Các tập tin được coi như một tập hợp các byte. FTP không quan tâm nội dung tập tin, sẽ chỉ đơn giản là di chuyển các tệp tin, các byte cùng 1 thời điểm, từ nơi này sang nơi khác.
  - FTP Data Types:
Phần đầu tiên của thông tin có thể được đưa ra về tập tin là kiểu dữ liệu của nó.

Có 4 kiểu dữ liệu khác nhau được quy định trong chuẩn của FTP.

   ASCII: file văn bản ASCII
  
   EBCDIC: tương tự ASCII, nhưng sử dụng kiểu kí tự EBCDIC do IBM đặt.
  
   Image: Các tập tin không có cấu trúc nội bộ chính thức.
  
   Local: Kiểu dữ liệu này được sử dụng để xử lí các tập tin có thể lưu trữ dữ liệu trong byte logic. Cách xác định loại này cùng với cách dữ liệu có cấu trúc cho phép dữ liệu được lưu trữ trên hệ thống đích một cách phù hợp với đại diện local của nó.

Trong thực tế, hai loại kiểu dữ liệu thường xuyên nhất được sử dụng là ASCII và Image. Kiểu ASCII được sử dụng cho các tập tin văn bản, và cho phép chúng được di chuyển giữa các hệ thống với dòng kết thúc mã chuyển đổi tự động. Loại Image được sử dụng cho các tập tin nhị phân, chẳng hạn như đồ họa hình ảnh, tập tin ZIP và các dữ liệu khác. Nó cũng thường được gọi là kiểu nhị phân vì lý do đó.
  - FTP Format Control:
Đối với các loại ASCII và EBCDIC, FTP xác định 1 tham số tùy chọn được gọi là “format control” (điều khiển định dạng), nó cho phép người dùng chỉ định một đại diện cụ thể cho cách sử dụng định dạng dọc để mô tả tệp. Các tùy chọn kiểm soát định dạng được tạo ra cho mục đích cụ thể đúng cách xử lý các tập tin chuyển giao từ các thiết bị máy chủ đến máy in. Nó không được sử dụng ngày nay, hoặc nếu nó được sử dụng, nó chỉ là trong ứng dụng đặc biệt.

3 tùy chọn trong FTP Format Control:

  Non Print : Đây là tùy chọn mặc định, cho biết không có định dạng dọc
  
  Telnet Format : Tệp sử dụng các kí tự điều khiển định dạng dọc, như được chỉ định trong giao thức Telnet
  
  Carriage Control/FORTRAN : Tệp sử dụng kí tự điều khiển được định dạng đưa ra làm kí tự đầu tiên của mỗi dòng, như được xác định cho ngôn ngữ lập trình FORTRAN.
  
  - FTP Data Structures:
  Ngoài việc xác định một loại dữ liệu tệp tin, ta cũng có thể xác định cấu trúc tệp tin theo 3 cách:

     File Structure : Tệp là 1 luồng byte liền kề không có cấu trúc bên trong. Đây là cách mặc định và được sử dụng cho hầu hết các loại tệp.
  
     Record Structure : Tệp bao gồm một tập hợp các bản ghi, mỗi bản ghi được phân định bằng đánh dấu end-of-record. Cấu trúc bản ghi có thể sử dụng cho các tệp văn bản ASCII, nhưng chúng thường được gửi với cấu trúc tệp thông thường sử dụng kiểu dữ liệu ASCII.
  
     Page Structure : Tệp chứa 1 trang dữ liệu được lập chỉ mục đặc biệt. Cấu trúc này không được sử dụng phổ biến. Nó được tạo ra cho 1 máy tính cổ xưa được sử dụng trong ARPAnet đời đầu.
      # 1. HTTP là gì?

Http (HyperText Transfer Protocol) là giao thức truyền tải siêu văn bản được sử dụng trong www dùng để truyền tải dữ liệu giữa Web server đến các trình duyệt Web và ngược lại. Giao thức này sử dụng cổng 80 (port 80) là chủ yếu. Hay bạn có thể hiểu khi bạn gõ vào 1 địa chỉ vào trình duyệt Web, lúc này trình duyệt Web sẽ gửi 1 yêu cầu qua giao thức Http đến Web server. Web server và sẽ nhận yêu cầu này và trả lại kết quả cho trình duyệt Web. Https (HyperText Transfer Protocol Secure) là giao thức Http có sử dụng thêm SSL (Secure Sockets Layer) để mã hóa dữ liệu trong lúc truyền tải dữ liệu nhầm gia tăng thêm tính an toàn cho việc truyền dữ liệu giữa Web server và trình duyệt Web. Giao thức Https thì sử dụng cổng 433 để truyền dữ liệu.

# 2. Khía cạnh cơ bản của HTTP
 
 **HTTP đơn giản:**

HTTP thường được thiết kế để trở nên đơn giản và thân thiện để con người có thể đọc được, ngay cả khi có thêm sự phức tạp được giới thiệu trong HTTP/2 bằng cách đóng gói các HTTP message thành các frame. Với các HTTP message, chúng ta có thể được đọc và hiểu được, cung cấp khả năng testing hơn cho các dev và giảm thiểu độ phức tạp cho bất cứ người mới nào.

 **HTTP có thể mở rộng:**

Được giới thiệu trong HTTP/1.0, các header HTTP làm cho giao thức này dễ dàng mở rộng và thử nghiệm hơn nữa. Chức năng mới thậm chí có thể được giới thiệu bằng 1 thỏa thuận đơn giản giữa 1 client và 1 máy chủ về ngữ nghĩa của 1 header mới.

 **HTTP là stateless, nhưng không sessionless:**

Không có liên kết giữa 2 yêu cầu được thực hiện liên tiếp trên cùng 1 kết nối. Điều này ngay lập tức có khả năng trở thành vấn để với người dùng cố gắng tương tác với các trang nhất định 1 cách mạch lạc, chẳng hạn như sử dụng shopping cart trên các trang e-commerce, tức thương mại điện tử.

Nhưng trong khi cốt lõi bản thân HTTP là stateless, các cookie HTTP cho phép sử dụng các session trạng thái. Sử dụng khả năng mở rộng header, các cookie HTTP được thêm vào quy trình vận hành, cho phép tạo các session trên mỗi yêu cầu HTTP để chia sẻ cùng 1 ngữ cảnh hay cùng 1 trạng thái.

# 3. Cấu trúc cơ bản của HTTP

![image](https://user-images.githubusercontent.com/55913475/157570928-d1da72ca-15b1-4bcd-bc1e-e124bebcb790.gif)

HTTP là 1 giao thức Yêu cầu – Phản hồi dựa trên cấu trúc Client – Server. Client và Server giao tiếp với nhau bằng cách trao đổi các message độc lập (trái ngược với 1 luồng dữ liệu). Các message được gửi bởi client, thông thường là 1 trình duyệt web, được gọi là các yêu cầu và message được gửi bởi server như 1 sự trả lời, được gọi là phản hồi.

# 4. Kết nối của HTTP

Một kết nối được kiểm soát tại layer truyền tải, do đó về cơ bản nằm ngoài phạm vi của HTTP. Dù HTTP không yêu cầu giao thức truyền tải cơ bản phải dựa trên sự kết nối, vì chỉ yêu cầu nó đáng tin cậy hoặc không bị mất message (ít nhất là trình báo 1 lỗi). Trong số hai giao thức truyền tải phổ biến nhất trên Internet, TCP thì đáng tin cậy còn UDP thì không. HTTP do đó dựa vào tiêu chuẩn TCP vốn là connection-based (dựa trên sự kết nối).

![image](https://user-images.githubusercontent.com/55913475/157573427-945cb7e9-5eb5-4469-b752-847f41665928.jpg)

Trước khi 1 client và server có thể trao đổi 1 cặp yêu cầu – phản hồi HTTP, chúng phải thiết lập 1 kết nối TCP, 1 quá trình vốn yêu cầu 1 số vòng lặp. Hoạt động mặc định của HTTP/1.0 là mở 1 kết nối TCP riêng biệt cho từng cặp yêu cầu – phản hồi HTTP. Điều này làm nó kém hiệu quả hơn việc chia sẻ 1 kết nối TCP đơn lẻ khi nhiều yêu cầu được gửi liên tiếp.

Để giảm thiểu lỗ hỏng này, HTTP/1.1 đã giới thiệu pipelining (nhưng được chứng minh là khá khó để thực hiện) và kết nối liên tục: kết nối TCP bên dưới có thể được kiểm soát 1 phần bằng cách sử dụng tiêu đề Connection. HTTP/2 đã tiến 1 bước xa hơn bằng cách ghép các thông báo qua 1 kết nối duy nhất, giúp giữ cho kết nối ổn định và hiệu quả hơn.

Các thử nghiệm đang được tiến hành để thiết kế một giao thức truyền tải tốt hơn phù hợp hơn với HTTP. Ví dụ: Google đang thử nghiệm QUIC được xây dựng trên UDP để cung cấp giao thức truyền tải cũng đáng tin cậy và hiệu quả hơn.

# 5. Một số lỗi thường gặp

-Lỗi 404 hay Http 404 tức là lỗi không tồn tại địa chỉ bạn đang truy cập

-Lỗi 401: lỗi này bạn truy cập vào nơi yêu cầu xác thực, nhưng không vượt qua được sẽ có lỗi này.

-Lỗi 500: lỗi này thường do Web server mà bạn truy cập bị lỗi nên không thể truy cập vào được.

Ngoài ra Http 200 tức là bạn truy cập thành công.
# SMTP là gì?

Simple Mail Transfer Protocol (viết tắt là SMTP) là hệ thống giao thức có nhiệm vụ nhận hay truyền tải dữ liệu trong email của người dùng. Hệ thống chỉ nhận và gửi thư điện tử email thông qua thiết bị có kết nối mạng Internet. Những thiết bị nhận và gửi email được gọi là máy chủ SMTP, mỗi máy chủ đều liên kết tới cổng mạng Internet 25 – cổng TCP.

# Hoạt động của giao thức SMTP

![image](https://user-images.githubusercontent.com/55913475/157623924-9117ad9a-194a-4c7e-800c-dac499827d34.jpg)Việc gửi thông báo được thực hiện bắt đầu bằng việc chuyển thông báo đến một SMTP Server chỉ định. Dựa vào tên miền của địa chỉ e-mail nhận (ví dụ, ‘tenemail.com’), SMTP Server bắt đầu trao đổi liên lạc với một DNS Server mà sẽ tìm kiếm và trả về host name của SMTP Server đích (ví dụ ‘mail.ten-email.com’) cho tên miền đó. Sau cùng SMTP Server đầu tiên trao đổi thông tin trực tiếp với SMTP Server đích thông qua cổng 25 của TCP/IP. Nếu tên người dùng của địa chỉ e-mail nhận trùng khớp với một trong những tài khoản người dùng được phép trong máy chủ đích. Thì thông báo e-mail gốc cuối cùng sẽ được đưa đến máy chủ này, rồi chỉ chờ người nhận lấy thông báo thông qua một chương trình gửi nhận mail như mail server Outlook chẳng hạn. Trong trường hợp SMTP Server đầu tiên không thể liên lạc và trao đổi thông tin trực tiếp với máy chủ đích, thì giao thức SMTP có cung cấp các cơ chế để chuyển các thông báo thông qua một hay nhiều SMTP Server chuyển tiếp trung gian. Một máy chủ trung gian sẽ nhận thông báo gốc và sau đó sẽ gửi nó tới máy chủ đích hoặc cũng có thể gửi nó một lần nữa tới một máy chủ trung gian khác. Quá trình này sẽ được thao tác nhiều lần cho đến khi thông báo được chuyển đi hoặc thời gian lưu giữ thông báo hết hạn.
# 1. SNMP là gì?
  
  SNMP (Simple Network Management Protocol) là một giao thức tầng ứng dụng được Hội đồng Kiến trúc Internet (IAB) xác định trong RFC1157 để trao đổi thông tin quản lý giữa các thiết bị mạng. Nó là một phần của Transmission Control Protocol/Internet Protocol (TCP/IP). Giao thức SNMP là một trong những giao thức mạng được chấp nhận rộng rãi để quản lý và giám sát các phần tử mạng. Hầu hết các thiết bị mạng được cung cấp đi kèm với SNMP agent. Các agent này phải được kích hoạt và cấu hình để giao tiếp với các công cụ giám sát mạng hoặc hệ thống quản lý mạng (NMS).
  
# 2. Các thành phần của SNMP

  **SNMP Manager**
  
  Trình quản lý hoặc hệ thống quản lý là một thực thể riêng biệt có trách nhiệm giao tiếp với các thiết bị mạng được triển khai SNMP agent. Đây thường là một máy tính được sử dụng để chạy một hoặc nhiều hệ thống quản lý mạng.

  Các chức năng chính của SNMP manager:

   - Agent truy vấn
   - Nhận response từ các agent
   - Đặt các biến trong agent
   - Xác nhận các sự kiện không đồng bộ từ các agent
    
  **SNMP Manager Device**
    
   Thiết bị được quản lý hoặc phần tử mạng là một phần của mạng yêu cầu một số hình thức giám sát và quản lý, ví dụ: router, switches, server, máy trạm, máy in, UPS, v.v.
    
  **SNMP Agent**
  
  Agent là một chương trình được đóng gói trong các thiết bị mạng. Việc kích hoạt agent cho phép nó thu thập cơ sở dữ liệu thông tin quản lý từ thiết bị cục bộ và cung cấp nó cho SNMP manager khi được truy vấn. Các agent này có thể là tiêu chuẩn (ví dụ: Net-SNMP) hoặc cụ thể cho một nhà cung cấp (ví dụ: HP insight agent).

  Các chức năng chính của SNMP agent:

   - Thu thập thông tin quản lý về các chỉ số hoạt động cuả thiết bị
   - Lưu trữ và truy xuất thông tin quản lý như được định nghĩa trong MIB.
   - Báo hiệu sự kiện cho trình quản lý.
   - Hoạt động như một proxy cho một số nút mạng không quản lý được – SNMP.
    
# 3. Cách thức hoạt động của SNMP

  ![image](https://user-images.githubusercontent.com/55913475/157618603-f00d2dcf-209f-4f23-b0ca-5dadef6d95bb.png)
  
  SNMP sử dụng một số command cơ bản để giao tiếp giữa manager và agent.
    
   - GET: Yêu cầu thông tin bất cứ lúc nào
  
  Để nhận thông tin trạng thái từ agent, manager có thể đưa ra message Get và GetNext để yêu cầu thông tin cho một biến cụ thể. Sau khi nhận được message Get hoặc GetNext, agent sẽ gửi message GetResponse cho manager. Nó sẽ chứa thông tin được yêu cầu hoặc lỗi giải thích tại sao không thể xử lý request.
    
   - SET: Điều khiển thiết bị từ xa 
  
  Message SET cho phép manager yêu cầu thực hiện thay đổi đối với đối tượng được quản lý (tức là rơle điều khiển). Sau đó, agent sẽ trả lời bằng message Set-response nếu thay đổi đã được thực hiện hoặc lỗi giải thích tại sao không thể thực hiện thay đổi.
    
   - TRAP: SNMP message phổ biến nhất
 
 Message TRAP được khởi xướng bởi agent và gửi đến manager khi một sự kiện quan trọng xảy ra. Trap dùng để cảnh báo cho manager – thay vì đợi request trạng thái từ manager khi cần thăm dò ý kiến của agent.
    
   - INFORM: Một loại message có giá trị khác
  
  Message INFORM rất giống với TRAP, nhưng chúng đáng tin cậy hơn. Các message INFORM được khởi tạo bởi agent và khi manager nhận được nó, nó sẽ gửi response đến agent cho biết message đã được nhận. Nếu agent không nhận được response từ manager thì agent sẽ gửi lại message INFORM.
    
   - SNMPWALK: Nhận tất cả dữ liệu
  
  SNMPWALK sử dụng nhiều request Get-Next để truy xuất toàn bộ cây dữ liệu mạng từ một đối tượng được quản lý. Công cụ iReasoning MIB Browser sẽ rất hữu ích để xem tất cả các OID mà một agent cung cấp.
  
# 4. Cấu trúc của SNMP

  ![image](https://user-images.githubusercontent.com/55913475/157618699-3f0b76aa-fdbf-43e8-a814-867e5d161069.png)

  Để gửi thông tin, SNMP sử dụng mô hình truyền thông phân lớp.

   - Layer 1 – Lớp ứng dụng (SNMP)
   - Layer 2 – Lớp vận chuyển (UDP)
   - Layer 3 – Lớp Internet (IP)
   - Layer 4 – Lớp Network interface
  
  Mặc dù mô hình nhiều lớp này có vẻ hơi khó hiểu, nhưng nó rất hiệu quả trong việc tách biệt các nhiệm vụ giao tiếp và hỗ trợ thiết kế, triển khai mạng.
  
# 5. Lợi ích của SNMP

  - Sử dụng SNMP cho phép bạn quản lý các asset mạng không có hệ điều hành, nhưng là các thành phần quan trọng của cơ sở hạ tầng. 
  - Đơn giản hóa nhiệm vụ và giúp bạn có thể tập trung mạng. Nó còn cho phép kiểm soát hiệu quả hơn, ngay cả đối với thiết bị không có hệ điều hành như máy in.
  - Có một ngôn ngữ duy nhất cho phép người dùng tương tác với tất cả các thiết bị từ các nhà sản xuất khác nhau.
  - Tương thích với hầu hết mọi asset và dịch vụ mạng, chẳng hạn như Windows, Linux, Mac và máy ảo Java.
  - Thiết kế đơn giản, dễ dàng triển khai nó trên mạng, vì nó không yêu cầu cấu hình lâu.
  - Hầu hết tất cả các nhà sản xuất thiết bị phần cứng liên mạng lớn, như switch hoặc router, đều triển khai hỗ trợ SNMP trong các sản phẩm của họ.
  - Dễ dàng cập nhật giao thức để đáp ứng nhu cầu của user trong tương lai.
  - SNMP dựa trên giao thức truyền tải UDP, yêu cầu ít tài nguyên hơn và kết nối đồng thời hơn với TCP.
  # 1. SSH là gì?

SSH, hay Secure (Socket) Shell, là một giao thức mạng cung cấp cho người dùng (đặc biệt là các QTV mạng) cách truy cập an toàn vào một máy tính qua một mạng không được bảo mật. Bên cạnh đó, SSH cũng cung cấp nhiều bộ tiện ích để triển khai giao thức SSH. Secure Shell là một giao thức cung cấp khả năng xác thực password mạnh mẽ, cùng với khả năng giao tiếp dữ liệu được mã hóa giữa hai máy tính kết nối với nhau qua một mạng mở như Internet. Bên cạnh đó, SSH cũng được sử dụng phổ biến bởi các QTV mạng để quản lý hệ thống và ứng dụng từ xa. Từ đó cho phép đăng nhập vào các máy tính khác qua mạng và thực hiện các tác vụ cơ bản như thực thi lệnh, di chuyển file,… SSH bao gồm cả giao thức mạng lẫn một bộ tiện ích để triển khai giao thức đó. SSH sử dụng mô hình client-server, kết nối một ứng dụng Secure Shell client (nơi session được hiển thị) với một SSH server (nơi session chạy). Triển khai SSH thường hỗ trợ cả các giao thức ứng dụng, dùng cho giả lập terminal hay truyền file. Ngoài ra, SSH cũng có thể được dùng để tạo các tunnel bảo mật cho nhiều giao thức ứng dụng. Chẳng hạn như để chạy các phiên đồ họa X Windows System từ xa. Một SSH server theo mặc định sẽ nghe trên cổng TCP 22.

# 2. Chức năng

SSH hỗ trợ các chức năng sau đây:

   - Truy cập từ xa an toàn vào các hệ thống hay thiết bị mạng có hỗ trợ SSH cho người dùng và các quá trình tự động khác.
   - Hỗ trợ phiên chuyển file an toàn
   - Tự động truyền file an toàn.
   - Thực thi lệnh an toàn trên các máy hay hệ thống từ xa.
   - Quản lý an toàn các thành phần cơ sở hạ tầng mạng.
  
  SSH có thể được sử dụng để enable các terminal session và nên được dùng thay thế cho các chương trình Telnet có độ bảo mật kém hơn. Ngoài ra, SSH cũng thường được dùng trong các script và nhiều phần mềm khác để cho phép các chương trình, hệ thống truy cập an toàn từ xa vào các tài nguyên khác.
  
# 3. Kỹ thuật mã hóa qua SSH

Lợi điểm khiến SSH hơn hẵn những giao thức cũ là khả năng mã hóa và truyền tải dữ liệu an toàn giữa host và client. Host đại diện cho máy chủ  từ xa bạn muốn kết nối tới và client là máy tính của bạn dùng để truy cập tới host. Có 3 cách khác nhau để mã hóa qua SSH:

  - Symmetrical encryption.
  - Asymmetrical encryption.
  - Hashing.
    
   **Symmetric Encryption**
   
  Symmetric encryption là một dạng mã hóa sử dụng secret key ở cả 2 chiều mã hóa và giải mã tin nhắnb bởi cả host và client. Có nghĩa là ai nắm được khóa đều có thể giải mã tin nhắn trong quá trình chuyền. Symmetrical encryption thường được gọi là shared key hoặc shared secret encryption. Vì có một khóa được sử dụng, hoặc một cặp khóa (pair key) mà một khóa có thể được tính ra từ khóa kia. Symmetric keys được sử dụng để mã hóa toàn bộ liên lạc trong phiên giao dịch SSH. Cả client và server tạo chung một key bí mật như là một phương thức thỏa thuận, và key đó không được tiết lộ cho bên thứ ba. Quá trình tạo symmetric key được thực hiện bởi key exchange algorithm. Điều khiến cho thuật toán an toàn là vì key không được truyền giữa client và host. Thay vào đó, cả 2 máy tính chia sẽ thông tin chung và sau đó sử dụng chúng để tính ra khóa bí mật.Kể cả có máy khác bắt được thông tin chung, nó cũng không thể tính ra key bí mật vì không biết được thuật toán tạo key. Cũng phải lưu ý rằng, tuy nhiên secret token được sử dụng cho một phiên SSH nhất định, và được tạo bởi chứng thực của client. Khi key đã được tạo, tất cả packets truyền giữa 2 máy phải được mã hóa bởi private key. Việc này bao gồm cả mật khẩu điền vào bởi user, vì vậy mật khẩu cũng có thể được bảo vệ khỏi những “lính bắn tỉa packet” trên mạng. Một số loại symmetrical encryption ciphers đã tồn tại, bao gồm, những không giới hạn AES (Advanced Encryption Standard), CAST128, Blowfish etc. Trước khi thiết lập kết nối an toàn client và host sẽ đồng ý loại cipher nào được sử dụng, bằng cách xuất bản danh sách cyphers được hỗ trợ để tham khảo. Cypher thích hợp nhất ở phía client sẽ hiển thị trong danh sách của host như là một bidirectional cypher.
  
  **Asymmetric Encryption**
  
  Không giống với symmetrical encryption, asymmetrical encryption sử dụng 2 khóa khác nhau để mã hóa và giải mã. 2 khóa này được gọi là public key và private key. Cả 2 hình thành nên một cặp khóa là public-private key pair. Khóa public, như tên gọi của nó sẽ được công khai cho tất cả các bên liên quan. Mặc dù nó liên quan mật thiết đến private key về chức năng, nhưng private key không thể được tính toán ra từ một public key. Sự liên quan này rất phức tạp: thư được mã hóa bởi public key của một máy, và chỉ có thể được giải mã bởi private key của chính máy đó. Sự liên quan một chiều này có nghĩa là public key không thể giải mã chính thư của nó, hoặc không thể giải mã bất kỳ thứ gì được mã hóa bằng private key. Private key phải luôn luôn được đảm bảo an toàn, ví dụ, kết nối an toàn, không có bên thứ 3 biết. Sức mạnh của cả chu trình kết nối phụ thuộc vào việc private key có bị tiết lộ hay không, vì chỉ có nó mới có khả năng giải mã thư được truyền đi mà được mã hóa bởi public key. Vì vậy, bất kỳ bên nào có thể giải mã thư được ký bởi public key có nghĩa là bên đó đang sở hữu private key tương ứng. Không giống với quan niệm thông thường, asymmetrical encryption không được dùng để mã hóa toàn bộ phiên SSH. Thay vào đó, nó chỉ được sử dụng trong quá trình trao đổi thuật toán của khóa của symmetric encryption. trước khi bắt đầu một phiên giao dịch an toàn, cả 2 đồng ý tạo ra một cặp public-private key tạm, chia sẽ private keys để tạo một khóa secret key chung. Khi kết nối symmetrict an toàn đã được thiết lập, server sử dụng public key của client để tạo và challenge và truyền nó tới client để chứng thực. Nếu client có thể giải mã tin nhắn, có nghĩa là nó đang giữa đúng private key cần thiết cho kết nối. Phiên giao dịch SSH bắt đầu.
  
  **Hashing**
  
  Hashing một chiều là một dạng mã hóa khác sử dụng trong Secure Shell Connections. Hash một chiều khác với cả 2 phương thức mã hóa trên ở chỗ nó không được sinh ra để giải mã. Chúng tạo ra một giá trị duy nhất với độ dài nhất định cho mỗi lần nhập liệu mà không có hướng nào khác để khai thác. Điều này khiến nó dường như không thể quay ngược lại giải mã. Rất dễ để tạo một cryptographic hash từ một lần input, nhưng không thể tạo ra lần input đó từ một hash. Có nghĩa là nếu client giữ đúng input đó, client có thể tạo ra một crypto-graphic hash giống như vậy và so sánh nó với giá trị ở đầu bên kia để xác định cả 2 bên nhập giống input. SSH sử dụng hashes để xác nhận tính xác thực của tin nhắn. Nó được thực hiện bởi HMACs, hoặc Hash-based Message Authentication Codes. Việc này đảm bảo lệnh không bị giả mạo bởi bất kỳ phương thức nào. Trong khi thuật toán symmetrical encryption được chọn, một thuật toán xác thực tin nhắn phù hợp cũng được chọn. Nó hoạt động tương tự việc cipher được chọn như thế nào, như bên trên mình đã giải thích trong phần symmetric encryption. Mỗi tin nhắn được truyền đi phải chứa MAC, được tính bởi symmetric key, packet sequence number, và nội dung tin nhắn. Nó truyền ra ngoài một gói dữ liệu được mã hóa symmetric như là một phần của communication packet.
  
