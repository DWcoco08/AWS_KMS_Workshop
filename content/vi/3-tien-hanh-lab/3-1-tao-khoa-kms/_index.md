---
title: "Tạo khóa chính KMS"
weight: 31
chapter: false
pre: "<b>3.1. </b>"
translationKey: "create-kms-key"
---

Trong phần này, chúng ta sẽ tạo một khóa chính KMS (Customer Master Key) để mã hóa dữ liệu.

### Các bước thực hiện

1. **Đăng nhập vào AWS Management Console**

   - Truy cập [AWS Console](https://console.aws.amazon.com)
   - Đăng nhập với tài khoản của bạn

   ![Đăng nhập AWS Console](/images/3.1/Picture1.png)

2. **Truy cập dịch vụ KMS**

   - Ở thanh tìm kiếm trên cùng, tìm và chọn **KMS**

   ![Tìm kiếm KMS](/images/3.1/Picture2.png)

3. **Bắt đầu tạo khóa**

   - Tại trang chính KMS, nhấp chọn **Create key**

   ![Trang chính KMS](/images/3.1/Picture3.png)

4. **Cấu hình loại khóa**

   - Tại trang **Configure key**
   - Chọn **Key type**: **Symmetric** (mặc định cho mã hóa dữ liệu)

   ![Cấu hình loại khóa](/images/3.1/Picture4.png)

   - Nhấn **Next**

5. **Thêm nhãn và mô tả**

   - Tại trang **Add labels**
   - **Alias**: `mykey` (hoặc tên bạn muốn)
   - **Description**: `KMS Key for S3 data` (Bạn nên mô tả khóa mã hóa được gắn với những dịch vụ nào)

   ![Thêm nhãn và mô tả](/images/3.1/Picture5.png)

   - Nhấn **Next**

6. **Cấu hình quyền quản trị**

   - Tại trang **Define key administrative permissions**
   - Chọn user hoặc role bạn đang sử dụng làm **Key administrators**

   ![Cấu hình quyền quản trị](/images/3.1/Picture6.png)

   - Nhấn **Next**

7. **Cấu hình quyền sử dụng**

   - Tại trang **Define key usage permissions**
   - Chọn user/role được phép sử dụng khóa để mã hóa/giải mã (Giống bước trước)

   ![Cấu hình quyền sử dụng](/images/3.1/Picture7.png)

   - Nhấn **Next**

8. **Xem lại và hoàn tất**

   - Tại trang **Review**
   - Kiểm tra lại tất cả cấu hình

   ![Xem lại cấu hình](/images/3.1/Picture8.png)

   - Nhấn **Finish**

### Xác nhận tạo thành công

Sau khi tạo xong, bạn sẽ thấy:

- Khóa mới xuất hiện trong danh sách **Customer managed keys**
- Status: **Enabled**
- Key ID và ARN được hiển thị

### Hoàn thành

✅ **Hoàn thành nhiệm vụ**: Bạn đã tạo thành công khóa chính KMS. Tiếp theo, chúng ta sẽ sử dụng khóa này để mã hóa dữ liệu trong S3.
