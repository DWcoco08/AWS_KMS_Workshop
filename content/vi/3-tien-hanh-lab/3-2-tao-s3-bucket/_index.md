---
title: "Cấu hình CloudTrail để lưu trữ nhật ký"
weight: 32
chapter: false
pre: "<b>3.2. </b>"
translationKey: "configure-cloudtrail"
---

Trong phần này, chúng ta sẽ cấu hình CloudTrail để lưu trữ các tệp nhật ký trong vùng lưu trữ S3 mới.

### Các bước thực hiện

1. **Truy cập CloudTrail**

   - Tại thanh tìm kiếm, hãy tìm và chọn dịch vụ **CloudTrail**

   ![Truy cập CloudTrail](/images/3.2/Picture9.png)

2. **Tạo Trail mới**

   - Trong thanh điều hướng bên trái, chọn **Trails** rồi nhấp chọn **Create trail**

   ![Create Trail button](/images/3.2/Picture10.png)

3. **Cấu hình Trail attributes**

   - Trong trang **Choose trail attributes**, hãy cấu hình các thông số:
     - **Trail name**: `mycloudtrail` (được sử dụng trong bài lab này)
     - **Trail log bucket and folder**: `mycloudtrail11` (được sử dụng trong bài lab này)
     - Bỏ chọn **Log file SSE-KMS encryption**

   ![Cấu hình trail attributes](/images/3.2/Picture11.png)

   - Chọn **Next**

4. **Chọn Log events**

   - Tại trang **Choose log events**, chọn các mục:
     - Chọn **Management events**
     - Chọn **Data events**
     - Chọn **Insights events**

   ![Chọn log events](/images/3.2/Picture12.png)

5. **Cấu hình Data events**

   - Tại phần **Data events**, chọn **Switch to basic event selectors**

   ![Cấu hình data events](/images/3.2/Picture13.png)

   - Chọn **Continue**

6. **Cấu hình Insights events**

   - Tại phần **Insights events**, tích chọn:
     - Chọn **API call rate**
     - Chọn **API error rate**

   ![Cấu hình insights events](/images/3.2/Picture14.png)

   - Chọn **Next**

7. **Xem lại và tạo Trail**

   - Trong trang **Review and create**, xem lại các thông số của cấu hình **Trail**

   ![Review và Create trail](/images/3.2/Picture15.png)

### Xác nhận tạo thành công

Sau khi tạo thành công, bạn sẽ thấy thông báo và các thông số của trail.

### Hoàn thành

✅ **Hoàn thành nhiệm vụ**: Bạn đã cấu hình thành công CloudTrail để lưu trữ nhật ký trong S3.
