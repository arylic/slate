## Set DHCP

> Request format:

```html
GET /httpapi.asp?command=setDhcp:<TYPE>
```
> Sample Response: 

```text
OK
```

Request to connect to a desired WiFi network. Mainly used during device setup.

Command: `setDhcp`  

Command parameters:

* `<TYPE>` - Network interface to set, could be `wifi` or `eth`

<aside class="notice">
Introduced in version 4.6.328252
</aside>
