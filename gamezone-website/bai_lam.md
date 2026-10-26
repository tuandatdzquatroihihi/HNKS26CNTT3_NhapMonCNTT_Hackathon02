# BÀI LÀM – THI THỬ HACKATHON 02 (GAMEZONE)

- **Họ tên:** Đào Tuấn Đạt   
- **Lớp:** HNKS26CNTT3
- **Link repository:** [GitHub](https://github.com/tuandatdzquatroihihi/HNKS26CNTT3_NhapMonCNTT_Hackathon02)
- **Hệ điều hành (Windows/macOS):** Windows

## 4.2. Thao tác CLI

### Các lệnh đã chạy

```shell
pwd
ls -r -Force
mv .\cap_nhat.txt .\docs\
mv .\logo_gamezone.png .\media\
cp .\media\logo_gamezone.png .\backup\
rm -r *.tmp
cd .\logs\
ls -r
cd ..
```

### Kết quả liệt kê toàn bộ dự án

```text
    Directory: D:\de-on-tap-game\starter-kit\gamezone-website\logs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/26/2026   1:10 PM            986 game.log


PS D:\de-on-tap-game\starter-kit\gamezone-website\logs> cd ..
PS D:\de-on-tap-game\starter-kit\gamezone-website> ls -r -Force


    Directory: D:\de-on-tap-game\starter-kit\gamezone-website


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        10/26/2026   1:14 PM                backup
d-----        10/26/2026   1:15 PM                data
d-----        10/26/2026   1:17 PM                docs
d-----        10/26/2026   1:15 PM                logs
d-----        10/26/2026   1:18 PM                media
-a----        10/26/2026   1:10 PM             70 .env


    Directory: D:\de-on-tap-game\starter-kit\gamezone-website\backup


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/26/2026   1:10 PM           8542 logo_gamezone.png


    Directory: D:\de-on-tap-game\starter-kit\gamezone-website\data


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/26/2026   1:10 PM           5814 giao_dich_thang_11.xlsx


    Directory: D:\de-on-tap-game\starter-kit\gamezone-website\docs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/26/2026   1:10 PM             61 cap_nhat.txt


    Directory: D:\de-on-tap-game\starter-kit\gamezone-website\logs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/26/2026   1:10 PM            986 game.log


    Directory: D:\de-on-tap-game\starter-kit\gamezone-website\media


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/26/2026   1:10 PM           8542 logo_gamezone.png
```

## 4.3. Lọc log thủ công

### Lệnh đã chạy

```shell
cat .\logs\game.log | Select-String "ERROR" > .\logs\daily_report.txt
```

### 2 dòng lỗi đầu tiên trong daily_report.txt

```text
2025-11-05 08:03:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:09:15 [ERROR] Mat ket noi may chu game
```

## 4.4. README.md

> Chấm trực tiếp trên `README.md` ở gốc dự án.

- [x] Heading 1
- [x] Mô tả in đậm + in nghiêng
- [x] Bảng `Thư mục | Nội dung` (≥3 dòng)
- [x] Code block lệnh liệt kê
- [x] Task list (≥2 việc, ≥1 đã xong)
- [x] Blockquote nhắc không upload `.env`

## 4.5. Chạy script auto_report

### Lệnh chạy

```shell
.\auto_report_khung.ps1
```

### Nội dung file logs/auto_report.txt

```text
=== BAO CAO LOI GAMEZONE ===

2025-11-05 08:03:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:09:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:12:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:39:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:42:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:51:15 [ERROR] Loi luu tien trinh choi
```

## 4.6. Đếm số dòng lỗi

### Lệnh

```shell
(cat .\logs\game.log | select-string "ERROR").count
```

### Kết quả đếm

```text
6

```

## 4.7. Báo cáo tổng hợp

### Các lệnh đã chạy

```shell
"=== TONG HOP LOG GAMEZONE" > .\logs\tong_hop.txt
cat .\logs\game.log | select-string "WARNING" >> .\logs\tong_hop.txt
cat .\logs\game.log | Select-String "ERROR" >> .\logs\tong_hop.txt
```

### Nội dung file logs/tong_hop.txt

```text
=== TONG HOP LOG GAMEZONE

2025-11-05 08:54:15 [WARNING] May chu qua tai CPU 90%



2025-11-05 08:03:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:09:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:12:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:39:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:42:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:51:15 [ERROR] Loi luu tien trinh choi
```

## 4.8. Excel

> Chấm trực tiếp trên file `data/giao_dich_thang_11.xlsx`.
