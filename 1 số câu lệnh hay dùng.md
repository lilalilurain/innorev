## Tạo port kết nối 2 máy 

B1: ping địa chỉ xem 2 máy có thông với nhau không 

B2: 
```
python -m http.server + port (tự đặt)
```

ví dụ: python -m http.server 1234

b3: truy cập http:// địa chỉ máy:port (ví dụ: 182.168.9.105:1234)

## Địa chỉ host
182.168.9.104 

port: 8077


Tài khoản 182.168.9.104:8077: innorev

pass: Innorev@123 (M28), 123456 (P27)


Tài khoản ftp dùng chung 

link: ftp://182.168.9.104

user: ftpUser

pass: ftp31gl

## Kiểm tra cổng sino
```
ls /dev/ttU*
```

Sau khi kiểm tra số lượng cổng:
```
bash DemoStart.sh
```

## Cấp quyền Chrome cho Mars
```
sudo chmod +x /home/innorev/Mars/stationmanager
```
