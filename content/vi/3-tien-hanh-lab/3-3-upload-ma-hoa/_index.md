---
title: "Upload ảnh lên S3 và mã hóa"
weight: 33
chapter: false
pre: "<b>3.3. </b>"
translationKey: "upload-encrypt"
---

Trong phần này, chúng ta sẽ tạo một bucket S3 mới và tải lên một hình ảnh, áp dụng mã hóa SSE-KMS.

### Các bước thực hiện

1. **Truy cập S3**

   - Ở đầu trang, trong thanh tìm kiếm, hãy tìm kiếm và chọn dịch vụ **S3**

   ![Tìm kiếm S3](/images/3.3/Picture16.png)

2. **Chọn bucket CloudTrail**

   - Chọn **mycloudtrail11** (tên Trail bạn đã tạo ở phần 2)

   ![Chọn bucket](/images/3.3/Picture17.png)

3. **Bắt đầu tải lên**

   - Từ tab **Objects**, chọn **Upload**

   ![Tab Objects và nút Upload](/images/3.3/Picture18.png)

4. **Thêm files**

   - Chọn **Add files**
   - Chọn hình ảnh từ máy tính của bạn

   ![Thêm files](/images/3.3/Picture19.png)

5. **Mở rộng Properties**

   - Kéo xuống dưới, mở rộng phần **Properties**

   ![Mở rộng Properties](/images/3.3/Picture20.png)

6. **Cấu hình mã hóa**

   - Trong phần **Server-side encryption settings**, chọn như sau:
     - Chọn **Specify an encryption key**
     - Chọn **Override bucket settings for default encryption**
     - Chọn **Server-side encryption with AWS Key Management Service keys (SSE-KMS)**
     - Chọn **Choose from your AWS KMS keys**

   ![Cấu hình mã hóa](/images/3.3/Picture21.png)

7. **Chọn KMS key**

   - Trong danh sách sổ xuống **Available AWS KMS keys**, chọn **mykey** (tên KMS Key mà bạn đã tạo ở phần 1)

   ![Chọn KMS key](/images/3.3/Picture22.png)

8. **Upload file**

   - Kéo xuống dưới cùng, chọn **Upload**
   - Sau khi Upload thành công tại trang **Upload: status** sẽ hiện thông báo

   ![Upload thành công](/images/3.3/Picture23.png)

   - Nhấn **Close**

### Xác nhận upload thành công

Tại tab **Objects** bạn sẽ thấy hình ảnh bạn vừa upload được liệt kê cùng với các tham số.

![Danh sách objects](/images/3.3/Picture24.png)

### Hoàn thành

✅ **Hoàn thành nhiệm vụ**: Bạn đã tải thành công một hình ảnh lên S3 và mã hóa nó với KMS key.