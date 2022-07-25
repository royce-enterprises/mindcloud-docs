# Order Object Doc

```
{
    "id" | "string",
    "purchaseOrderId" | "string",
    "customerOrderId" | "string",
    "customerEmailId" | "string",
    "transactionId" | "string",
    "orderDate" | "string",
    "vendorReference" | "string",
    "lines" | [
        {
            "index" | "string",
            "merchantLineItemNo" | "string",
            "primaryKey" | "string",
            "item" | {
                "primaryKey" | "string",
                "productName" | "string",
                "sku" | "string",
                "retailSalesPrice" | "string",
                "retailCommissionValue" | 0,
                "retailCommissionRate" | "string",
                "netProceeds" | "string",
                "currency" | "string",
                "amount" | "string"
            },
            "charges" | [
                {
                    "type" | "string",
                    "name" | "string",
                    "currency" | "string",
                    "taxName" | "string",
                    "taxCurrency" | "string",
                    "taxAmount" | "string"
                }
            ],
            "quantity" | "string",
            "statusDate" | "string",
            "statuses" | {
                "status" | "string",
                "quantity" | "string",
                "amount" | "string",
                "cancellationReason" | "string"
            }
        }
    ],
    "shippingInfo" | {
        "phone" | "string",
        "email" | "string",
        "estimatedDeliveryDate" | "string",
        "estimatedShipDate" | "string",
        "methodCode" | "string",
        "postalAddress" | {
            "name" | "string",
            "address1" | "string",
            "address2" | "string",
            "city" | "string",
            "state" | "string",
            "stateName" | "string",
            "postalCode" | "string",
            "country" | "string",
            "addressType" | "string"
        }
    },
    "shipNode" | "string"
}
```  
### Field Definitions

| Field | Description |
| ----------- | ----------- |
| id | Unique Id of this order, prefixed by the third party name eg `walmart-1234567890`|
| purchaseOrderId | The Purchase Order Id of this order|
| customerOrderId | If the third party has a separate order number|
| customerEmailId | Customer's email address|
| transactionId | For any additional transaction Id that may be needed that is different than the PO or Order Id|
| orderDate | Date of the Order|
| vendorReference | Additional vendor identifier|
| lines | An array of order lines|
| index | The order line number sequence|
| merchantLineItemNo | Third parties line item number|
| item | Object containing the order line item details |
| primaryKey | Third party SKU of this order line item|
| productName | Name of the product|
| sku | Internal SKU of product|
| retailSalesPrice | Retail sales price of this item|
| retailCommissionValue | Commission value for this item|
| retailCommissionRate | Commission percentage rate for this item|
| currency | Currency for this item amount|
| amount | Total Amount for this item|
| charges | Object containing the additional charges on this item|
| type | Additional charge type|
| name | Additional change name|
| currency | Currency of additional charge|
| taxName | Name of tax|
| taxCurrency | Currency of tax|
| taxAmount | Amount of tax|
| quantity | parseInt(line.quantity_open || 0),|
| statusDate | new Date(n.updated_at),|
| statuses | |
| status | Status of the order line|
| quantity | Quantity of the order line |
| amount | Amount of the order line |
| cancellationReason | Reason, if order line was cancelled|
| shippingInfo | Object containing the shipping info|
| phone | Deliver phone number|
| email | Delivery email address|
| estimatedDeliveryDate | Estimated delivery date|
| estimatedShipDate | Estimated shipping date|
| methodCode | Shipping method|
| postalAddress | Object containing the shipping address|
| name | Customer name|
| address1 |
| address2|
| city |
| state |
| stateName:|
| postalCode:|
| country | |
| addressType:|
| shipNode | Additional shipping infromation|
| meta | Object containing any additional custom information |
