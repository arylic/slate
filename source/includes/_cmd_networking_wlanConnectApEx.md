## Connect to WiFi

Request to connect to a desired WiFi network. Mainly used during device setup.

> Request format:

```html
GET /httpapi.asp?command=wlanConnectApEx:ssid=<SSID>:ch=<CHANNEL>:auth=<AUTH>:encry=<ENCRYPT>:pwd=<PASSWORD>:chext=1
```

Command: `wlanConnectApEx`  
Command parameters:

* `ssid` - `[hexed string]` of the WiFi SSID
* `ch` - WiFi channel to connect (1-12)
* `auth` - WiFi authorization mechanism, `OPEN` or `WPA2PSK`
* `encry` - Encryption type, `AES` or `NONE`
* `pwd` - `[hexed string]` of the WiFi password
* `chext` - 1

<aside class="notice">
This request has no response, you can call <strong>wlanGetConnectState</strong> to get the connection state.
</aside>
