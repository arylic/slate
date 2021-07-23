## Abstract

> Assuming a module IP address of `192.168.10.1`, the general request format would look like:

```html
 GET http://192.168.10.1/httpapi.asp?command={command}
```

Our `Axx` modules are SoC modules for WiFi Audio solutions, which supports Smartlink, DLNA, Spotify Connect and Airplay. They also provide support for an `HTTP` API to get quick access.

To communicate with a board you have to send `HTTP GET` requests.  
The response is in `JSON` format.

<aside class="notice">
All values in this <code>JSON</code> are strings. Even numeric values comes as string representation!
</aside>
