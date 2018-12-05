# EnOS Technical Architecture

This article describes the architecture of the EnOS AIoT platform. The architecture of EnOS consists of the EnOS Edge layer and EnOS Cloud layer.
- EnOS Edge connects devices to EnOS Cloud. Device data is transmitted through supported protocols from EnOS Edge to EnOS Cloud, in the format of standard models that are predefined. Edge computing is supported wherever needed.
- EnOS Cloud receives device data through MQTT protocol and data will go through its stream computing engine to distributed storage cluster. EnOS cloud support both EnOS Edge and third-party edge.


## EnOS Edge

EnOS Edge is the front end of the EnOS platform. In close contact with your enterprise assets, EnOS Edge helps securely exchange data with cloud-based services in the EnOS Cloud such as asset management and big data analytics. The results of the big data analytics algorithms and the asset management commands can then be transmitted to the devices to optimize and maximize performance, or to implement critical actions.

![](media/edge_architecture.png)

-   **Connectivity engine** provides rich industry standard protocols. User can configure the engine to achieve data connection from remote devices.

-   **Redis** provides content data management.

-   **AMQ message engine** is the messaging broker middleware that routes data to other core modules.

-   **Model data management** module stores device model data from cloud.

-   **HA engine** provides high availability for ensure system resilience.

-   **Cloud access interface** provides cloud-based communication management, including authentication and authorization, MQTT client and etc.

## EnOS Cloud

![](media/cloud_architecture.png)

### Infrastructure Layer

The infrastructure layer of EnOS Cloud provides the whole cluster of databases such as Redis, MySQL, Hbase/HDFS and Common FS. EnOS Cloud applies Ranger for data security and management and provides time-series data management and offline SQL data management through Yarn Distributed Resource Manager.

Among these system components, except for time-series database (TSDB), which is developed by Envision, the rest are leading open source for big data systems.

- **Envision-developed TSDB** works with Hive to ensure high-responsiveness and offline storage of large data volume.

- **Ranger** ensures the security of data management.

- **Yarn** provides resource scheduling capability.

Other open source components act as the base data storage system, among which Common FS encapsulates the common file service and shield the data from hosting environment
- **Redis**: stores the snapshot of data transmitted from device hub and make the real-time telemetries accessible immediately.

- **Mongo DB**: stores master data of assets that are connected into EnOS Cloud. For example, the asset data of a wind farm is stored as JSON arrays and persisted in the Mongo DB. Dimension table is also implemented by Mongo DB due to its advantage of schema free.

- **MySQL**: stores device models and the data instance data in the device library. This type of data, changes less frequently and has relatively small amount.

- **HBase**: which high-volumn time-series database is based on.

- **HDFS**: stores all historical data. The major purpose is to optimize batch data processing through Hadoop cluster.

- **ELK (elasticsearch，logstash，kibanna)**: used for collecting, querying, and presenting logs. Allows advanced and complex queries against log data.

### Core Engine Layer

The core engine layer of EnOS provides the following engines:

-   **Event engine** provides event alerts. Event engine obtains device abnormality information through event rules such as cross-threshold and combination of complex rules.

-   **Rule engine** functions as an IoT Hub. Rule engine distributes data to different engines for further processing based on rules configured.

-   **Stream computing and batch job process engines** provide core computing capability and can sup custom computing and data storage requirements from applications.

-   **AI engine** is a dedicated engine for machine learning.

The core engine layer facilitates application development through the service
layer.

### Service Layer

In the service layer, functions of the service modules are described as follows:

-   **Edge management service** supports full lifecycle management for edge computing devices. The service can monitor and connect device states.

-   **Device data access service** provides data ingestion and acquisition service through API and SDK with bi-directional access to data access points and calculation points.

-   **Common Data Service** provides data services such as weather, electricity price, and other common data in the IoT industrial.

-   **Application management suite** provides application management and debugging tools, such as access control and system isolation.

### Device Model and User Access Modules

The core engine layer and service layer provide external services through user access and device model modules.

Device model module is a device information database. It provides description information for device that is connected to EnOS and it allows the connection of new devices.

User access module provides asset-owner account management and application account management functions, which provides authentication and authorization from assets to application.

### EnOS Console and API Layer

EnOS Console and API layer is a scalable access interface of EnOS. In addition to the core capabilities of EnOS, this interface layer can also be scaled to support third-party application and tools.
