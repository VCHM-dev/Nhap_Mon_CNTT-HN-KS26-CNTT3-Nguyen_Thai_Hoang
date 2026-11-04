# Bai8

## Phần 1:

### 1.
* **`OPENAI_API_KEY`**: Bị kẻ xấu hoặc bot tự động đánh cắp gọi mô hình AI (GPT-4) trái phép, gây thiệt hại tài chính lớn
* **`STEAM_WEB_API_KEY`**: Bị lợi dụng truy cập Web API Steam, thao túng dữ liệu hoặc thông tin tài khoản người dùng, gây rò rỉ hệ thống
* **`MONGO_URI`**: Lộ quyền quản trị cơ sở dữ liệu MongoDB Atlas, hacker có thể đánh cắp toàn bộ dữ liệu người chơi game hoặc phá hủy/xóa (`Drop Database`) cơ sở dữ liệu
* **`JWT_SECRET`**: Lộ khóa mã hóa token đăng nhập, cho phép hacker tự tạo Token giả mạo quyền Admin để chiếm quyền điều khiển bất kỳ tài khoản nào

### 2. 
* **GitHub Scraper Bot:** Các bot tự động trên mạng quét và cào toàn bộ API Key trên các public repository trong vòng **vài giây** sau khi push
* **Lịch sử Git (Git History):** Dù xóa file hoặc đổi quyền repo, các commit cũ vẫn lưu trữ trên local cache hoặc hệ thống ngầm. Do đó buộc phải thu hồi (`Revoke`) và tạo khóa mới lập tức trên bảng điều khiển nhà cung cấp

---

## Phần 2: 

### 3.
```env
PORT=3000
OPENAI_API_KEY=sk-proj-998822abcfed7711aaff00998877665544332211
STEAM_WEB_API_KEY=STEAM_SECRET_KEY_882910AAFFBBDD
MONGO_URI=mongodb+srv://admin_root:SuperSecretPass2026@cluster0.pixelforge.net/cyberrealm_db
JWT_SECRET=pixel_forge_super_private_token_key_9988
```