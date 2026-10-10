# Hướng dẫn đưa TaskOffice lên GitHub Pages

## Trước khi công khai
- Chỉ sử dụng dữ liệu giả lập có sẵn trong website.
- Không nhập văn bản thật, tên cán bộ, thông tin nội bộ hoặc dữ liệu nhạy cảm.
- TaskOffice V4 lưu dữ liệu bằng LocalStorage của trình duyệt; dữ liệu không đồng bộ giữa các máy.
- Đây là website demo tĩnh, chưa có đăng nhập, phân quyền hay máy chủ.

## A. Tạo repository GitHub
1. Đăng nhập GitHub và chọn **New repository**.
2. Đặt tên repository, ví dụ `taskoffice-demo`.
3. Chọn **Public** nếu muốn giảng viên mở được đường dẫn demo; không đưa dữ liệu nhạy cảm vào repository.
4. Tạo repository. Nếu GitHub hỏi tạo README, có thể bỏ chọn vì dự án đã có README.

## B. Tải mã nguồn lên
1. Giải nén `TaskOffice_MVP_V4.zip` trên máy tính.
2. Mở repository vừa tạo trên GitHub.
3. Chọn **Add file → Upload files**.
4. Tải lên các tệp và thư mục bên trong `TaskOffice_MVP_V4` — cần thấy `index.html`, `styles.css`, `app.js`, `README.md`, `DAC_TA_NGHIEP_VU.md` ở thư mục gốc của repository, không nằm trong một thư mục con khác.
5. Chọn **Commit changes**.

## C. Bật GitHub Pages
1. Vào tab **Settings** của repository.
2. Mở mục **Pages** ở thanh bên.
3. Trong **Build and deployment**, chọn **Deploy from a branch**.
4. Chọn branch `main` và folder `/(root)`, sau đó chọn **Save**.
5. Đợi GitHub hoàn tất triển khai. Đường dẫn thường có dạng `https://TEN-TAI-KHOAN.github.io/taskoffice-demo/`.
6. Chỉ sử dụng đường dẫn thật được GitHub hiển thị trong mục Pages; không tự đoán URL.

## D. Kiểm tra sau triển khai
- Mở URL Pages trong cửa sổ trình duyệt mới.
- Kiểm tra các mục Tổng quan, Thông báo kết luận, Quản lý nhiệm vụ, Theo dõi/đôn đốc và Báo cáo tổng hợp.
- Thử thêm một nhiệm vụ giả lập, tải lại trang và kiểm tra dữ liệu còn trong cùng trình duyệt.
- Thử xuất CSV và nhập lại CSV.
- Kiểm tra trên điện thoại hoặc thu nhỏ cửa sổ trình duyệt.
- Nhớ rằng LocalStorage trên URL GitHub Pages tách biệt với dữ liệu khi mở `index.html` trực tiếp trên máy.

## E. Đưa liên kết vào báo cáo
Sau khi triển khai thành công, cập nhật hai dòng trong báo cáo và slide:
- Website demo: `[dán URL Pages được GitHub cung cấp]`
- Mã nguồn: `[dán URL repository]`

Không ghi rằng website đã được triển khai nếu chưa mở URL và kiểm tra thành công.
