[Home](./readme.md)

# EC2 - Phân loại theo mục đích sử dụng

## Thông thường: A, T, M

    - cân bằng cho mục đích tính toán, bộ nhớ và mạng
    - dùng cho webserver, code repositories

## Tính toán: C

    - cho hệ thống cần sức mạnh cpu lớn
    - dùng cho: server game, server engines, scientific modeling

## Tối ưu bộ nhớ ram: R, X, Z1D

    - Tốc độ bộ nhớ nhanh, xử lý dữ liệu lớn
    - dùng cho: cache, database sử dụng ram, realtime với dữ liệu lớn

## Tăng tốc tối ưu hóa: P, G, F

    - dùng cho: mechine learning, nhận diện giọng nói, phân tích dữ liệu tài chính, seismic - địa chắc

## Tối ưu bộ nhớ: I, D, H

    - tối ưu tốc độ đọc ghi bộ nhớ
    - dùng cho: NoSQL, data warehousing

# EC2 - UserData

- chạy script do người dùng chỉ định 1 cách tự động sau khi khởi chạy instance. ví dụ: cài apache2
- Lấy thông tin: curl https://169.254.169.254/lasest

# EC2 Placement groups

## Cluster

- Gom nhóm các ec2 trong cùng 1 az
- giảm độ trễ giữa các instance => tăng performance => thích hợp cho công việc đòi hỏi tính toán hiệu suất cao
- ko thể multi az

## Partition

- trải cách instance trên các vùng riêng biệt - spreads instance across logical partitions
- mỗi partition thì không share phần cứng với nhau
- thích hợp với ứng dụng cần phân phối lớn như Hadoop, cassandra, kafka

## Spread

-

# EC2 - Tips

- AWS EMR - xử lý ứng dụng với khối lượng dữ liệu lớn --> ko phải realtime
