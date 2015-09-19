# Tim-hieu-mo-hinh-OSI-va-TCP-IP
Mô hình OSI, mô hình TCP/IP và sự khác biệt giữa chúng

#1. Mô Hình OSI (Open Systems Interconnection Reference Model)

- Mô hình OSI (OpenSystemInterconnection): là mô hình được tổ chức ISO đề xuất từ 1977 và công bố lần đầu vào 1984. Để các máy tính và các thiết bị mạng có thể truyền thông với nhau phải có những qui tắc giao tiếp được các bên chấp nhận. Mô hình OSI là một khuôn mẫu giúp chúng ta hiểu dữ liệu đi xuyên qua mạng như thế nào đồng thời cũng giúp chúng ta hiểu được các chức năng mạng diễn ra tại mỗi lớp.

##1.1 Mô tả

- Trong mô hình OSI có bảy lớp, mỗi lớp mô tả một phần chức năng độc lập. Sự tách lớp của mô hình này mang lại những lợi ích sau:
<ul>
<li>Chia hoạt động thông tin mạng thành những phần nhỏ hơn, đơn giản hơn giúp chúng ta dễ khảo sát và tìm hiểu hơn.</li>
<li>Chuẩn hóa các thành phần mạng để cho phép phát triển mạng từ nhiều nhà cung cấp sản phẩm.</li>
<li>Ngăn chặn được tình trạng sự thay đổi của một lớp làm ảnh hưởng đến các lớp khác, như vậy giúp mỗi lớp có thể phát triển độc lập và nhanh chóng hơn.</li>
</ul>

- Mô hình tham chiếu OSI định nghĩa các qui tắc cho các nội dung sau:
<ul>
<li>Cách thức các thiết bị giao tiếp và truyền thông được với nhau.</li>
<liCác phương pháp để các thiết bị trên mạng khi nào thì được truyền dữ liệu, khi nào thì không được.</li>
<li>Các phương pháp để đảm bảo truyền đúng dữ liệu và đúng bên nhận.</li>
<li>Cách thức vận tải, truyền, sắp xếp và kết nối với nhau.</li>
<li>Cách thức đảm bảo các thiết bị mạng duy trì tốc độ truyền dữ liệu thích hợp.</li>
<li>Cách biểu diễn một bit thiết bị truyền dẫn.</li>
</ul>

##1.2 Các tầng của mô hình OSI


Mô hình tham chiếu OSI được chia thành bảy lớp với các chức năng sau:

+ Application : (ứng dụng): giao diện giữa ứng dụng và mạng (Tầng 7)

+ Presentation: (trình bày): thoả thuận khuôn dạng trao đổi dữ liệu (Tầng 6)

+ Session : (phiên): cho phép người dùng thiết lập các kết nối (Tầng 5)

+ Transport : (vận chuyển): đảm bảo truyền thông giữa hai hệ thống. (Tầng 4)

+ NetWork : (mạng):định hướng dữ liệu truyền trong liên mạng.(Tầng 3)

+ Data Link : (liên kết dữ liệu): xác định việc truy xuất đến thiết bị. (Tầng 2)

+ Physical : (vật lý): chuyển đổi dữ liệu thành các bit và truyền đi. (Tầng 1)

|   | Mô Hình OSI 7 Tầng |      Ý nghĩa các tầng           | Data Unit |
|---|--------------------|---------------------------------|-----------|
| 7 | Application | Các quá trình giao tiếp với các ứng dụng | Data |
| 6 | Presentation | Biểu diễn dữ liệu | Data |
| 5 | Session | Thông tin liên host | Data |
| 4 | Transport | Kết thúc từ đầu cuối đến đầu cuối | Segments |
| 3 | Network | Định địa chỉ và chọn đường dẫn tốt nhất | Packets |
| 2 | Data Link | Truy xuất môi trường truyền | Frames |
| 1 | Physical | Truyền dẫn nhị phân | Bits |

###1.2.1 Lớp ứng dụng (ApplicationLayer)

- Giao diện giữa các chương trình ứng dụng của người dùng và mạng. Lớp Application xử lý truy nhập mạng chung, kiểm soát luồng và phục hồi lỗi. Lớp này không cung cấp các dịch vụ cho lớp nào mà nó cung cấp dịch vụ cho các ứng dụng như: truyền file, gởi nhận E-mail, Telnet, HTTP, FTP, SMTP…

###1.2.2 Lớp trình bày (PresentationLayer) 

- Chịu trách nhiệm thương lượng và xác lập dạng thức dữ liệu được trao đổi. Nó đảm bảo thông tin mà lớp ứng dụng của một hệ thống đầu cuối gởi đi, lớp ứng dụng của hệ thống khác có thể đọc được. Lớp trình bày thông dịch giữa nhiều dạng dữ liệu khác nhau thông qua một dạng chung, đồng thời nó cũng nén và giải nén dữ liệu. Thứ tự byte, bit bên gởi và bên nhận qui ước qui tắc gởi nhận một chuỗi byte, bit từ trái qua phải hay từ phải qua trái. Nếu hai bên không thống nhất thì sẽ có sự chuyển đổi thứ tự các byte bit vào trước hoặc sau khi truyền. Lớp presentationcũng quản lý các cấp độ nén dữ liệu nhằm giảm số bit cần truyền. Ví dụ: JPEG,ASCCI, EBCDIC....

###1.2.3 Lớp phiên (SessionLayer)

- Có chức năng thiết lập, quản lý, và kết thúc các phiên thông tin giữa hai thiết bị truyền nhận. Lớp phiên cung cấp các dịch vụ cho lớp trình bày. Lớp Session cung cấp sự đồng bộ hóa giữa các tác vụ người dùng bằng cách đặt những điểm kiểm tra vào luồng dữ liệu. Bằng cách này, nếu mạng không hoạt động thì chỉ có dữ liệu truyền sau điểm kiểm tra cuối cùng mới phải truyền lại. Lớp này cũng thi hành kiểm soát hội thoại giữa các quá trình giao tiếp, điều chỉnh bên nào truyền, khi nào, trong bao lâu. Ví dụ như: RPC,NFS,... Lớp này kết nối theo ba cách: Haft-duplex, Simplex, Full-duplex.

###1.2.4 Lớp vận chuyển (TransportLayer)

- Phân đoạn dữ liệu từ hệ thống máy truyền và tái thiết lập dữ liệu vào một luồng dữ liệu tại hệ thống máy nhận đảm bảo rằng việc bàn giao các thông điệp giữa các thiết bị đáng tin cậy. Dữ liệu tại lớp này gọi là segment. Lớp này thiết lập, duy trì và kết thúc các mạch ảo đảm bảo cung cấp các dịch vụ sau:
<ul>
<li>Xếp thứ tự các phân đoạn: khi một thông điệp lớn được tách thành nhiều phân đoạn nhỏ để bàn giao, lớp vận chuyển sẽ sắp xếp thứ tự các phân đoạn trước khi ráp nối các phân đoạn thành thông điệp ban đầu.</li>
<li>Kiểm soát lỗi: khi có phân đoạn bị thất bại, sai hoặc trùng lắp, lớp vận chuyển sẽ yêu cầu truyền lại.</li>
<li>Kiểm soát luồng: lớp vận chuyển dùng các tín hiệu báo nhận để xác nhận. Bên gửi sẽ không truyền đi phân đoạn dữ liệu kế tiếp nếu bên nhận chưa gởi tín hiệu xác nhận rằng đã nhận được phân đoạn dữ liệu trước đó đầy đủ.</li>
</ul>

###1.2.5 Lớp mạng (NetworkLayer)

- Chịu trách nhiệm lập địa chỉ các thông điệp, diễn dịch địa chỉ và tên logic thành địa chỉ vật lý đồng thời nó cũng chịu trách nhiệm gởi packet từ mạng nguồn đến mạng đích. Lớp này quyết định đường đi từ máy tính nguồn đến máy tính đích. Nó quyết định dữ liệu sẽ truyền trên đường nào dựa vào tình trạng, ưu tiên dịch vụ và các yếu tố khác. Nó cũng quản lý lưu lượng trên mạng chẳng hạn như chuyển đổi gói, định tuyến, và kiểm soát sự tắc nghẽn dữ liệu. Nếu bộ thích ứng mạng trên bộ định tuyến (router) không thể truyền đủ đoạn dữ liệu mà máy tính nguồn gởi đi, lớp Network trên bộ định tuyến sẽ chia dữ liệu thành những đơn vị nhỏ hơn, nói cách khác, nếu máy tính nguồn gởi đi các gói tin có kích thước là 20Kb, trong khi Router chỉ cho phép các gói tin có kích thước là 10Kb đi qua, thì lúc đó lớp Network của Router sẽ chia gói tin ra làm 2, mỗi gói tin có kích thước là 10Kb. Ở đầu nhận, lớp Network ráp nối lại dữ liệu. Ví dụ: một số giao thức lớp này: IP, IPX,... Dữ liệu ở lớp này gọi packet hoặc datagram.

###1.2.6 Lớp liên kết dữ liệu (Data link Layer)

- Cung cấp khả năng chuyển dữ liệu tin cậy xuyên qua một liên kết vật lý. Lớp này liên quan đến:
<ul>
<li>Địa chỉ vật lý.</li>
<li>Mô hình mạng.</li>
<li>Cơ chế truy cập đường truyền.</li>
<li>Thông báo lỗi.</li>
<li>Thứ tự phân phối frame.</li>
<li>Điều khiển dòng.</li>
</ul>

- Tại lớp datalink, các bít đến từ lớp vật lý được chuyển thành các frame dữ liệu bằng cách dùng một số nghi thức tại lớp này. Lớp data linkđược chia thành hai lớp con: Lớp con LLC (logical link control), lớp con MAC (media access control).

####1.2.6.1 Lớp con LLC (logical link control).

- Lớp con LLC là phần trên so với các giao thức truy cập đường truyền khác, nó cung cấp sự mềm dẻo về giao tiếp. Bởi vì lớp con LLC hoạt động độc lập với các giao thức truy cập đường truyền, cho nên các giao thức lớp trên hơn (ví dụ như IP ở lớp mạng) có thể hoạt động mà không phụ thuộc vào loại phương tiện LAN. Lớp con LLC có thể lệ thuộc vào các lớp thấp hơn trong việc cung cấp truy cập đường truyền.

####1.2.6.2 Lớp con MAC (media access control).

- Lớp con MAC cung cấp tính thứ tự truy cập vào môi trường LAN. Khi nhiều trạm cùng truy cập chia sẻ môi trường truyền, để định danh mỗi trạm, lớp cho MAC định nghĩa một trường địa chỉ phần cứng, gọi là địa chỉ MAC address. Địa chỉ MAC là một con số đơn nhất đối với mỗi giao tiếp LAN (card mạng).

###1.2.7 Lớp vật lý (PhysicalLayer)

Định nghĩa các qui cách về điện, cơ, thủ tục và các đặc tả chức năng để kích hoạt, duy trì và dừng một liên kết vật lý giữa các hệ thống đầu cuối. Một số các đặc điểm trong lớp vật lý này bao gồm:
<ul>
<li>Mức điện thế.</li>
<li>Khoảng thời gian thay đổi điện thế.</li>
<li>Tốc độ dữ liệu vật lý.</li>
<li>Khoảng đường truyền tối đa.</li>
<li>Các đầu nối vật lý.</li>
</ul>

#2. Mô hình TCP/IP

#3. So sánh mô hình OSI và mô hình TCP/IP
