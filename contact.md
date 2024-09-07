# 🟢 GET `/api/v1/contact`
Get a list of all contacts from the profile associated with the access token.

#### Parameters
| Required | Name | Type | Value |
|----------|------|------|-------|
| ✅ | Authorization | Header | Bearer [access_token] |

#### Returns
```json
[
    {
        "user": "Jona Zwetsloot",
        "url": "Jona-Zwetsloot",
        "description": "Hallo! Ik ben Jona, en ik heb dit chat-platform gemaakt.",
        "picture": "ev9ZIhODo37iKgagn3ZmxEugeWo3VgYOqKSIDsxVTXk7gojV6h.webp",
        "banner": "HI6K4MmciUOiNvTm93Lz4ueA4uLPMO4Pq0t13ciSS4CSIFOG37.webp",
        "score": 30343,
        "made": "2023-01-27 00:00:00",
        "online": "2024-07-23 19:35:53",
        "status": "justoffline",
        "unseen": 14
    },
    ...
]
```

<br>

# 🟡 POST `/api/v1/contact`
Follow a contact and add them to the contact list.

#### Parameters
| Required | Name | Type | Value |
|----------|------|------|-------|
| ✅ | Authorization | Header | Bearer [access_token] |
| ✅ | user | Parameter | The user you want to follow |

#### Returns
```json
{
    "status": "success"
}
```

<br>

# 🔴 DELETE `/api/v1/contact`
Unfollow a contact and delete them from the contact list.

#### Parameters
| Required | Name | Type | Value |
|----------|------|------|-------|
| ✅ | Authorization | Header | Bearer [access_token] |
| ✅ | user | Parameter | The user you want to unfollow |

#### Returns
```json
{
    "status": "success"
}
```