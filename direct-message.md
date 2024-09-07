# 🟢 GET `/api/v1/direct-message`
Get a list of all direct messages the profile associated with the access token has sent to a contact.

#### Parameters
| Required | Name | Type | Value |
|----------|------|------|-------|
| ✅ | Authorization | Header | Bearer [access_token] |
| ✅ | user | Parameter | The contact you want the conversation from |

#### Returns
```json
[
    {
        "id": 24,
        "user": "Jona Zwetsloot",
        "seen": true,
        "message": "Hello. This is a DM!",
        "time": "2024-07-23 19:35:53",
        "attachments": [
            "xUsPeJhDWnvIT8z11tjaNCklBabKnwKRy7PMQfyfsY4BVMs0sK.webp"
        ]
    },
    ...
]
```

<br>

# 🟡 POST `/api/v1/direct-message`
Send a direct message to a contact.

#### Parameters
| Required | Name | Type | Value |
|----------|------|------|-------|
| ✅ | Authorization | Header | Bearer [access_token] |
| ✅ | user | Parameter | The user you want to send a DM to |
| ✅ | message | Parameter | The message you want to send |
| ✅ | attachments | Parameter | List of images you want to send, comma+space separated |

#### Returns
```json
{
    "status": "success"
}
```

<br>

# 🔴 DELETE `/api/v1/direct-message`
Delete a direct message.

#### Parameters
| Required | Name | Type | Value |
|----------|------|------|-------|
| ✅ | Authorization | Header | Bearer [access_token] |
| ✅ | id | Parameter | The id of the DM you want to delete |

#### Returns
```json
{
    "status": "success"
}
```