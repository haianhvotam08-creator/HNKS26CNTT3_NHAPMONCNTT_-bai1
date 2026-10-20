

# Bài làm Ngày 1 - Nhập môn Công nghệ Thông tin
**Họ và tên: Nguyễn Hải Anh**  
**Lớp: CNTT3**  
Markdown
---
## Phần A - Tổ chức thư mục bằng GUI*(Đã hoàn thành các thao tác trên giao diện File Explorer)*
---
## Phần B - Thao tác bằng CLI (PowerShell)
### B1. Hiển thị đường dẫn tuyệt đối của thư mục hiện tại```powershell
pwd
Output:
Path 
----
C:\Users\Admin\trung-tam-tieng-anh
Liệt kê nội dung file ẩn
ls -Force
Output:
Directory: C:\Users\Admin\trung-tam-tieng-anh
Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        20/10/2026   19:00                archive
d-----        20/10/2026   19:00                data
d-----        20/10/2026   19:00                docs
d-----        20/10/2026   19:00                logs
d-----        20/10/2026   19:00                media
-a----        20/10/2026   19:00          12bai_lam_ngay1.md
-a-h--        20/10/2026   19:00             45 .env
B3 di chuyển file lịch học vào docs di chuyển logo và ảnh lớp học và media
mv lich_hoc.txt docs/
mv logo_trung_tam.png media/
mv anh_lop_hoc.jpg media/
B4 Sao chép logo từ media vào archive
cp media/logo_trung_tam.png archive/
B5 Xóa 2 file.tmp tại thư mục gốc
rm temp_201.tmp
rm temp_202.tmp
B6 Dùng đường dẫn tương đối vào logs, liệt kê nội dung rồi quay lại thư mục gốc
cd logs
ls
cd ..
B7 Di chuyển vào docs, dùng đường dẫn tương đối sao chép ảnh lớp học từ media sang archive, quay lại thư mục gốc
cd docs
cp ../media/anh_lop_hoc.jpg ../archive/
cd ..
B8 Get-ChildItem -r -force  ```  ### Kết quả B1 (pwd)  ```PowerShell  pwd  D:\Project_CNTT\testNMCNTT\trung-tam-tieng-anh  ```  ### Kết quả liệt kê toàn bộ dự án – B8 (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)  ```PowerShell  Get-ChildItem -r -force  Directory: D:\Project_CNTT\testNMCNTT\trung-tam-tieng-anh  Mode LastWriteTime Length Name  ---- ------------- ------ ----  d----- 10/20/2026 9:01 PM archive  d----- 10/20/2026 8:33 PM data  d----- 10/20/2026 8:47 PM docs  d----- 10/20/2026 8:33 PM logs  d----- 10/20/2026 8:51 PM media  d----- 10/20/2026 8:53 PM Trung Tam Tieng Anh FINAL  ------ 10/19/2026 10:04 AM 902 bai_lam_ngay1.md  Directory: D:\Project_CNTT\testNMCNTT\trung-tam-tieng-anh\archive  Mode LastWriteTime Length Name  ---- ------------- ------ ----  -a---- 10/19/2026 10:04 AM 13559 anh_lop_hoc.JPG  -a---- 10/19/2026 10:04 AM 5184 logo_trung_tam.PNG  Directory: D:\Project_CNTT\testNMCNTT\trung-tam-tieng-anh\data  Mode LastWriteTime Length Name  ---- ------------- ------ ----  -a---- 10/19/2026 10:04 AM 5070 hoc_vien_khoa_3.xlsx  Directory: D:\Project_CNTT\testNMCNTT\trung-tam-tieng-anh\docs  Mode LastWriteTime Length Name  ---- ------------- ------ ----  -a---- 10/19/2026 10:04 AM 67 lich_hoc.txt  Directory: D:\Project_CNTT\testNMCNTT\trung-tam-tieng-anh\logs  Mode LastWriteTime Length Name  ---- ------------- ------ ----  -a---- 10/19/2026 10:04 AM 1072 access.log  Directory: D:\Project_CNTT\testNMCNTT\trung-tam-tieng-anh\media  Mode LastWriteTime Length Name  ---- ------------- ------ ----  -a---- 10/19/2026 10:04 AM 13559 anh_lop_hoc.JPG  -a---- 10/19/2026 10:04 AM 5184 logo_trung_tam.PNG  Directory: D:\Project_CNTT\testNMCNTT\trung-tam-tieng-anh\Trung Tam Tieng Anh FINAL  Mode LastWriteTime Length Name  ---- ------------- ------ ----  ------ 10/19/2026 10:04 AM 83 .env  -a---- 10/19/2026 10:04 AM 902 bai_lam_ngay1.md  ```
   

