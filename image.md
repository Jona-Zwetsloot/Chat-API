# 🟢 GET `/api/v1/image`
Retrieve an image from the Chat server. This is the only way to get secret images (which are sent in DMs).

Tip: if you want to fetch public images, you can also fetch the source webp files from the https://jonazwetsloot.nl/chat/uploads/ directory (this allows you to just put the URL in an image element if you are using HTML). This will not work with private images because those are protected.

#### Parameters
| Required | Name | Type | Value |
|----------|------|------|-------|
| ✅ | Authorization | Header | Bearer [access_token] |
| ✅ | file | Parameter | The name of the file |
| ❌ | type | Parameter | The desired filetype (has to be 'png', 'jpeg', 'gif', 'webp', 'avif' or 'bmp'), defaults to 'png' |
| ❌ | secret | Parameter | Boolean: Whether the image is secret, defaults to 'false' |
| ❌ | quality | Parameter | Image quality in 0-100 range (only for jpeg, webp and avif) |

#### Returns
The request returns an image file.

<br>

# 🟡 POST `/api/v1/image`
Upload an image to the Chat server.

#### Parameters
| Required | Name | Type | Value |
|----------|------|------|-------|
| ✅ | Authorization | Header | Bearer [access_token] |
| ✅ | name | Parameter | New name of image file |
| ✅ | width | Parameter | Image width in pixels |
| ✅ | height | Parameter | Image height in pixels |
| ✅ | size | Parameter | Image filesize in KB |

#### Returns
```json
{
    "name": "841qwaIeyvytS0mIQjq4fktFziKKlcSvbBSfmv8mFK4dY5RKZ1li1wD2npaHWrFzprJ5LZRXy2S.webp",
    "width": 1200,
    "height": 572,
    "size": 27
}
```

<br>

# 🔴 DELETE `/api/v1/image`
Delete an image on the Chat server. The image has to be uploaded by the profile associated with the access token.

#### Parameters
| Required | Name | Type | Value |
|----------|------|------|-------|
| ✅ | Authorization | Header | Bearer [access_token] |
| ✅ | file | Parameter | The name of the file |
| ❌ | secret | Parameter | Boolean: Whether the image is secret, defaults to 'false' |

#### Returns
```json
{
    "status": "success"
}
```