# The Yandex.Checkout API PHP Client Library

[Russian](https://github.com/yandex-money/yandex-checkout-sdk-php/blob/master/README.md) | English

This product is used for managing payments under [The Yandex.Checkout API](https://kassa.yandex.ru/docs/checkout-api/)
For usage by those who implemented Yandex.Checkout using the API method.

## Requirements
PHP 5.3.2 (or later version) with the libcurl library

## Installation
### Under console using Composer

1. Install Composer, a package manger.
2. In the console, run the following command:
```bash
composer require yandex-money/yandex-checkout-sdk-php
```

### Do the following for the composer.json file of your project:
1. Add a string `"yandex-money/yandex-checkout-sdk-php": "*"` to the list of dependencies of your project in the composer.json file
```js
...
   "require": {
        "php": ">=5.3.0",
	"yandex-money/yandex-checkout-sdk-php": "*"
...
```
2. Refresh the project's dependencies. In the console, navigate to the catalog with composer.json and run the following command:
```bash
composer update
```

### Manually

1. Download [the Yandex.Checkout API PHP Client Library archive](https://github.com/yandex-money/yandex-checkout-sdk-php/releases/download/v1.0.3/yandex-checkout-sdk-php-v1.0.3.zip), extract it and copy the lib catalog to the required place of your project.
2. Adjust your project's code to activate automated uploading of files for our product:
```php
require __DIR__ . '/lib/autoload.php'; 
```

## Commencing work

1. Activate the dependency
```php
require __DIR__ . '/vendor/autoload.php';
```
2. Import required classes
```php
use YaMoney\Client\YandexMoneyApi;
```
3. Create a sample of a client object, then set the store's identifier and secret key (you can get them under your Yandex.Checkout's Merchant Profile). [Issuing a secret key](https://yandex.com/support/checkout/payments/keys.html)
```php
$client = new YandexMoneyApi();
$client->setAuth('shopId', 'secretKey');
```
4. Call the required API method. [More details in our documentation for the Yandex.Chechout API](https://checkout.yandex.com/docs/checkout-api/)
