# Docker Image
***
## Khái niệm
- Image trong docker là những phần mềm được đóng góp và quản lý bởi docker
- Khi Image được docker khởi chạy thì gọi là Container
## Các lệnh cơ bản trong Docker
Để hiển thị thông tin các Image thực hiện lệnh 
```
docker images
```
Tim Image trên trang chủ của docker sử dụng lệnh
```
docker search
```
Để tải Image sử dụng lệnh sau
```
docker pull <tên image>:<tag>
```
Xóa image
```
docker image rm <tên image>:<tag>
docker image rm <id image>
```
Chạy một container
```
docker run [OPTIONS] IMAGE [COMMAND] [ARG...]
```
Trong đó:
- [OPTIONS] các thiết lập khi tạo container, có rất nhiều thiết lập tùy mục đích tạo container. Ví dụ -it, t cho phép kết nối terminal, i duy trì mở stdin để nhập lệnh.
- IMAGE tên image hoặc ID của image từ nó sinh ra container.
- [COMMAND] [ARG...] lệnh và tham số khi container chạy.

Kiểm tra xem có container nào đang chạy và tất cả container
```
docker ps
docker ps -a
```
Để chạy container mà đang dừng, sử dụng
```
docker start <ID>
```
Muốn vào container sử dụng
```
docker attach <ID>
```
Muốn thoát khỏi container mà nó vẫn tiếp tục chạy dùng tổ hợp phím Ctrl+P+Q

Muốn dừng container lại
```
docker stop <tên hoặc id>
```
Đặt tên cho container
```
docker run -it --name "CONTAINER NAME"  -h HOSTNAME image
```
Xóa container
```
docker rm -f <ID>
```