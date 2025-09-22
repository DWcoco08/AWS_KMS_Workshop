---
title: "Tổng quan bài Lab"
weight: 20
chapter: true
pre: "<b>2. </b>"
translationKey: "overview"
---

Bài lab này hướng dẫn bạn cách sử dụng AWS KMS để mã hóa dữ liệu trong Amazon S3, đồng thời giám sát hoạt động thông qua AWS CloudTrail.

## Mục tiêu

Sau khi hoàn thành bài lab, bạn sẽ:

- ✅ Hiểu cách tạo và quản lý khóa KMS
- ✅ Tạo khóa mã hóa Customer Master Key
- ✅ Tạo S3 bucket với tính năng ghi nhật ký CloudTrail
- ✅ Mã hóa dữ liệu trong S3 bằng khóa KMS
- ✅ Giám sát việc sử dụng khóa qua CloudTrail
- ✅ Quản lý quyền truy cập khóa cho người dùng và vai trò

## Các dịch vụ AWS sử dụng

### AWS KMS

Dịch vụ quản lý khóa giúp bạn dễ dàng tạo và kiểm soát các khóa mã hóa. KMS sử dụng Hardware Security Modules (HSMs) để bảo vệ tính bảo mật của khóa.

### Amazon S3

Dịch vụ lưu trữ đối tượng được thiết kế để lưu trữ và truy xuất bất kỳ lượng dữ liệu nào. S3 cung cấp độ bền 99.999999999% và tích hợp hoàn hảo với KMS để mã hóa dữ liệu.

### AWS CloudTrail

Dịch vụ ghi nhật ký cho phép giám sát và lưu giữ hoạt động tài khoản. CloudTrail cung cấp lịch sử sự kiện của mọi hoạt động liên quan đến khóa KMS.

## Yêu cầu

### Kiến thức cần có

- Hiểu biết cơ bản về AWS Console
- Kiến thức về IAM (Identity and Access Management)
- Làm quen với khái niệm mã hóa dữ liệu

### Tài nguyên cần thiết

- **Tài khoản AWS**: Với quyền truy cập IAM đầy đủ
- **Quyền hạn**: Cho KMS, S3, và CloudTrail
- **Vùng AWS**: us-east-1 (mặc định)
- **Thời gian**: 30-45 phút

## Quy trình thực hiện

1. **Tạo KMS Key** → Khởi tạo Customer Master Key
2. **Cấu hình S3** → Tạo bucket với mã hóa KMS
3. **Upload dữ liệu** → Test mã hóa tự động
4. **Kiểm tra CloudTrail** → Xem nhật ký hoạt động
5. **Quản lý quyền** → Cấu hình IAM policies
