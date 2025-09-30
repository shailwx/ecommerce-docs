# Order Service Specification

## Overview
Tracks user orders and statuses.

## API Endpoints
- `GET /orders`
- `GET /orders/:orderId`
- `PUT /orders/:orderId/status` (admin)

## Data Model
- Order: id, userId, items, status, createdAt

## Business Rules
- Only users can view their own orders
- Only admins can update order status