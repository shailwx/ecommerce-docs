# API Cookbook & Reference

## Common Operations

### List Products
**Request:**
```http
GET /products
```
**Response:**
```json
[
  { "id": "123", "name": "Sample Product", "price": 99.99 }
]
```

### Add Item to Cart
**Request:**
```http
POST /cart/add
Content-Type: application/json

{
  "productId": "123",
  "quantity": 2
}
```
**Response:**
```json
{
  "cartId": "abc123",
  "items": [ { "productId": "123", "quantity": 2 } ]
}
```

### Place Order
**Request:**
```http
POST /checkout
Content-Type: application/json

{
  "cartId": "abc123",
  "address": "123 Main St"
}
```
**Response:**
```json
{
  "orderId": "order789",
  "status": "pending"
}
```

### Error Example
**Response:**
```json
{
  "error": "Product not found",
  "code": 404
}
```