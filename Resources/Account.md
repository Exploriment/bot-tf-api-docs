# Resource: /account

## Retrieve account credit
```http
GET /account/credit
```

#### Parameters
None.

#### Response
```json
{
  "credit": {
    "amount": 1000,
    "currency": "USD",
    "symbol": "$"
  }
}
```
| Parameter | Type | Description |
|:-----------|:---------|:---------|
| `credit` | object | Contains data about your account credit. |
| `credit.amount` | integer | Your account credit in __cents__. |
| `credit.currency` | string | Currency code in ISO 4217 format. |
| `credit.symbol` | string | Currency symbol. |