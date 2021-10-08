## Query networking status 

> Request format:

```html
GET /httpapi.asp?command=getStaticIP
```
> Example response for ETH DHCP:

```json
{
	"wifi": "-1",
	"eth": "1"
}
```
> Example response for ETH Manual IP:

```json
{
	"wifi": "-1",
	"eth": "0",
	"eth_static_ip": "192.168.10.103",
	"eth_static_mask": "255.255.255.0",
	"eth_static_gateway": "192.168.10.1",
	"eth_static_dns1": "192.168.10.1",
	"eth_static_dns2": ""
}
```

Query current networking status

Command: `getStaticIP`  

### Description of response values
Key | Value Description
---|---
`wifi` | state of WiFi: <br>`-1` - not connected<br>`0` - Static IP<br>`1` - DHCP
`eth` | state of ETH: <br>`-1` - not connected<br>`0` - Static IP<br>`1` - DHCP
`eth_static_ip` | Available when `eth` is `0`, Manually set IP address
`eth_static_mask` | Available when `eth` is `0`, Net mask 
`eth_static_gateway` | Available when `eth` is `0`, Gateway
`eth_static_dns1` | Available when `eth` is `0`, Prefered DNS
`eth_static_dsn2` | Available when `eth` is `0`, Alternate DNS
`wifi_static_ip` | Available when `wifi` is `0`, Manually set IP address
`wifi_static_mask` | Available when `wifi` is `0`, Net mask 
`wifi_static_gateway` | Available when `wifi` is `0`, Gateway
`wifi_static_dns1` | Available when `wifi` is `0`, Prefered DNS
`wifi_static_dsn2` | Available when `wifi` is `0`, Alternate DNS

<aside class="notice">
Introduced in version 4.6.328252
</aside>
