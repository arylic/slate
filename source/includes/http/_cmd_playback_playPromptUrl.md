## Play Notification Sound

When this API is used, the device will lower current volume of playback (NETWORK or USB mode only), and play the url for notification sound. Normally used in condition for a door bell in home automation system.

Command: `playPromptUrl:<url>`

> Request format:

```html
GET /httpapi.asp?command=playPromptUrl:<url>
```

Parameter | Description
---|---
`url` | A complete `URL` for an notification audio on the internet or addressable local device

> Example response:

```text
OK
```
<aside class="notice">
Only works in NETWORK or USB playback mode<br>
Introduced in version 4.6.415145
</aside>
