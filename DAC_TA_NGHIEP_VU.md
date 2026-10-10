# ĐẶC TẢ YÊU CẦU NGHIỆP VỤ — TASKOFFICE MVP V3

## 1. Bài toán
Cán bộ tổng hợp tiếp nhận nhiều văn bản chỉ đạo theo tuần/tháng. Mỗi văn bản có thể giao nhiều nhiệm vụ cho các đơn vị khác nhau. Cần có cách quản lý tập trung nhiệm vụ, thời hạn, trạng thái, lịch sử cập nhật và thông tin đôn đốc để hỗ trợ tổng hợp báo cáo.

## 2. Mục tiêu
Xây dựng website minh họa giúp người dùng quản lý văn bản nguồn và nhiệm vụ, phát hiện nhiệm vụ cần chú ý, lưu lịch sử theo dõi và xuất danh sách tổng hợp.

## 3. Vai trò người dùng
MVP mô phỏng một người dùng là cán bộ tổng hợp. Chưa có đăng nhập hoặc phân quyền nhiều tài khoản.

## 4. Cấu trúc 5 trang
1. Tổng quan nhiệm vụ.
2. Thông báo kết luận.
3. Quản lý nhiệm vụ.
4. Theo dõi, đôn đốc.
5. Báo cáo tổng hợp.

## 5. Quy tắc nghiệp vụ
- Một văn bản có thể gắn với nhiều nhiệm vụ.
- Mỗi nhiệm vụ có một văn bản nguồn chính.
- Trạng thái chính gồm: Chưa thực hiện, Đang thực hiện, Đã hoàn thành.
- Nhiệm vụ quá hạn khi chưa hoàn thành và ngày hạn nhỏ hơn ngày hiện tại.
- Nhiệm vụ sắp đến hạn khi chưa hoàn thành và hạn nằm trong 0–3 ngày tới.
- Nhiệm vụ lâu chưa cập nhật khi chưa hoàn thành và ngày cập nhật gần nhất cách ngày hiện tại ít nhất 5 ngày.
- Khi cập nhật trạng thái/tiến độ/kết quả, hệ thống lưu một bản ghi lịch sử.
- Mỗi lần đôn đốc được lưu thành bản ghi riêng.
- Thống kê được tính từ dữ liệu hiện có, không nhập số liệu tổng hợp thủ công.

## 6. Yêu cầu chức năng
- FR01: Xem thống kê tổng quan.
- FR02: Thêm, sửa, tìm kiếm văn bản nguồn.
- FR03: Thêm, sửa, tìm kiếm nhiệm vụ.
- FR04: Liên kết nhiệm vụ với văn bản nguồn.
- FR05: Lọc nhiệm vụ theo đơn vị, trạng thái, thời hạn.
- FR06: Tự nhận diện nhiệm vụ sắp đến hạn/quá hạn.
- FR07: Ghi nhận lịch sử cập nhật nhiệm vụ.
- FR08: Ghi nhận lịch sử đôn đốc.
- FR09: Tổng hợp số liệu theo đơn vị và điều kiện lọc.
- FR10: Xuất danh sách báo cáo ra CSV mở bằng Excel.
- FR11: Lưu dữ liệu trên trình duyệt bằng LocalStorage.

## 7. Yêu cầu phi chức năng
- Giao diện tiếng Việt, rõ ràng, dễ đọc.
- Responsive ở màn hình máy tính và điện thoại.
- Có thông báo khi lưu dữ liệu.
- Dùng dữ liệu demo, không chứa dữ liệu nội bộ.
- Mã nguồn tĩnh, có thể triển khai trên GitHub Pages.
- Cảnh báo rõ rằng dữ liệu LocalStorage chỉ nằm trên trình duyệt hiện tại.

## 8. Giới hạn MVP
- Không có đăng nhập/phân quyền.
- Không đồng bộ dữ liệu giữa các máy.
- Không gửi email/tin nhắn tự động.
- Không tự động đọc văn bản bằng AI.
- Không tích hợp hệ thống quản lý văn bản chính thức.
- Không xem đây là kho lưu trữ an toàn cho dữ liệu nhạy cảm.

## 9. Kế hoạch kiểm thử sơ bộ
- Tạo văn bản mới và xác nhận xuất hiện trong danh sách.
- Tạo nhiệm vụ và gắn với văn bản nguồn.
- Thử cập nhật trạng thái, tiến độ và kết quả.
- Kiểm tra nhiệm vụ quá hạn/sắp đến hạn theo ngày hệ thống.
- Ghi một lần đôn đốc và kiểm tra lịch sử.
- Lọc theo đơn vị/trạng thái/thời hạn.
- Xuất CSV và mở bằng Excel.
- Tải lại trang và xác nhận dữ liệu vẫn còn trên cùng trình duyệt.
- Kiểm tra giao diện ở màn hình hẹp.

## 10. Bổ sung ở V2
- Hiển thị lịch sử cập nhật và lịch sử đôn đốc ngay trong cửa sổ chỉnh sửa nhiệm vụ.
- Từ chối lưu nhiệm vụ nếu ngày hoàn thành sớm hơn ngày giao.

## 11. Bổ sung ở V3
- FR12: Xuất danh sách nhiệm vụ ra CSV.
- FR13: Nhập danh sách nhiệm vụ từ CSV, kiểm tra các trường bắt buộc và ngày giao/thời hạn.
- FR14: Cập nhật thời điểm cập nhật khi ghi nhận đôn đốc.

## Quy tắc nghiệp vụ được chuẩn hóa ở V4
- Nhiệm vụ mới cần gắn với văn bản nguồn đã có trong danh mục.
- Khi nhập CSV, không tự động gắn nhiệm vụ vào văn bản đầu tiên nếu số hiệu văn bản nguồn trống hoặc không khớp; dòng này được bỏ qua và thống kê trong thông báo kết quả.
- Ngày giao mặc định là ngày hiện tại nếu để trống; nếu ngày được cung cấp nhưng sai định dạng thì bỏ qua dòng.
- Thời hạn hoàn thành có thể để trống; nếu có thì không được trước ngày giao.
- Trạng thái hoàn thành có tiến độ 100%; trạng thái chưa hoàn thành không được giữ tiến độ 100%.
- Lịch sử ghi nhận các thay đổi quan trọng: trạng thái, tiến độ, kết quả/ghi chú, đơn vị chủ trì, thời hạn và văn bản nguồn.
- Cảnh báo đôn đốc: quá hạn; sắp đến hạn trong 3 ngày; hoặc từ 5 ngày chưa cập nhật. Các nhóm được xếp theo thứ tự ưu tiên, không phải ba bộ đếm độc lập.
