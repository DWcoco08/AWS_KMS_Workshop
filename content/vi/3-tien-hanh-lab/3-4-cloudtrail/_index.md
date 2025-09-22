---
title: "Truy cập hình ảnh được mã hóa"
weight: 34
chapter: false
pre: "<b>3.4. </b>"
translationKey: "access-encrypted"
---

Trong phần này, chúng ta sẽ kiểm tra cách truy cập hình ảnh được mã hóa bằng KMS từ S3.

### Các bước thực hiện

1. **Mở hình ảnh từ Console**

   - Trong tab **Objects**, chọn tên hình ảnh rồi chọn **Open**

   ![Chọn và mở hình ảnh](/images/3.4/Picture25.png)

   Hình ảnh sẽ mở ra trong một tab/cửa sổ mới. Amazon S3 và AWS KMS thực hiện các hành động sau khi bạn yêu cầu giải mã dữ liệu:

   - Amazon S3 gửi khóa dữ liệu được mã hóa đến AWS KMS
   - AWS KMS giải mã khóa bằng cách sử dụng khóa chính thích hợp và gửi khóa văn bản thuần túy trở lại Amazon S3
   - Amazon S3 giải mã văn bản mật mã và xóa khóa dữ liệu văn bản thuần túy khỏi bộ nhớ càng sớm càng tốt

   ![Hình ảnh hiển thị thành công](/images/3.4/Picture26.png)

   <center><i>(hình ảnh bạn upload lên S3 sẽ hiển thị trong tab mới)</i></center>

2. **Thử truy cập qua URL công khai**

   - Với hình ảnh được chọn, hãy chọn **Copy URL** rồi dán vào trình duyệt và nhấn Enter

   ![Copy URL](/images/3.4/Picture27.png)

3. **Xem thông báo lỗi**

   - Xem thông báo bạn nhận được

   ![Access denied](/images/3.4/Picture28.png)

   Nó hiển thị quyền truy cập bị từ chối. Điều này là do, theo mặc định, quyền truy cập công khai không được phép.

4. **Truy cập Permissions**

   - Tại trang **mycloudtrail11**, chọn tab **Permissions**

   ![Tab Permissions](/images/3.4/Picture29.png)

5. **Chỉnh sửa Block public access**

   - Tại phần **Block public access (bucket settings)**, chọn **Edit**

   ![Edit block public access](/images/3.4/Picture30.png)

6. **Bỏ chặn public access**

   - Bỏ chọn **Block all public access**

   ![Uncheck block all public access](/images/3.4/Picture31.png)

7. **Xác nhận thay đổi**

   - Nhấn **Save changes**, gõ `confirm` rồi chọn **Confirm**

8. **Chỉnh sửa Object Ownership**

   - Kéo xuống phần **Object Ownership**, chọn **Edit**

   ![Edit Object Ownership](/images/3.4/Picture32.png)

9. **Bật ACLs**

   - Chọn **ACLs enabled**, rồi chọn **I acknowledge that ACLs will be restored**

   ![Enable ACLs](/images/3.4/Picture1.png)

   - Chọn **Save changes**

10. **Công khai hình ảnh**

- Quay trở lại tab **Objects**, chọn hình ảnh mà bạn đã upload rồi chọn **Actions**
- Từ menu thả xuống, chọn **Make public using ACL**

![Save changes ACLs](/images/3.4/Picture33.png)

11. **Xác nhận công khai**

- Trong trang **Make public**, chọn **Make public**

12. **Kiểm tra trạng thái**

- Tại trang **Make public: status**, bạn sẽ nhận được thông báo thay đổi thành công

![Make public using ACL](/images/3.4/Picture34.png)

- Nhấn **Close**

13. **Thử lại với URL công khai**

- Trở lại cửa sổ trình duyệt với URL đối tượng S3 của bạn (URL đã copy ở bước 2)
- Tải lại trang hoặc dán vào trình duyệt rồi nhấn **Enter**

14. **Xem thông báo lỗi KMS**

![KMS encryption error](/images/3.4/Picture35.png)

Vì hình ảnh được mã hóa bằng SSE-KMS, bạn không thể xem nó qua liên kết công khai. Bạn sẽ thấy thông báo lỗi: **"Requests specifying Server Side Encryption with AWS KMS managed keys require AWS Signature Version 4."**

### Giải thích

Khi tải lên hoặc truy cập các đối tượng được mã hóa bằng SSE-KMS, bạn cần sử dụng AWS Signature Version 4 để tăng cường bảo mật. Signature Version 4 là quy trình thêm thông tin xác thực vào các yêu cầu AWS. Nếu sử dụng AWS CLI hoặc các AWS SDK, các công cụ này sẽ tự động ký yêu cầu bằng access key mà bạn đã cấu hình, nên bạn không cần học cách ký thủ công.

### Hoàn thành

✅ **Hoàn thành nhiệm vụ**: Bạn đã cố gắng truy cập đối tượng S3 thông qua cả AWS Management Console và liên kết S3 công khai, hiểu được cách KMS bảo vệ dữ liệu.
