## Set Manual IP

> Request format:

```html
GET /httpapi.asp?command=setStaticIP:{"type":"<TYPE>","ip":"<IP>","mask":"<MASK>","gateway":"<GW>","dns":[{"service":"<DNS1>"},{"service":"<DNS2>"}]}
```
> Sample Response: 

```text
OK
```

Manually set network parameters for WiFi or Ethernet. The API will accept a json format string as parameter.

Command: `setStaticIP:<info>`

### Parameters in `info`:

Field | Description
---|---
`TYPE` | Network interface to set, could be `wifi` or `eth`
`IP` | IPV4 address to manually set, eg: `192.168.0.100`
`MASK` | network mask, eg: `255.255.255.0`
`GW` | Gateway, eg: `192.168.0.1`
`DNS1` | Prefered DNS, eg: `8.8.8.8`
`DNS2` | Alternate DNS, eg: `8.8.8.8`

<aside class="notice">
Introduced in version 4.6.328252
</aside>
