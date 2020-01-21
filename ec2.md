[Home](./readme.md)

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
