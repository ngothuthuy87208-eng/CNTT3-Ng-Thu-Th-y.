# BÀI LÀM – HACKATHON 01

- **Mã đề:** 14
- **Họ tên:** Ngô Thu Thúy
- **Lớp:**  CNTT3
- **Link repository:**githup 
- **Hệ điều hành (Windows/macOS):**Windows 

## 4.2. Thao tác máy tính cơ bản bằng CLI

### Các lệnh đã chạy

```shell
# 1:pwd
  2:ls -Force
  3:mv .\huong_dan_cham_soc.txt .\docs
    mv .\logo_nha_khoa.png .\media
  4: cp .\logs .\media
  5:rm .\temp_226.tmp
  6:cd .\logs\
    Get-content .\clinic.log
    cd..

```

### Kết quả liệt kê toàn bộ dự án (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)

```text

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        10/28/2026  10:53 AM                backup
d-----        10/28/2026  11:29 AM                data
d-----        10/28/2026  11:02 AM                docs
d-----        10/28/2026  11:13 AM                logs
d-----        10/28/2026  11:04 AM                media
------        10/27/2026   1:32 AM             65 .env
-a----        10/27/2026   1:32 AM           2224 bai_lam.md


PS C:\Users\MY LAPTOP\Downloads\starter-kit\starter-kit\nha-khoa-website> ls -Recurse -Force


    Directory: C:\Users\MY LAPTOP\Downloads\starter-kit\starter-kit\nha-khoa-website


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        10/28/2026  10:53 AM                backup
d-----        10/28/2026  11:29 AM                data
d-----        10/28/2026  11:02 AM                docs
d-----        10/28/2026  11:13 AM                logs
d-----        10/28/2026  11:04 AM                media
------        10/27/2026   1:32 AM             65 .env
-a----        10/27/2026   1:32 AM           2224 bai_lam.md


    Directory: C:\Users\MY LAPTOP\Downloads\starter-kit\starter-kit\nha-khoa-website\data


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/28/2026  11:29 AM          11044 dieu_tri_thang_4.xlsx
-a-h--        10/28/2026  11:25 AM            165 ~$dieu_tri_thang_4.xlsx


    Directory: C:\Users\MY LAPTOP\Downloads\starter-kit\starter-kit\nha-khoa-website\docs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/27/2026   1:32 AM             63 huong_dan_cham_soc.txt


    Directory: C:\Users\MY LAPTOP\Downloads\starter-kit\starter-kit\nha-khoa-website\logs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/27/2026   1:32 AM           1079 clinic.log
-a----        10/28/2026  11:13 AM            630 daily_report.txt


    Directory: C:\Users\MY LAPTOP\Downloads\starter-kit\starter-kit\nha-khoa-website\media


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        10/28/2026  11:04 AM                logs
-a----        10/27/2026   1:32 AM           5736 logo_nha_khoa.png
```

## 4.3. Lọc log thủ công

### Lệnh đã chạy

```shell
# Get-content .\logs\clinic.log | select-string "ERROR" >logs\daily_report.txt

```

### 2 dòng lỗi đầu tiên trong daily_report.txt

```text
2026-04-28 09:51:29 [ERROR] Ket noi he thong ho so that bai
2026-04-28 10:07:29 [ERROR] Khong tim thay trang /bang-gia-dich-vu (404)

```

## 4.4. Thao tác với tài liệu Markdown (README.md)

> README.md được chấm trực tiếp trên file `README.md` ở gốc dự án. Đánh dấu `[x]` vào các mục đã làm để tự kiểm tra.

- [x] Heading 1: tên dự án
- [x] Mô tả ngắn có cả **in đậm** và *in nghiêng*
- [x] Bảng `Thư mục | Nội dung`, ít nhất 3 dòng dữ liệu
- [x] Code block chứa lệnh PowerShell/Terminal liệt kê nội dung dự án
- [x] Task list ít nhất 2 công việc, có ít nhất 1 mục đã hoàn thành
- [x] Blockquote nhắc không upload `.env`

## 4.5. Chạy script auto_report (.ps1 hoặc .sh)

### Lệnh chạy (Windows: nếu dùng Phụ lục 2 thì ghi cả 2 lệnh)

```shell
# # Tac gia: Ngô Thu Thúy
# Ngay tao: 28/10/2026

"=== BAO CAO LOI GAMEZONE ===" > .\logs\auto_report.txt 
Get-Content .\logs\clinic.log | Select-String "ERROR" >> .\logs\auto_report.txt
Write-Host "Da tao bao cao:"thanh cong"

```

### Kết quả hiển thị

```text
2026-04-28 09:19:29 [INFO] Benh nhan dat lich kham
2026-04-28 09:23:29 [INFO] Gui tin nhan nhac lich
2026-04-28 09:27:29 [WARNING] Thoi gian phan hoi cham
2026-04-28 09:31:29 [WARNING] Anh X-quang dung luong lon
2026-04-28 09:35:29 [INFO] Bac si cap nhat ho so
2026-04-28 09:39:29 [WARNING] Anh X-quang dung luong lon
2026-04-28 09:43:29 [INFO] Bac si cap nhat ho so
2026-04-28 09:47:29 [INFO] Benh nhan dat lich kham
2026-04-28 09:51:29 [ERROR] Ket noi he thong ho so that bai
2026-04-28 09:55:29 [INFO] Benh nhan dat lich kham
2026-04-28 09:59:29 [INFO] Bac si cap nhat ho so
2026-04-28 10:03:29 [INFO] Benh nhan dat lich kham
2026-04-28 10:07:29 [ERROR] Khong tim thay trang /bang-gia-dich-vu (404)
2026-04-28 10:11:29 [WARNING] Lich kham chieu thu bay sap kin
2026-04-28 10:15:29 [INFO] Benh nhan dat lich kham
2026-04-28 10:19:29 [ERROR] Ket noi he thong ho so that bai
2026-04-28 10:23:29 [INFO] Xac nhan lich hen
2026-04-28 10:27:29 [ERROR] Ket noi he thong ho so that bai
2026-04-28 10:31:29 [INFO] Thanh toan thanh cong
2026-04-28 10:35:29 [ERROR] Dat lich hen that bai


```

## 4.6. Đếm số dòng lỗi

### Lệnh

```shell
# (Get-content .\logs\clinic.log | select-string "ERROR").count

```

### Kết quả đếm (Windows: giá trị Count; macOS: con số in ra)

```text
5
```

## 4.7. Báo cáo tổng hợp

### Các lệnh đã chạy

```shell
# Ghi lần lượt các lệnh đã chạy, mỗi lệnh một dòng (xoá dòng này)

```

### Nội dung file logs/tong_hop.txt

```text
(Dán kết quả vào đây – xoá dòng này)

```

## 4.8. Excel

> Phần Excel được chấm trực tiếp trên file `data/dieu_tri_thang_4.xlsx`, không cần ghi vào đây.
