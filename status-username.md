# 🟢 GET `/api/v1/status-username`
Check if a username is available.

#### Parameters
| Required | Name | Type | Value |
|----------|------|------|-------|
| ✅ | Authorization | Header | Bearer [access_token] |
| ✅ | user | Parameter | The username you want to check |

#### Returns
```json
{
    "available": true
}
```