# Bài tập lý thuyết

## Tìm hiểu Docker và docker-composer
`Docker` là một nền tảng cho phép các Developers có thể develop, deploy và run applications. Mỗi ứng dụng và các Dependencies sẽ được đóng gói trong một `Container`, tạo ra môi trường độc lập và tách biệt đối với máy chủ. Khi cần phải deploy ứng dụng thì chỉ cần chạy `Container` là tất cả các phần của ứng dụng sẽ được chạy.

`Docker Compose` là một tool cho phép định nghĩa và run một ứng dụng bao gồm nhiều container khác nhau. Ví dụ như một container đảm nhận front-end, một container đảm nhận back-end, một cái khác lại đảm nhận database cho web app. Các containers sẽ giao tiếp với nhau thông qua network được định nghĩa trong file `docker-compose.yml`.

## Linux, Unix, BSD hay *nix? macOs thuộc loại nào?
- `Unix` là một hệ điều hành ra đời từ rất lâu về trước, cụ thể là năm 1969. Unix được cấu trúc theo mô hình `Kernel-Shell`. Kernel là trung tâm của hệ điều hành, quản lý tài nguyên, bộ nhớ, phần cứng và tệp tin. Qua đó, Kernel sẽ phân bổ thời gian cho các chương trình xử lý. Còn Shell là giao diện dòng lệnh của Unix, là nơi giao tiếp giữa người dùng và Kernel. Qua Shell, người dùng có thể sử dụng và tương tác với hệ thống máy tính.

- `BSD` là phiên bản giáo dục của Unix được xây dựng bởi *Computer Systems Research Group*. Do đó, cấu trúc của BSD tương tự với Unix, nhưng cũng có những nét đặc trưng riêng. Ví dụ phiên bản OpenBSD nổi bật với tính năng bảo mật mạnh mẽ, nghiêm ngặt. BSD cũng là nền tảng để phát triển nhiều hệ điều hành thương mại hiện nay như macOs, tvOs, …

- `Linux` thực chất là một loại Kernel được code bởi *Linus Torvalds*, và được sử dụng cho một hệ điều hành khác giống với Unix, GNU. Sự kết hợp của các phần mềm thuộc GNU Project và Linux Kernel đã tạo nên hệ điều hành GNU/ Linux, gọi tắt là Linux. Linux có nhiều điểm tương đồng với Unix và BSD. Tuy nhiên, đây là open source nên người dùng Linux sẽ linh hoạt và thoải mái hơn.

- `*nix` là để chỉ các hệ điều hành thuộc `Unix-Like`, tức là có cách thức hoạt động tương tự với hệ điều hành Unix. Có 3 loại Unix-like: Genetic UNIX, Trademark UNIX và Functional UNIX.

## Alpine và Ubuntu
Alpine và Ubuntu là hai bản phân phối phổ biến của Linux.
- `Alpine` là phiên bản tối giản, cả về không gian và phạm vi. Bên cạnh đó, tính bảo mật cũng cao hơn do sử dụng các tệp position-independent executables để ngẫu nhiên hoá vị trí các chương trình trong bộ nhớ.

- `Ubuntu` là phiên bản đầy đủ hơn, có nhiều features hơn so với Alpine. Ubuntu quản lý các package thông qua APT, tuy nhiên kích thước lớn đồng nghĩa với việc Ubuntu sẽ phải đối mặt với nhiều nguy cơ bị tấn công hơn.

## VNC 
`VNC`, hay `Virtual Network Computing`, là công nghệ cho phép người sử dụng điều khiển và truy cập một máy tính từ xa thông qua Internet. Cụ thể, VNC sẽ cung cấp GUI, quyền sử dụng chuột, bàn phím và các thiết bị khác để tương tác với máy tính. VNC hoạt động theo mô hình Client/Server. Máy tính bị điều khiển đóng vai trò là Server, đợi các kết nối từ Client. Còn máy tính local sử dụng từ xa sẽ sử dụng một trình xem VNC với vai trò là Client kết nối và sử dụng Server.