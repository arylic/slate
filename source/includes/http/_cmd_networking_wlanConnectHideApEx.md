## Connect to hidden WiFi

Connect the device to a hidden WiFi network. When connecting, the device connection may be lost.

> Request format with password:

```html
GET /httpapi.asp?command=wlanConnectHideApEx:ssid=<SSID>:pwd=<PWD>
```

> Request format without password:

```html
GET /httpapi.asp?command=wlanConnectHideApEx:ssid=<SSID>
```

Command: `wlanConnectHideApEx`  
Command parameters:

* `ssid` - `[hexed string]` of the WiFi SSID
* `pwd` - `[hexed string]` of the WiFi password<br>(optional value)

<aside class="notice">
This request has no response, you can call <strong>wlanGetConnectState</strong> to get the connection state.
</aside>
