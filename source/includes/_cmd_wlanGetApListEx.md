## List of scanned AP's

Retrieves a list of nearby scanned WiFi Access Points.

Command: `wlanGetApListEx`

> Request format:

```html
GET /httpapi.asp?command=wlanGetApListEx
```

> Example response:

```json
{
   "res": "2",
   "aplist": [
      {
         "auth": "AES",
         "bssid": "b4:fb:e4:f4:73:81",
         "channel": "11",
         "extch": "0",
         "rssi": "37",
         "ssid": "57696E6B656C6761737365"
      },
      {
         "auth": "WPA2PSK",
         "bssid": "18:e8:29:9d:75:c5",
         "channel": "6",
         "encry": "AES",
         "extch": "0",
         "rssi": "24",
         "ssid": "42657465696765757A65556E696669"
      }
   ]
}
```

### Description of response values

Key | Value Description
---|---
`res` | Number of SSID's found
`aplist` | The key to get the list of scanned Access Points

### Description of an AP response object

Key | Value Description
---|---
`auth` | Required WiFi authorization mechanism
`bssid` | The MAC address of that WiFi
`channel` | Used WiFi channel
`extch` | *!! Documentation is MISSING !!*
`rssi` | RSSI Level that WiFi<br>Value ranges from `0 - 100`.<br>`100` means best signal strength.
`ssid` | The SSID of that WiFi network<br>`[hexed string]`
