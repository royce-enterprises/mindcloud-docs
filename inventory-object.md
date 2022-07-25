# Inventory Object Doc

Inventory is retrieved from the source system and mapped to the following standard inventory object:

```
{
    "id": "string",
    "sku": "string",
    "description": "string",
    "availableQuantity": "integer",
    "name": "string",
    "lastModified": "datetime"
}
```  
### Field Definitions

- id: Primary key of the source inventory record
- sku: SKU of this product
- description: Product description
- availableQuantity: Available quantity of this SKU
- name: Name of product
- lastModified: Date this inventory was last updated
