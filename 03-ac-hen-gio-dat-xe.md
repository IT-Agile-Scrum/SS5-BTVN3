# Acceptance Criteria hẹn giờ đặt xe

## Kịch bản

| Kịch bản | Trạng thái ban đầu | Hành động hoặc sự kiện | Kết quả mong đợi |
|---|---|---|---|
| Giờ hợp lệ và tìm tài xế | Giờ đón cách lúc đặt từ 30 phút đến 24 giờ | Khách xác nhận hẹn; đến mốc trước giờ đón 15 phút | Lưu chuyến và bắt đầu tìm tài xế đúng mốc. |
| Giờ ngoài phạm vi | Giờ đón dưới 30 phút hoặc trên 24 giờ | Khách xác nhận hẹn | Từ chối đặt và thông báo phạm vi hợp lệ. |
| Không có tài xế, trả ví | Đã hẹn và thanh toán ví | Kết thúc tìm mà không có tài xế | Hủy, thông báo và hoàn đủ tiền ví. |
| Không có tài xế, trả tiền mặt | Đã hẹn và chọn tiền mặt | Kết thúc tìm mà không có tài xế | Hủy, thông báo; không hoàn ví vì chưa thu tiền. |

## Given – When – Then

1. Given khách chọn giờ đón cách hiện tại từ 30 phút đến 24 giờ, When khách xác nhận đặt, Then hệ thống lưu chuyến hẹn và lên lịch tìm tài xế trước giờ đón 15 phút. Kiểm thử cả hai mốc đúng 30 phút và đúng 24 giờ.
2. Given giờ đón cách hiện tại dưới 30 phút hoặc trên 24 giờ, When khách xác nhận đặt, Then hệ thống không tạo chuyến và báo “Giờ đón phải cách hiện tại từ 30 phút đến 24 giờ”.
3. Given chuyến hẹn đã trả bằng RikkeiPay, When quá trình tìm kết thúc mà không có tài xế nhận, Then hệ thống hủy chuyến, thông báo khách và hoàn đủ tiền vào ví.
4. Given chuyến hẹn chọn trả tiền mặt và chưa thu tiền, When quá trình tìm kết thúc mà không có tài xế nhận, Then hệ thống hủy chuyến, thông báo khách và không tạo giao dịch hoàn ví.

Thời điểm kết thúc tìm tài xế cần Product Owner làm rõ vì đề chưa quy định.
