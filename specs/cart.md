# Cart Service Specification

## Overview
Manages user shopping carts.

## API Endpoints
- `GET /cart`
- `POST /cart/add`
- `PUT /cart/update`
- `DELETE /cart/remove`

## Data Model
- Cart: userId, items [productId, quantity]

## Business Rules
- Only in-stock items can be added
- Cart persists for logged-in users