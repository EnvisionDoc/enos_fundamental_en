# Overview

Default resources will be allocated for an organization when it is created, for running basic operations on EnOS. If you need to expand or adjust the capabilities of your clusters on EnOS, you can request resources, change resource quota, or manage resource allocation online.

## Resource Specification

Different resource specifications correspond to different data processing and storage capabilities. For detailed information about the capability of resource units, see [Resource Specification](reference).

## Online Resource Management

Currently, you can request the following resources online:

- **Stream Analytics**: Computing resources for stream data processing
- **TSDB**: Storage resources for time series data
- **Batch Computing**: Computing resources for data analytics
- **Data Warehouse**: Storage resources for data to be stored in Hive
- **File Storage HDFS**: Storage resources for files to be stored in HDFS

## Scenarios

**Request resources**

The default deployment of organizations on EnOS supports basic capabilities for device management only. If your business requires data storage in TSDB and stream data processing, you need to request related resources.

**Change quota**

With business growth, allocated resources may not meet new requirements. You can request resources with higher specification.

With business stabilizing, allocated resources may exceed the business requirements. You can scale down the resource specification to save costs.

**Set alarms**

To avoid the impact of insufficient resources on the normal operation of business, you can set alarms against the resource usage rate by monitoring resource utilization in real time. Once the resource usage rate exceeds the specified threshold, the system sends an alert immediately so that the receivers can process the situation in time to ensure stable operation of the business.

## Related Concepts

Major concepts involved in resource management are as follows:

**Stream Analytics Computing Resources**

Computing capability of different specifications correspond to different data processing capability and efficiency. Higher resource specifications support processing bigger amount of data within unit time.

**Data Points**

The amount of data that can be processed by running stream data processing tasks within unit time. The method for counting data points is: **Number of measure points** X **Number of devices**.

**TSDB Write Specification**

The amount of data points that can be stored in TSDB in 1 second.

**Batch Computing Specification**

Computing capability for offline data analytics jobs. If the jobs require higher CPU occupancy, choose the Computing-Intensive specification; if the jobs require higher memory occupancy, choose the Memory-Intensive specification.

## Usage Limit

- Currently, each organization can request 1 resource instance for stream analytics, TSDB, data warehouse, and file storage HDFS. 
- An organization can request 3 resource instances for batch computing, with globally unique queue names.
