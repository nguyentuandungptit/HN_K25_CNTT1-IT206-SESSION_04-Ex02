# Bài tập: Viết User Story, Acceptance Criteria và theo dõi thẻ R5 trên Trello

## Bước 1: Viết User Story cho yêu cầu R5

### User Story
Là một người quản lý phòng khám,  
Tôi muốn tự cập nhật giá các gói khám của cơ sở mình trên hệ thống,  
Để chủ động điều chỉnh bảng giá nhanh chóng mà không cần gửi email nhờ admin hỗ trợ thủ công.

### Giải thích lý do chọn vai trò
Vai trò được chọn là "người quản lý phòng khám" thay vì "admin RikkeiCare" vì các lý do sau:
- Người hưởng lợi trực tiếp từ giá trị nghiệp vụ: Quản lý phòng khám là người phụ trách kinh doanh và nắm rõ giá dịch vụ của cơ sở. Họ là đối tượng có nhu cầu chủ động cập nhật giá để phục vụ bệnh nhân kịp thời.
- Bản chất công việc của admin hiện tại: Admin RikkeiCare cập nhật qua email chỉ là giải pháp tạm thời khi hệ thống chưa có tính năng tự phục vụ. Khi tính năng hoàn thành, công việc này biến mất. Chọn vai trò admin sẽ phản ánh sai đối tượng sử dụng chính của chức năng.

## Bước 2: Viết tiêu chí nghiệm thu (Acceptance Criteria) cho R5

### AC 1 (Thành công)
- Given: Quản lý phòng khám đã đăng nhập vào hệ thống quản trị của phòng khám.
- When: Nhập giá mới hợp lệ cho một gói khám rồi nhấn "Lưu".
- Then: Hệ thống cập nhật giá mới vào cơ sở dữ liệu, hiển thị thông báo "Cập nhật giá thành công", và danh sách gói khám lập tức hiển thị mức giá mới cho cả phòng khám lẫn bệnh nhân đặt lịch.

### AC 2 (Thất bại)
- Given: Quản lý phòng khám đang ở màn hình chỉnh sửa giá gói khám và để trống ô giá.
- When: Nhấn "Lưu".
- Then: Hệ thống không lưu thay đổi, giữ nguyên giá cũ, hiển thị thông báo lỗi "Vui lòng nhập giá cho gói khám" ngay bên dưới ô nhập liệu và đặt con trỏ chuột vào ô này.

## Bước 3: Đánh giá điều kiện sẵn sàng (Definition of Ready) của thẻ R5

Thẻ R5 chưa thể kéo sang cột "Ready for Sprint".

### Đối chiếu với 4 tiêu chí Definition of Ready (DoR) của nhóm
1. Có User Story đủ 3 vế: Đạt. Thẻ đã nêu rõ vai trò (quản lý phòng khám), hành động mong muốn (tự sửa giá) và mục đích (chủ động, bỏ khâu email trung gian).
2. Có tiêu chí nghiệm thu: Đạt. Thẻ đã có 2 kịch bản AC rõ ràng theo mẫu Given - When - Then cho trường hợp thành công và trường hợp nhập thiếu dữ liệu.
3. Đã được ước lượng: Chưa đạt. Thẻ mới được Product Owner chuẩn bị nội dung, nhóm phát triển chưa tham gia buổi Backlog Refinement để thảo luận kỹ thuật và ước lượng độ phức tạp (chưa có Story Points).
4. Đủ nhỏ để làm xong trong 1 Sprint: Chưa đạt. Khi chưa có ước lượng từ nhóm phát triển, nhóm chưa đủ căn cứ để kết luận khối lượng công việc này có thể hoàn thành trọn vẹn trong một Sprint hay không.

### Kết luận
Để một thẻ đủ điều kiện vào cột "Ready for Sprint", thẻ phải đáp ứng đủ cả 4 tiêu chí DoR. Thẻ R5 hiện mới thỏa mãn 2 tiêu chí đầu về mô tả yêu cầu, còn thiếu khâu ước lượng và xác nhận kích thước từ nhóm phát triển. Product Owner cần giữ thẻ tại "Product Backlog" cho đến khi nhóm hoàn tất phiên Refinement.

## Bước 4: Hoàn thiện thẻ R5 trên Trello

Sau khi được nhóm ước lượng và chọn vào Sprint Backlog, thẻ R5 được thiết lập như sau:

- Tiêu đề thẻ: R5: Quản lý phòng khám tự cập nhật giá các gói khám
- Nhãn (Label): Xanh dương (Feature), vì đây là tính năng nghiệp vụ mới phục vụ người dùng.
- Người phụ trách (Assignee): Lập trình viên phụ trách phát triển tính năng (ví dụ: Fullstack Developer hoặc Backend Developer phụ trách module giá).
- Hạn hoàn thành (Due date): Ngày kết thúc Sprint hiện tại, hoặc trước ngày kết thúc 1-2 ngày để đội kiểm thử có thời gian nghiệm thu.
- Danh sách công việc (Checklist):
  1. Xây dựng giao diện chỉnh sửa giá và hiển thị thông báo lỗi (Frontend).
  2. Xây dựng API kiểm tra dữ liệu và lưu giá mới vào cơ sở dữ liệu (Backend).
  3. Kiểm thử kịch bản thành công và kịch bản bỏ trống giá theo AC (QA/Tester).

### Vị trí đặt thẻ
Nếu R5 là công việc có độ ưu tiên cao nhất trong Sprint, thẻ phải được đặt ở vị trí trên cùng (đầu cột) của cột Sprint Backlog.

Lý do: Bảng công việc được theo dõi từ trên xuống dưới theo thứ tự ưu tiên. Đặt thẻ ở vị trí cao nhất giúp cả nhóm nhận biết đây là mục tiêu cần làm trước khi nhận việc.
