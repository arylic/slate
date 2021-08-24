## Mute a Player

Enables to mute a specific player of a Multiroom group.

Sub-Command: `SlaveMute`

> Request format:

```html
GET /httpapi.asp?command=multiroom:SlaveMute:<ip_address>:<mute>
```

> Example Response:

```plaintext
OK
```

### Parameter Description

Parameter | Description
---|---
`ip_address` | The IP address of the child player which should be muted
`mute` | The desired mute status<br>`0` - Unmuted<br>`1` - Muted


<aside class="notice">
The response isn't in JSON format. It is just plaintext.
</aside>
