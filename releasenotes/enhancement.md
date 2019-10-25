# What’s Changed?

This section lists the enhancements and behavior changes in this release.


## API

For details of updated APIs, log into the EnOS Console and click **EnOS API > Release Notes** from the navigation menu.

### Alert Service


.. list-table::
   :widths: auto
   :header-rows: 1

   * - API
     - Description
   * - Create Alert Rule
     - A new parameter ``triggeringDelayTimer`` is supported in request body to indicate the time of delaying the alert triggering.
   * - Search Active Alert
     - The response parameter ``value`` in the ``ActiveAlert`` struct supports recording the measurement point value when ``triggeringDelayTimer`` starts counting.
   * - Search Alert Rule
     - A new parameter ``triggeringDelayTimer`` is supported in ``AlertRule`` struct to indicate the time of delaying the alert triggering.
   * - Search History Alert
     - The function is changed to query historical alarms in the **last three months**.
        The response parameter ``value`` in the ``HistoryAlert`` struct supports recording the measurement point value when ``triggeringDelayTimer`` starts counting.
   * - Update Alert Rule
     - A new parameter ``triggeringDelayTimer`` is supported in ``alertRule`` struct to indicate the time of delaying the alert triggering.




### TSDB Data Service


.. list-table::
   :widths: auto
   :header-rows: 1

   * - API
     - Description
   * - Get Asset AI Raw Data
     - A new parameter ``withQuality`` is supported in request URI to get the quality indicator.
   * - Get Asset Generic Data
     - A new parameter ``withQuality`` is supported in request URI to get the quality indicator.
   * - Get Asset Raw Data by Time Range
     - A new parameter ``withQuality`` is supported in request URI to get the quality indicator.




## EnOS Edge

.. csv-table::
   :header: "Service/Function Module", "Before", "After", "Impact"
   :widths: auto

   "Edge Management", "Users cannot export mapping of collection points all devices for data forwarding", "Users can export mapping of collection points all devices for data forwarding", "None"
   "Template", "Users have to manually map collection points to every measurement point.", "Usera can have collection points automatically mapped to every measurement point.", "None"
   "Template", "Only system timestamp can be used for collection points.", "OEM timestamp can be used for collection points if the device supports OEM timestamp.", "None"
   "Template", "All collection points must be sent to EnOS Cloud.", "Some collection points can be configured not to be sent to EnOS Cloud.", "None"
   "Protocol", "Users cannot specify a custom version number when creating a protocol.", "Users can specify custom version numbers following EnOS-standard format.", "None"




## Device Management 

.. csv-table::
   :header: "Service/Function Module", "Before", "After", "Impact"
   :widths: auto

   "Model, Product, Device, Asset Tree", "Only em dash (-), underscore (_), period (.), and colon (:) are supported in model, device, product, asset tree, and asset names.", "Slash (/), asterisk (*), plus (+), number sign (#), and space ( ) are also supported in in model, device, product, asset tree, and asset names.", "None"
   "Device", "Users can only use model, device name, device key, and asset ID to search for a device.", "Product name can be used to search for device and exporting devices of the same product in batch is supported.", "None"
   "Device", "Users have to define sample data for, start, stop, or delete simulators one at a time.", "Defining data sample for, start, stop, and deleting simulators in batch are supported.", "None"
   "Alert", "Users have to create severity, type, content, and rule one at a time.", "Up to 10000 entries can be uploaded in batch for severity, type, content, and rule by editing and uploading template.", "None"
   "Alert", "Users have to use content and rule ID for searching.", "Added support of using model for searching content and rule, and exporting selected search results.", "None"
