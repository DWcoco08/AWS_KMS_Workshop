---
title: "Configure CloudTrail to Store Logs"
weight: 32
chapter: false
pre: "<b>3.2. </b>"
translationKey: "configure-cloudtrail"
---

In this section, we will configure CloudTrail to store log files in a new S3 storage area.

### Implementation Steps

1. **Access CloudTrail**

   - In the search bar, find and select the **CloudTrail** service

   ![Access CloudTrail](/images/3.2/Picture9.png)

2. **Create New Trail**

   - In the left navigation bar, select **Trails** then click **Create trail**

   ![Create Trail button](/images/3.2/Picture10.png)

3. **Configure Trail Attributes**

   - On the **Choose trail attributes** page, configure these parameters:
   - **Trail name**: `mycloudtrail` (used in this lab)
   - **Trail log bucket and folder**: `mycloudtrail11` (used in this lab)
   - Uncheck **Log file SSE-KMS encryption**

   ![Configure trail attributes](/images/3.2/Picture11.png)

   - Select **Next**

4. **Choose Log Events**

   - On the **Choose log events** page, select:
   - Select **Management events**
   - Select **Data events**
   - Select **Insights events**

   ![Choose log events](/images/3.2/Picture12.png)

5. **Configure Data Events**

   - In the **Data events** section, select **Switch to basic event selectors**

   ![Configure data events](/images/3.2/Picture13.png)

   - Select **Continue**

6. **Configure Insights Events**

   - In the **Insights events** section, check:
   - Select **API call rate**
   - Select **API error rate**

   ![Configure insights events](/images/3.2/Picture14.png)

   - Select **Next**

7. **Review and Create Trail**

   - On the **Review and create** page, review the **Trail** configuration parameters
   - Select **Create trail** at the bottom of the page

   ![Review and Create trail](/images/3.2/Picture15.png)

### Verify Successful Creation

After successful creation, you will see a notification and the trail parameters.

### Complete

You have successfully configured CloudTrail to store logs in S3.