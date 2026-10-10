# TaskOffice MVP V4

**Tên đề tài:** Xây dựng website TaskOffice – Công cụ hỗ trợ theo dõi, đôn đốc và tổng hợp tiến độ thực hiện nhiệm vụ.

## 1. Phạm vi
Website minh họa gồm 5 khu vực: Tổng quan nhiệm vụ; Quản lý thông báo kết luận; Quản lý nhiệm vụ; Theo dõi, đôn đốc; Báo cáo tổng hợp.

## 2. Chức năng hiện có
- Thêm/sửa thông báo kết luận giả lập và nhiệm vụ.
- Liên kết nhiệm vụ với văn bản nguồn; lọc theo trạng thái, đơn vị và thời hạn.
- Ghi lịch sử cập nhật và lịch sử đôn đốc.
- Phân loại nhiệm vụ quá hạn, sắp đến hạn (trong 3 ngày) và lâu chưa cập nhật (từ 5 ngày).
- Xuất báo cáo/danh sách nhiệm vụ CSV; nhập CSV với kiểm tra dữ liệu.
- Khi nhập CSV, số hiệu văn bản nguồn phải khớp chính xác (không phân biệt hoa/thường và khoảng trắng ngoài). Dòng không khớp văn bản bị bỏ qua, không tự gắn nhầm vào văn bản đầu tiên.
- Ghi lịch sử khi thay đổi trạng thái, tiến độ, kết quả, đơn vị chủ trì, thời hạn hoặc văn bản nguồn.

## 3. Cách chạy
1. Giải nén tệp ZIP.
2. Mở `index.html` bằng trình duyệt hiện đại.
3. Không cần cài đặt máy chủ hoặc thư viện ngoài.

## 4. Công nghệ
HTML5, CSS3, JavaScript thuần, LocalStorage, CSV, Git/GitHub.

## 5. Cấu trúc
- `index.html`: giao diện 5 khu vực.
- `styles.css`: kiểu giao diện và responsive.
- `app.js`: dữ liệu minh họa và logic nghiệp vụ.
- `DAC_TA_NGHIEP_VU.md`: mô tả bài toán, vai trò, quy tắc theo dõi.

## 6. Giới hạn và an toàn dữ liệu
- Dữ liệu ban đầu là dữ liệu giả lập, không dùng văn bản thật, dữ liệu cá nhân hay thông tin nội bộ.
- Dữ liệu lưu trên LocalStorage của trình duyệt hiện tại; không đồng bộ giữa thiết bị, không có đăng nhập/phân quyền, máy chủ hay cơ sở dữ liệu tập trung.
- Đây là nguyên mẫu phục vụ học tập, không thay thế hệ thống quản lý văn bản chính thức.

## 7. Kiểm thử gợi ý
1. Mở trang và kiểm tra 5 khu vực, số liệu tổng quan.
2. Thêm nhiệm vụ, thử nhập thời hạn trước ngày giao và xác nhận hệ thống chặn lưu.
3. Cập nhật trạng thái/tiến độ/đơn vị/thời hạn rồi mở lại nhiệm vụ để xem lịch sử.
4. Ghi nhận đôn đốc và kiểm tra lịch sử.
5. Xuất danh sách nhiệm vụ CSV; nhập lại tệp vừa xuất và kiểm tra số lượng.
6. Thử nhập CSV có số hiệu văn bản không tồn tại; dòng đó phải bị bỏ qua và thông báo số dòng không khớp.
7. Thử ngày sai định dạng và thời hạn trước ngày giao; các dòng lỗi phải bị bỏ qua.
