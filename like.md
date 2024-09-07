# 🟢 GET `/api/v1/like`
Get the amount of likes of a message/reaction. Also returns a boolean which indicates if the message is liked.

#### Parameters
| Required | Name | Type | Value |
|----------|------|------|-------|
| ✅ | Authorization | Header | Bearer [access_token] |
| ✅ | id | Parameter | The ID of the message/reaction you want to get the amount of likes from |

#### Returns
```json
{
  "likes": 4,
  "liked": true
}
```

<br>

# 🟡 POST `/api/v1/like`
Like or unlike a message or reaction.

#### Parameters
| Required | Name | Type | Value |
|----------|------|------|-------|
| ✅ | Authorization | Header | Bearer [access_token] |
| ✅ | id | Parameter | The ID of the message/reaction you want to like/unlike |
| ✅ | like | Parameter | Boolean: whether you want to like ('true') or unlike ('false') |

#### Returns
```json
{
    "status": "success"
}
```