# Overview

Default resources will be allocated for an organization when it is created, for running basic operations on EnOS. If you need to expand or adjust the capabilities of your clusters on EnOS, you can request resources, extend current resource allocation, or manage resource allocation online.

## Resource Specification

Different resource specifications correspond to different data processing capabilities. For detailed information about the capability of resource units, see [Resource Specification](reference).

## Online Resource Management

Currently, you can request the following resources online:

- **Stream Analytics**: Computing resources for stream data processing
- **TSDB**: Storage resources for time-series data

## Scenarios

**Request resources**

The default deployment of organizations on EnOS supports basic capabilities for device management only. If your business requires data storage in TSDB and stream data processing, you need to request related resources.

**Extend resources**

With business growth, allocated resources may not meet new requirements. You can request resources with higher specification.

## Related Concepts

Major concepts involved in resource management are as follows:

**Stream Analytics Computing Resources**

Computing capability of different specifications correspond to different data processing capability and efficiency. Higher resource specifications support processing bigger amount of data within unit time.

**Data Points**

The amount of data that can be processed by running stream data processing tasks within unit time. The method for counting data points is: **Number of measure points** X **Number of devices**.



## Usage Limit

- Currently, each organization can request 1 resource instance for stream analytics and 1 resource instance for TSDB. 
- Allocated resources for stream analytics cannot be scaled down. When requesting resources, select reasonable resource specification.
