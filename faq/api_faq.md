# FAQs about EnOS APIs

The topic lists frequently asked questions about calling EnOS APIs.

**Q: What is the amount limit of historical data supported by the *getAssetsRawDataByTimeRange* API?**

A: The *getAssetsRawDataByTimeRange* API retrieves data from TSDB. According to the current logic of TSDB, the *getAssetsRawDataByTimeRange* API supports retrieving historical data in the past 3 months.



**Q: If needed, how to retrieve historical data beyond the amount limit (> 3 months)?**

A: If there is business requirement, the internal API *DataDownload* supports retrieving historical data beyond the limit of the *getAssetsRawDataByTimeRange* API. Contact the support team to enable the *DataDownload* API.



**Q: For organizations with big amount of devices, how to retrieve asset tree?**

A: Call the listAssets API repeatedly with the *pageSize* and the *pageToken* parameters specified. The list of assets will be returned by pages.



**Q: Why is authentication failed for 3rd party users who call the APIs using authorized APP key and secret?**

A: Contact EnOS support team to enable permission for 3rd party users to access the application of the authorized customer.