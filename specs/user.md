# User Service Specification

## Overview
Manages user accounts and authentication.

## API Endpoints
- `POST /register`
- `POST /login`
- `GET /profile`
- `PUT /profile`

## Data Model
- User: id, email, password, name, address, role

## Business Rules
- Email must be unique
- Passwords stored securely