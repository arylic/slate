## Remove Guest Device from Multi-Room Group
> Request format:

```html
GET /httpapi.asp?command=multiroom:SlaveKickout:<ip_address>
```

> Example Response:

```plaintext
OK
```

Sub-Command: `SlaveKickout`

This command will remove the required Guest Device from the Multi-Room Group

### Parameter Description

Parameter | Description
---|---
`ip_address` | The IP address of the Guest Device to control with this command


<aside class="notice">
The response isn't in JSON format. It is just plaintext.
</aside>
