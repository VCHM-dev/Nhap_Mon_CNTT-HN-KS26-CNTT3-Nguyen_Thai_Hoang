# Bài 7

## Phần 1: Phân tích hiểm họa, lỗi vi phạm
1. **3 sai lầm chí mạng:**
   - Mở file đính kèm lạ từ email chưa kiểm thực danh tính người gửi
   - Tắt hoàn toàn phần mềm bảo vệ (Windows Defender/Antivirus) để cài phần mềm Crack
   - Thiếu cảnh giác với các chiêu trò mồi nhử tài chính

2. **Kỹ thuật tấn công, mục đích:**
   - **Typosquatting:** Dùng tên miền giả mạo một ký tự (`epig-games.com` thay vì `epicgames.com`) để đánh lừa thị giác
   - **Double Extension (Đuôi file kép):** Đặt tên file là `Sponsorship_Agreement_v2.pdf.exe` nhưng lợi dụng Windows ẩn đuôi file để hiển thị thành `Sponsorship_Agreement_v2.pdf`, dụ người dùng bấm mở file thực thi mã độc

3. **Bản chất phần mềm Crack, infostealer:**
   - Trang crack yêu cầu tắt Antivirus để phần mềm độc hại không bị chặn khi thực thi
   - Trong 2 giây màn hình nhấp nháy, mã độc **Infostealer** đã âm thầm quét RAM, trích xuất session cookies, token Discord/Steam và các SSH Key trên máy tính

## Phần 2: Phương án Cấp cứu, phòng ngừa
4. **Quy trình Cấp cứu 4 Bước:**
   - **Bước 1:** Ngắt mạng khẩn cấp để chặn kết nối dữ liệu về máy chủ C2 của hacker
   - **Bước 2:** Đổi toàn bộ mật khẩu tài khoản quan trọng từ một thiết bị sạch khác
   - **Bước 3:** Thu hồi toàn bộ Access Tokens, API Keys, và SSH Keys đang liên kết với dự án
   - **Bước 4:** Cài lại toàn bộ hệ điều hành để loại bỏ triệt để mã độc ẩn sâu

5. **2 thiết lập cấu hình trên Windows chống đuôi file kép:**
   - Mở File Explorer ➔ Chọn tab **View** (hoặc Options) ➔ Tích **bỏ** chọn mục **Hide extensions for known file types**
   - Thiết lập mở rộng hiển thị các file ẩn/hệ thống khi cần thiết
