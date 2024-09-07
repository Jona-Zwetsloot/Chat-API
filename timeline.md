# 🟢 GET `/api/v1/timeline`
Fetch public messages from the timeline.

#### Parameters
| Required | Name | Type | Value | Default value |
|----------|------|------|-------|---------------|
| ✅ | Authorization | Header | Bearer [access_token] | - |
| ❌ | sort | Parameter | The sorting. Can be 'time', 'random' and 'likes' | 'time' |
| ❌ | limit | Parameter | The limit of messages (not including reactions) | 50 |
| ❌ | layers | Parameter | How many layers deep the reactions can go. 0 = no reactions, 1 = one layer of reactions, etc | Infinity |
| ❌ | reaction_limit | Parameter | The limit of reactions in any reaction layer | 10 |
| ❌ | offset | Parameter | The offset can be used to skip the first n messages | 0 |
| ❌ | offset_id | Parameter | Only fetches messages with an ID lower than offset_id | Infinity |

#### Returns
```json
[
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
    },
    ...
]
```