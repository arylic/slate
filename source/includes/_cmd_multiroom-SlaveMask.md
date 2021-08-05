## Hide a Player from Network

Mask one slave, If slave is masked, it will act as a standalone device.

Sub-Command: `SlaveMask`

> Request format:

```html
GET /httpapi.asp?command=multiroom:SlaveMask:<ip_address>
```

> Example Response:

```plaintext
OK
```

### Parameter Description

Parameter | Description
---|---
`ip_address` | The IP address of the child player that has to be masked


<aside class="notice">
The response isn't in JSON format. It is just plaintext.
</aside>
