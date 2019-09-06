# Documentation Updates

Learn about all the latest updates for EnOS documentation.

This page lists all the documentation updates that are not listed in the [Release Notes](releasenotes/index).

## Updates in 2019/09/06 Refresh

- Restored description about how to add event features when creating or editing models; added a note about configuring TSDB storage policies in time for new measuring points when creating or editing models. For details, see [Creating a Model](/docs/device-connection/en/latest/howto/model/creating_model).

- Added "Step 4: Configuring Storage Policy for Measuring Point Data" to the "Connecting a Smart Device into EnOS Cloud" topic. For details, see [Connecting a Smart Device into EnOS Cloud](/docs/device-connection/en/latest/quickstart/gettingstarted_device_connection.html#step-4-configuring-storage-policy-for-measuring-point-data).

- Updated sample codes in the following topics:

  - [Connecting to EnOS Cloud](/docs/device-connection/en/latest/howto/device/develop/java/connect)
  - [Connecting to EnOS Cloud through SSL/TLS](/docs/device-connection/en/latest/howto/device/develop/java/connect_ssl)
  - [Connecting to EnOS by using profiles](/docs/device-connection/en/latest/howto/device/develop/java/connect_viaprofile)
  - [Send Data to EnOS Cloud](/docs/device-connection/en/latest/howto/device/develop/java/post_data_to_cloud)
  - [Send Command to Device](/docs/device-connection/en/latest/howto/device/develop/java/send_command_to_device)

- Updated description on how to connect devices through CoAP protocol without DTLS encryption. When you do not use DTLS encryption, AES encryption capability is no longer required for the device to be connected. The following topics are updated: 

  - [CoAP-based Connection and Communication (Non-DTLS)](/docs/device-connection/en/latest/reference/coap/coap_non_dtls/connection_non_dtls)
  - [Reporting Attributes, Measure points and Events to EnOS (Non-DTLS)](/docs/device-connection/en/latest/reference/coap/coap_non_dtls/reporting_data_non_dtls)
  - [Setting Measure Points and Invoking Services (Non-DTLS)](/docs/device-connection/en/latest/reference/coap/coap_non_dtls/invoking_service_setting_measure_point_non_dtls)

- Updated the diagram displaying overall device connection through MQTT protocol, deleting the part for cloud clustering. For more information, see [MQTT-based Connection](/docs/device-connection/en/latest/learn/message_flow)。

- Updated the structure of the documentation for Resource Management and added detailed description of resources that can be requested online. For details, see [Resource Management on EnOS](/docs/enos/en/dev/resourcemanagement/overview.html).

## Updates in 2019/04/10 Refresh

- Added information about how you can manage the device lifecycle on EnOS, see [Device Lifecycle Management](/docs/device-connection/en/latest/learn/device_lifecycle_management).
- Added information about the data ingestion scenarios and the data format accepted by EnOS, see [Data Ingestion](/docs/device-connection/en/latest/learn/ingestion/index).
- Added sample code in the following quick start tutorials:
  - [Connecting a Smart Device into EnOS Cloud](/docs/device-connection/en/latest/quickstart/gettingstarted_device_connection)
  - [Connecting a Non-Smart Device to EnOS Cloud via Edge](/docs/device-connection/en/latest/quickstart/gettingstarted_edge_connection)
- Added developer guide for Java SDK, see [Using Java SDK to Develop](/docs/device-connection/en/latest/howto/device/develop/java/index).
- Updated information about the device types supported by EnOS, see [Device Connectivity](/docs/device-connection/en/latest/learn/connection_scenarios).
- Updated information about how to use data parsing script to parse data that is not sent via EnOS standard JSON format, see [Creating Data Parsing Script](/docs/device-connection/en/latest/howto/device/manage/creating_data_parsing_script).
- Updated information about how to connect to EnOS through our MQTT-based device protocol, see [Establishing Connection with EnOS Cloud using the MQTT Protocol](/docs/device-connection/en/latest/reference/mqtt/nonsdk_login).
