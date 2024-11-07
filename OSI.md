# **MÔ HÌNH OSI (Open Systems Interconnection Model)**
Mô hình OSI (Open Systems Interconnection) là một mô hình lý thuyết dùng để hiểu cách các hệ thống mạng giao tiếp với nhau. Mô hình này chia quá trình giao tiếp giữa các thiết bị và ứng dụng thông qua mạng thành 7 lớp, mỗi lớp có một chức năng riêng biệt. Mô hình OSI giúp chuẩn hóa giao tiếp giữa các hệ thống và thiết bị mạng khác nhau, từ đó làm việc hiệu quả hơn trong môi trường mạng phức tạp
## 1. **Sự quan trọng của mô hình OSI**
- Mô hình OSI giúp các kỹ sư phân loại và thiết kế cấu trúc cho các hệ thống mạng phức tạp bằng cách chia hoạt động thành các lớp, dựa vào các chức năng cốt lõi. Từ đó làm cho việc quản lý và nắm bắt bản chất của hệ thống trở nên minh bạch và dễ dàng hơn.
- Mô hình OSI giúp các kĩ sư vận hành có thể dễ dàng truy lỗi hoặc sự cố đang nằm ở lớp nào từ đó rút gọn quá trình phát hiện và xử lý lỗi
- Trong quá trình thiết kế hệ thống mới, mô hình OSI giúp kỹ sư nắm bắt chi tiết công việc của họ một cách chính xác. Điều này tạo điều kiện cho việc tạo ra công nghệ mới cần thiết để đảm bảo hệ thống mạng mới hoạt động mượt mà. Hơn nữa, nó cũng hỗ trợ tăng tốc độ phát triển hệ thống thông qua việc áp dụng các quy trình và giao thức đã được chuẩn hóa.
## 2. **Các lớp trong mô hình OSI**
### 2.1 ***Lớp vật lý ( Physical Layer )***
- #### **Nhiệm vụ** : Chịu trách nhiệm truyền tín hiệu giữa các thiết bị, đảm bảo tín hiệu được gửi đi mà không gặp lỗi vật lý. 
- #### **Ví dụ** : Bạn dùng cáp Ethernet, cáp quang, Wifi để truyền tín hiệu va dữ liệu giữa các thiết bị. 
### 2.2 ***Lớp liên kết dữ liệu ( Data Link Layer )***
- #### **Nhiệm vụ** : Đóng gói dữ liệu thành các khung (frame) và đảm bảo dữ liệu truyền đi không bị lỗi. 
- #### **Ví dụ** : Tạo 1 con đường cho dữ liệu có thể truyền đi (Ethernet, Wifi). 
### 2.3 ***Lớp mạng ( Network Layer )***
- #### **Nhiệm vụ** : Định tuyến và chuyển gói tin đến đích.
- #### **Ví dụ** : Tạo 1 con đường và tìm địa chỉ đích đến cho dữ liệu (IPv4 IPv6). 
### 2.4 ***Lớp vận chuyển ( Transport Layer )***
- #### **Nhiệm vụ** : Có chức năng là chia nhỏ các gói tin lớn khi truyền và tập hợp lại chúng khi nhận. Đảm bảo dữ liệu không bị mất mát.
- #### **Ví dụ** : Các giao thức TCP và UDP
### 2.5 ***Lớp phiên ( Session Layer )***
- #### **Nhiệm vụ** : Quản lý các kết nối giữa các ứng dụng, đồng bộ hóa dữ liệu, đảm bảo rằng các phiên làm việc giữa các ứng dụng được duy trì và kết thúc đúng cách.
- #### **Ví dụ** : Khi đang nói chuyện qua Skype , lớp này sẽ duy trì kết nối để cuộc gọi không bị ngắt giữa chừng.
### 2.6 ***Lớp trình bày ( Presentation Layer )***
- #### **Nhiệm vụ** : Đảm bảo dữ liệu được mã hóa đúng định dạng để phần mềm có thể hiểu được.
- #### **Ví dụ** : HTML, JSON, XML.
### 2.7 ***Lớp ứng dụng ( Application  Layer )***
- #### **Nhiệm vụ** : Cung cấp các dịch vụ và giao diện cho người dùng cuối hoặc các ứng dụng.
- #### **Ví dụ** : HTTP ( dùng để duyệt web ), SMTP ( dùng để gửi mail ).
## 3. **Các giao thức liên quan đến mô hình OSI**
- **HTTP** (HyperText Transfer Protocol): Dùng trong Lớp Ứng dụng để giao tiếp trên web.
- **TCP/IP** (Transmission Control Protocol/Internet Protocol): Cung cấp các giao thức vận chuyển và mạng, chủ yếu sử dụng trong Lớp Vận chuyển và Lớp Mạng.
- **Ethernet**: Là giao thức liên kết dữ liệu phổ biến trong mạng LAN.
- **IP** (Internet Protocol): Được sử dụng trong Lớp Mạng để định tuyến và phân phối gói dữ liệu.
## Kết luận

#### Mô hình OSI giúp đơn giản hóa quá trình truyền tải và giao tiếp trong mạng máy tính, giúp các nhà phát triển và kỹ sư mạng dễ dàng hiểu và xử lý các vấn đề liên quan đến kết nối mạng. Mặc dù mô hình OSI không được sử dụng trực tiếp trong tất cả các mạng hiện đại, nó vẫn là một công cụ quan trọng trong việc thiết kế và hiểu các hệ thống mạng phức tạp.
