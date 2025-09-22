---
title: "Manage Encryption Keys"
weight: 35
chapter: false
pre: "<b>3.5. </b>"
translationKey: "manage-permissions"
---

In this section, you will learn how to manage encryption keys for users and roles.

### Implementation Steps

1. **Access KMS**

   - At the top of the page, in the search bar, search for and select the **KMS** service

   ![Search KMS](/images/3.5/Picture36.png)

2. **Select Customer managed keys**

   - In the left navigation bar, select **Customer managed keys**

   ![Customer managed keys](/images/3.5/Picture37.png)

3. **Select key to manage**

   - Select **mykey** (the KMS Key name you created in section 1)

   ![Select mykey](/images/3.5/Picture38.png)

   This will open a page where you can make changes to KMS settings. One of the configurable settings is **Add** or **Remove** - key administrators and key users.

4. **Remove user permissions**

   - In the **Key users** section, select the user or role you are logged in with
   - Select **Remove**

   ![Remove key user](/images/3.5/Picture39.png)

   Immediately, the user's permission to use this key will be removed.

5. **Restore user permissions**

   - In the **Key users** section, select **Add**
   - Search for and select the user or role you just removed
   - Select **Add**

   ![Add key user](/images/3.5/Picture40.png)

   Immediately, the user's permission to use this key will be restored.

### Explanation

This shows how you can control which IAM user or role can use the KMS Key you create. The same process can be used to control which IAM user can manage the KMS key.

![Manage KMS permissions](/images/3.5/Picture41.png)

### Complete

You have managed encryption keys and user permissions.