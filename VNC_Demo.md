# Họ tên: Nguyễn Trung Hiếu
# Mã sinh viên: 21020017

# Demo sử dụng VNC
Các bước thực hiện như sau:

## Cài đặt docker compose
Cài đặt docker compose thông qua lệnh sau:

`sudo pip install docker-compose`

![Install docker compose](figures\install_docker_compose.png)

## Viết Dockerfile

Để tạo ra một Container, ta cần phải viết `Dockerfile` để định nghĩa Image và các câu lệnh cần chạy. Trong hình dưới là nội dung Dockerfile cho phép cài đặt và cấu hình cho SSH, đồng thời mở các Ports để truy cập từ xa.

![Dockerfile](figures\dockerfile.png)

## Viết docker-compose.yml

Sau đó, để sử dụng được docker compose, trong project cần phải có file `docker-compose.yml`, định nghĩa các containers có trong project. Đồng thời ánh xạ các port của container với port của host để sử dụng cho SSH.

![docker-compose-yml](figures\docker-compose.png)

## Truy cập vào container thông qua SSH

Chạy `apt-get update` để cập nhật các package. 

![update](figures\apt-get-update.png)

Sử dụng port tương ứng với `port 22` của localhost để truy cập vào container.

`ssh root@localhost -p <PORT>`

[^1]: Thay PORT bằNg port tương ứng với port 22 của localhost.

![ssh](figures\log-in-via-ssh.png)

## Cài đặt Desktop Environment và VNC Server

Trong demo này, tôi sử dụng DE `Xfce4` và `Tightvncserver` để làm VNC server. Cài đặt thông qua lệnh sau:

`apt install xfce4 xfce4-goodies tightvncserver`

![vncserver](figures\install-xfce4.png)

## Chạy VNC server

Run `vncserver` để tạo file `~/.vnc/xstartup` và tạo mật khẩu đăng nhập.

![password](figures\set-password.png)

Kill process

`vncserver -kill :1`

![kill](figures\kill_process.png)

Sửa file `~/.vnc/xstartup` và thêm  `startxfce4` vào cuối file. Việc này cho phép run xfce4 mỗi khi run server.

Run VNC server.

![run-again](figures\run_vnc_again.png)

## Kết nối với VNC server
Sử dụng VNC Viewer để kết nối với VNC Server. Địa chỉ kết nối: `localhost:<PORT>` với PORT là port tương ứng với port 5901 của Container.

![connect](figures\connect.png)

Nhập mật khẩu.

![input](figures\input-password.png)

Kết quả nhận được như sau:

![result](figures\result.png)