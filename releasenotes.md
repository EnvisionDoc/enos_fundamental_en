# 2019/02/21

The 2019/02/21 release offers the following new services, features, and enhancements:

## Device Management

### Support of Statistics Dashboard

EnOS Device Manager now supports the dashboard function that provides the statistics of device connections. The dashboard shows the connection status of devices and the statitics of inbound and outbound messages, thereby, enables you to quickly determine the situations and make business decisions.

.. image:: media/dashboard.png

#### Statistical Indicators

The statitical indicators are mainly targeting to the device management and operation staffs. This new feature provides statistical data of the current account at near-realtime. The feature also provides data and visualization of key business indicators such as concurrent connections and message transmissions of user-specified time span.

The EnOS Device Manager service currently provides the following statistical indicators:

.. list-table::
   :widths: 35 65

   * - Indicator
     - Description
   * - Overview
     - The total number of products and devices that are created in the current account till the current day, and the message throughput of the current day.
   * - Online devices
     - Number of devices maintaining long connection with IoT Hub in the specified time cycle, classified by protocol type. 
   * - Trend
     - Number of registered, activated, and online devices in the specified time cycle.
   * - MQTT Messages (Bytes)
     - Amount of inbound and outbound messages in byte in the time cycle.
   * - MQTT Messages (Count)
     - Number of inbound and outbound messages in the specified time, assuming average message size is 512 bytes.

#### How to Use

To access the device dashboard, click **Device Management > Overview** from the left navigation of EnOS Console.

In addition to the **Overview** section at the top of the page, you can view the statistics of all or select products for your designated time span. The dashboard provides convenient time filters to help you show the statistics of the recent 1 hour, 1 day, 7 days, and 30 days.

Because the dashboard features adopts a static visualization panel technology, delays might occur for data presentation. You can click the **Refresh** icon to show the latest data.

### Support of Dynamic Activation of Devices

Support to activate devices through the `productKey`, `productSecret` and `deviceKey`. The `deviceSecret` is retrieved dymanically when the device attempts to log into EnOS Cloud. Dynamic activiation helps to achieve batch registeration and login of devices. For more information about dymanic activation, see [Secret-based Authentication](https://www.envisioniot.com/docs/device-connection/en/latest/secretbased_authentication.html).

### Updates to Device SDK for Java

The device SDK for Java adds support for:

- NTP synchronization
- Dynamic Activation of Devices

To obtain the latest Java SDK, go to https://github.com/EnvisionIot/enos-mqtt-sdk-java.

### Data Asset Management

Data Asset Management is a new service of EnOS that targets to help you manage your data assets more efficiently. The service mainly brings the following benefits:

- lower cost of datastore due to more flexible configuration
- stronger data analytics service
- lower barrier of stream data processing development and higher data development efficiency
- more effective data retention and access based on domain expertise accumulation.