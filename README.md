# EpayPolicySdk

This API supports the processing of credit card and eCheck/ACH payments.

For more information, please visit [http://epay3.com](http://epay3.com).

## Installation & Usage

### Requirements

PHP 7.4 and later.
Should also work with PHP 8.0.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/GIT_USER_ID/GIT_REPO_ID.git"
    }
  ],
  "require": {
    "GIT_USER_ID/GIT_REPO_ID": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/EpayPolicySdk/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



// Configure HTTP basic authorization: basic
$config = Tns\\EpayPolicy\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Tns\\EpayPolicy\Api\AutoPayApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | The Id of the AutoPay.
$impersonation_account_key = 'impersonation_account_key_example'; // string | The key that allows impersonation of another account for which the transaction(s) will be processed. Only specify a value if the account being impersonated is different from the account that is submitting this request.

try {
    $apiInstance->autoPayCancel($id, $impersonation_account_key);
} catch (Exception $e) {
    echo 'Exception when calling AutoPayApi->autoPayCancel: ', $e->getMessage(), PHP_EOL;
}

```

## API Endpoints

All URIs are relative to *https://api-sandbox.epaypolicy.com:443*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AutoPayApi* | [**autoPayCancel**](docs/Api/AutoPayApi.md#autopaycancel) | **POST** /api/v1/autoPay/{id}/cancel | Cancels an active Auto Pay.
*AutoPayApi* | [**autoPayGet**](docs/Api/AutoPayApi.md#autopayget) | **GET** /api/v1/autoPay/{id} | Retrieves the details of an AutoPay.
*AutoPayApi* | [**autoPayPost**](docs/Api/AutoPayApi.md#autopaypost) | **POST** /api/v1/autoPay | Creates an Auto Pay.
*AutoPayApi* | [**autoPaySearch**](docs/Api/AutoPayApi.md#autopaysearch) | **GET** /api/v1/autoPays | Retrieves a list of auto pays based on search parameters.
*BatchesApi* | [**batchesGet**](docs/Api/BatchesApi.md#batchesget) | **GET** /api/v1/batches | Gets a collection of Batches.
*FinanceApi* | [**financeConvertQuote**](docs/Api/FinanceApi.md#financeconvertquote) | **POST** /api/v1/Finance/ConvertQuote | ConvertQuote is to convert the given Quote and Creates an AutoPay subscription
*InvoicesApi* | [**invoicesEmail**](docs/Api/InvoicesApi.md#invoicesemail) | **POST** /api/v1/Invoices/Email | Sends an email for a collection of invoices in the management system.
*InvoicesApi* | [**invoicesGet**](docs/Api/InvoicesApi.md#invoicesget) | **GET** /api/v1/Invoices | Gets a collection of invoices given lookup attributes. Add these attributes as individual parameters.
*InvoicesApi* | [**invoicesPayments**](docs/Api/InvoicesApi.md#invoicespayments) | **POST** /api/v1/Invoices/Payments | Updates a collection of invoices in the management system.
*InvoicesApi* | [**invoicesUpdate**](docs/Api/InvoicesApi.md#invoicesupdate) | **POST** /api/v1/Invoices | Updates a collection of invoices in the management system.
*IvrSessionsApi* | [**ivrSessionsPost**](docs/Api/IvrSessionsApi.md#ivrsessionspost) | **POST** /api/v1/ivrSessions | Creates a temporary \&quot;session\&quot; with parameters so that the caller can be forwarded to the IVR service with this context.
*ManagedInvoicesApi* | [**managedInvoicesFinance**](docs/Api/ManagedInvoicesApi.md#managedinvoicesfinance) | **POST** /api/v1/managedInvoices/{id}/finance | Creates Managed Invoice with Financing.
*ManagedInvoicesApi* | [**managedInvoicesGet**](docs/Api/ManagedInvoicesApi.md#managedinvoicesget) | **GET** /api/v1/managedInvoices/{id} | Retrieves the details of a managed invoice.
*ManagedInvoicesApi* | [**managedInvoicesPost**](docs/Api/ManagedInvoicesApi.md#managedinvoicespost) | **POST** /api/v1/managedInvoices | Creates Managed Invoice.
*ManagedInvoicesApi* | [**managedInvoicesSearch**](docs/Api/ManagedInvoicesApi.md#managedinvoicessearch) | **GET** /api/v1/managedInvoices | Retrieves a list of Managed invoices based on search parameters.
*ManagedInvoicesApi* | [**managedInvoicesVoid**](docs/Api/ManagedInvoicesApi.md#managedinvoicesvoid) | **POST** /api/v1/managedInvoices/{id}/void | Processes a void of a managed invoice.
*PaymentSchedulesApi* | [**paymentSchedulesCancel**](docs/Api/PaymentSchedulesApi.md#paymentschedulescancel) | **POST** /api/v1/paymentSchedules/{id}/cancel | Cancels an active payment schedule.
*PaymentSchedulesApi* | [**paymentSchedulesGet**](docs/Api/PaymentSchedulesApi.md#paymentschedulesget) | **GET** /api/v1/paymentSchedules/{id} | Retrieves the details of a payment schedule.
*PaymentSchedulesApi* | [**paymentSchedulesPost**](docs/Api/PaymentSchedulesApi.md#paymentschedulespost) | **POST** /api/v1/paymentSchedules | Creates a payment schedule for a delayed payment or recurring payments.
*TokenPageSessionsApi* | [**tokenPageSessionsPost**](docs/Api/TokenPageSessionsApi.md#tokenpagesessionspost) | **POST** /api/v1/tokenPageSessions | Creates a temporary \&quot;session\&quot; with parameters so that the user can be forwarded to the token page with this context.
*TokensApi* | [**tokensDelete**](docs/Api/TokensApi.md#tokensdelete) | **DELETE** /api/v1/tokens/{id} | Removes a stored token.
*TokensApi* | [**tokensGet**](docs/Api/TokensApi.md#tokensget) | **GET** /api/v1/tokens/{id} | Retrieves the details of a token.
*TokensApi* | [**tokensPost**](docs/Api/TokensApi.md#tokenspost) | **POST** /api/v1/tokens | Stores a token for either ACH or credit card payments.
*TransactionFeesApi* | [**transactionFeesGet**](docs/Api/TransactionFeesApi.md#transactionfeesget) | **GET** /api/v1/transactionFees | Calculates and returns transaction fees for a given net amount due based on the account.
*TransactionsApi* | [**transactionsAuthorize**](docs/Api/TransactionsApi.md#transactionsauthorize) | **POST** /api/v1/transactions/authorize | Creates an authorization on a credit card.
*TransactionsApi* | [**transactionsGet**](docs/Api/TransactionsApi.md#transactionsget) | **GET** /api/v1/transactions/{id} | Retrieves the details of a transaction.
*TransactionsApi* | [**transactionsPost**](docs/Api/TransactionsApi.md#transactionspost) | **POST** /api/v1/transactions | Processes a sale transaction for either ACH or credit card.
*TransactionsApi* | [**transactionsRefund**](docs/Api/TransactionsApi.md#transactionsrefund) | **POST** /api/v1/transactions/{id}/refund | Processes a refund of a transaction.
*TransactionsApi* | [**transactionsSearch**](docs/Api/TransactionsApi.md#transactionssearch) | **GET** /api/v1/transactions | Retrieves a list of Transactions based on search parameters.
*TransactionsApi* | [**transactionsVoid**](docs/Api/TransactionsApi.md#transactionsvoid) | **POST** /api/v1/transactions/{id}/void | Processes a void of a transaction.

## Models

- [AttachmentModel](docs/Model/AttachmentModel.md)
- [AttributeMetadataModel](docs/Model/AttributeMetadataModel.md)
- [AttributeValueModel](docs/Model/AttributeValueModel.md)
- [BankAccountInformationModel](docs/Model/BankAccountInformationModel.md)
- [BatchListItemModel](docs/Model/BatchListItemModel.md)
- [CreditCardInformationModel](docs/Model/CreditCardInformationModel.md)
- [DivisionViewModel](docs/Model/DivisionViewModel.md)
- [GetAutoPayResponseModel](docs/Model/GetAutoPayResponseModel.md)
- [GetAutoPaysResponseModel](docs/Model/GetAutoPaysResponseModel.md)
- [GetBatchesResponseModel](docs/Model/GetBatchesResponseModel.md)
- [GetManagedInvoiceResponseModel](docs/Model/GetManagedInvoiceResponseModel.md)
- [GetManagedInvoicesResponseModel](docs/Model/GetManagedInvoicesResponseModel.md)
- [GetPaymentScheduleResponseModel](docs/Model/GetPaymentScheduleResponseModel.md)
- [GetTokenResponseModel](docs/Model/GetTokenResponseModel.md)
- [GetTransactionFeesResponseModel](docs/Model/GetTransactionFeesResponseModel.md)
- [GetTransactionResponseModel](docs/Model/GetTransactionResponseModel.md)
- [GetTransactionsResponseModel](docs/Model/GetTransactionsResponseModel.md)
- [InvoiceItemModel](docs/Model/InvoiceItemModel.md)
- [InvoiceModel](docs/Model/InvoiceModel.md)
- [InvoicesModel](docs/Model/InvoicesModel.md)
- [LookUpModelByte](docs/Model/LookUpModelByte.md)
- [PaidInvoiceModel](docs/Model/PaidInvoiceModel.md)
- [PostAuthorizeTransactionRequestModel](docs/Model/PostAuthorizeTransactionRequestModel.md)
- [PostAuthorizeTransactionResponseModel](docs/Model/PostAuthorizeTransactionResponseModel.md)
- [PostAutoPayRequestModel](docs/Model/PostAutoPayRequestModel.md)
- [PostConvertQuoteRequestModel](docs/Model/PostConvertQuoteRequestModel.md)
- [PostCreateManagedInvoicesContactModel](docs/Model/PostCreateManagedInvoicesContactModel.md)
- [PostCreateManagedInvoicesFinanceRequestModel](docs/Model/PostCreateManagedInvoicesFinanceRequestModel.md)
- [PostCreateManagedInvoicesRequestModel](docs/Model/PostCreateManagedInvoicesRequestModel.md)
- [PostIvrSessionRequestModel](docs/Model/PostIvrSessionRequestModel.md)
- [PostPaymentScheduleRequestModel](docs/Model/PostPaymentScheduleRequestModel.md)
- [PostRefundTransactionRequestModel](docs/Model/PostRefundTransactionRequestModel.md)
- [PostRefundTransactionResponseModel](docs/Model/PostRefundTransactionResponseModel.md)
- [PostSendInvoiceEmailRequestModel](docs/Model/PostSendInvoiceEmailRequestModel.md)
- [PostTokenPageSessionRequestModel](docs/Model/PostTokenPageSessionRequestModel.md)
- [PostTokenRequestModel](docs/Model/PostTokenRequestModel.md)
- [PostTransactionRequestModelV1](docs/Model/PostTransactionRequestModelV1.md)
- [PostTransactionResponseModel](docs/Model/PostTransactionResponseModel.md)
- [PostVoidManagedInvoiceResponseModel](docs/Model/PostVoidManagedInvoiceResponseModel.md)
- [PostVoidTransactionRequestModel](docs/Model/PostVoidTransactionRequestModel.md)
- [PostVoidTransactionResponseModel](docs/Model/PostVoidTransactionResponseModel.md)
- [QuickQuoteModel](docs/Model/QuickQuoteModel.md)
- [QuoteInvoiceFinancingInfoModel](docs/Model/QuoteInvoiceFinancingInfoModel.md)
- [QuoteInvoiceLineItem](docs/Model/QuoteInvoiceLineItem.md)
- [SerializableException](docs/Model/SerializableException.md)
- [TransactionEventModel](docs/Model/TransactionEventModel.md)
- [UnderwritingContactModel](docs/Model/UnderwritingContactModel.md)
- [UpdateInvoicesRequestModel](docs/Model/UpdateInvoicesRequestModel.md)

## Authorization

Authentication schemes defined for the API:
### basic

- **Type**: HTTP basic authentication

## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author

support@epay3.com

## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `v1`
    - Generator version: `7.6.0`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`
