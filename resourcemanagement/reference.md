# Resource Specification

## Stream Analytics Computing Resources

**Resource Specification**

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

.. note:: The computing capability refers to the total amount of data that can be processed by running stream processing jobs in unit time. For a stream processing job, the number of data points equals to the number of measure points multiplied by the number of devices. 

<!--


* - Standard X 2
  - 6000 data points / second
  - With 10 measure points / second, supporting about 600 devices

-->

## TSDB Resources

**Resource Specification**

The TSDB resources include write resource and storage resource. Currently, only standard specification can be requested. The system will measure and charge the actual use of resources.