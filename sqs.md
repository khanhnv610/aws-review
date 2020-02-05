# SQS

- lưu trữ message queue từ 60 giây mặc định là 4 ngày, tối đa là 14 ngày, lưu trữ lên tới 120.000 message
- message size từ 1 byte đến 256 kb, có thể sử dụng java để tăng lên đến 2GB

# SQS types

## SQS - Standard

- Gần như ko giới hạn transactions
- Guarantees that a message will delivered at least once ???
- provides best-effort ordering that helps ensure a message is generally delivered in the same order that it was sent

## SQS -FIFO Queues

- đảm bảo message xử lý theo 1 thứ tự với 1 queue duy nhất
- giới hạn 300 transactions trong 1 giây

# SQS - Visibility timeout

- Tối thiểu: 0 giây, mặc định: 30 giây, tối đa: 12 giờ

- Nhằm tránh tình trạng xử lý chung 1 message queue
- Là khoảng thời gian message hiển thị lại ở trong queue sau khi được lấy ra khỏi sqs
- message sẽ được xóa sau khi job đã được xử lý.
- nếu job ko được xử lý trước khi visibility hết hạn thì nó được hiện thị lại vào queue và chờ được xử lý
  ==> Như vậy, cùng 1 message có thể được xử lý 2 lần

# SQS short và long polling

- Polling là method lấy message nhận từ queue

- Short polling (default) sẽ trả về message ngay lập tức.

- Long polling sẽ trả về message với 1 timeout nhất định => giảm chi phí => giảm số message rỗng.
