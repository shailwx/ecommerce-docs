# Catalog Service Specification

## Overview
Handles product listings, categories, and product details.

## API Endpoints
- `GET /products`
- `GET /products/:id`
- `POST /products` (admin)
- `PUT /products/:id` (admin)
- `DELETE /products/:id` (admin)

## Data Model
- Product: id, name, description, price, image, category, stock

## Business Rules
- Only show products in stock
- Admins can manage products