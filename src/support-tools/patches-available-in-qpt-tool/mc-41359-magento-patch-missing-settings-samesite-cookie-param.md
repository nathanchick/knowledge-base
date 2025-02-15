---
title: "MC-41359 commerce patch: missing settings SameSite cookie param"
labels: 2.3.6-p1,2.4.2,QPT 1.0.20,QPT patches,Magento Commerce,Magento Commerce Cloud,SameSite,browser,cookies,error,settings,support tools,Adobe Commerce,cloud architecture
---

The MC-41359 commerce patch fixes the issue with missing SameSite cookie parameters settings. This patch is available when the [Quality Patches Tool (QPT)](https://support.magento.com/hc/en-us/articles/360047139492) 1.0.20 is installed. The patch ID is MC-41359. Please note that the issue is scheduled to be fixed in Adobe Commerce 2.4.3.

## Affected products and versions

 **The patch is created for Adobe Commerce version:** Adobe Commerce on our cloud infrastructure 2.4.2

 **Compatible with Adobe Commerce versions:** Adobe Commerce and Adobe Commerce on our cloud Infrastructure  2.3.6-p1, 2.4.2, 2.4.2-p1

>![info]
>
>Note: the patch might become applicable to other versions with new QPT tool releases. To check if the patch is compatible with your Magento version, run `./vendor/bin/magento-patches status`.

## Issue

Missing settings of the SameSite cookie parameter.

 <ins>Steps to reproduce:</ins>

Prerequisites:

* Open Chrome and go to chrome://flags/
* Enable **SameSite by default cookies** and **Cookies without SameSite must be secure**.
* Open the Chrome inspector.

 <ins>Scenario 1:</ins>

1. Enable PayPal.
1. Go to the store front.
1. Add a product to the cart.
1. Go to checkout.

 <ins>Scenario 2:</ins>

If you have New Relic [enabled](https://docs.magento.com/user-guide/reports/new-relic-reporting.html) the warning appears on any frontend page.

<ins>Actual result:</ins>

Warning message in the browser console: *A cookie associated with a cross-site resource was set without a SameSite attribute.*

 <ins>Expected result:</ins>

"lax" should not be added to the cookie domain; the samesite attribute should be present with default value.

## Apply the patch

For instructions on how to apply an QPT patch, use the following links depending on your Magento product:

* Adobe Commerce: [Apply patches using Quality Patches Tool](https://devdocs.magento.com/guides/v2.4/comp-mgr/patching/mqp.html) in our developer documentation.
* Adobe Commerce on our cloud infrastructure: [Upgrades and Patches > Apply patches](https://devdocs.magento.com/cloud/project/project-patch.html) in our developer documentation.

## Related reading

To learn more about Quality Patches Tool, refer to:

* [Quality Patches Tool released: a new tool to self-serve quality patches](https://support.magento.com/hc/en-us/articles/360047139492).
* [Check if patch is available for your Adobe Commerce issue using Quality Patches Tool](https://support.magento.com/hc/en-us/articles/360047125252).

For info about other patches available in QPT tool, refer to the [Patches available in QPT tool](https://support.magento.com/hc/en-us/sections/360010506631-Patches-available-in-QPT-tool-) section.
