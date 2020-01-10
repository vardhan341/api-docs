{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/coworkerinvoices" %}
{% api-method-summary %}
Find
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of coworkerinvoices based on one or more filter querystring parameters.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Basic Authentication token. Base64 encoding of 'username:password'.
{% endapi-method-parameter %}
{% api-method-parameter name="Content" type="string" required=true %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}

{% api-method-parameter name="Id" type="int" %}
?Id=...
{% endapi-method-parameter %}

{% api-method-parameter name="UniqueId" type="Guid" %}
?UniqueId=...
{% endapi-method-parameter %}

{% api-method-parameter name="SystemId" type="string" %}
?CoworkerInvoice\_SystemId=...
{% endapi-method-parameter %}


{% api-method-parameter name="Coworker" type="Coworker" %}
?CoworkerInvoice\_Coworker=...
{% endapi-method-parameter %}


{% api-method-parameter name="Business" type="Business" %}
?CoworkerInvoice\_Business=...
{% endapi-method-parameter %}


{% api-method-parameter name="InvoiceNumber" type="string" %}
?CoworkerInvoice\_InvoiceNumber=...
{% endapi-method-parameter %}


{% api-method-parameter name="PaymentReference" type="string" %}
?CoworkerInvoice\_PaymentReference=...
{% endapi-method-parameter %}


{% api-method-parameter name="BillToName" type="string" %}
?CoworkerInvoice\_BillToName=...
{% endapi-method-parameter %}


{% api-method-parameter name="BillToAddress" type="string" %}
?CoworkerInvoice\_BillToAddress=...
{% endapi-method-parameter %}


{% api-method-parameter name="BillToCity" type="string" %}
?CoworkerInvoice\_BillToCity=...
{% endapi-method-parameter %}


{% api-method-parameter name="BillToPostCode" type="string" %}
?CoworkerInvoice\_BillToPostCode=...
{% endapi-method-parameter %}


{% api-method-parameter name="BillToPhone" type="string" %}
?CoworkerInvoice\_BillToPhone=...
{% endapi-method-parameter %}


{% api-method-parameter name="BillToFax" type="string" %}
?CoworkerInvoice\_BillToFax=...
{% endapi-method-parameter %}


{% api-method-parameter name="BillToCountry" type="Country" %}
?CoworkerInvoice\_BillToCountry=...
{% endapi-method-parameter %}


{% api-method-parameter name="BillToBankAccount" type="string" %}
?CoworkerInvoice\_BillToBankAccount=...
{% endapi-method-parameter %}


{% api-method-parameter name="BillToTaxIDNumber" type="string" %}
?CoworkerInvoice\_BillToTaxIDNumber=...
{% endapi-method-parameter %}


{% api-method-parameter name="PurchaseOrder" type="string" %}
?CoworkerInvoice\_PurchaseOrder=...
{% endapi-method-parameter %}


{% api-method-parameter name="Description" type="string" %}
?CoworkerInvoice\_Description=...
{% endapi-method-parameter %}


{% api-method-parameter name="DiscountAmount" type="decimal" %}
?CoworkerInvoice\_DiscountAmount=...
{% endapi-method-parameter %}


{% api-method-parameter name="DueDate" type="DateTime?" %}
?CoworkerInvoice\_DueDate=...
{% endapi-method-parameter %}


{% api-method-parameter name="InvoiceFromDate" type="DateTime?" %}
?CoworkerInvoice\_InvoiceFromDate=...
{% endapi-method-parameter %}


{% api-method-parameter name="InvoiceToDate" type="DateTime?" %}
?CoworkerInvoice\_InvoiceToDate=...
{% endapi-method-parameter %}


{% api-method-parameter name="TotalAmount" type="decimal" %}
?CoworkerInvoice\_TotalAmount=...
{% endapi-method-parameter %}


{% api-method-parameter name="PaidAmount" type="decimal?" %}
?CoworkerInvoice\_PaidAmount=...
{% endapi-method-parameter %}


{% api-method-parameter name="Currency" type="Currency" %}
?CoworkerInvoice\_Currency=...
{% endapi-method-parameter %}


{% api-method-parameter name="TaxAmount" type="decimal" %}
?CoworkerInvoice\_TaxAmount=...
{% endapi-method-parameter %}


{% api-method-parameter name="Draft" type="bool" %}
?CoworkerInvoice\_Draft=...
{% endapi-method-parameter %}


{% api-method-parameter name="Paid" type="bool" %}
?CoworkerInvoice\_Paid=...
{% endapi-method-parameter %}


{% api-method-parameter name="Sent" type="bool" %}
?CoworkerInvoice\_Sent=...
{% endapi-method-parameter %}


{% api-method-parameter name="SentOn" type="DateTime?" %}
?CoworkerInvoice\_SentOn=...
{% endapi-method-parameter %}


{% api-method-parameter name="PaidOn" type="DateTime?" %}
?CoworkerInvoice\_PaidOn=...
{% endapi-method-parameter %}


{% api-method-parameter name="Refunded" type="bool" %}
?CoworkerInvoice\_Refunded=...
{% endapi-method-parameter %}


{% api-method-parameter name="XeroInvoiceTransfered" type="bool" %}
?CoworkerInvoice\_XeroInvoiceTransfered=...
{% endapi-method-parameter %}


{% api-method-parameter name="XeroPaymentTransfered" type="bool" %}
?CoworkerInvoice\_XeroPaymentTransfered=...
{% endapi-method-parameter %}


{% api-method-parameter name="RefundedOn" type="DateTime?" %}
?CoworkerInvoice\_RefundedOn=...
{% endapi-method-parameter %}


{% api-method-parameter name="CreditNote" type="bool" %}
?CoworkerInvoice\_CreditNote=...
{% endapi-method-parameter %}


{% api-method-parameter name="OriginalInvoiceGuid" type="Guid?" %}
?CoworkerInvoice\_OriginalInvoiceGuid=...
{% endapi-method-parameter %}


{% api-method-parameter name="ContractGuid" type="Guid?" %}
?CoworkerInvoice\_ContractGuid=...
{% endapi-method-parameter %}


{% api-method-parameter name="CustomData" type="string" %}
?CoworkerInvoice\_CustomData=...
{% endapi-method-parameter %}


{% api-method-parameter name="ReceivedAmount" type="decimal?" %}
?CoworkerInvoice\_ReceivedAmount=...
{% endapi-method-parameter %}


{% api-method-parameter name="CreditedAmount" type="decimal?" %}
?CoworkerInvoice\_CreditedAmount=...
{% endapi-method-parameter %}


{% api-method-parameter name="RefundedAmount" type="decimal?" %}
?CoworkerInvoice\_RefundedAmount=...
{% endapi-method-parameter %}


{% api-method-parameter name="Coworker\_FullName" type="string" %}
?CoworkerInvoice\_Coworker\_FullName=...
{% endapi-method-parameter %}


{% api-method-parameter name="Coworker\_RegularPaymentContractNumber" type="string" %}
?CoworkerInvoice\_Coworker\_RegularPaymentContractNumber=...
{% endapi-method-parameter %}


{% api-method-parameter name="Coworker\_RegularPaymentProvider" type="string" %}
?CoworkerInvoice\_Coworker\_RegularPaymentProvider=...
{% endapi-method-parameter %}


{% api-method-parameter name="Coworker\_CardNumber" type="string" %}
?CoworkerInvoice\_Coworker\_CardNumber=...
{% endapi-method-parameter %}


{% api-method-parameter name="Coworker\_GoCardlessContractNumber" type="string" %}
?CoworkerInvoice\_Coworker\_GoCardlessContractNumber=...
{% endapi-method-parameter %}


{% api-method-parameter name="Coworker\_EnableGoCardlessPayments" type="string" %}
?CoworkerInvoice\_Coworker\_EnableGoCardlessPayments=...
{% endapi-method-parameter %}


{% api-method-parameter name="Coworker\_BillingEmail" type="string" %}
?CoworkerInvoice\_Coworker\_BillingEmail=...
{% endapi-method-parameter %}


{% api-method-parameter name="Coworker\_NotifyOnNewInvoice" type="string" %}
?CoworkerInvoice\_Coworker\_NotifyOnNewInvoice=...
{% endapi-method-parameter %}


{% api-method-parameter name="Coworker\_NotifyOnNewPayment" type="string" %}
?CoworkerInvoice\_Coworker\_NotifyOnNewPayment=...
{% endapi-method-parameter %}


{% api-method-parameter name="Coworker\_NotifyOnFailedPayment" type="string" %}
?CoworkerInvoice\_Coworker\_NotifyOnFailedPayment=...
{% endapi-method-parameter %}


{% api-method-parameter name="Coworker\_DoNotProcessInvoicesAutomatically" type="string" %}
?CoworkerInvoice\_Coworker\_DoNotProcessInvoicesAutomatically=...
{% endapi-method-parameter %}


{% api-method-parameter name="Business\_Name" type="string" %}
?CoworkerInvoice\_Business\_Name=...
{% endapi-method-parameter %}


{% api-method-parameter name="BillToCountry\_Name" type="string" %}
?CoworkerInvoice\_BillToCountry\_Name=...
{% endapi-method-parameter %}


{% api-method-parameter name="BillToCountry\_TwoDigitsCode" type="string" %}
?CoworkerInvoice\_BillToCountry\_TwoDigitsCode=...
{% endapi-method-parameter %}


{% api-method-parameter name="TransactionCurrency\_Code" type="string" %}
?CoworkerInvoice\_TransactionCurrency\_Code=...
{% endapi-method-parameter %}


{% api-method-parameter name="Currency\_Code" type="string" %}
?CoworkerInvoice\_Currency\_Code=...
{% endapi-method-parameter %}


{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}


```javascript
{
    "Records": [{
        "Coworker": null,
        "Business": null,
        "InvoiceNumber": "00001",
        "PaymentReference": "00001",
        "BillToName": "BillToName",
        "BillToAddress": "BillToAddress",
        "BillToCity": "BillToCity",
        "BillToPostCode": "BillToPostCode",
        "BillToPhone": "BillToPhone",
        "BillToFax": "BillToFax",
        "BillToCountry": null,
        "BillToBankAccount": "123456",
        "BillToTaxIDNumber": "123456",
        "PurchaseOrder": "PurchaseOrder",
        "Description": "[DataType(DataType.MultilineText)]",
        "DiscountAmount": 0,
        "DueDate": null,
        "InvoiceFromDate": null,
        "InvoiceToDate": null,
        "TotalAmount": 0,
        "PaidAmount": null,
        "Currency": null,
        "TaxAmount": 0,
        "Draft": false,
        "Paid": false,
        "Sent": false,
        "SentOn": false,
        "PaidOn": null,
        "Refunded": false,
        "XeroInvoiceTransfered": false,
        "XeroPaymentTransfered": false,
        "RefundedOn": null,
        "CreditNote": false,
        "OriginalInvoiceGuid": false,
        "ContractGuid": false,
        "CustomData": "null",
        "ReceivedAmount": ,
        "CreditedAmount": ,
        "RefundedAmount": ,
		"CoworkerInvoiceCoworkerFullName": "...",
		"CoworkerInvoiceCoworkerRegularPaymentContractNumber": "...",
		"CoworkerInvoiceCoworkerRegularPaymentProvider": "...",
		"CoworkerInvoiceCoworkerCardNumber": "...",
		"CoworkerInvoiceCoworkerGoCardlessContractNumber": "...",
		"CoworkerInvoiceCoworkerEnableGoCardlessPayments": "...",
		"CoworkerInvoiceCoworkerBillingEmail": "...",
		"CoworkerInvoiceCoworkerNotifyOnNewInvoice": "...",
		"CoworkerInvoiceCoworkerNotifyOnNewPayment": "...",
		"CoworkerInvoiceCoworkerNotifyOnFailedPayment": "...",
		"CoworkerInvoiceCoworkerDoNotProcessInvoicesAutomatically": "...",
		"CoworkerInvoiceBusinessName": "...",
		"CoworkerInvoiceBillToCountryName": "...",
		"CoworkerInvoiceBillToCountryTwoDigitsCode": "...",
		"CoworkerInvoiceTransactionCurrencyCode": "...",
		"CoworkerInvoiceCurrencyCode": "...",

    }],
    "CurrentPageSize": 25,
    "CurrentPage": 1,
    "CurrentOrderField": "Id",
    "CurrentSortDirection": 1,
    "FirstItem": 1,
    "HasNextPage": true,
    "HasPreviousPage": false,
    "LastItem": 25,
    "PageNumber": 1,
    "PageSize": 25,
    "TotalItems": 60,
    "TotalPages": 3
}

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

> 🔒 Requires user role `coworkerinvoice-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/coworkerinvoices" %}
{% api-method-summary %}
List
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of coworkerinvoices.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Basic Authentication token. Base64 encoding of 'username:password'.
{% endapi-method-parameter %}
{% api-method-parameter name="Content" type="string" required=true %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="dir" type="string" required=false %}
one of 'Ascending' or 'Ascending'
{% endapi-method-parameter %}

{% api-method-parameter name="orderby" type="string" required=false %}
?orderby=Id
{% endapi-method-parameter %}

{% api-method-parameter name="page" type="integer" required=false %}
?page=1
{% endapi-method-parameter %}

{% api-method-parameter name="size" type="integer" required=false %}
size=25 \(maximum=1000\)
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "Records": [{
        "Coworker": null,
        "Business": null,
        "InvoiceNumber": "00001",
        "PaymentReference": "00001",
        "BillToName": "BillToName",
        "BillToAddress": "BillToAddress",
        "BillToCity": "BillToCity",
        "BillToPostCode": "BillToPostCode",
        "BillToPhone": "BillToPhone",
        "BillToFax": "BillToFax",
        "BillToCountry": null,
        "BillToBankAccount": "123456",
        "BillToTaxIDNumber": "123456",
        "PurchaseOrder": "PurchaseOrder",
        "Description": "[DataType(DataType.MultilineText)]",
        "DiscountAmount": 0,
        "DueDate": null,
        "InvoiceFromDate": null,
        "InvoiceToDate": null,
        "TotalAmount": 0,
        "PaidAmount": null,
        "Currency": null,
        "TaxAmount": 0,
        "Draft": false,
        "Paid": false,
        "Sent": false,
        "SentOn": false,
        "PaidOn": null,
        "Refunded": false,
        "XeroInvoiceTransfered": false,
        "XeroPaymentTransfered": false,
        "RefundedOn": null,
        "CreditNote": false,
        "OriginalInvoiceGuid": false,
        "ContractGuid": false,
        "CustomData": "null",
        "ReceivedAmount": ,
        "CreditedAmount": ,
        "RefundedAmount": ,
    }],
    }],
    "CurrentPageSize": 25,
    "CurrentPage": 1,
    "CurrentOrderField": "Id",
    "CurrentSortDirection": 1,
    "FirstItem": 1,
    "HasNextPage": true,
    "HasPreviousPage": false,
    "LastItem": 25,
    "PageNumber": 1,
    "PageSize": 25,
    "TotalItems": 60,
    "TotalPages": 3
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

> 🔒 Requires user role `coworkerinvoice-list`

{% hint style="info" %}
You can also get a list of records based when they were created or updated. This is useful if you want to get a list of records created after or before a particular point in time. 
You can also use range query parameters for all date, integer and decimal properties.
{% endhint %}

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/coworkerinvoices" %}
{% api-method-summary %}
By date or number range
{% endapi-method-summary %}

{% api-method-description %}
Gets a list of coworkerinvoices based on a range of dates, integer or decimal properties.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Basic Authentication token. Base64 encoding of 'username:password'.
{% endapi-method-parameter %}
{% api-method-parameter name="Content" type="string" required=true %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="CreatedOn" type="object" required=false %}
?to\_CoworkerInvoice\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="CreatedOn" type="object" required=false %}
?from\_CoworkerInvoice\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?to\_CoworkerInvoice\_UpdatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?from\_CoworkerInvoice\_UpdatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="DiscountAmount" type="decimal" required=false %}
?from\_CoworkerInvoice\_DiscountAmount=...
{% endapi-method-parameter %}
{% api-method-parameter name="DiscountAmount" type="decimal" required=false %}
?to\_CoworkerInvoice\_DiscountAmount=...
{% endapi-method-parameter %}
{% api-method-parameter name="DueDate" type="datetime" required=false %}
?from\_CoworkerInvoice\_DueDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="DueDate" type="datetime" required=false %}
?to\_CoworkerInvoice\_DueDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="InvoiceFromDate" type="datetime" required=false %}
?from\_CoworkerInvoice\_InvoiceFromDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="InvoiceFromDate" type="datetime" required=false %}
?to\_CoworkerInvoice\_InvoiceFromDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="InvoiceToDate" type="datetime" required=false %}
?from\_CoworkerInvoice\_InvoiceToDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="InvoiceToDate" type="datetime" required=false %}
?to\_CoworkerInvoice\_InvoiceToDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="TotalAmount" type="decimal" required=false %}
?from\_CoworkerInvoice\_TotalAmount=...
{% endapi-method-parameter %}
{% api-method-parameter name="TotalAmount" type="decimal" required=false %}
?to\_CoworkerInvoice\_TotalAmount=...
{% endapi-method-parameter %}
{% api-method-parameter name="PaidAmount" type="decimal" required=false %}
?from\_CoworkerInvoice\_PaidAmount=...
{% endapi-method-parameter %}
{% api-method-parameter name="PaidAmount" type="decimal" required=false %}
?to\_CoworkerInvoice\_PaidAmount=...
{% endapi-method-parameter %}
{% api-method-parameter name="TaxAmount" type="decimal" required=false %}
?from\_CoworkerInvoice\_TaxAmount=...
{% endapi-method-parameter %}
{% api-method-parameter name="TaxAmount" type="decimal" required=false %}
?to\_CoworkerInvoice\_TaxAmount=...
{% endapi-method-parameter %}
{% api-method-parameter name="SentOn" type="datetime" required=false %}
?from\_CoworkerInvoice\_SentOn=...
{% endapi-method-parameter %}
{% api-method-parameter name="SentOn" type="datetime" required=false %}
?to\_CoworkerInvoice\_SentOn=...
{% endapi-method-parameter %}
{% api-method-parameter name="PaidOn" type="datetime" required=false %}
?from\_CoworkerInvoice\_PaidOn=...
{% endapi-method-parameter %}
{% api-method-parameter name="PaidOn" type="datetime" required=false %}
?to\_CoworkerInvoice\_PaidOn=...
{% endapi-method-parameter %}
{% api-method-parameter name="RefundedOn" type="datetime" required=false %}
?from\_CoworkerInvoice\_RefundedOn=...
{% endapi-method-parameter %}
{% api-method-parameter name="RefundedOn" type="datetime" required=false %}
?to\_CoworkerInvoice\_RefundedOn=...
{% endapi-method-parameter %}
{% api-method-parameter name="ReceivedAmount" type="decimal" required=false %}
?from\_CoworkerInvoice\_ReceivedAmount=...
{% endapi-method-parameter %}
{% api-method-parameter name="ReceivedAmount" type="decimal" required=false %}
?to\_CoworkerInvoice\_ReceivedAmount=...
{% endapi-method-parameter %}
{% api-method-parameter name="CreditedAmount" type="decimal" required=false %}
?from\_CoworkerInvoice\_CreditedAmount=...
{% endapi-method-parameter %}
{% api-method-parameter name="CreditedAmount" type="decimal" required=false %}
?to\_CoworkerInvoice\_CreditedAmount=...
{% endapi-method-parameter %}
{% api-method-parameter name="RefundedAmount" type="decimal" required=false %}
?from\_CoworkerInvoice\_RefundedAmount=...
{% endapi-method-parameter %}
{% api-method-parameter name="RefundedAmount" type="decimal" required=false %}
?to\_CoworkerInvoice\_RefundedAmount=...
{% endapi-method-parameter %}

{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "Records": [{
        "Coworker": null,
        "Business": null,
        "InvoiceNumber": "00001",
        "PaymentReference": "00001",
        "BillToName": "BillToName",
        "BillToAddress": "BillToAddress",
        "BillToCity": "BillToCity",
        "BillToPostCode": "BillToPostCode",
        "BillToPhone": "BillToPhone",
        "BillToFax": "BillToFax",
        "BillToCountry": null,
        "BillToBankAccount": "123456",
        "BillToTaxIDNumber": "123456",
        "PurchaseOrder": "PurchaseOrder",
        "Description": "[DataType(DataType.MultilineText)]",
        "DiscountAmount": 0,
        "DueDate": null,
        "InvoiceFromDate": null,
        "InvoiceToDate": null,
        "TotalAmount": 0,
        "PaidAmount": null,
        "Currency": null,
        "TaxAmount": 0,
        "Draft": false,
        "Paid": false,
        "Sent": false,
        "SentOn": false,
        "PaidOn": null,
        "Refunded": false,
        "XeroInvoiceTransfered": false,
        "XeroPaymentTransfered": false,
        "RefundedOn": null,
        "CreditNote": false,
        "OriginalInvoiceGuid": false,
        "ContractGuid": false,
        "CustomData": "null",
        "ReceivedAmount": ,
        "CreditedAmount": ,
        "RefundedAmount": ,
    }],
    }],
    "CurrentPageSize": 25,
    "CurrentPage": 1,
    "CurrentOrderField": "Id",
    "CurrentSortDirection": 1,
    "FirstItem": 1,
    "HasNextPage": true,
    "HasPreviousPage": false,
    "LastItem": 25,
    "PageNumber": 1,
    "PageSize": 25,
    "TotalItems": 60,
    "TotalPages": 3
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

> 🔒 Requires user role `coworkerinvoice-list`


{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/coworkerinvoices?CoworkerInvoice_Id=[:id1,:id2,...]" %}
{% api-method-summary %}
List by Ids
{% endapi-method-summary %}

{% api-method-description %}
Gets one or more coworkerinvoice records based on their Id.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Basic Authentication token. Base64 encoding of 'username:password'.
{% endapi-method-parameter %}
{% api-method-parameter name="Content" type="string" required=true %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
Comma-separated list of IDs of every coworkerinvoice to fetch. I.e. [123456,789102,...] 
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "Records": [{
        "Coworker": null,
        "Business": null,
        "InvoiceNumber": "00001",
        "PaymentReference": "00001",
        "BillToName": "BillToName",
        "BillToAddress": "BillToAddress",
        "BillToCity": "BillToCity",
        "BillToPostCode": "BillToPostCode",
        "BillToPhone": "BillToPhone",
        "BillToFax": "BillToFax",
        "BillToCountry": null,
        "BillToBankAccount": "123456",
        "BillToTaxIDNumber": "123456",
        "PurchaseOrder": "PurchaseOrder",
        "Description": "[DataType(DataType.MultilineText)]",
        "DiscountAmount": 0,
        "DueDate": null,
        "InvoiceFromDate": null,
        "InvoiceToDate": null,
        "TotalAmount": 0,
        "PaidAmount": null,
        "Currency": null,
        "TaxAmount": 0,
        "Draft": false,
        "Paid": false,
        "Sent": false,
        "SentOn": false,
        "PaidOn": null,
        "Refunded": false,
        "XeroInvoiceTransfered": false,
        "XeroPaymentTransfered": false,
        "RefundedOn": null,
        "CreditNote": false,
        "OriginalInvoiceGuid": false,
        "ContractGuid": false,
        "CustomData": "null",
        "ReceivedAmount": ,
        "CreditedAmount": ,
        "RefundedAmount": ,
    }],
    }],
    "CurrentPageSize": 25,
    "CurrentPage": 1,
    "CurrentOrderField": "Id",
    "CurrentSortDirection": 1,
    "FirstItem": 1,
    "HasNextPage": true,
    "HasPreviousPage": false,
    "LastItem": 25,
    "PageNumber": 1,
    "PageSize": 25,
    "TotalItems": 60,
    "TotalPages": 3
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
"Not found"
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

> 🔒 Requires user role `coworkerinvoice-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/coworkerinvoices/:id" %}
{% api-method-summary %}
One by Id
{% endapi-method-summary %}

{% api-method-description %}
Gets one coworkerinvoice record.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Basic Authentication token. Base64 encoding of 'username:password'.
{% endapi-method-parameter %}
{% api-method-parameter name="Content" type="string" required=true %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The ID of the coworkerinvoice to fetch.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
        "Coworker": null,
        "Business": null,
        "InvoiceNumber": "00001",
        "PaymentReference": "00001",
        "BillToName": "BillToName",
        "BillToAddress": "BillToAddress",
        "BillToCity": "BillToCity",
        "BillToPostCode": "BillToPostCode",
        "BillToPhone": "BillToPhone",
        "BillToFax": "BillToFax",
        "BillToCountry": null,
        "BillToBankAccount": "123456",
        "BillToTaxIDNumber": "123456",
        "PurchaseOrder": "PurchaseOrder",
        "Description": "[DataType(DataType.MultilineText)]",
        "DiscountAmount": 0,
        "DueDate": null,
        "InvoiceFromDate": null,
        "InvoiceToDate": null,
        "TotalAmount": 0,
        "PaidAmount": null,
        "Currency": null,
        "TaxAmount": 0,
        "Draft": false,
        "Paid": false,
        "Sent": false,
        "SentOn": false,
        "PaidOn": null,
        "Refunded": false,
        "XeroInvoiceTransfered": false,
        "XeroPaymentTransfered": false,
        "RefundedOn": null,
        "CreditNote": false,
        "OriginalInvoiceGuid": false,
        "ContractGuid": false,
        "CustomData": "null",
        "ReceivedAmount": ,
        "CreditedAmount": ,
        "RefundedAmount": ,
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
"Not found"
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

> 🔒 Requires user role `coworkerinvoice-read`


{% api-method method="post" host="https://spaces.nexudus.com/api" path="/billing/coworkerinvoices" %}
{% api-method-summary %}
Create
{% endapi-method-summary %}

{% api-method-description %}
Creates a new coworkerinvoice.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Basic Authentication token. Base64 encoding of 'username:password'.
{% endapi-method-parameter %}
{% api-method-parameter name="Content" type="string" required=true %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="CoworkerId" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="BusinessId" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="InvoiceNumber" type="string" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="PaymentReference" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="BillToName" type="string" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="BillToAddress" type="string" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="BillToCity" type="string" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="BillToPostCode" type="string" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="BillToPhone" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="BillToFax" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="BillToCountryId" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="BillToBankAccount" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="BillToTaxIDNumber" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="PurchaseOrder" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="DueDate" type="DateTime?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="InvoiceFromDate" type="DateTime?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="InvoiceToDate" type="DateTime?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CurrencyId" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="Draft" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="PaidOn" type="DateTime?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CustomData" type="string" required=false %}
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}

{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "Status": 200,
    "WasSuccessful": true,
    "Message": "Record 'Name of the record' has been succesfully created.",
    "Value": {
        "Id": 12354678,
    }
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
_This response is an example, errors and messages will follow this structure but keys and descriptions may be different for each record._  
{% endapi-method-response-example-description %}

```javascript
{
    "Status": 500,
    "Message": "Email: may not be null or empty",
    "Value": null,
    "WasSuccessful": false,
    "Errors": [
        {
            "AttemptedValue": null,
            "Message": "may not be null or empty",
            "PropertyName": "FullName"
        },
        {
            "AttemptedValue": null,
            "Message": "may not be null or empty",
            "PropertyName": "Email"
        },
        {
            "AttemptedValue": null,
            "Message": "may not be null",
            "PropertyName": "Country"
        },
        {
            "AttemptedValue": null,
            "Message": "may not be null",
            "PropertyName": "SimpleTimeZone"
        }
    ]
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=500 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "Message": "An error has occurred."
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

> 🔒 Requires user role `coworkerinvoice-create`

```javascript
{
	"Coworker": 12345678,
	"Business": 12345678,
	"InvoiceNumber": "00001",
	"PaymentReference": "00001",
	"BillToName": "BillToName",
	"BillToAddress": "BillToAddress",
	"BillToCity": "BillToCity",
	"BillToPostCode": "BillToPostCode",
	"BillToPhone": "BillToPhone",
	"BillToFax": "BillToFax",
	"BillToCountry": 12345678,
	"BillToBankAccount": "123456",
	"BillToTaxIDNumber": "123456",
	"PurchaseOrder": "PurchaseOrder",
	"DueDate": null,
	"InvoiceFromDate": null,
	"InvoiceToDate": null,
	"Currency": 12345678,
	"Draft": false,
	"PaidOn": null,
	"CustomData": "null",
}

```

{% api-method method="put" host="https://spaces.nexudus.com/api" path="/billing/coworkerinvoices" %}
{% api-method-summary %}
Update
{% endapi-method-summary %}

{% api-method-description %}
Updates and existing coworkerinvoice. PUT requests require ALL record properties to be submitted with every request. Any missing properties will be cleared or set to false.
  
Required User Role: `coworkerinvoice-edit`
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Basic Authentication token. Base64 encoding of 'username:password'.
{% endapi-method-parameter %}
{% api-method-parameter name="Content" type="string" required=true %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}

{% api-method-parameter name="Id" type="int" required="true" %}
{% api-method-parameter name="CoworkerId" type="int" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="BusinessId" type="int" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="InvoiceNumber" type="string" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="PaymentReference" type="string" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="BillToName" type="string" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="BillToAddress" type="string" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="BillToCity" type="string" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="BillToPostCode" type="string" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="BillToPhone" type="string" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="BillToFax" type="string" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="BillToCountryId" type="int" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="BillToBankAccount" type="string" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="BillToTaxIDNumber" type="string" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="PurchaseOrder" type="string" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="DueDate" type="DateTime?" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="InvoiceFromDate" type="DateTime?" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="InvoiceToDate" type="DateTime?" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="CurrencyId" type="int" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Draft" type="bool" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="PaidOn" type="DateTime?" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="CustomData" type="string" required="true" %}
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "Status": 200,
    "WasSuccessful": true,
    "Message": "The record 'name of the record' was updated successfully,
    "Value": {
        "Id": 123456
    },
    "OpenInDialog": false,
    "Errors": null
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
_This response is an example, errors and messages will follow this structure but keys and descriptions may be different for each record._  
{% endapi-method-response-example-description %}

```javascript
{
    "Status": 500,
    "Message": "Email: may not be null or empty",
    "Value": null,
    "WasSuccessful": false,
    "Errors": [
        {
            "AttemptedValue": null,
            "Message": "may not be null or empty",
            "PropertyName": "FullName"
        },
        {
            "AttemptedValue": null,
            "Message": "may not be null or empty",
            "PropertyName": "Email"
        },
        {
            "AttemptedValue": null,
            "Message": "may not be null",
            "PropertyName": "Country"
        },
        {
            "AttemptedValue": null,
            "Message": "may not be null",
            "PropertyName": "SimpleTimeZone"
        }
    ]
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=500 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "Message": "An error has occurred."
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

> 🔒 Requires user role `coworkerinvoice-edit`

```javascript
{
	"Coworker": 12345678,
	"Business": 12345678,
	"InvoiceNumber": "00001",
	"PaymentReference": "00001",
	"BillToName": "BillToName",
	"BillToAddress": "BillToAddress",
	"BillToCity": "BillToCity",
	"BillToPostCode": "BillToPostCode",
	"BillToPhone": "BillToPhone",
	"BillToFax": "BillToFax",
	"BillToCountry": 12345678,
	"BillToBankAccount": "123456",
	"BillToTaxIDNumber": "123456",
	"PurchaseOrder": "PurchaseOrder",
	"DueDate": null,
	"InvoiceFromDate": null,
	"InvoiceToDate": null,
	"Currency": 12345678,
	"Draft": false,
	"PaidOn": null,
	"CustomData": "null",
}

```




## Commands

Commands allow to perform actions against one or more coworkerinvoice records. Some commands accept only one record while others can run an action for a number of records at the same time.  Each command has metadata with information about how it can be used and the amount of records, if any, it needs to run.

> ```javascript
> {
>     "AppliesOnlyToMultipleEntities": false|true,
>     "AppliesOnlyToOneEntity": false|true,
>     "AppliesOnlyToTwoEntities": false|true,
>     ...
> }
> ```

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/coworkerinvoices/commands" %}
{% api-method-summary %}
Commands
{% endapi-method-summary %}

{% api-method-description %}
Get all commands available to run for coworkerinvoice records.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Basic Authentication token. Base64 encoding of 'username:password'.
{% endapi-method-parameter %}
{% api-method-parameter name="Content" type="string" required=true %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
_This response is an example._  
{% endapi-method-response-example-description %}

```javascript
[
    {
        "Key": "COMMAND_KEY_1",
        "Name": "Command English Description",
        "AppliesOnlyToMultipleEntities": false,
        "AppliesOnlyToOneEntity": false,
        "AppliesOnlyToTwoEntities": false,
        "NeedsEntitiesToRun": true,
        "Order": 1,
        "RequiresParameters": []
    },
    {
        "Key": "COMMAND_KEY_2",
        "Name": "Command 2 English Description",
        "AppliesOnlyToMultipleEntities": true
        "AppliesOnlyToOneEntity": false,
        "AppliesOnlyToTwoEntities": false,
        "NeedsEntitiesToRun": true,
        "Order": 2,
        "RequiresParameters": []
    },
    ...
]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/coworkerinvoices/runcommand" %}
{% api-method-summary %}
Run Command
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Basic Authentication token. Base64 encoding of 'username:password'.
{% endapi-method-parameter %}
{% api-method-parameter name="Content" type="string" required=true %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="Key" type="string" required=true %}
The command Key defining the command to run. `"COMMAND_KEY_1"`
{% endapi-method-parameter %}

{% api-method-parameter name="Parameters" type="array" required=false %}
A list of object with the structure below. The parameters required for each command are returned in the "RequiresParameters" array return by the "commands" endpoint.  
  
`[  
   {  
      "Name": "Name",   
      "Type":"Type",   
      "Value":recordId  
    }  
]`
{% endapi-method-parameter %}

{% api-method-parameter name="Ids" type="array" required=true %}
A list of integer IDs for each of the records to run this command for.  
  
`[987654321, 123565978]`
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
_Commands also return a status 200 when they fail to process one or more of the records. Use the 'WasSuccessful'  property to know if the command run succeeded._  
{% endapi-method-response-example-description %}

```javascript
{  
   "Status":500 or 200,
   "Message":"Command error description",
   "Value":null,
   "Errors":null,
   "WasSuccessful":false
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

> 🔒 Requires user role `coworkerinvoice-edit`

## Enumerated values

## Binary files

The following endpoints return binary data. Check the `ContentType` header to understand the type of file being returned in the response stream.


## Related Entities
* [Coworker](../spaces/coworker.md)
* [Business](../sys/business.md)
* [Country](../sys/country.md)
* [Currency](../sys/currency.md)
* [Currency](../sys/currency.md)
