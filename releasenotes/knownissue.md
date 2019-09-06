# EnOS Known Issues and Limitations

The article lists the knowns issues and limitations of EnOS in terms of products and services categorization.

.. list-table:: EnOS Known Issues and Limitations
   :widths: 30 30 22 6 6 6
   :header-rows: 1

   * - Issue Description
     - Symptom
     - Known Workaround
     - Discovery Time
     - State
     - Resolution Time
   * - The asset tree tag supports Chinese characters as the key, however, when the subscription service filters data based on asset tags, Chinese characters are not supported.
     - Applications cannot subscribe to data from assets whose tag contains Chinese characters. Streaming Service does not support to process data from assets whose tag contains Chinese characters either.
     - NA
     - 2019/08
     - Planning
     - 
   * - Non-device assets can only be viewed from the Asset Tree interface of EnOS Console.
     - When a non-device asset is removed from an asset tree, the asset still exists, however, there is no way to view the asset from EnOS Console anymore.
     - NA
     - 2019/08
     - Planning
     - 

<!--end-->