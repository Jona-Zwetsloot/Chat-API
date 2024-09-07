# 🟢 GET `/api/v1/profile`
Fetch the profile information of a user. If no user is specified, the profile associated with the access token is retrieved.

#### Parameters
| Required | Name | Type | Value |
|----------|------|------|-------|
| ❌ | user | Parameter | The username of the requested profile |

#### Returns
```json
{
    "user": "Jona Zwetsloot",
    "url": "Jona-Zwetsloot",
    "description": "Hallo! Ik ben Jona, en ik heb dit chat-platform gemaakt.",
    "picture": "ev9ZIhODo37iKgagn3ZmxEugeWo3VgYOqKSIDsxVTXk7gojV6h.webp",
    "banner": "HI6K4MmciUOiNvTm93Lz4ueA4uLPMO4Pq0t13ciSS4CSIFOG37.webp",
    "score": 30343,
    "made": "2023-01-27 00:00:00",
    "online": "2024-07-23 19:35:53",
    "status": "justoffline"
}
```

<br>

# 🟡 POST `/api/v1/profile`
Create a new profile. When you create an account using the API, there will be no permission dialog displayed because the user consciously decided to create an account in a third-party application. Note that the user must still verify their email address before you can use their access key to perform actions.

#### Parameters
| Required | Name | Type | Value |
|----------|------|------|-------|
| ✅ | client_id | Parameter | Your client ID |
| ✅ | client_secret | Parameter | Your client secret |
| ✅ | user | Parameter | The username of the new account |
| ✅ | mail | Parameter | The email adress of the new account |
| ✅ | pass | Parameter | The password of the new account |

#### Returns
```json
{
    "user": "Just @n Example U$ername",
    "url": "Just-n-Example-Uername",
    "access_token": "VKBKpaPnuyXH0t25xcNqMbFTu69pFN",
    "token_type": "Bearer",
    "expires_in": "3600",
    "refresh_token": "J1SQFTRpPA9hcAibhEtQwwTqGPqGCS",
    "scope": "accounts+messages+contacts+profile+delete",
    "status": "r7fknmbjze"
}
```

<br>

# 🔵 PUT `/api/v1/profile`
Change the description, profile image and banner of a profile. In some cases, sending images to this endpoint will not work. If this is the case, you can make a POST request to `/api/v1/profile-save` instead.

#### Parameters
| Required | Name | Type | Value |
|----------|------|------|-------|
| ✅ | Authorization | Header | Bearer [access_token] |
| ❌ | description | Parameter | The new description |
| ❌ | picture | File | The new profile picture |
| ❌ | banner | File | The new banner |

#### Returns
```json
{
    "status": "success"
}
```

<br>

# 🔴 DELETE `/api/v1/profile`
Delete the profile associated with the access token. This will sends a verification email which asks the user to confirm their account deletion

#### Parameters
| Required | Name | Type | Value |
|----------|------|------|-------|
| ✅ | Authorization | Header | Bearer [access_token] |


#### Returns
```json
{
    "status": "success"
}
```