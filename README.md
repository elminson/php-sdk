# Payment Rails PHP staging SDK

## Requirements

PHP 5.4.0 and later

## Installation & Usage


### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/PaymentRailsClient-php/autoload.php');
```

### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com/PaymentRails/php-sdk.git"
    }
  ],
  "require": {
    "PaymentRails/php-sdk": "*"
  }
}
```

Then run `composer install`


## Tests

To run the unit tests:

```
composer install
./vendor/bin/phpunit lib/Tests
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: merchantKey
PaymentRails\Client\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// PaymentRails\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$api_instance = new PaymentRails\Client\Api\BalancesApi();

try {
    $result = $api_instance->getPaymentrails();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BalancesApi->getPaymentrails: ', $e->getMessage(), PHP_EOL;
}

?>
```

## Documentation for API Endpoints

All URIs are relative to *http://api.railz.io/v1*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*BalancesApi* | [**getPaymentrails**](docs/Api/BalancesApi.md#getpaymentrails) | **GET** /profile/balances/paymentrails |
*BalancesApi* | [**getPaypal**](docs/Api/BalancesApi.md#getpaypal) | **GET** /profile/balances/paypal |
*BalancesApi* | [**queryBalances**](docs/Api/BalancesApi.md#querybalances) | **GET** /profile/balances |
*BatchApi* | [**getBatch**](docs/Api/BatchApi.md#getbatch) | **GET** /batches/{batchId} |
*BatchApi* | [**startProcessingBatch**](docs/Api/BatchApi.md#startprocessingbatch) | **POST** /batches/{batchId}/start-processing |
*BatchApi* | [**updateBatch**](docs/Api/BatchApi.md#updatebatch) | **PATCH** /batches/{batchId} |
*BatchesApi* | [**createBatch**](docs/Api/BatchesApi.md#createbatch) | **POST** /batches |
*BatchesApi* | [**queryBatches**](docs/Api/BatchesApi.md#querybatches) | **GET** /batches |
*PaymentsApi* | [**getPayment**](docs/Api/PaymentsApi.md#getpayment) | **GET** /v1/payments/{paymentId} |
*PaymentsApi* | [**queryPayments**](docs/Api/PaymentsApi.md#querypayments) | **GET** /payments |
*RecipientApi* | [**createBankAccount**](docs/Api/RecipientApi.md#createbankaccount) | **POST** /recipients/{recipientId}/payout-methods/accounts/bank |
*RecipientApi* | [**createPaypalAccount**](docs/Api/RecipientApi.md#createpaypalaccount) | **POST** /recipients/{recipientId}/payout-methods/accounts/paypal |
*RecipientApi* | [**createRecipientPayoutMethods**](docs/Api/RecipientApi.md#createrecipientpayoutmethods) | **POST** /recipients/{recipientId}/payout-methods |
*RecipientApi* | [**deleteRecipient**](docs/Api/RecipientApi.md#deleterecipient) | **DELETE** /recipients/{recipientId} |
*RecipientApi* | [**getBankAccount**](docs/Api/RecipientApi.md#getbankaccount) | **GET** /recipients/{recipientId}/payout-methods/accounts/bank |
*RecipientApi* | [**getPaypalAccount**](docs/Api/RecipientApi.md#getpaypalaccount) | **GET** /recipients/{recipientId}/payout-methods/accounts/paypal |
*RecipientApi* | [**getRecipient**](docs/Api/RecipientApi.md#getrecipient) | **GET** /recipients/{recipientId} |
*RecipientApi* | [**getRecipientInfo**](docs/Api/RecipientApi.md#getrecipientinfo) | **GET** /recipients/{recipientId}/info |
*RecipientApi* | [**getRecipientPayoutMethods**](docs/Api/RecipientApi.md#getrecipientpayoutmethods) | **GET** /recipients/{recipientId}/payout-methods |
*RecipientApi* | [**queryRecipientComplianceHistory**](docs/Api/RecipientApi.md#queryrecipientcompliancehistory) | **GET** /recipients/{recipientId}/compliance |
*RecipientApi* | [**queryRecipientLogHistory**](docs/Api/RecipientApi.md#queryrecipientloghistory) | **GET** /recipients/{recipientId}/logs |
*RecipientApi* | [**queryRecipientPaymentHistory**](docs/Api/RecipientApi.md#queryrecipientpaymenthistory) | **GET** /recipients/{recipientId}/payments |
*RecipientApi* | [**updateBankAccount**](docs/Api/RecipientApi.md#updatebankaccount) | **PATCH** /recipients/{recipientId}/payout-methods/accounts/bank |
*RecipientApi* | [**updatePaypalAccount**](docs/Api/RecipientApi.md#updatepaypalaccount) | **PATCH** /recipients/{recipientId}/payout-methods/accounts/paypal |
*RecipientApi* | [**updateRecipient**](docs/Api/RecipientApi.md#updaterecipient) | **PATCH** /recipients/{recipientId} |
*RecipientApi* | [**updateRecipientInfo**](docs/Api/RecipientApi.md#updaterecipientinfo) | **PATCH** /recipients/{recipientId}/info |
*RecipientApi* | [**updateRecipientPayoutMethods**](docs/Api/RecipientApi.md#updaterecipientpayoutmethods) | **PATCH** /recipients/{recipientId}/payout-methods |
*RecipientsApi* | [**createRecipient**](docs/Api/RecipientsApi.md#createrecipient) | **POST** /recipients |
*RecipientsApi* | [**deleteRecipients**](docs/Api/RecipientsApi.md#deleterecipients) | **DELETE** /recipients |
*RecipientsApi* | [**exportRecipientCsv**](docs/Api/RecipientsApi.md#exportrecipientcsv) | **GET** /recipients/exports.csv |
*RecipientsApi* | [**queryRecipients**](docs/Api/RecipientsApi.md#queryrecipients) | **GET** /recipients |
*RecipientsApi* | [**uploadRecipientCsv**](docs/Api/RecipientsApi.md#uploadrecipientcsv) | **POST** /recipients/upload |
*UtilsApi* | [**getCurrency**](docs/Api/UtilsApi.md#getcurrency) | **GET** /forex/currencies/{currencyCode} |
*UtilsApi* | [**queryCurrencies**](docs/Api/UtilsApi.md#querycurrencies) | **GET** /forex/currencies |


## Documentation For Models

 - [Balance](docs/Model/Balance.md)
 - [BankAccount](docs/Model/BankAccount.md)
 - [Batch](docs/Model/Batch.md)
 - [BatchList](docs/Model/BatchList.md)
 - [BatchPayment](docs/Model/BatchPayment.md)
 - [BatchPaymentPatch](docs/Model/BatchPaymentPatch.md)
 - [BatchPaymentPost](docs/Model/BatchPaymentPost.md)
 - [BatchPaymentRecipient](docs/Model/BatchPaymentRecipient.md)
 - [BatchPost](docs/Model/BatchPost.md)
 - [BatchUpdate](docs/Model/BatchUpdate.md)
 - [Currency](docs/Model/Currency.md)
 - [DeleteIds](docs/Model/DeleteIds.md)
 - [InlineResponse200](docs/Model/InlineResponse200.md)
 - [InlineResponse2001](docs/Model/InlineResponse2001.md)
 - [InlineResponse2002](docs/Model/InlineResponse2002.md)
 - [InlineResponse2003](docs/Model/InlineResponse2003.md)
 - [InlineResponse2004](docs/Model/InlineResponse2004.md)
 - [InlineResponse2005](docs/Model/InlineResponse2005.md)
 - [InlineResponse2006](docs/Model/InlineResponse2006.md)
 - [MetaQuery](docs/Model/MetaQuery.md)
 - [PaymentBatch](docs/Model/PaymentBatch.md)
 - [PaymentComplianceStatus](docs/Model/PaymentComplianceStatus.md)
 - [PaymentOut](docs/Model/PaymentOut.md)
 - [PaymentRecipient](docs/Model/PaymentRecipient.md)
 - [PaypalAccount](docs/Model/PaypalAccount.md)
 - [Recipient](docs/Model/Recipient.md)
 - [RecipientAddress](docs/Model/RecipientAddress.md)
 - [RecipientCompliance](docs/Model/RecipientCompliance.md)
 - [RecipientComplianceStatus](docs/Model/RecipientComplianceStatus.md)
 - [RecipientInfoIn](docs/Model/RecipientInfoIn.md)
 - [RecipientInfoOut](docs/Model/RecipientInfoOut.md)
 - [RecipientLog](docs/Model/RecipientLog.md)
 - [RecipientPayment](docs/Model/RecipientPayment.md)
 - [RecipientPayoutAccounts](docs/Model/RecipientPayoutAccounts.md)
 - [RecipientPayoutMethods](docs/Model/RecipientPayoutMethods.md)
 - [RecipientPayoutMethodsLimit](docs/Model/RecipientPayoutMethodsLimit.md)
 - [RecipientPayoutMethodsPrimary](docs/Model/RecipientPayoutMethodsPrimary.md)
 - [RecipientPost](docs/Model/RecipientPost.md)


## Documentation For Authorization


## merchantKey

- **Type**: API key
- **API key parameter name**: x-api-key
- **Location**: HTTP header


## Author
