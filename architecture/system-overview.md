# System Architecture Overview

## Microservices

- **Catalog Service:** Product and category management
- **Cart Service:** Shopping cart management
- **Checkout Service:** Payment, order placement
- **User Service:** Authentication and profile
- **Order Service:** Order tracking and history
- **Admin Service:** Admin dashboard and controls
- **Gateway (optional):** API gateway/proxy

## Diagram

```mermaid
graph LR
  Catalog -->|Product Info| Gateway
  Cart -->|Cart Data| Gateway
  Checkout -->|Order/Payment| Gateway
  User -->|Auth/Profile| Gateway
  Order -->|Order Status| Gateway
  Admin -->|Manage| Gateway
  Gateway -->|Unified API| Frontend
```

## Communication

- REST APIs between services
- Auth via JWT or similar