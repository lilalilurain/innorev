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

Sau khi kiểm tra số lượng cổng mở innorev.debug, nếu không lên thì check lỗi:
```
bash DemoStart.sh
```
M28 thường có 4 cổng, P27 6 cổng

## Cấp quyền Chrome cho Mars
```
sudo chmod +x /home/innorev/Mars/stationmanager
```

## Tạo auto service ngoài desktop nếu config có thêm group
```
python install_autoservice.py --create-shortcut "AutoService" --station-type FATP-CAM-COMBO-2
```
## Kiểm tra tường lửa
```
sudo ufw status
```
## Cài IMUC
IMUC có thể chạy chung trên 1 ubuntu, cần nhờ bên anh Đức set port trước (2 port khác nhau và không trùng với port IMUT)

Trước khi run cần tắt đọc PLC. Mở file .yaml trong station sửa simulation trong hàm station_name thành true.
Trong file AutoService mở terminal chạy lệnh:
```
python run.py --config "config/L1/IMUC/service/IMUC_01.json"
```
Mở 1 terminal khác (không chạy cùng 1 terminal):
```
python run.py --config "config/L1/IMUC/service/IMUC_02.json"
```

