# 🟢 GET `/api/v1/token`
Get an access token, or refresh one.

<br>

<details><summary>Get user access token</summary>
  
  Exchange an authorization code for an user access token.
  
  #### Parameters
  
  | Required | Name | Type | Value |
  |----------|------|------|-------|
  | ✅ | grant_type | Parameter | 'authorization_code' |
  | ✅ | code | Parameter | Your authorization code |
  | ✅ | redirect_uri | Parameter | Same URI as at authorization step |
  | ✅ | client_id | Parameter | Your client ID |
  | ✅ | client_secret | Parameter | Your client secret |
  | ❌ | code_verifier | Parameter | This parameter is only required if you set code_challenge in the authorization step. If code_challenge_method was set to 'S256', this value must be the SHA256-hashed and base64-url-encoded value of code_challenge. If code_challenge_method was set to 'plain' this value must be same as code_challenge. |
  
  #### Returns
  ```json
{
    "access_token": "VKBKpaPnuyXH0t25xcNqMbFTu69pFN",
    "token_type": "Bearer",
    "expires_in": "3600",
    "refresh_token": "J1SQFTRpPA9hcAibhEtQwwTqGPqGCS",
    "scope": "accounts+messages+contacts+profile+delete",
    "state": "r7fknmbjze"
}
  ```
  
</details>

<br>

<details><summary>Get client access token</summary>

  Exchange client credentials for a client access token. A client access token can perform significantly less actions compared to a user access token, because it is not associated with an account and thus cannot perform actions such as liking a post.
  
  #### Parameters
  
  | Required | Name | Type | Value |
  |----------|------|------|-------|
  | ✅ | grant_type | Parameter | 'refresh_token' |
  | ✅ | refresh_token | Parameter | Your refresh token |
  | ✅ | client_id | Parameter | Your client ID |
  | ✅ | client_secret | Parameter | Your client secret |
  
  #### Returns
  ```json
{
    "access_token": "VKBKpaPnuyXH0t25xcNqMbFTu69pFN",
    "token_type": "Bearer",
    "expires_in": "3600",
    "refresh_token": "J1SQFTRpPA9hcAibhEtQwwTqGPqGCS",
    "scope": "accounts+messages+contacts+profile+delete"
}
  ```
  
</details>

<br>

<details><summary>Refresh access token</summary>
  
  Exchange a refresh token for a new access token.
  
  #### Parameters
  
  | Required | Name | Type | Value |
  |----------|------|------|-------|
  | ✅ | grant_type | Parameter | 'client_credentials' |
  | ✅ | client_id | Parameter | Your client ID |
  | ✅ | client_secret | Parameter | Your client secret |
  
  #### Returns
  ```json
{
    "access_token": "VKBKpaPnuyXH0t25xcNqMbFTu69pFN",
    "token_type": "Bearer",
    "expires_in": "3600",
    "refresh_token": "J1SQFTRpPA9hcAibhEtQwwTqGPqGCS"
}
  ```
  
</details>