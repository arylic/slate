## Disable Multiroom Mode
> Request format:

```html
GET /httpapi.asp?command=multiroom:Ungroup
```

> Example Response:

```plaintext
OK
```

This sub-command disables Multiroom mode on the Host Device, and will split up the entire group.  All devices are returned to stand alone mode.

Sub-Command: `Ungroup`



<aside class="notice">
The response isn't in JSON format. It is just plaintext.
</aside>
