## Abstract

> Assuming a device IP address of `192.168.10.1`, the general request format would look like:

```html
 GET http://192.168.10.1/httpapi.asp?command={command}
```

Arylic's `Axx` modules are SoC modules for WiFi Audio solutions, which supports Smartlink, DLNA, Spotify Connect and Airplay. They also provide support for an `HTTP` API to get quick access.

To communicate with a board you have to send `HTTP GET` requests.  
The response is in `JSON` format.

<aside class="notice">
All response examples in this documentation are from different devices (<strong>Up2Stream Amp v4</strong>, <strong>Up2Stream mini v3</strong>) but same firmware version (<code>4.6.9724.26</code>). It is possible that responses from older firmware may differ.
</aside>


