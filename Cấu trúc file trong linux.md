 # Mục lục
[Cấu trúc thư mục](#cấu-trúc-thư-mục)
- [Root – Thư mục gốc](#1---root--thư-mục-gốc)
- [2. /bin – Các tập tin thực thi của người dùng](#2-bin--các-tập-tin-thực-thi-của-người-dùng)
- [3. /sbin – Các tập tin thực thi của hệ thống](#3-sbin--các-tập-tin-thực-thi-của-hệ-thống)
- [4. /etc – Các tập tin cấu hình](#4-etc--các-tập-tin-cấu-hình)

[Quản lý memory của linux](#quản-lý-memory-của-linux)


 
 ## Cấu trúc thư mục
 
 Sơ lược thì hệ thống thư mục của ubuntu sẽ như sau:
 ![alt](https://raw.githubusercontent.com/anh1609/Linux/main/t%E1%BB%87p-h%C3%ACnh%20%E1%BA%A3nh/h%C3%ACnh%20%E1%BA%A3nh%20linux/treelinux.jpg)
 
 ## 1. / – Root – Thư mục gốc
 
 + Mỗi tập tin đơn và thư mục được bắt đầu thư mục gốc.
+ Chỉ người dùng root mới có quyền ghi trong thư mục này.
+ Lưu ý: rằng thư mục /root là thư mục của người dùng root chứ không phải là thư mục /.

## 2. /bin – Các tập tin thực thi của người dùng
+ Chứa các tập tin thực thi.
+ Các lệnh thường dùng của Linux mà bạn cần để dùng trong chế độ người dùng đơn được lưu ở đây.
+ Các lệnh được sử dụng bởi tất cả người dùng trong hệ thống được lưu ở đây.
Ví dụ: ps, ls, ping, grep, cp.

## 3. /sbin – Các tập tin thực thi của hệ thống
+ Giống như /bin, /sbin cũng chứa các tập tin thực thi.
+ Nhưng, các lệnh được lưu trong thư mục này về cơ bản được dùng cho người quản trị và được dùng để bảo trì hệ thống.
* Ví dụ: iptables, reboot, fdisk, ifconfig, swapon

## 4. /etc – Các tập tin cấu hình
+ Chứa các tập tin cấu hình cần thiết cho tất cả các chương trình.
+ Nó cũng chứa các đoạn mã khởi động và tắt mà được dùng để khởi động/dừng các chương trình đơn lẻ.
Ví dụ: /etc/resolv.conf, /etc/logrotate.conf

## 5. /dev – Các tập tin thiết bị
+ Chứa các tập tin thiết bị.
+ Nó chứa các tập tin thiết bị đầu cuối như là USB hay bất kỳ thiết bị nào gắn vào hệ thống.
Ví dụ: /dev/tty1, /dev/usbmon0

## 6. /proc – Thông tin tiến trình

+ Chứa thông tin về các tiến trình của hệ thống.
+ Như các tập tin chứa thông tin về các tiến trình đang chạy. Ví dụ: /proc/{pid} directory >>> lưu thông tin về tiến trình với pid bạn chọn.
+ Hay các tập tin hệ thống ảo với nội dung về tài nguyên hệ thống. Ví dụ: /proc/uptime

## 7. /var – Các tập tin biến đổi
+ var là viết tắt của các tập tin biến đổi.
+ Gồm những tập tin mà dung lượng lớn dần theo thời gian sử dụng.
+ Chẳng hạn — các tập tin ghi chú hệ thống (/var/log); các gói và các tập tin cơ sở dữ liệu (/var/lib); thư điện tử (/var/mail); hàng đợi – in queues (/var/spool); các tập tin khóa (/var/lock); các tập tin tạm được dùng khi khởi động lại (/var/tmp). 

## 8. /tmp – Thư mục chứa các tập tin tạm
+ Thư mục chứa các tập tin tạm được tạo bởi hệ thống và người dùng.
Các tập tin trong thư mục này bị xóa khi hệ thống khởi động lại.

## 9. /usr – Các chương trình của người dùng
+ Tập trung các tập tin thực thi, thư viện, tài liệu, và mã nguồn cho các chương trình mức độ thứ hai.
+ /usr/bin chứa các tập tin thực thi cho các chương trình của người dùng. Nếu bạn không thể tìm thấy trong thư mục /bin thì tìm trong /usr/bin. Ví dụ: at, awk, cc, less, scp
+ /usr/sbin chứa các tập tin thực thi cho quản trị hệ thống. Nếu bạn không thể tìm thấy trong /sbin thì tìm trong /usr/sbin. Ví dụ: atd, cron, sshd, useradd, userdel
+ /usr/lib chứa các tập tin thư viện /usr/bin và /usr/sbin
+ /usr/local chứa các chương trình của người dùng mà bạn cài từ mã nguồn. Ví dụ, khi bạn cài Apache từ mã nguồn, nó được đưa vào thư mục /usr/local/apache2z

## 10. /home – Thư mục người dùng10. /home – Thư mục người dùng

+ Chứa các tập tin của các người dùng trong hệ thống.
Ví dụ: /home/john, /home/nikita

## 11. /boot – Các tập tin của chương trình khởi động máy
+ Chứa những tập tin liên quan tới chương trình quản lý khởi động máy.
+ Các tập tin initrd, vmlinux, grub được lưu trong thư mục /boot
Ví dụ: initrd.img-2.6.32-24-generic, vmlinuz-2.6.32-24-generic

# 12. /lib – Các tập tin thư viện của hệ thống
+ Chứa các tập tin thư viện để hỗ trợ các tập tin thực thi được lưu trong /bin và /sbin
- Tên của các tập tin này là ld* hay lib*.so.*
Ví dụ: ld-2.11.1.so, libncurses.so.5.7

## 13. /opt – Các ứng dụng tùy chọn hay thêm

- opt là viết tắt của optional.
- Chứa các ứng dụng thêm của các hãng khác nhau.
Các ứng dụng thêm nên được cài trong thư mục con của thư mục /opt/.

## 14. /mnt – Thư mục Mount
_ Thư mục mount tạm thời nơi mà người quản trị hệ thống có thể mount các tập tin hệ thống.

## 15. /media – Các thiết bị tháo lắp
- Thư mục chưa các mount tạm thời cho các thiết bị tháo lắp.
Ví dụ: /medica/cdrom cho CD-ROM; /media/floppy cho ổ đĩa mềm; /media/cdrecorder cho ổ đĩa ghi CD.

## 16. /srv – Dữ liệu dịch vụ-
- srv là viết tắt của service.
- Chứa dữ liệu liên quan tới các dịch vụ trên máy chủ.
Ví dụ: /srv/cvs chứa dữ liệu liên quan tới CVS.


# Quản lý memory của linux



