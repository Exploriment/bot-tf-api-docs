# Resource: /offers

## Retrieve a single offer
```http
GET /offers/:offerid
```

#### Parameters
None.

#### Response
```json
{
  "offer": {
    "id": 9537560,
    "botid": 35,
    "steamid": "76561198325843174",
    "steamofferid": 3204296803,
    "sentbyme": false,
    "message": "",
    "isdonation": false,
    "escrow": false,
    "state": {
      "code": 3,
      "description": "Accepted",
      "date": 1527365387
    },
    "creation": 1527365381,
    "action": {
      "code": "ACCEPT",
      "reason": "VALID"
    },
    "itemsme": [
      {
        "id": 104790064,
        "appid": 440,
        "amount": 1,
        "assetid": "6860315496",
        "classid": "815886",
        "instanceid": "653344249",
        "defindex": 389,
        "icon": "https://steamcommunity-a.akamaihd.net/economy/image/fWFc82js0fmoRAP-qOIPu5THSWqfSmTELLqcUywGkijVjZULUrsm1j-9xgEGbQMuWALnhzRCms_jQ_PaWeMCzYNi55NUiWA6k1MrMeW2MTM0JFaTVqQMBaBupwq1WSRkv5MtRNmxScdZFWA",
        "name": "Googly Gazer",
        "marketname": "Googly Gazer",
        "description": "<span style=\"color:#756b5e\">Style: Mad Science</span><br />Keep one eye on your enemy and\nthe other one on everything else.<br /><span style=\"color:#7ea9d1\">\nGift from: ★][BLVCK&#039;][&#039;VLON][★</span><br />Date Received: Friday, November 28, 2014 (13:32:54) GMT<br />",
        "type": "Level 36 Cosmetic Augmentation",
        "specks": "",
        "proks": "",
        "effect": null,
        "quality": 6,
        "craftable": true,
        "marketable": false,
        "australium": false,
        "attributes": {}
      }
    ],
    "itemsthem": [
      {
        "id": 104790065,
        "appid": 440,
        "amount": 1,
        "assetid": "6876096089",
        "classid": "2674",
        "instanceid": "11040547",
        "defindex": 5002,
        "icon": "https://steamcommunity-a.akamaihd.net/economy/image/fWFc82js0fmoRAP-qOIPu5THSWqfSmTELLqcUywGkijVjZULUrsm1j-9xgEbZQsUYhTkhzJWhsO1Mv6NGucF1Ygzt8ZQijJukFMiMrbhYDEwI1yRVKNfD6xorQ3qW3Jr6546DNPuou9IOVK4p4kWJaA",
        "name": "Refined Metal",
        "marketname": "Refined Metal",
        "description": "",
        "type": "Level 3 Craft Item",
        "specks": "",
        "proks": "",
        "effect": null,
        "quality": 6,
        "craftable": true,
        "marketable": false,
        "australium": false,
        "attributes": {}
      },
      {
        "id": 104790066,
        "appid": 440,
        "amount": 1,
        "assetid": "6876117508",
        "classid": "5564",
        "instanceid": "11040547",
        "defindex": 5001,
        "icon": "https://steamcommunity-a.akamaihd.net/economy/image/fWFc82js0fmoRAP-qOIPu5THSWqfSmTELLqcUywGkijVjZULUrsm1j-9xgEbZQsUYhTkhzJWhsO0Mv6NGucF1YJlscMEgDdvxVYsMLPkMmFjI1OSUvMHDPBp9lu0CnVluZQxA9Gwp-hIOVK4sMMNWF4",
        "name": "Reclaimed Metal",
        "marketname": "Reclaimed Metal",
        "description": "",
        "type": "Level 2 Craft Item",
        "specks": "",
        "proks": "",
        "effect": null,
        "quality": 6,
        "craftable": true,
        "marketable": false,
        "australium": false,
        "attributes": {}
      }
    ]
  }
}
```

Most parameters are self-explanatory, those are not documented below.

| Parameter | Type | Description |
|:-----------|:---------|:---------|
| `id` | integer | Offer ID used by Bot.tf. |
| `steamofferid` | integer | Offer ID used by Steam. |
| `itemsme` | array | All the items on the bot's side. |
| `itemsthem` | array | All the items on the user's side. |
| `itemsme[n].id` | integer | ID item used by Bot.tf. |
| `itemsme[n].appid` | integer | ID of the app (440 = TF2). |
| `itemsme[n].defindex` | integer/null | Def index of the item (TF2 only). `null` if other game. |
| `itemsme[n].specks` | string | Specialized Killstreak sheen name (TF2). |
| `itemsme[n].proks` | string | Professional Killstreak effect name (TF2). |
| `itemsme[n].effect`| integer/null | ID of the unusual effect (TF2). `null` if none. |
| `itemsme[n].quality` | integer | Quality ID of the item (TF2). `0` if other game. |
| `itemsme[n].craftable` | boolean | Craftability of the item (TF2). Always `true` if other game. |
| `itemsme[n].australium` | boolean | Is this item australium? (TF2). Always `false` if other game. |
| `itemsme[n].attributes` | object | Object with attributes of the item (Steam tags). Always empty if TF2. |
