---
title: "Access Encrypted Image"
weight: 34
chapter: false
pre: "<b>3.4. </b>"
translationKey: "access-encrypted"
---

In this section, we will test how to access KMS-encrypted images from S3.

### Implementation Steps

1. **Open image from Console**

   - In the **Objects** tab, select the image name and choose **Open**

   ![Select and open image](/images/3.4/Picture25.png)

   The image will open in a new tab/window. Amazon S3 and AWS KMS perform the following actions when you request to decrypt your data:
   - Amazon S3 sends the encrypted data key to AWS KMS
   - AWS KMS decrypts the key using the appropriate master key and sends the plaintext key back to Amazon S3
   - Amazon S3 decrypts the ciphertext and removes the plaintext data key from memory as soon as possible

   ![Image displays successfully](/images/3.4/Picture26.png)

   <center><i>(the image you uploaded to S3 will display in a new tab)</i></center>

2. **Try accessing via public URL**

   - With the image selected, choose **Copy URL** then paste into browser and press Enter

   ![Copy URL](/images/3.4/Picture27.png)

3. **View error message**

   - View the message you receive

   ![Access denied](/images/3.4/Picture28.png)

   It displays access denied. This is because, by default, public access is not allowed.

4. **Access Permissions**

   - On the **mycloudtrail11** page, select the **Permissions** tab

   ![Permissions tab](/images/3.4/Picture29.png)

5. **Edit Block public access**

   - In the **Block public access (bucket settings)** section, select **Edit**

   ![Edit block public access](/images/3.4/Picture30.png)

6. **Unblock public access**

   - Uncheck **Block all public access**

   ![Uncheck block all public access](/images/3.4/Picture31.png)

7. **Confirm changes**

   - Click **Save changes**, type `confirm` and select **Confirm**

8. **Edit Object Ownership**

   - Scroll down to **Object Ownership** section, select **Edit**

   ![Edit Object Ownership](/images/3.4/Picture32.png)

9. **Enable ACLs**

   - Select **ACLs enabled**, then select **I acknowledge that ACLs will be restored**

   ![Enable ACLs](/images/3.4/Picture1.png)

   - Select **Save changes**

10. **Make image public**

- Return to the **Objects** tab, select the image you uploaded and choose **Actions**
- From the dropdown menu, select **Make public using ACL**

![Save changes ACLs](/images/3.4/Picture33.png)

11. **Confirm make public**

- On the **Make public** page, select **Make public**

12. **Check status**

- On the **Make public: status** page, you will receive a successful change notification

![Make public using ACL](/images/3.4/Picture34.png)

- Click **Close**

13. **Retry with public URL**

- Return to the browser window with your S3 object URL (URL copied in step 2)
- Reload the page or paste into browser and press **Enter**

14. **View KMS error message**

![KMS encryption error](/images/3.4/Picture35.png)

Because the image is encrypted with SSE-KMS, you cannot view it via public link. You will see the error message: **"Requests specifying Server Side Encryption with AWS KMS managed keys require AWS Signature Version 4."**

### Explanation

When uploading or accessing objects encrypted with SSE-KMS, you need to use AWS Signature Version 4 for enhanced security. Signature Version 4 is the process of adding authentication information to AWS requests. If using AWS CLI or AWS SDKs, these tools will automatically sign requests with the access key you've configured, so you don't need to learn how to sign manually.

### Complete

You have attempted to access an S3 object through both AWS Management Console and public S3 link, understanding how KMS protects data.