# Resource Management on EnOS

Default resources are allocated when an organization is created, for performing basic operations such as connecting devices into EnOS. If you need to expand or adjust the capabilities of your clusters on EnOS, you'll need additional resources or adjust your existing resource quota. EnOS offering online resource management for specific types of resources.

## Which Resource can I Manage Online?

Currently, you can manage the following computing and storage resources online based on your business needs:

**Stream Analytics**

Computing resource for stream data processing. Before running stream data processing jobs, you need to request the Stream Analytics computing resource. Otherwise, the stream data processing jobs cannot be started.

**TSDB**

Storage resource for time series data. Before configuring TSDB storage policy for measuring point data, you need to request the TSDB resource.

**Batch Computing**

Computing resource for data analytics. To run data integration and off-line data analytics jobs, you need to request Batch Computing resource.

**Data Warehouse**

Storage resource for data to be stored in EnOS Hive. To run off-line data analytics jobs and save data in EnOS Hive, you need to request Data Warehouse resource.

**Data Explorer**

Sandbox resource for using data explorer to develop data processing and analytics programs. To run scripts to transform data and extract insights from data, you need to request Data Explorer resource.

**File Storage HDFS**

Storage resource for files to be stored in HDFS. To run data analytics jobs and save files in HDFS, or run data archiving jobs to store files in HDFS, you need to request File Storage HDFS resource.

Different resource specifications correspond to different data processing and storage capabilities. For detailed information about the capability of resource units, see [Resource Specification](reference).

## When Do I Need to Manage My Resources?

### Requesting New Resources

The default deployment of organizations on EnOS supports basic capabilities for device management only. If your business requires data storage in TSDB and stream data processing, you need to request related resources.

### Adjusting Existing Resource Quota

With business growth, allocated resources may not meet new requirements. You can request resources with higher specification.

With business stabilizing, allocated resources may exceed the business requirements. You can scale down the resource specification to save costs.

### Setting Alarms for Resource Consumption Threshold

To avoid the impact of insufficient resources on the normal operation of business, you can set alarms against the resource usage rate by monitoring resource utilization in real time. Once the resource usage rate exceeds the specified threshold, the system sends an alert immediately so that the receivers can process the situation in time to ensure stable operation of the business.

## Related Concepts

Major concepts involved in resource management are as follows:

**Stream Analytics Computing Resources**

Computing capability of different specifications correspond to different data processing capability and efficiency. Higher resource specifications support processing bigger amount of data within unit time.

**Data Points**

The amount of data that can be processed by running stream data processing tasks within unit time. The method for counting data points is: **Number of measuring points** x **Number of devices**.

**TSDB Writing Specification**

The amount of data points that can be stored in TSDB in 1 second.

**Batch Computing Specification**

Computing capability for offline data analytics jobs. If the jobs require higher CPU occupancy, choose the Computing-Intensive specification; if the jobs require higher memory occupancy, choose the Memory-Intensive specification.

## Capacity and Limitations

- Currently, each organization can request 1 resource instance for stream analytics, TSDB, data warehouse, and file storage HDFS. 
- Each organization can request 3 resource instances for batch computing and data explorer, with globally unique queue and sandbox names.

For the capacity of standard resource instances, see [Resource Specification](reference).
