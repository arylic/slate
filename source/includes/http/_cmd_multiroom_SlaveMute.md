## Mute a Guest Device 
> Request format:

```html
GET /httpapi.asp?command=multiroom:SlaveMute:<ip_address>:<flag_mute>
```

> Example Response:

```plaintext
OK
```

Mute a specific Guest Device of a Multiroom group.

Sub-Command: `SlaveMute`


### Parameter Description

Parameter | Description
---|---
`ip_address` | The IP address of the Guest Device to control with this command
`flag_mute` | The desired mute status<br>`0`: Unmuted<br>`1`: Muted


<aside class="notice">
The response isn't in JSON format. It is just plaintext.
</aside>

