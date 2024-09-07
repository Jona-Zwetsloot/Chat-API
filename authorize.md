# 🟢 GET `/api/v1/authorize`
Send the user to this endpoint to get an authorization code.

The scope can consist out of multiple values separated by a '+'. The scope cannot surpass the scope of the application. Available scopes are 'accounts', 'messages', 'contacts', 'profile' and 'delete'.

#### Parameters
| Required | Name | Type | Value |
|----------|------|------|-------|
| ✅ | response_type | Parameter | 'code' |
| ✅ | client_id | Parameter | Your client ID |
| ✅ | redirect_uri | Parameter | URI to redirect to once done |
| ❌ | scope | Parameter | The scope you want access to |
| ❌ | state | Parameter | A random state code you can use for verification |
| ❌ | code_challenge | Parameter | Random string used to check client validity |
| ❌ | code_challenge_method | Parameter | 'S256' - or - 'plain' |

#### Returns
If the user approves your authorization request, you will get the authorization code at your specified `redirect_uri` with a hash like this: `#code=Uy6BZu72N1XzmRUpfgmfEPvRZmDqWF&state=r7fknmbjze`.