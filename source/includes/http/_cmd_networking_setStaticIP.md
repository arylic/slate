## Set Manual IP

> Request format:

```html
GET /httpapi.asp?command=setStaticIP:{"type":"<TYPE>","ip":"<IP>","mask":"<MASK>","gateway":"<GW>","dns":[{"service":"<DNS1>"},{"service":"<DNS2>"}]}
```
> Sample Response: 

```text
OK
```

Manually set network parameters for WiFi or Ethernet.

Command: `setStaticIP`  

Command parameters:

* `<TYPE>` - Network interface to set, could be `wifi` or `eth`
* `<IP>` - IPV4 address to manually set
* `<MASK>` - network mask 
* `<GW>` - Gateway
* `<DNS1>` - Prefered DNS
* `<DNS2>` - Alternate DNS

<aside class="notice">
Introduced in version 4.6.328252
</aside>
