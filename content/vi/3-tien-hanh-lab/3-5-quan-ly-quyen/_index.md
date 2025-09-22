---
title: "Quản lý khóa mã hóa"
weight: 35
chapter: false
pre: "<b>3.5. </b>"
translationKey: "manage-permissions"
---

Trong phần này, bạn sẽ học cách quản lý khóa mã hóa cho người dùng và vai trò.

### Các bước thực hiện

1. **Truy cập KMS**

   - Ở đầu trang, trong thanh tìm kiếm, hãy tìm kiếm và chọn dịch vụ **KMS**

   ![Tìm kiếm KMS](/images/3.5/Picture36.png)

2. **Chọn Customer managed keys**

   - Trong thanh điều hướng bên trái, chọn **Customer managed keys**

   ![Customer managed keys](/images/3.5/Picture37.png)

3. **Chọn khóa để quản lý**

   - Chọn **mykey** (tên KMS Key mà bạn tạo ở phần 1)

   ![Chọn mykey](/images/3.5/Picture38.png)

   Thao tác này sẽ mở ra một trang nơi bạn có thể thực hiện các thay đổi cài đặt KMS. Một trong những cài đặt có thể định cấu hình là **Add** hoặc **Remove** - key administrators và key users.

4. **Xóa quyền người dùng**

   - Trong phần **Key users**, hãy chọn người dùng hoặc vai trò mà bạn đã đăng nhập
   - Chọn **Remove**

   ![Remove key user](/images/3.5/Picture39.png)

   Ngay lập tức, quyền sử dụng khóa này của người dùng sẽ bị xóa.

5. **Khôi phục quyền người dùng**

   - Trong phần **Key users**, chọn **Add**
   - Tìm kiếm và chọn người dùng hoặc vai trò mà bạn vừa xóa
   - Chọn **Add**

   ![Add key user](/images/3.5/Picture40.png)

   Ngay lập tức, quyền sử dụng khóa này của người dùng sẽ được khôi phục.

### Giải thích

Điều này cho thấy cách bạn có thể kiểm soát người dùng hoặc vai trò IAM nào có thể sử dụng Khóa KMS mà bạn tạo. Quy trình tương tự có thể được sử dụng để kiểm soát người dùng IAM nào có thể quản lý khóa KMS.

![Quản lý quyền KMS](/images/3.5/Picture41.png)

### Hoàn thành

✅ **Hoàn thành nhiệm vụ**: Bạn đã quản lý các khóa mã hóa, quyền của người dùng.