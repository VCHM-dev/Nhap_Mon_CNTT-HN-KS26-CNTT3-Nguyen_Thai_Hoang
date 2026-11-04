# Bai9

---

## Phần 1:

### 1. 
* **Cơ chế lưu:** Chrome lưu thông tin đăng nhập trong SQLite và mã hóa bằng DPAI
* **Yếu thế trước Infostealer:** Lợi dụng quyền truy cập của người dùng gọi hàm giải mã hoặc đánh cắp trực tiếp
* **Mối họa với lập trình viên:** Mất toàn bộ session và quyền truy cập tài khoản

### 2. 
* **Zero-Knowledge:** Bên cung cấp không bao giờ biết dữ liệu thực tế của người dùng vì đã đc mã hóa rồi lên máy chủ
* **Client-side Decryption:** Mọi thao tác đều diễn ra trên thiết bị của người dùng, máy chủ chỉ lưu trữ các gói dữ liệu không quan trọng 
* **Máy chủ bị hack dữ liệu có bị lộ không?** **Không.** Kẻ tấn công chỉ thu được dữ liệu mã hóa AES-256 không thể giải mã nếu không có Master Password gốc 

---

## Phần 2:

### 3. Phương pháp tạo Master Passphrase đạt chuẩn
* **Phương pháp:** Kết hợp chuỗi từ ngẫu nhiên  kèm ký tự hoa/thường, số và ký tự đặc biệt để đạt độ dài lớn, dễ nhớ với con người
* **Ví dụ chuẩn:** `Tai-Nghe-Sieu-Tram-2026-PixelForge!`

### 4. Bảng 

| Thông số cấu hình | Giá trị chuẩn áp dụng |
| :--- | :--- |
| **Loại (Type)** | Password |
| **Độ dài (Length)** | Từ **24 đến 32** ký tự |
| **Chữ thường (A-z)** | Bật |
| **Chữ hoa (A-Z)** | Bật |
| **Số (0-9)** | Bật |
| **Ký tự đặc biệt (!@#$)** | Bật |

### 5. 
* Bitwarden không nhìn giao diện để điền mà dựa vào **tên miền gốc chính xác** đã được lưu
* Khi truy cập trang giả mạo , Bitwarden nhận diện sai tên miền và **từ chối tự động điền**, ngăn chặn tuyệt đối việc rò rỉ thông tin

### 6. 
1. **Xuất file:** Tạo tệp PDF chứa Emergency Kit từ tài khoản quản trị Bitwarden
2. **Mã hóa phân đoạn:** Nén và mã hóa tệp bằng phần mềm bảo mật ; chia nhỏ mật khẩu giải nén gửi qua các kênh độc lập
3. **Lưu trữ vật lý:** In bản cứng, niêm phong trong phong bì bảo mật và lưu vào két sắt công ty để phòng sự cố khẩn cấp