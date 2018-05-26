# Bot.tf API documentation

## Introduction
The Bot.tf API is encrypted and restricted by rate limits. Authentication is required. In order to get access to this API, please access the <a href="https://panel.bot.tf/api" target="_blank">Control panel</a> and create your API key.

## Endpoint
```
https://api.bot.tf/v1/
```

## Authentication
The Bot.tf API uses API keys to allow access to the API, it expects the API key to be included in every request in the `Authorization` HTTP header, like this:

```http
Authorization: Token YOUR_API_KEY
```

## Rate limits
By default you have a rate limit of 500 requests per hour, this is reset every hour. The API will return a `429 Too Many Requests` error when this rate limit has been exceeded, continuing making requests during this time may result in a suspension.

You may request higher limits by raising a support ticket and stating your usage of the API.

## Response template
```json
{
  "data": { },
  "errors": [
    {
      "code": "api_error",
      "message": "Something went wrong"
    }
  ],
  "rate": {
    "limit": 500,
    "current": 0,
    "resetin": 0,
    "resetdate": 1527364800
  },
  "status": false
}
```
| Parameter | Type | Description |
|:-----------|:---------|:---------|
| `data` | object | Contains any data returned by the resource. |
| `errors` | array | An array of errors that occurred while processing your API request. This array is empty if `status` is `true`. |
| `rate` | object | Object containing information about your current rate limits. |
| `rate.limit` | integer | Your requests per hour limit. |
| `rate.current` | integer | Your current usage this hour. |
| `rate.resetin` | integer | The number of seconds until the next rate limit reset. |
| `rate.resetdate` | integer | UNIX timestamp of the date when the rate limit is reset. |
| `status` | boolean | `true` if the request was successful, `false` if there are errors (see `errors`) |