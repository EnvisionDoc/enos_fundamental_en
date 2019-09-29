# EnOS Overview

EnOS™ is an intelligent IoT operating system for enterprises and cities to accelerate digital transformation and ecosystem development. EnOS builds on top of open standards and best design to ensure it operates in an open eco-system.

EnOS consists of the cloud side and edge side as shown in the following figure.

.. image:: media/architecture.png

## EnOS Cloud

EnOS Cloud provides fundamental capabilities of model-based device management, data acquisition, stream data processing, batch data processing, custom event triggering and time-sequence data query service. To streamline your digitalization journey through connectivity, analytics, and development, EnOS provides the following offerings:

### Device Management Offering

Device Management Offering helps abstract device models and allows connection of heterogeneous of devices in various domains such as industry, smart city, and smart building. By enabling secure and reliable connectivity, EnOS helps to achieve the real-time monitoring of devices and the end-to-end device lifecycle management from the cloud. For more information about the services, see [Device Management](/docs/device-connection/en/2.0.8/device_management_overview).

### Data Asset Management Offering

Data Asset Management Offering aims to help coap with the challenges of managing huge amount of data resulted from extensive connectivity. With industry knowledge accumulation, the Data Asset Management Services enable enterprises to manage data end-to-end on EnOS securely, effectively, flexibly, while with optimized cost. Through lowering barrier of stream data analytics, optimizing storage schema based on industry scenarios, opening storage policy configurability, and increasing data acquisition efficiency, Data Asset Management Services help reduce your total cost of ownership on data. For more information about the services, see [Data Asset Management](/docs/data-asset/en/2.0.8/data_asset_overview).

### Data Analytics Offering

Data Analytics Services provides large volume of data storage with low-cost and high computing capacity in a distributed architecture to help you integrate and process large volumnes of data at high speed. The services provides tools help you extract, transform, and load data from heterogeneous data sources such as your existing IT and OT systems and quickly obtain insights, explore new business models, and make your business decisions. With robust AI-ready architecture, you can also apply AI/machine learning as you integrate your data into EnOS. For more information about the services, see [Data Analytics](/docs/offline-data/en/2.0.8/datalake_analytics_overview).

### Data Visualization Offering

Data visualization offering contains the following services:

- Data Report, which helps you quickly render reports from your data in EnOS. For more information, see [Data Report](/docs/analysis-report/en/2.0.8/report_overview).

- Graph Tool, which enables you to build presentation of your assets efficiently in a drag-n-drop model.

## EnOS Edge

EnOS Edge provides capabilities of device data acquisition, device controlling, data normalization, and model-based real-time computing. The data communication channels between EnOS Edge and EnOS Cloud are secured by TLS/SSL protocol with dedicated X.509 certificate for each edge device and EnOS Cloud access point. For more information, see [EnOS Edge](/docs/enos-edge/en/2.0.8/edge_overview.html).

If a 3rd party edge is required, EnOS Cloud also supports 3rd party edges that are compatible with the EnOS device connection framework.

## Major Advantages

### Extensive connectivity

Simplified ubiquitous connectivity based on rich protocol library.

- EnOS supports direct device connections through the MQTT protocol and connections through the EnOS Edge or third-party edge products according to your business needs.
- EnOS Edge supports a rich set of industry-standard protocols and some private protocols of mainstream IoT vendors. EnOS also provides toolsets to help you develop your own protocol.

### Deployment flexibility

Enterprise-grade software stack with flexible deployment options (public, private, and hybrid cloud).

EnOS can operate in private cloud and public cloud hosting environment to enable clients to develop, run and operate their applications without handling the complexity of managing software stacks.

EnOS can also be deployed in virtual private cloud (VPC) on public cloud hosting environment and private cloud without dependency on underlying hypervisors. You can also deploy the solution that best suits your requirements for cost, control, configurability, scalability, location and security.

EnOS is compatible with most popular IaaS vendors such as Amazon AWS and Microsoft Azure. In order to keep the best compatibility, Public EnOS clusters only depends on the virtual machines and NFS services from selected IaaS providers. Many major components of EnOS IoT Core are built with state-of-the-art open source software. They are well supported by common OS environment running on virtual machines. EnOS cloud integrates with the management API of IaaS, making it possible to adjust the scale of an existing cluster or create new clusters in automation.

### Domain expertise

Domain driven data architecture promised by rich experience with smart energy devices and scenarios.

Through extensive domain metadata, EnOS supports standardized data acquisition policies, ingestion rules, event handling rules, data retention policies, ODS schema, access control policies and data quality policies. With configurable metadata mapping from the data source to the data target, this process will significantly reduce the effort required for data cleansing and normalization.

### Eco-system

Seamless integration with native and third-party applications, end-to-end tooling that empowers you to build your own platform.

EnOS allows users such as IoT engineers, data scientists, application developers, to perform operations such as managing devices and models, exploring data ingested from devices, configuring event triggering policies, rendering data analysis reports, and managing applications that are developed through the EnOS toolsets.

<!--Need to add description about the end user, system admins and application users-->
