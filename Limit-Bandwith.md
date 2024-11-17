#  **Tìm Hiểu Về Limit Bandwidth (Giới Hạn Băng Thông)**

**Limit Bandwidth** là kỹ thuật giới hạn tốc độ truyền dữ liệu trong mạng để kiểm soát việc sử dụng băng thông, tối ưu hóa hiệu suất mạng và đảm bảo công bằng giữa các thiết bị hoặc ứng dụng.

---

## 1. **Limit Bandwidth là gì?**
- **Limit Bandwidth** (Giới hạn băng thông) là việc thiết lập mức tối đa dữ liệu có thể truyền đi hoặc nhận được trên một đường mạng trong một khoảng thời gian.
- Thường được áp dụng tại các thiết bị mạng như router, switch, hoặc server.

---

## 2. **Tại sao cần Limit Bandwidth?**
### a. **Quản lý tài nguyên mạng**
- Tránh tình trạng một thiết bị hoặc ứng dụng chiếm hết băng thông.
- Duy trì mạng ổn định khi có nhiều người dùng.

### b. **Cải thiện trải nghiệm người dùng**
- Phân bổ băng thông công bằng, giúp các ứng dụng quan trọng như họp trực tuyến, video call không bị ảnh hưởng.

### c. **Tăng cường bảo mật**
- Hạn chế lưu lượng mạng quá mức từ các thiết bị hoặc ứng dụng đáng ngờ.

### d. **Giảm chi phí**
- Tránh sử dụng vượt mức băng thông, đặc biệt trong môi trường có giới hạn tài nguyên mạng.

---

## 3. **Cách Limit Bandwidth**
### a. **Sử dụng Router**
Hầu hết các router hiện đại đều hỗ trợ tính năng giới hạn băng thông:
1. **Truy cập giao diện quản lý của router**:
   - Vào địa chỉ IP của router (thường là `192.168.1.1` hoặc `192.168.0.1`).
2. **Tìm mục Bandwidth Control (QoS)**:
   - Nằm trong các phần như **Advanced Settings** hoặc **Traffic Management**.
3. **Cấu hình tốc độ**:
   - Gán băng thông tối đa cho từng thiết bị dựa trên địa chỉ IP hoặc MAC Address.

### b. **Sử dụng phần mềm**
- Một số phần mềm hỗ trợ giới hạn băng thông trên từng thiết bị:
  - **NetLimiter** (Windows).
  - **Trickle** (Linux).
  - **Bandwidth+** (macOS).

### c. **Sử dụng lệnh trên Linux**
Ví dụ: Giới hạn băng thông sử dụng **tc** (Traffic Control) trên Linux:
```bash
# Giới hạn tốc độ tải xuống là 1Mbps trên giao diện eth0
sudo tc qdisc add dev eth0 root tbf rate 1mbit burst 32kbit latency 400ms
