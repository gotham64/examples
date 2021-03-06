<div align="center">

# Bandwidth All-Number-Orderer

![BW_all](../../.readme_images/BW_PhoneNumbers.png)
</div>

## Brief Descirption

Requests for every area code in the US will be created in your Bandwidth account.

To view the results of the request, you can go to your bandwidth dashboard and view orders.
If you see a failed order, this is likely due to Bandwidth not having numbers in this area code.

You can see the list of failed orders and their reasons in your bandwidth dashboard, under the subaccount/site you ordered it with within the "alerts" section.

## Prereqs

* Bandwidth Account
* Bandwidth Subaccount/Site Created
* Bandwidth Location/Sippeer Created on your Subaccount/Site
* NodeJS setup and configured on your machine

## Instructions

To get the script to run properly please do the following IN ORDER in the command line or bash:

1. Download this OrderPhoneNumebrInAllAreaCodes directory (you can git clone this repository). Change directory until you are in this one(the OrderPhoneNumberInAllAreaCodes directory).
2. Set the environemnt variables as seen below

### Environment Variables

The following environmental variables need to be set

| Variable                 | Description                        |
|:-------------------------|:-----------------------------------|
| `BANDWIDTH_ACCOUNT_ID`   | Your Bandwidth account ID          |
| `BANDWIDTH_API_USER`     | Your Bandwidth API username        |
| `BANDWIDTH_API_PASSWORD` | Your Bandwidth API password        |
| `BANDWIDTH_SITE_ID`      | Your Bandwidth Subaccount/Site ID  |

#### How-to

Replace your_dashboard_username with your bandwidth dashboard username, and likewise for the others.
Site is the subaccount you would like to order the numbers under.

```
set BANDWIDTH_API_USER=your_dashboard_username
set BANDWIDTH_API_PASSWORD=your_dashboard_password
set BANDWIDTH_ACCOUNT_ID=your_account_id
set BANDWIDTH_SITE_ID=your_site_id
```

This will set the environment variables so that the program can securely access and use them to place phone orders.
_NOTE THAT FOR MAC AND LINUX, SETTING ENVIRONMENT VARIABLES TAKES A DIFFERENT SYNTAX._
If you are using a mac system, a helpful google would be "mac setting environment variables".

### Install and run

Then run the following in the same directory of the script (in OrderNumbers):

```
npm install .
```

Then, run the program with:

```
node app.js
```
