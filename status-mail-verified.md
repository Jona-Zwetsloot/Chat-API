# 🟢 GET `/api/v1/status-mail-verified`
Check if a user has verified their email address.

#### Parameters
| Required | Name | Type | Value |
|----------|------|------|-------|
| ✅ | Authorization | Header | Bearer [access_token] |
| ✅ | user | Parameter | The user whose e-mail verification status you want to check. |

#### Returns
```json
{
    "verified": true
}
```