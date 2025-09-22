---
title: "Giới thiệu AWS KMS"
weight: 10
chapter: true
pre: "<b>1. </b>"
translationKey: "introduction"
---

AWS Key Management Service (KMS) là một dịch vụ được quản lý bởi AWS, cho phép bạn tạo và quản lý các khóa mã hóa một cách dễ dàng để bảo vệ dữ liệu của mình.

## Tính năng chính

- **Mã hóa dữ liệu**: Hỗ trợ mã hóa dữ liệu tại chỗ (at-rest) và trong quá trình truyền (in-transit)
- **Tích hợp đa dịch vụ**: Hoạt động với Amazon S3, Amazon EBS, Amazon RDS, và nhiều dịch vụ AWS khác
- **Quản lý khóa tập trung**: Kiểm soát quyền truy cập vào các khóa mã hóa từ một điểm duy nhất
- **Xoay khóa tự động**: Kích hoạt xoay khóa định kỳ để tăng cường bảo mật
- **Giám sát hoạt động**: Tích hợp với AWS CloudTrail để theo dõi mọi hoạt động sử dụng khóa

## Lợi ích

### Bảo mật cao

- Sử dụng Mô-đun bảo mật phần cứng (HSM) được xác thực FIPS 140-2 Level 2
- Phân tách nhiệm vụ giữa quản lý khóa và truy cập dữ liệu

### Tuân thủ quy định

- Đáp ứng các tiêu chuẩn bảo mật như PCI DSS, HIPAA, và GDPR
- Cung cấp khả năng kiểm toán toàn diện

### Hiệu quả chi phí

- Chỉ trả tiền cho những gì bạn sử dụng
- Không có chi phí trả trước hoặc phí tối thiểu
- Giảm chi phí vận hành

## Các loại khóa KMS

### Customer Master Keys (CMKs)

- **AWS Managed CMKs**: Khóa do AWS tạo và quản lý thay mặt bạn
- **Customer Managed CMKs**: Khóa do bạn tạo, sở hữu và quản lý
- **AWS Owned CMKs**: Khóa do AWS sở hữu và sử dụng cho nhiều tài khoản

### Data Keys

- Dùng để mã hóa lượng lớn dữ liệu
- Được tạo bởi KMS nhưng sử dụng bên ngoài KMS
- Có thể ở dạng mã hóa hoặc plaintext
