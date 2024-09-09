# 🟢 GET `/api/v1/storage`
Returns the amount of storage used by a user in KB.

Normal storage is the amount of storage used by public images. Secret storage is the amount of storage used by private images.

#### Parameters
| Required | Name | Type | Value |
|----------|------|------|-------|
| ✅ | Authorization | Header | Bearer [access_token] |

#### Returns
```json
{
    "normal": 2751111,
    "secret": 1163561,
    "limit": 50000000
}
```