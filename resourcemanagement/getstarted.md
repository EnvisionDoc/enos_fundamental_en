# Managing Resources

Using stream analytics resources as example, this topic introduces how to request resources, extend resource allocation, change resource quota, view the status of resource allocation, and set alarms for resource usage rate. 

## Prerequisites

Full Access permission to the Resource Management module.

## Procedure
The procedure for managing stream analytics resources is as follows:
1. Request stream analytics resources
2. View resource allocation status
3. Extend stream analytics resource allocation

## Requesting  stream analytics resources
1. Log in EnOS and click **Resource Management** from the left navigation panel.
2. Under the **Data Asset Management** tab, click the **Request Resource** button for Stream Analytics. 
3. View the description of computing resource specification, estimate the needed resources, and select a resource specification.
4. Click the **Request Now** button to submit the request. The system will allocate resources according to the request review result.

### Viewing resource allocation status
After submitting the resource request, return to the **Resource Management** page to view the status of resource allocation.

- The status **Allocating** indicates that the resource allocation is still in progress.
- The status **Allocated** indicates that the resource allocation is completed. You can start the published stream processing jobs. For details about stream processing job operation, see [Monitoring the Stream Processing Job](/docs/data-asset/en/latest/howto/stream/monitoring_job.html).

## Extending resource allocation
If allocated resource cannot meet the growing business needs, you can extend the resource allocation.

1. On the Resource Management page, find the resource request in **Allocated** status.
2. Click the **Change Quota** icon from the **Operations** column of the resource request.
3. Select a higher stream analytics specification and click the **Request Now** button.
4. View the status of new resource allocation. When the new resource specification is displayed in the **Specification** column, and the status is changed to **Allocated**, the resource expansion is completed successfully.

## Changing resource quota

If allocated resource exceeds the business needs, you can change the resource quota.

1. On the Resource Management page, find the resource request in **Allocated** status.
2. Click the **Change Quota** icon from the **Operations** column of the resource request.
3. Select a lower stream analytics specification and click the **Request Now** button.
4. View the status of new resource allocation. When the new resource specification is displayed in the **Specification** column, and the status is changed to **Allocated**, the resource quota is scaled down successfully.

.. note:: If the resources currently in usage are more than the scaled down resource specification, you need to release resources (such as stopping stream processing jobs) first, and then request to change resource quota.

## Setting alarms against resource usage rate

To avoid the impact of insufficient resources on the normal operation of business, you can set alarms for resource usage rate.

1. On the Resource Management page, click the **Alarm Setting** icon from the **Operations** column of the resource request.
2. Enable the **Resource Usage Alert** switch and set the resource usage alert threshold (0.1 ~ 1.0).
3. Select receivers for the alerts. At most 3 receivers can be selected.
4.  Select the alert sending mode, through email or SMS.
5. Click **Confirm** to save the setting.