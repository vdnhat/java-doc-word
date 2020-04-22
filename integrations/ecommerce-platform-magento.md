---
description: 'Magento version: 2.3.x'
---

# Ecommerce Platform: Magento

* **Step 1:** Download [**extension files**](https://firebasestorage.googleapis.com/v0/b/gitbook-28427.appspot.com/o/assets%2F-LvxycBHx7ziVQP2E5we%2F-M3Cq3Bh1lI-1FspMvYU%2F-M3CvGkQVtuh8fprJS0D%2FCDP.zip?alt=media&token=65c9f1bf-1203-4371-ab8f-7f04ddffbe6e)\*\*\*\*
* **Step 2:** Copy the extension files to below paths of your magento 2 instance. If 'app/code/CDP' folder is missing, please create it manually: app/code/CDP 
* **Step 3:**. Access the root of your magento 2 project from command line and run the following commands: 
  * php bin/magento module:enable CDP\_Backend --clear-static-content ;
  * php bin/magento module:enable CDP\_Insight --clear-static-content ; 
  * php bin/magento setup:upgrade ; 
  * php bin/magento cache:flush ; 
  * php bin/magento setup:di:compile ; 
  * php bin/magento setup:static-content:deploy -f vi\_VN en\_US -j5
  * 
* **Step 4:** Flush any cache that you might still have enabled on your server or in Magento. 
* **Step 5:** Woohoo, the extension is installed!

![](../.gitbook/assets/magento-cdp-plugin.png)

