# Shipment Object Doc

Shipment is marked in the source system and is then mapped to the standard shipment object and updated in the destination retail sites:

```
{
    "order" | {order-object},
    "orderShipment" | {
        "orderLines" | [{
            "orderLine" | {
                "lineNumber" | "string",
                "merchantLineNumber" | "string",
                "sku" | "string",
                "quantity" | "string",
                "sellerOrderId" | "string",
                "orderLineStatuses" | [{
                    "orderLineStatus" | {
                        "status" | "string",
                        "trackingInfo" | {
                            "shipDateTime" | "string",
                            "carrierName" | {
                                "carrier" | "string",
                            },
                            "methodCode" | "string",
                            "trackingNumber" | "string",
                            "trackingURL" | "string",
                        },
                    },
                }]
            }
        }]
    }
}
```  
### Field Definitions
| Field | Description |
| ----------- | ----------- |
| order | Order object |
| orderShipment | 
| orderLines | 
| orderLine | 
| lineNumber | Order line number |
| merchantLineNumber | Merchant order line number |
| sku | Order line SKU |
| quantity | Order line quantity |
| sellerOrderId | Seller's order id |
| orderLineStatuses | 
| orderLineStatus | 
| status | `Shipped` |
| trackingInfo | 
| shipDateTime | Datetime of when package shipped |
| carrierName | 
| carrier | Shipment carrier name |
| methodCode | Shipment method code |
| trackingNumber | Tracking number |
| trackingURL | Tracking URL |
