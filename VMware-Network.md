# Tìm Hiểu Về Network trong VMware

**Network trong VMware** là một phần quan trọng để kết nối các máy ảo với nhau và với các tài nguyên mạng bên ngoài. VMware cung cấp các tùy chọn mạng mạnh mẽ giúp quản lý lưu lượng mạng giữa các máy ảo và máy chủ vật lý.

---

## 1. **Các loại Network trong VMware**

VMware hỗ trợ ba kiểu kết nối mạng cơ bản cho các máy ảo:

### a. **Bridged Networking**
   - **Chức năng**: Kết nối máy ảo trực tiếp với mạng vật lý, giống như một máy tính thực.
   - **Cách hoạt động**: Máy ảo sẽ nhận một địa chỉ IP từ cùng một dải mạng với máy chủ vật lý, giống như cách mà các thiết bị trong mạng LAN giao tiếp với nhau.
   - **Ứng dụng**: Sử dụng khi bạn muốn máy ảo có thể giao tiếp với các thiết bị khác trong mạng vật lý hoặc Internet mà không qua máy chủ host.

### b. **NAT (Network Address Translation)**
   - **Chức năng**: Cho phép máy ảo sử dụng địa chỉ IP của máy chủ host để kết nối với mạng bên ngoài (Internet).
   - **Cách hoạt động**: Máy ảo sẽ không có địa chỉ IP riêng mà sử dụng IP của máy chủ host thông qua NAT để giao tiếp với mạng ngoài.
   - **Ứng dụng**: Sử dụng khi bạn không muốn máy ảo có địa chỉ IP public, nhưng vẫn cần kết nối Internet (thường dùng trong môi trường test, phát triển).

### c. **Host-Only Networking**
   - **Chức năng**: Máy ảo chỉ có thể giao tiếp với máy chủ host và các máy ảo khác trong cùng một host.
   - **Cách hoạt động**: Mạng này không kết nối với mạng ngoài hoặc Internet, chỉ giới hạn trong môi trường máy ảo và host.
   - **Ứng dụng**: Sử dụng trong testing phần mềm ứng dụng khi bạn muốn máy ảo giao tiếp nội bộ mà không cần kết nối Internet.

## 2. **Cấu hình mạng trong VMware Workstation và VMware ESXi**

### a. **VMware Workstation**
   - VMware Workstation cung cấp giao diện người dùng dễ dàng để cấu hình các loại mạng như Bridged, NAT và Host-Only.
   - **Cách cấu hình**:
     1. Mở VMware Workstation.
     2. Chọn máy ảo cần cấu hình.
     3. Vào **Settings** của máy ảo, chọn **Network Adapter**.
     4. Chọn một trong ba tùy chọn mạng: **Bridged**, **NAT**, hoặc **Host-Only**.

# Continue ....