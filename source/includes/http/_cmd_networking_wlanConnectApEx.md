## Connect to WiFi
> Request format:

```html
GET /httpapi.asp?command=wlanConnectApEx:
    ssid=<hex_ssid>:ch=<num_channel>:auth=<text_auth>:encry=<text_encry>:pwd=<hex_pwd>:chext=1
```

Request to connect to a desired WiFi network. Mainly used during device setup.


Command: `wlanConnectApEx`  

Parameter | Description
---|---
`hex_ssid` | `[hexed string]` of the WiFi SSID
`num_channel` | WiFi channel to connect (1-12)
`text_auth` | WiFi authorization mechanism, `OPEN` or `WPA2PSK`
`text_encry` | Encryption type, `AES` or `NONE`
`hex_pwd` | `[hexed string]` of the WiFi password
`flag_chext` | 1

<aside class="notice">
This request has no response, you can call <strong>`wlanGetConnectState`</strong> to get the connection status.
</aside>
