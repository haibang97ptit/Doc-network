#  Tìm Hiểu Về Policy Routing (Chính Sách Định Tuyến)

**Policy Routing** (chính sách định tuyến) là kỹ thuật định tuyến cho phép điều chỉnh cách gói dữ liệu được xử lý và định tuyến dựa trên các tiêu chí khác nhau, không chỉ dựa vào địa chỉ IP đích.

---

## 1. **Policy Routing là gì?**
- **Policy Routing** là một hình thức định tuyến linh hoạt, trong đó các gói dữ liệu được định tuyến dựa trên:
  - Nguồn gốc của gói (source IP).
  - Loại giao thức (protocol).
  - Cổng mạng (port).
  - Các thông số khác như tốc độ, chi phí, hoặc SLA.
  
- Thay vì chỉ dựa vào **bảng định tuyến truyền thống** (routing table), Policy Routing sử dụng các **chính sách** (policy) để quyết định đường đi của gói dữ liệu.

---

## 2. **Tại sao cần Policy Routing?**
Policy Routing được sử dụng trong các tình huống cần kiểm soát lưu lượng mạng linh hoạt hơn, ví dụ:
- **Quản lý lưu lượng**: Chuyển lưu lượng của ứng dụng cụ thể qua các đường mạng khác nhau.
- **Định tuyến dự phòng**: Chuyển lưu lượng qua một đường khác khi mạng chính gặp sự cố.
- **Đa ISP**: Chọn đường đi qua một nhà cung cấp dịch vụ Internet (ISP) cụ thể dựa trên gói nguồn hoặc loại ứng dụng.
- **Bảo mật**: Tách lưu lượng theo ứng dụng hoặc giao thức để đi qua các firewall hoặc VPN cụ thể.

---

## 3. **Cách thức hoạt động của Policy Routing**
1. **Xác định các chính sách**:
   - Sử dụng các tiêu chí như địa chỉ IP nguồn, đích, giao thức, cổng mạng, v.v.
   - Ví dụ: Gói dữ liệu từ một dải IP cụ thể sẽ đi qua ISP A, trong khi dữ liệu từ một dải IP khác sẽ đi qua ISP B.

2. **Áp dụng chính sách vào bảng định tuyến**:
   - Chính sách định tuyến được áp dụng bằng các công cụ hỗ trợ Policy Routing, chẳng hạn như:
     - `ip rule` trên Linux.
     - Cấu hình trong các thiết bị mạng của Cisco hoặc Juniper.

3. **Chọn đường đi phù hợp**:
   - Router kiểm tra chính sách trước khi quyết định sử dụng bảng định tuyến.

---

## 4. **Ví dụ minh họa về Policy Routing**

### **Ví dụ 1: Chuyển lưu lượng qua ISP khác nhau**
- Tình huống: Một công ty sử dụng hai nhà mạng là ISP A (VNPT) và ISP B (VIETTEL)
- Yêu cầu:
  - Lưu lượng từ dải IP 192.168.1.0/24 đi qua ISP A.
  - Lưu lượng từ dải IP 192.168.2.0/24 đi qua ISP B.

#### **Cách thực hiện trên Linux**:
1. Thêm các bảng định tuyến:
   ```bash
   echo "1 isp_a" >> /etc/iproute2/rt_tables
   echo "2 isp_b" >> /etc/iproute2/rt_tables
2. Cấu hình bảng định tuyến cho ISP A
    ```bash
    ip route add default via <gateway_ISP_A> table isp_a
3. Cấu hình bảng định tuyến cho ISP B
    ```bash
    ip route add default via <gateway_ISP_B> table isp_b
4. Thêm các quy tắc định tuyến    
    ```bash
    ip rule add from 192.168.1.0/24 table isp_a
ip rule add from 192.168.2.0/24 table isp_b

