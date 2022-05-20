## 1.1 Loading BIOS, Constructing Interrupt Vector Table, and Activating Interrupt Service Routines in the Real Mode

Ta không thể vận hành một máy tính mà không có bất kỳ phần mềm nào.

khi khởi động, bộ nhớ của máy tính (tức là bộ nhớ truy cập ngẫu nhiên [RAM]) trống,và hệ điều hành trên đĩa mềm.
Từ CPU chỉ có thể chạy chương trình trong bộ nhớ của nó,nó không thể chạy OS từ một đĩa mềm .Để chạy được OS nó cần tải vào bộ nhớ từ một đĩa mềm trước tiên

### 1 Procedure for Starting BIOS
Trước khi mô tả cách BIOS tải OS vào trong bộ nhớ,chúng ta nên biết thủ tục để bắt đầu BIOS .Để thực thi một chương trình ta cần phải kích đúp 2 lần 
hoặc vào dòng lệnh trong giao diện  command line trong trường hợp nó thực sự chạy trên OS thực thi

Tuy nhiên hiện tại đang bật nguồn ,không chương trình trong bộ nhớ ,ngay cả với Os


BIOS không thể thực thi theo cách thủ công,ai sẽ thực thi nó ?

it is  0xFFFF0!!!

Từ quan điểm của hệ thống ,chúng ta không thể thực hiện BIOS trên bất kì phần mềm nhưng thay vào đó bằng phần cứng.

Một  Intel 80×86 series CPU có thể làm việc với chế độ  16-bit địa chỉ thực và 32-bit chế độ bảo vệ

![]()
Điều quan trọng nhất ở đây là CPU buộc CS thành 0xFFFF và
IP thành 0x0000; do đó, địa chỉ của CS: IP là 0xFFFF0, như được mô tả trong Hình 1.1, trong đó
chúng ta có thể xác nhận rằng 0xFFFF0 thực sự là địa chỉ của BIOS.

### Tip
IP / EIP: instruction pointer Trong CPU, IP lưu trữ tập hợp các hướng dẫn để được thực thi trong mã.