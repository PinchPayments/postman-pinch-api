# Postman Collection to access the Pinch Payments API

![image](https://user-images.githubusercontent.com/241857/116962566-a6291600-ace9-11eb-9084-d0e303274f4f.png)

This is a Postman Collection for the Pinch API v2020.1 endpoints. 

Refer to the main [Pinch API documentation](https://docs.getpinch.com.au/docs) for more details.

## Installation

Download, install and run Postman from the website [https://www.postman.com/downloads/](https://www.postman.com/downloads/)

Import into the Postman app by selecting `File -> Import` and importing the [Pinch API v2020.1.postman_collection.json](https://raw.githubusercontent.com/PinchPayments/postman-pinch-api/main/Pinch%20API%20v2020.1.postman_collection.json) and [Pinch API v2020.1.postman_environment.json](https://raw.githubusercontent.com/PinchPayments/postman-pinch-api/main/Pinch%20API%20v2020.1.postman_environment.json) files from this repository.

## Environment

Visit [https://web.getpinch.com.au/api-keys](https://web.getpinch.com.au/api-keys) to get your test & production API keys.

This Collection includes a pre-configured Environment. You will need to set up the following environment variables to the `Current Value` column in order to run each request:

|Name|Description|
|---|---|
|`merchantId`|Your Merchant Id. Starts with `mch_test_` for test.|
|`secretKey`|Secret Key. Starts with `sk_test_` for test.|
|`publishableKey`|Publishable Key. Starts with `pk_test_` for test.|
|`currentAccessToken`|Leave empty - populated automatically by postman.|
|`accessTokenExpiry`|Leave empty - populated automatically by postman.|
|`baseUrl`|https://api.getpinch.com.au|
|`authUrl`|https://auth.getpinch.com.au|

## Running the API Endpoints

The Postman pre-request script will take care of gathering a valid access token for all requests - so once you fill in the keys above with your test keys, you can call all requests without worrying about authentication.

## (Optional) Collection Variables


|Name|Description|
|---|---|
|`pinchVersion`|Set to `2020.1` by default. Can be changed to `2019.1`, `2017.2` or `2017.1`.|
|`environment`|Set to `test` by default. Can be changed to `live`.|

**For testing, these should be left as default values: `2020.1` and `test`.**

If you would like to run this collection against an earlier Pinch API version, you can change the `pinchVersion` property (which is sent as a header to the API with each request) to a previous version of the API. Previous versions are `2019.1`, `2017.2` and `2017.1`.

If you would like to run this collection against your production tenant you will need to change your `merchantId` and `secretKey` values set in the environment variables to the production keys and set this `environment` collection variable to `live`.
