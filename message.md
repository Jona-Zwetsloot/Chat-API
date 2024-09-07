# 🟢 GET `/api/v1/message`
Fetch a single message by id.

#### Parameters
| Required | Name | Type | Value |
|----------|------|------|-------|
| ✅ | Authorization | Header | Bearer [access_token] |
| ✅ | id | Parameter | The ID of the message you want to fetch |

#### Returns
```json
{
  "id": 7,
  "user": "Jona Zwetsloot",
  "message": "Afbeeldingen van andere sites kunnen nu ook ingevoegd worden!",
  "time": "2023-08-30 10:48:01",
  "attachments": [
    "xUsPeJhDWnvIT8z11tjaNCklBabKnwKRy7PMQfyfsY4BVMs0sK.webp",
    "https://www.youtube.com/embed/2yJgwwDcgV8",
    "https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d1251832.192339737!2d3.9605096163551985!3d52.20732461079114!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x47c609c3db87e4bb%3A0xb3a175ceffbd0a9f!2sNederland!5e0!3m2!1snl!2snl!4v1725636130668!5m2!1snl!2snl"
  ],
  "likes": 4,
  "liked": false,
  "reactions": [
    {
      "id": 119,
      "user": "Jona Zwetsloot",
      "message": "De afbeeldingen gaan nu via een proxy, dus dat is nu wat privacyvriendelijker. ",
      "time": "2024-04-29 09:28:54",
      "likes": 1,
      "liked": false,
      "reactions": []
    },
    ...
  ]
}
```

<br>

# 🟡 POST `/api/v1/message`
Create a new message or reaction.

The attachments list can consist of Chat hosted images, Youtube video-URLs/embed-URLs, Google Maps URLs/embed-URLs.

#### Parameters
| Required | Name | Type | Value |
|----------|------|------|-------|
| ✅ | Authorization | Header | Bearer [access_token] |
| ✅ | message | Parameter | The message you want to send |
| ❌ | id | Parameter | Only if you want to send a reaction: the message/reaction ID you want to respond to |
| ❌ | attachments | Parameter | Only if you want to send a message: List of images/embeds you want to send, comma+space separated |

#### Returns
```json
{
    "id": 7
}
```

<br>

# 🔴 DELETE `/api/v1/message`
Delete a message. The message has to be sent by the profile associated with the access token.

#### Parameters
| Required | Name | Type | Value |
|----------|------|------|-------|
| ✅ | Authorization | Header | Bearer [access_token] |
| ✅ | id | Parameter | The ID of the message you want to delete |

#### Returns
```json
{
    "status": "success"
}
```