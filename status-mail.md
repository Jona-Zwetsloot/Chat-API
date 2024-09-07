# 🟢 GET `/api/v1/status-mail`
Check if an email address is available.

#### Parameters
| Required | Name | Type | Value |
|----------|------|------|-------|
| ✅ | Authorization | Header | Bearer [access_token] |
| ✅ | mail | Parameter | The email address you want to check. |

#### Returns
```json
{
    "available": true,
    "valid": true
}
```