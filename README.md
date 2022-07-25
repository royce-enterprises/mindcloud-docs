# MindCloud Channels Documentation

MindCloud Channels is an eCommerce platform to automate and synchronize the creation of orders, cancellation of orders, inventory and shipment tracking. While there is not yet a public API, this documents the main API jobs and the expected body for each. 
## Create Orders API
This retrieves orders from a destination retail site maps to our standard Order object and then is created in the source ERP, CRM or database. New orders from the vendor are queried for, received and mapped into a standard order object.

- [Order Object Documentation](/order-object.md)

This standard object is then sent to the internal database connector (such as Salesforce) and persisted. The third party vendor is then acknowleged.

## Cancel Order API
An order that is marked as cancelled in the source system is then updated in the destination site as cancelled. 

- [Cancel Object Documentation](/cancel-object.md)

## Credit Stock API

Inventory stock information from the source system is updated by SKU in all destination retail sites with matching SKUs.

- [Inventory Object Documentation](/inventory-object.md)

## Update Shipments API
When an order is fulfilled, the shipment tracking information, shipment date and method is updated in the destination retail site.

- [Shipment Object Documentation](/shipment-object.md)
