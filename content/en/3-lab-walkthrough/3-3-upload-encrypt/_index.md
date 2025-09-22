---
title: "Upload Image to S3 and Encrypt"
weight: 33
chapter: false
pre: "<b>3.3. </b>"
translationKey: "upload-encrypt"
---

In this section, we will create a new S3 bucket and upload an image, applying SSE-KMS encryption.

### Implementation Steps

1. **Access S3**

   - At the top of the page, in the search bar, search for and select the **S3** service

   ![Search S3](/images/3.3/Picture16.png)

2. **Select CloudTrail bucket**

   - Select **mycloudtrail11** (the Trail name you created in section 2)

   ![Select bucket](/images/3.3/Picture17.png)

3. **Start upload**

   - From the **Objects** tab, select **Upload**

   ![Objects tab and Upload button](/images/3.3/Picture18.png)

4. **Add files**

   - Select **Add files**
   - Choose an image from your computer

   ![Add files](/images/3.3/Picture19.png)

5. **Expand Properties**

   - Scroll down and expand the **Properties** section

   ![Expand Properties](/images/3.3/Picture20.png)

6. **Configure encryption**

   - In the **Server-side encryption settings** section, select as follows:
     - Select **Specify an encryption key**
     - Select **Override bucket settings for default encryption**
     - Select **Server-side encryption with AWS Key Management Service keys (SSE-KMS)**
     - Select **Choose from your AWS KMS keys**

   ![Configure encryption](/images/3.3/Picture21.png)

7. **Select KMS key**

   - In the **Available AWS KMS keys** dropdown list, select **mykey** (the KMS Key name you created in section 1)

   ![Select KMS key](/images/3.3/Picture22.png)

8. **Upload file**

   - Scroll to the bottom and select **Upload**
   - After successful upload, the **Upload: status** page will show a notification

   ![Upload successful](/images/3.3/Picture23.png)

   - Click **Close**

### Verify successful upload

In the **Objects** tab you will see the image you just uploaded listed along with the parameters.

![Objects list](/images/3.3/Picture24.png)

### Complete

You have successfully uploaded an image to S3 and encrypted it with KMS key.