## Device connection status
> Request format:

```html
GET /httpapi.asp?command=wlanGetConnectState
```

> Example response:

```plaintext
OK
```

Command: `wlanGetConnectState`  

This command will return the status of the WiFi connection. The possible return values are as follows.

Value | Value Description
---|---
`PROCESS` | Connection still in progress.
`PAIRFAIL` | WiFi connection attempt failed. Wrong password given.
`FAIL` | WiFi connection attempt failed. Also this will be the reply for a device that is connected by LAN Ethernet port.
`OK` | Device is connected.

<aside class="notice">
The response value is NOT in JSON format! It is just a plaintext string.
</aside>
