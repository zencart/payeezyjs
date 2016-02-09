# Payeezy JS Payment Module for Zen Cart

## About

The Payeezy JS payment service is a PCI Compliant payment solution which *does* show credit card fields on your store, to accept credit card payments, but does *all* the processing offsite (via background javascript/ajax processing), so that none of the card data ever touches your store/server. 
There is no redirecting of customers offsite, so customers enjoy a more seamless checkout experience.

The payment gateway is powered by First Data, and is availalble to all First Data and Global Gateway E4 merchants.

## Compatibility

This module is compatible with Zen Cart® v1.5.4 and v1.5.5

This module requires minimum PHP 5.6.0

## Installation

### PHP Files
Simply upload these files into the corresponding folders on your own store:

`/includes/modules/payment/payeezyjszc.php`

`/includes/languages/english/modules/payment/payeezyjszc.php`

`/includes/modules/pages/checkout_payment/jscript_payeezy.php`

**Note: You should not copy the README.md, LICENSE or changelog.txt files to your live server.**
 
### Admin module configuration
This module requires that you enter 5 configuration settings from your Payeezy and GGe4 account:

* API Key:         From your Payeezy account 
* API Secret:      From your Payeezy account
* Merchant Token:  From your Payeezy account
* JS Security Key: From your Payeezy account
* TA Token:        From your GGe4 account ("Trans Armor Token")

## Merchant Account Requirements

It uses your existing First Data or GGe4 merchant account after you create a profile on [payeezy.com](https://payeezy.com) and ask your First Data account rep to link the accounts. 

Details at [Payeezy FAQs](https://developer.payeezy.com/faqs/current-first-data-merchant-i-want-transact-through-payeezy-apismobile-payments-what-process)

