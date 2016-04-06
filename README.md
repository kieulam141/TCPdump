#Tổng quan TCPDump
## Mục lục
[1.Khái niệm] (#1)

[2.Cấu trúc] (#2)

[3.Ví dụ] (#3)

<a name="1"></a>
### 1.Khái niệm

- TCPDump là 1 công cụ nghe lén cũng như phân tích gói tin rất mạnh và được sử dụng rộng rãi.
- Nó bắt hoặc lọc các gói tin TCP/IP được truyền trên mạng qua card mạng nào đó.
- Nó được sử dụng bởi hầu hết các hệ điều hành unix/linux.
- Chúng ta có thể lưu lại những thông tin mà nó bắt được thành file định dạng pcap. 
Sau đó có thể xem lại bằng lệnh tcpdump hoặc phần mềm wireshark.

<a name="2"></a>
### 2.Cấu trúc
#### tcpdump tùy chọn
*Các tùy chọn*
- `-i tên interface` lắng nghe trên *interface* được chọn, nếu không tcpdump sẽ tìm danh sách interface trong hệ thống từ bé đến lớn,
mà những interface đó đã được cấu hình và có thể bật lên.
- `-c count` dừng lại sau khi nhận *count* gói tin.
- `-A` thể hiện gói tin với định dạng ASCII.1 dạng chương trình mã hóa kí tự.
- `-XX` thể hiện gói tin với định dạng Hex và ASCII
- `-D` show ra những interface có trên hệ thống.
- `-w tên file` capture và lưu lại thành file .pcap.
- `-r tên file` đọc và phân tích các gói tin đã chụp được.
- `-n` khi không có tùy chọn -n thì trên màn hình sẽ hiển thị ra hostname của máy, nếu muốn hiển thị ip address thì thêm tùy chọn này.
- thêm tùy chọn `tcp` vào sau để chỉ bắt gói tin tcp.
- thêm tùy chọn `port + number` để bắt các gói tin của port đấy.
- thêm tùy chọn `src + ip` để bắt các gói tin có source là ip.
- thêm tùy chọn `dst + ip` để bắt các gói tin có destination là ip.

<a name="3"></a>
### 3.Ví dụ
Trong các ví dụ tôi sẽ thêm tùy chọn -c để tiện cho việc theo dõi.

- a.Chỉ bắt c gói tin.
<img src="http://i.imgur.com/myKohdz.png" />

- b.Thể hiện gói tin với định dạng ASCII
<img src="http://i.imgur.com/or7VzVB.png" height=50% weight=50% />

- c.Thể hiện gói tin với định dạng Hex và ASCII
<img src="http://i.imgur.com/Q8JEBXE.png" height=60% weight=50% />

- d.Show ra những interface có trên hệ thống
<img src="http://i.imgur.com/v1krrCq.png" >

- e.Capture và lưu lại thành file .pcap
<img src="http://i.imgur.com/u4nR6o5.png" />

- f.Đọc và phân tích các gói tin đã chụp được
<img src="http://i.imgur.com/2wiHStZ.png" />

- g.Hiển thị ip address
<img src="http://i.imgur.com/x5fHoDj.png" />

- h.Bắt gói tin tcp
<img src="http://i.imgur.com/FYaoKu2.png" />

- i.bắt các gói tin theo port
Trước đó tôi đã telnet vào.
<img src="http://i.imgur.com/EhZdQC4.png" />

- k.Bắt gói tin theo source
<img src="http://i.imgur.com/yOtwfM2.png" />

- l.Bắt gói tin theo destination
<img src="http://i.imgur.com/01h8ohM.png" />
