## Redirect OTA Server

> Request format:

```html
GET /httpapi.asp?command=SetUpdateServer:<url>
```

> Example response:

```plaintext
OK
```

It is used to redirect the OTA server, so user can select different OTA server manually, normally for alpha testing or pre-release purpose. Afer redirected, the web page will response with OK, and user need to check the APP for the device and see if there's a new version. And click to update when found new version. After next boot, the OTA server will resume to default one. And another point, the MCU firmware will be detected as new version when found different, even it's larger.

Command: `SetUpdateServer:<url>`

### Parameter Description
Parameter | Description
---|---
`url` | URL of OTA server, and for Arylic device, you can set it to `http://ota.rakoit.com/alpha`
