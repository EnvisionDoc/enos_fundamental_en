# Resource Specification

## Stream Analytics Computing Resources

Multiple resource specifications are available to meet the requirements of different data amounts and processing efficiency. Resource specifications and corresponding data processing capabilities are as follows:

.. list-table::
   :widths: 20 30 50

   * - Specification
     - Computing Capability
     - Reference
   * - Standard
     - 1500 data points / second
     - With 10 measure points / second, supporting about 150 devices
   * - Standard X 2
     - 3000 data points / second
     - With 10 measure points / second, supporting about 300 devices

.. note:: The computing capability refers to the total amount of data that can be processed by running stream processing jobs in unit time. For a stream processing job, the number of data points is equal to the number of measure points multiplied by the number of devices.

<!--


* - Standard X 4
  - 6000 data points / second
  - With 10 measure points / second, supporting about 600 devices

-->

## TSDB Resources

The TSDB resources include write resource and storage resource.

- Write specification: only standard specification can be requested (5,000 data points per sencond). The system will measure and charge the actual use of resources.
- Storage space: can be requested based on actual business needs (10 ~ 1,000 GB).

## Batch Computing Resources

Batch computing resources can be requested based on computing unit (CU), with two kinds of computing specifications, Computing-Intensive and Memory-Intensive. You can request appropriate computing specification according to the characteristics of offline data analytics jobs (1 ~ 20 CU).

.. list-table::
   :widths: 40 60

   * - Computing Specification
     - Allocated Resources
   * - Computing-Intensive
     - 1CU = 1 core CPU + 2GB Memory
   * - Memory-Intensive
     - 1CU = 1 core CPU + 4GB Memory

## Data Warehouse Resources

Data warehouse (EnOS Hive) is a subject-oriented and integrated data storage environment for data analysis. Select the appropriate storage size according to actual business requirements. Storage capacity that can be requested is 10 ~ 1,000 GB.

## Data Explorer Resources

Data Explorer sandbox provides running environment for the data analytics applications developed by data scientists and data engineers. Select the appropriate CPU, memory, and storage according to actual business requirements. CPU that can be requested is 2~10 vcore; memory that can be requested is 4~20GB; storage that can be requested is 1~10GB.

## File Storage HDFS Resources

HDFS is used for big data analysis and storage scenarios (including data archiving). Select the appropriate storage size according to actual business requirements. Storage capacity that can be requested is 10 ~ 1,000 GB.
