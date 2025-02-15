---
title: "MDVA-19640 Magento patch: Advanced reporting shows no data"
labels: 2.3.1,2.3.2,2.3.2-p2,2.3.3,2.3.3-p1,2.3.4,2.3.4-p1,2.3.4-p2,2.3.5,2.3.5-p1,2.3.5-p2,2.3.6,2.3.6-p1,2.4.0,2.4.0-p1,2.4.1,2.4.1-p1,2.4.1-p2,2.4.2,Advanced Reporting,QPT 1.0.20,QPT patches,Magento Commerce,Magento Commerce Cloud,empty,no data,Quality Patches Tool,QPT 1.0.20,QPT patches
---

The MDVA-19640 Magento patch fixes the issue when Advanced Reporting shows no data. This patch is available when the [Quality Patches Tool (QPT)](https://support.magento.com/hc/en-us/articles/360047139492) 1.0.20 is installed. The patch ID is MDVA-19640. Please note that there is no current plan to fix this issue in future versions.

## Affected products and versions

 **The patch is created for Magento version:** Magento Commerce Cloud 2.3.0

 **Compatible with Magento versions:** Magento Commerce and Magneto Commerce Cloud 2.3.1-2.4.2

>![info]
>
>Note: the patch might become applicable to other versions with new QPT tool releases. To check if the patch is compatible with your Magento version, run `./vendor/bin/magento-patches status` .

## Issue

 <span class="wysiwyg-underline">Steps to reproduce</span> :

1. In Admin go to **Reports > Business Intelligence** and select **Advanced Reporting** .
1. View the **Advanced Reporting** page.

 <span class="wysiwyg-underline">Expected results</span> :

The Advanced Reporting report contains information, as expected.

 <span class="wysiwyg-underline">Actual results</span> :

The Advanced Reporting report shows no data.

## Apply the patch

To apply individual patches use the following links depending on your Magento product:

* Magento Commerce: DevDocs [Software Update Guide > Apply Patches](https://devdocs.magento.com/guides/v2.4/comp-mgr/patching.html) .
* Magento Commerce Cloud: DevDocs [Upgrades and Patches > Apply Patches](https://devdocs.magento.com/cloud/project/project-patch.html) .

## Related reading

To learn more about Quality Patches Tool, refer to:

* [Quality Patches Tool released: a new tool to self-serve quality patches](https://support.magento.com/hc/en-us/articles/360047139492) .
* [Check patch for Magento issue with Quality Patches Tool](https://support.magento.com/hc/en-us/articles/360047125252) .

For info about other patches available in QPT tool, refer to the [Patches available in QPT tool](https://support.magento.com/hc/en-us/sections/360010506631-Patches-available-in-QPT-tool-) section.