# AutoService Thao tác triển khai đơn giản SOP (Phiên bản tiếng Việt)[cite: 1]

**Số phiên bản:** 20260322_1[cite: 1]

---

## Mục lục
1. [Cấu hình địa chỉ IP](#1-cấu-hình-địa-chỉ-ip)[cite: 1]
2. [Cài đặt AutoService](#2-cài-đặt-autoservice)[cite: 1]
3. [Khác](#3-khác)[cite: 1]

---

## 1. Cấu hình địa chỉ IP

Trước khi cài đặt AutoService, cần đảm bảo cáp mạng của máy tính đã được kết nối bình thường và địa chỉ IP mạng đã được cấu hình chính xác[cite: 1].

**Bảng địa chỉ IP của dây chuyền đóng gói:**[cite: 1]

| Tên thiết bị | Địa chỉ IP |
| :--- | :--- |
| GDS-1 | `192.168.1.30` |
| Provision-1 | `192.168.1.32` |
| Provision-2 | `192.168.1.33` |
| Provision-3 | `192.168.1.34` |
| Provision-4 | `192.168.1.35` |
| Provision-5 | `192.168.1.36` |
| Provision-6 | `192.168.1.37` |
| Provision-7 | `192.168.1.38` |
| Provision-8 | `192.168.1.39` |
| Freset-1 | `192.168.1.51` |
| Freset-2 | `192.168.1.52` |
| Freset-3 | `192.168.1.53` |
| Freset-4 | `192.168.1.54` |[cite: 1]

### Các bước thực hiện:
1. Nhấn vào góc trên bên phải màn hình, chọn **Settings**[cite: 1].
2. Tìm mục **Network**, nhấp vào nút cài đặt mạng và truy cập vào đó *(tại đây sẽ hiển thị hai tùy chọn mạng, một là `CVC`, còn tùy chọn chúng ta cần cài đặt là `AutoService`)*[cite: 1].
3. Nhấn chọn **IPv4**, tích vào tùy chọn **Manual**, điền địa chỉ IP của máy kiểm thử tương ứng vào ô **Address** phía dưới, nhập `24` vào mục **Netmask**, rồi nhấn **Apply** để lưu lại[cite: 1].

---

## 2. Cài đặt AutoService

1. Tìm gói nén `AutoService` (`AutoService.zip`), nếu không có thì bạn có thể nén một bản sao từ thiết bị đang hoạt động bình thường khác rồi mang sang[cite: 1]. Đặt gói nén `AutoService` vào thư mục **Home** và giải nén nó[cite: 1].
2. Truy cập thư mục `AutoService`, tìm tệp nén `AutoServiceWeb_whl.zip` rồi giải nén tệp đó[cite: 1].
3. Truy cập vào thư mục `AutoServiceWeb_whl`, sau đó tiếp tục truy cập vào thư mục `web_whl`, nhấp chuột phải chọn **Open in Terminal**, nhập lệnh sau rồi nhấn phím **Enter**:[cite: 1]
   ```bash
   bash run.sh
   ```[cite: 1]
4. Quay lại thư mục `AutoService`, tìm tệp `AutoService.desktop` và sao chép nó vào thư mục **Desktop** nằm trong thư mục **Home**[cite: 1].
5. Nhấp đúp chuột vào tệp `AutoService.desktop` và tìm dòng đường dẫn bên dưới[cite: 1]. Đây là đường dẫn thực thi của AutoService; nếu đường dẫn không đúng, bạn sẽ không thể mở được ứng dụng[cite: 1]:
   ```ini
   Exec=bash /home/sta5fatpflashre010/AutoService/AutoService.sh
   ```[cite: 1]
6. Quay lại thư mục `AutoService`, nhấn tổ hợp phím `Ctrl + L` để hiển thị đường dẫn của thư mục hiện tại *(ví dụ: `/home/innorev/AutoService/`)*, sau đó sao chép đường dẫn này[cite: 1].
7. Thay thế đường dẫn trong tệp `AutoService.desktop`, sau đó lưu và thoát[cite: 1]:
   ```ini
   Exec=bash /home/innorev/AutoService/AutoService.sh
   ```[cite: 1]
8. Quay lại màn hình chính, bạn sẽ thấy tệp `AutoService.desktop` xuất hiện[cite: 1]. Hãy nhấp chuột phải vào tệp này, chọn mục **Allow Launching**, sau đó bạn có thể khởi chạy AutoService bình thường[cite: 1].

---

## 3. Khác

> **Lưu ý:** Để AutoService hoạt động bình thường, tất cả cấu hình của **Mars** phải chính xác; nếu không, hệ thống sẽ hiển thị thông báo lỗi[cite: 1].
