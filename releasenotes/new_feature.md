# What’s New?

This section describes the new services and features in this release.


## Common Resource

We added support of data explorer sandbox resource management and registering GitLab data connection. Details are as follows:

### Resource Management

- In this release, we added support of requesting data explorer sandbox resource, which is compatible with the enhancement to EnOS Data Explorer. Before using data explorer for data processing, analysis, and visualization, you need to request data explorer sandbox resource based on your business needs. For more information, see [Resource Management on EnOS](/docs/enos/en/2.0.9/resourcemanagement/overview.html).

### Data Connection

- In this release, we added support of registering GitLab data source. When using the Jupyter Notebook in data explorer, you can save your code and notebook in the registered GitLab repository, achieving version control of your scripts. For more information, see [Configuring a GitLab Data Connection](/docs/offline-data/en/2.0.9/data_source/connecting_gitlab.html).
- Support for network connection testing for configured data source connection, improving the efficiency of data source configuration. For more information, see [Data Connection](/docs/offline-data/en/2.0.9/data_source/index.html).

## EnOS Edge

### Asset Tree

Added support of viewing asset trees that the sub-devices of an EnOS Edge are bound to. On these trees only the nodes where Edge-related logical assets and sub-devices are located are displayed. For more information, see [Managing Asset Tree](/docs/device-connection/en/2.0.9/howto/asset_tree/index).

### Metadata Export Service

Added support of exporting metadata, including model, asset, and asset tree, to a MySQL table to be used by applications.

### Alert

Provide similar alert service as provided on EnOS Cloud, including alert severity, type, content, and rule management. Alert masking, setting attribute as threshold, and triggering delay timer are not supported for now.

For more information, see [Managing Device Alerts](/docs/device-connection/en/2.0.9/howto/alert/index)。


### Stream Analytics

- Added support of StreamSets-based stream analytics capability on EnOS Edge.
- Added support of all general StreamSets operators that EnOS Cloud supports and photovoltaic-industry-specific StreamSets operators. For more information on what operators EnOS Edge supports, see [Edge Computing](/docs/enos-edge/en/2.0.9/learn/edge_computing#streamsets-operator-reference).
- Added support of StreamSets capability for EnOS Edge high availability (HA) deploying modes.
- Added support of StreamSets Pipeline configuration and management GUI as supported by EnOS Cloud.

For more information on how to develop StreamSets operators on EnOS Edge, see [Developing with StreamSets Operators](/docs/data-asset/en/2.0.9/howto/stream/streamsets).

### TSDB

We added support of TSDB on EnOS Edge. Details are as follows:

- Added support of reading from and writing data to the TSDB on EnOS Edge. Relevant APIs are provided to query from and write to TSDB.
- Added support of second-level storage of raw data and one-minute-level storage of normalized data.
- Added support of EnOS Edge HA. TSDB can be deployed on both the active and standby Edges to support HA deploying mode.

### IAM and Application Portal on EnOS Edge

- Added support of identity and access management (IAM) on EnOS Edge.

- Added support of Application Portal on EnOS Portal, including application integration and permission management.


## Device Management

We added support of alert triggering delay timer, and logical asset management. Details are as follows:

### Alert

- Added support of setting alert to be triggered when measurement points satisfying the alert rule is continuously reported for some time. In some scenarios, alerts need to be delayed until it persists for a specified time instead of being immediately triggered when there is an anomaly. You can set a triggering delay timer for these alert in alert rule. The timer starts when a measurement point satisfying the rule is reported. If subsequent measurement points continue to satisfy the rule, timer goes on. If any subsequent measurement point reported does not satisfy alert rule, the timer is reset. When the timer times out after the specified triggering delay, the alert is triggered. For more information, see [Tutorial: Setting Alert Triggering Delay Timer](/docs/device-connection/en/2.0.9/howto/alert/setting_alert_triggering_delay_timer)。

.. image:: media/alert_triggering_delay_timer.gif

### Locigal Asset Management

- Added support of logical asset management. You can manage your non-device assets created in **Asset Tree** in **Device Management > Logic Asset** . Editing and deleting logical assets are supported for now. For more information, see [Managing Asset Tree](/docs/device-connection/en/2.0.9/howto/device/manage/managing_assettree).

.. image:: media/non_device_asset_management.gif

## Data Analytics

In this release, we added support of the Jupyter Notebook data exploring tool. Details are as follows:

### Data Explorer

In addition to the Zeppelin Notebook, we added support of the Jupyter Notebook data exploring tool, which introduces Python2.x, Python3.x, and R kernels. Jupyter Notebook is an interactive data exploration tool, enabling data engineers and scientists to perform data processing and visualization in the same environment, create shared code and documents, simplify their workflow, and achieve higher productivity and better collaboration. For more information, see [Data Explorer](/docs/offline-data/en/2.0.9/data_explorer/index.html).

The workflow of data exploration is as follows:

.. image:: media/data_explorer_workflow.png

The general processing of creating and using the Jupyter Notebook is as follows:

.. image:: media/data_explorer.gif



## Application Enablement

### Service Hosting Center

Add support of switching organization in Service Hosting Center.

.. image:: media/shc_selectou.gif

### Application Portal

To enhance the experience of our clients using multiple applications, we’ve released EnOS Application Portal V1.0 in June 2019, which is a centralized access management and login portal for multiple applications registered and developed based on EnOS. Consisted of an admin console and application portal, EnOS Application Portal provides a One Product experience for enterprise and organization users with centralized and hierarchical management of applications based on users, roles, organization structure, applications, and asset permissions. 

- Through the admin console, the OU administrator of enterprises or organizations can make centralized and hierarchical management based on user, role, organization structure, application, and asset permission.
- The application portal provides application users with a unified portal for accessing applications of multiple domains. It enables users to access applications cross enterprises or organizations, switch languages, switch roles, view and handle application messages, and visiting the help center.

.. image:: media/app_portal.gif

Since the first release, we’ve added a couple of new features to meet more complex business scenarios:

- Message center: Centralized message center for displaying messages from multiple applications, with pop-up and ring notification, helping users to view and handle messages quickly.
- Application shortcut: Combining menus of multiple applications to form application shortcuts (virtual applications), meeting the requirement of different users and complex business scenarios.
- Soring applications: Change the order of applications in the admin console, so that the applications will be displayed accordingly in the application portal.
- Single Sign On (SSO): Support of the domain account system of enterprises or organizations, allowing users to log in Application Portal with domain accounts.
- Edge: Application Portal can be deployed on the Edge platform, achieving the usage of the Application Portal in Edge environment.
- Responsive web design: Users can access the portal functions through mobile browsers, such as switching between applications, viewing application, switching languages, and personal settings, etc.
- Importing users: When adding users to the organization, you can import multiple users with their roles and assigned organization structure defined in the Excel template provided by Application Portal. 

For more information, see [About Application Portal](/docs/app-development/en/2.0.9/app_portal/overview.html).
