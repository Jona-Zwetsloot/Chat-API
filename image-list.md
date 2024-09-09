# 🟢 GET `/api/v1/image-list`
Get a list of images used by a user. Also returns private images if your scope includes `contacts`.

#### Parameters
| Required | Name | Type | Value |
|----------|------|------|-------|
| ✅ | Authorization | Header | Bearer [access_token] |

#### Returns
```json
[
    {
        "name": "55FX19HszBUvsZvp3HlMqAxBOP19aEwXpHomaJ7FRyVtYJFqITbvbTEkJWc3GzPbfxQzgjog1Uw.webp",
        "secret": false
    },
    ...
]
```