## Connect to hidden WiFi
> Request format with password:

```html
GET /httpapi.asp?command=wlanConnectHideApEx:ssid=<hex_ssid>:pwd=<hex_pwd>
```

> Request format without password:

```html
GET /httpapi.asp?command=wlanConnectHideApEx:ssid=<hex_ssid>
```

Connect the device to a hidden WiFi network. When connecting, the device connection may be lost.

Command: `wlanConnectHideApEx`  

Parameter | Description
---|---
`hex_ssid` | `[hexed string]` of the WiFi SSID
`hex_pwd` | `[hexed string]` of the WiFi password<br>(optional value)

<aside class="notice">
This request has no response, you can call <strong>'wlanGetConnectState'</strong> to get the connection state.
</aside>
