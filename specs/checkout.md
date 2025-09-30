# Checkout Service Specification

## Overview
Handles checkout and payment processes.

## API Endpoints
- `POST /checkout`
- `POST /payment`
- `GET /order-confirmation/:orderId`

## Data Model
- Order: id, userId, cart, address, status, paymentInfo

## Business Rules
- Validate cart and address before checkout
- Simulated payment for MVP