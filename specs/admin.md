# Admin Service Specification

## Overview
Admin operations for catalog and orders.

## API Endpoints
- `GET /admin/products`
- `POST /admin/products`
- `PUT /admin/products/:id`
- `DELETE /admin/products/:id`
- `GET /admin/orders`
- `PUT /admin/orders/:orderId/status`

## Business Rules
- Admin access only
- Audit actions for product/order changes