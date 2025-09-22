---
title: "Create KMS Master Key"
weight: 31
chapter: false
pre: "<b>3.1. </b>"
translationKey: "create-kms-key"
---

In this section, we will create a KMS Customer Master Key (CMK) to encrypt data.

### Implementation Steps

1. **Sign in to AWS Management Console**

   - Access [AWS Console](https://console.aws.amazon.com)
   - Sign in with your account

   ![Sign in to AWS Console](/images/3.1/Picture1.png)

2. **Access KMS Service**

   - In the top search bar, find and select **KMS**

   ![Search for KMS](/images/3.1/Picture2.png)

3. **Start Creating Key**

   - On the KMS main page, click **Create key**

   ![KMS main page](/images/3.1/Picture3.png)

4. **Configure Key Type**

   - On the **Configure key** page
   - Select **Key type**: **Symmetric** (default for data encryption)

   ![Configure key type](/images/3.1/Picture4.png)

   - Click **Next**

5. **Add Labels and Description**

   - On the **Add labels** page
   - **Alias**: `mykey` (or your preferred name)
   - **Description**: `KMS Key for S3 data` (You should describe which services the encryption key is associated with)

   ![Add labels and description](/images/3.1/Picture5.png)

   - Click **Next**

6. **Configure Administrative Permissions**

   - On the **Define key administrative permissions** page
   - Select the user or role you're using as **Key administrators**

   ![Configure administrative permissions](/images/3.1/Picture6.png)

   - Click **Next**

7. **Configure Usage Permissions**

   - On the **Define key usage permissions** page
   - Select users/roles allowed to use the key for encryption/decryption (Same as previous step)

   ![Configure usage permissions](/images/3.1/Picture7.png)

   - Click **Next**

8. **Review and Finish**

   - On the **Review** page
   - Review all configurations

   ![Review configuration](/images/3.1/Picture8.png)

   - Click **Finish**

### Verify Successful Creation

After creation, you will see:

- The new key appears in the **Customer managed keys** list
- Status: **Enabled**
- Key ID and ARN are displayed

### Complete

You have successfully created a KMS master key. Next, we will use this key to encrypt data in S3.