# DumbBudget API Documentation

This document describes the API endpoints available for DumbCal integration with DumbBudget.

## Authentication

All API requests must include the `DUMB_SECRET` in the request headers:

```
Authorization: Bearer YOUR_DUMB_SECRET
```

If the secret is invalid or missing, the API will return a 401 Unauthorized response.

## Endpoints

### GET /api/calendar/transactions

Returns all transactions within a specified date range.

**Query Parameters:**
- `start_date`: (Required) Start date in ISO format (YYYY-MM-DD)
- `end_date`: (Required) End date in ISO format (YYYY-MM-DD)

**Example Request:**
```
GET /api/calendar/transactions?start_date=2024-03-01&end_date=2024-03-31
Authorization: Bearer YOUR_DUMB_SECRET
```

**Response Format:**
```json
{
  "transactions": [
    {
      "type": "income"|"expense",
      "amount": number,
      "description": string,
      "date": string (ISO date),
      "category": string
    }
  ]
}
```

**Example Response:**
```json
{
  "transactions": [
    {
      "type": "expense",
      "amount": 50.00,
      "description": "Grocery shopping",
      "date": "2024-03-15",
      "category": "Food"
    },
    {
      "type": "income",
      "amount": 2000.00,
      "description": "Salary",
      "date": "2024-03-01",
      "category": "Salary"
    }
  ]
}
```

**Error Responses:**
- 400 Bad Request: Invalid date format or missing parameters
- 401 Unauthorized: Invalid or missing DUMB_SECRET
- 500 Internal Server Error: Server-side error

## Rate Limiting
To prevent abuse, the API is rate-limited to 100 requests per hour per API key. 