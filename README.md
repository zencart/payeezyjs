# Payeezy JS (Payments.js Version 1) Payment Module for Zen Cart

## About

The Payeezy JS payment service is a PCI Compliant payment solution which *does* show credit card fields on your store, to accept credit card payments, but does *all* the processing offsite (via background javascript/ajax processing), so that none of the card data ever touches your store/server. 
There is no redirecting of customers offsite, so customers enjoy a more seamless checkout experience.

The payment gateway is powered by First Data, and is available to all First Data and Global Gateway E4 merchants.

## Compatibility

This module is compatible with Zen Cart® v1.5.4 and v1.5.5

This module works with PHP 5 up to PHP 7.1. Not tested extensively on higher PHP versions.

## Installation

### PHP Files
Simply upload these files into the corresponding folders on your own store:

`/includes/modules/payment/payeezyjszc.php`

`/includes/languages/english/modules/payment/payeezyjszc.php`

`/includes/modules/pages/checkout_payment/jscript_payeezy.php`

**Note: You should not copy the README.md, LICENSE files to your live server.**
 
### Admin module configuration
This module requires that you enter 5 configuration settings from your Payeezy and GGe4 account:

* `API Key`:         From your Payeezy account 
* `API Secret`:      From your Payeezy account
* `Merchant Token`:  From your Payeezy account
* `JS Security Key`: From your Payeezy account
* `TA Token`:        From your GGe4 account ("Trans Armor Token")

## Merchant Account Requirements

It uses your existing First Data or GGe4 merchant account after you create a profile on [payeezy.com](https://payeezy.com) and ask your First Data account rep to link the accounts. 

Details at [Payeezy FAQs](https://developer.payeezy.com/faqs/current-first-data-merchant-i-want-transact-through-payeezy-apismobile-payments-what-process)

## Detailed Payeezy Merchant Setup Instructions
It may seem odd, but it starts out with creating a Payeezy Developer account, which then is linked to your live Merchant account. Don't be confused by the terminology ;)
 
1. Merchant Quick Registration

 Sign up for a free Payeezy developer account at https://developer.payeezy.com. All you need is your First name, Last name and a valid email address. Note: Portal registration requires a valid e-mail address. Once registered, your email address cannot be changed in future. All e-mails from the Payeezy system will be sent to this registered email address. The e-mail address will not be made public and will only be used if you wish to receive notifications by e-mail. After you provide registration information an email is sent to you with further instructions to activate your account.

2. Get Certified

 Payeezy developer accounts need to be certified before being able to perform live transactions.
 
 To get certified,  
  a. Navigate to Account -> Get Certified.  
  b. Enter your full profile information.  
  c. Click on “Certify”.  
  d. Save.  
 You will be certified after submitting the CERTIFICATION form. This is basically immediate.

3. Add Merchant(s)  
 Once your certification is complete, the developer portal will automatically redirect to “Add Merchant” page. Click on "Live" and then click on "Add a merchant".  
 
  • If you DO already have a Payeezy merchant account with First Data, select "Add your existing merchant account" and follow the instructions on the screen. In order for this to work, the First Data merchant account must be enabled for Payeezy API. If you are not sure what this is, check with the merchant service provider (ie: call your First Data rep).  
  
  • If you DO NOT have a Payeezy merchant account and need to apply for one, select "Sign up for a merchant account" and follow the instructions.
  

 If you are unable to add your merchant account for some reason,  email payeezyboarding@firstdata.com with the Merchant ID (or storeID), DBA name and developer account email address. We (First Data) will add the merchant account to your developer account manually within 2 business days and send you a notification.

 After your merchant account is added and approved, you will see the `Merchant Token` and `JS Security Key`.

 The `TA_TOKEN` (or Transarmor token) can be obtained by logging in to https://globalgatewaye4.firstdata.com, navigating to the Terminals page and selecting your terminal. 
  If the Transarmor token is blank, it means that your account has not been enabled for Transarmor yet. To enable Transarmor for your account, you will need to reach out to your account representative or call 1-855-799-0790. 
  

4. Create an API -- within Payeezy your registered API gives you a pair of Key/Secret values which allow you to do Payeezy transactions.

 • Login to your Payeezy developer account and navigate to the "APIs" page.   
 • Click the “+ ADD A NEW API” button.  
 • On the next screen you name your application. Call it "My Store" or whatever you want to appear on reports.  
 • Choose "Sandbox” and "Live".  
 • Click on “Create your API”. You will be taken back to the APIs page.  
 • Click on the API you just created. You will see your `API key` and `API secret`.   

5.	Go Live In Zen Cart
 Enter the following in your Zen Cart module for Payeezy, as you obtained them from the steps above.  
 •	`API Key`  
 •	`API Secret`  
 •	`Merchant Token`  
 •	`JS_Security_Key`  
 •	`TA_TOKEN` (Only required for US domiciled merchants; leave blank outside the US)  

