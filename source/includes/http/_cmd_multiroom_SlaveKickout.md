## Remove Player from Group

Sub-Command: `SlaveKickout`

> Request format:

```html
GET /httpapi.asp?command=multiroom:SlaveKickout:<ip_address>
```

> Example Response:

```plaintext
OK
```

### Parameter Description

Parameter | Description
---|---
`ip_address` | The IP address of the child player to be removed from the group


<aside class="notice">
The response isn't in JSON format. It is just plaintext.
</aside>
