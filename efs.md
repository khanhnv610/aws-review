# EFS

- elastic file serve cho ec2.
- use case chính: Giúp share file giữa các ec2, tận dụng tốc độ để giảm độ trễ.
- hỗ trợ life cycle => chuyển sang efs infrequent access
- tính tiền theo: GB / tháng
- có thể scale lên Petabyte
- support hàng nghìn lượt kết nối đồng thời.
- lưu trữ ở nhiều az trong 1 region
- read after write consistency

# EBS

- là ổ cứng với ec2
- có 5 loại: general purpose, provisioned iops, throughput optimized hdd, cold hdd, ebs magnetic

# EBS - Moving volumes

## Chuyển sang az khác cùng region

- tạo snapshot
- tạo ami từ snapshot
- chạy ec2 mới từ ami

## Chuyển sang region khác

- tạo snapshot
- tạo ami từ snapshot
- copy ami sang region khác
- chạy từ ami dc copy

## Encrypt root volume

- có thể encrypt khi tạo mới ec2

## Encrypt existing volume

- Tạo snapshot
- tạo bản copy với option encryption
- tạo AMI từ bản bản snapshot encryption
- chạy ec2 từ ami trên
