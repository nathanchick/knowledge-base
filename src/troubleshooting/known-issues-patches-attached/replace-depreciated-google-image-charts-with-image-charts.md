---
title: Replace depreciated Google Image Charts with Image-Charts
labels: Google Image Charts,Magento Commerce,Magento Commerce Cloud,patch,troubleshooting
---

Updated April 16th

Most Magento editions and versions currently use [Google Image Charts](https://developers.google.com/chart/image/) to render static charts in Admin dashboards. As of March 14, 2019, Google will stop supporting Google Image Charts. To resolve this issue, we are providing a patch to replace Google Image Charts with [Image-Charts](https://www.image-charts.com/) free service.

## Affected versions

* Magento 1.X all editions
* Magento 2.X all editions

>![info]
>
>Magento Commerce 1.14.4.1, Magento Open Source 1.9.4.1, Magento Commerce and Cloud 2.3.2 will include this chart update. Upgrading to these versions continues support for image charts without additional patches.

## Issue

Google stop supporting Google Image Charts on March 14, 2019. Users of Magento 1.X and Magento 2.2.X all versions will not be able to view static charts unless they download and apply the patch, replacing Google Image Charts with Image-Charts solution. Displayed charts will have the same design and functionality of Google Image Charts through the Image-Charts free account service with a [GDPR](https://www.image-charts.com/data-processing-addendum.html) compliance privacy policy. For additional options, please see [Image-Charts](https://www.image-charts.com/) .

## Solution

To be able to view static charts in Magento Admin, download and apply the patch provided by Magento. No additional configuration is necessary.

### Magento 2 Commerce

1. Save the [attached MAGETWO-98833\_composer\_patch-2019-04-15-04-38-57.patch](assets/MAGETWO-98833_composer_patch-2019-04-15-04-38-57.patch.zip) patch and upload it to your Magento root directory.
1. Run the following SSH command, having replaced the patch name with actual one:    ```git    patch -p1 < MAGETWO-98833_composer_patch-2019-04-15-04-38-57.patch    ```    (If the above command does not work, try using `-p2` instead of `-p1` )
1. For the changes to be reflected, refresh the cache in the Admin under **System** > **Cache Management** .

### Magento 2 Cloud

For Cloud merchants, the patch will be included to the nearest ECE-tools update.

### Magento 2 Open Source

1. Go to [https://magento.com/tech-resources/download\#download2291](https://magento.com/tech-resources/download#download2291) .
1. In the **Select your format** drop-down list, select the composer version and click **Download** .
1. Upload the patch to your Magento root directory.
1. Run the following SSH command, having replaced the patch name with actual one:    ```git    patch -p1 < MAGETWO-98833_composer_patch-2019-04-15-04-37-48.patch    ```    (If the above command does not work, try using `-p2` instead of `-p1` )
1. For the changes to be reflected, refresh the cache in the Admin under **System** > **Cache Management** .

### Magento 1 Commerce

Follow these steps to download and apply the patch:

1. Save the [attached MPERF-10509-EE-2019-03-13-06-32-19.diff](assets/MPERF-10509-EE-2019-03-13-06-32-19.diff.zip) patch and upload it to your Magento root directory.
1. Run the following SSH command:    ```git    patch -p1 < MPERF-10509-EE-2019-03-13-06-32-19.diff    ```    (If the above command does not work, try using `-p2` instead of `-p1` )
1. For the changes to be reflected, refresh the cache in the Admin under **System** > **Cache Management** .

### Magento 1 Open Source

Follow these steps to download and apply the patch:

1. Click [ **this link** ](https://magento.com/tech-resources/download#download2283) to locate the Admin Dashboard Charts Patch.
1. Select    ```git    MPERF-10509.diff    ```    from the **Select your format** drop-down and click Download.
1. Upload the file to the Magento root directory.
1. Run the following SSH command:    ```git    patch -p1 < MPERF-10509.diff    ```    (If the above command does not work, try using `-p2` instead of `-p1` )
1. For the changes to be reflected, refresh the cache in the Admin under **System** > **Cache Management** .

## Attached Files
