### Phần 1: Thiết kế Prompt 3 Thành phần Chuẩn hóa

Lý do: Cấu trúc hỏi thiếu Ngữ cảnh (Context) và Mã lỗi (Raw Error).

Mẫu Prompt chuẩn:

- [Context]: Đang vận hành trạm sạc VoltCharge (Win 11), trạm 04 bị sập.

- [Raw Error]: (Dán nguyên văn 8 dòng log lỗi).

- [Instruction]: Dịch lỗi sang tiếng Việt đơn giản và cho 3 bước xử lý.

Phần 2: Xử lý lỗi & Bảo mật

-Bản chất lỗi `UnauthorizedAccessException`: Ứng dụng bị hệ điều hành chặn vì không có quyền ghi dữ liệu vào thư mục bảo vệ `C:\Program Files`.

-3 Bước khắc phục:

- Xử lý nhanh: Chuột phải biểu tượng VoltCharge ➔ chọn Run as administrator.

- Xử lý tự động: Chuột phải biểu tượng ➔ Properties ➔ Compatibility ➔ Tick Run this program as an administrator.

- Tối ưu bảo mật: Chuột phải thư mục `data` ➔ Properties ➔ Security ➔ Edit ➔ Cấp quyền Write và Modify cho nhóm Users.

-Xử lý API Key: Bắt buộc đổi thành `[ĐÃ CHE]` hoặc `***` trước khi dán vào AI. Việc để lộ API Key lên máy chủ đám mây có thể khiến trạm sạc bị hacker chiếm quyền điều khiển.