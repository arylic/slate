## Device connection state

Command: `wlanGetConnectState`  

> Request format:

```html
GET /httpapi.asp?command=wlanGetConnectState
```

> Example response:

```plaintext
OK
```

Possible return values:

Value | Value Description
-+-
`PROCESS` | Connection still in progress.
`PAIRFAIL` | WiFi connection attempt failed. Wrong password given.
`FAIL` | WiFi connection attempt failed.
`OK` | Device is connected.

<aside class="notice">
The response value is NOT in JSON format! It is just a plaintext string.
</aside>
