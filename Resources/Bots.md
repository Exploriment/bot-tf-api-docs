# Resource: /bots

## Retrieve all your bots
```http
GET /bots
```

#### Parameters
None.

#### Response
```json
{
  "bots": [
    {
      "id": 36,
      "steamid": "76561198296137471",
      "name": "Alerts & Payments | bot.tf",
      "avatar": "https://i.imgur.com/9Ta5l83.jpg",
      "bgasset": "7925219710",
      "gamename": "Bot.tf: No bots available 😞",
      "offerurl": "https://steamcommunity.com/tradeoffer/new/?partner=335871743&token=rUHP_4eI",
      "autorenew": true,
      "allowescrow": false,
      "allowoverpay": true,
      "allowprivate": true,
      "manualitemoffers": false,
      "description": "[i]Add me if you would like to receive a notification whenever Bot.tf has bots available![/i]\r\n\r\nThis bot [b][u]NEVER[/u][/b] sends you a trade offer taking items from you! :2016snocone:",
      "hideinfeed": true,
      "invitegroupid": "103582791452307934",
      "tf2": {
        "maxslots": 1000,
        "autocraft": false,
        "autocraftweapons": true,
        "autosorttype": 3,
        "riskytradethreshold": 15,
        "backpacktf": {
          "enabled": false,
          "buynotes": "[⇄] 24/7 TRADING BOT! // Send me a trade offer!",
          "sellnotes": "[⇄] 24/7 TRADING BOT! // Send me a trade offer!",
          "premium": false
        },
        "autoprice": {
          "enabled": false,
          "interval": 2,
          "last": null
        }
      }
    }
  ]
}
```

Most parameters are self-explanatory, those are not documented below.

| Parameter | Type | Description |
|:-----------|:---------|:---------|
| `bgasset` | string/null | Asset ID of the profile background. `null` if no background. |
| `gamename` | string | Custom game name of the bot. |
| `invitegroupid` | string | Steam ID of the Steam group that the bot automatically invites users to. |
| `tf2.autosorttype` | integer | Type ID of how the backpack is sorted. |
| `tf2.autoprice.last` | integer/null | UNIX timestamp of the last autoprice, `null` if never. |

## Retrieve a single bot
```http
GET /bots/:botid
```

#### Parameters
None.

#### Response
See `GET /bots`

## Restart a bot
```http
POST /bots/:botid/restart
```

#### Parameters
None.

#### Response
Empty response on success.

## Use a Team Fortress 2 item
```http
POST /bots/:botid/item/:assetid
```
Primarily used to use Backpack Expanders.

#### Parameters
None.

#### Response
Empty response on success.
