---
title: Installation xdebug maximum function nesting level error
labels: Magento Commerce,Magento Commerce Cloud,PHP Fatal Error,how to,level,nesting,xdebug
---

This article provides a fix for the xdebug maximum function nesting level error, during installation.

## Details

During Magento installation, a message similar to the following displays:

 `PHP Fatal error: Maximum function nesting level of '100' reached, aborting! in <path>/ClassLoader.php` 

It is strongly recommended that you DO NOT USE `xdebug` on a Production environment!

## Solution

There is a known issue with `xdebug` that can affect Magento installations or access to the storefront or Magento Admin after installation.

For details, see [Known issue with xdebug](https://support.magento.com/hc/en-us/articles/360034242212) .