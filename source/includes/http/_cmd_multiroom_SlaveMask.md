## Hide a Guest Device from Network
> Request format:

```html
GET /httpapi.asp?command=multiroom:SlaveMask:<ip_address>
```

> Example Response:

```plaintext
OK
```

This sub-command will Mask one of the Guest Devices, If the Guest Device is masked, it will act as a standalone device.

Sub-Command: `SlaveMask`


### Parameter Description

Parameter | Description
---|---
`ip_address` | The IP address of the Guest Device to control with this command

<aside class="notice">
The response isn't in JSON format. It is just plaintext.
</aside>
