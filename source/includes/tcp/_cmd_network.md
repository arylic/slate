## Network Information Commands

### Get Status of Ethernet Connection (RJ45 Network)
> Get command format:

```html
MCU+PAS+RAKOIT:ETH&:
```

> Example Response:

```plaintext
MCU+PAS+RAKOIT:ETH:0& or MCU+PAS+RAKOIT:ETH:1&
```
This command will return the status of the device on the Local Area Network (LAN).  

Command: `MCU+PAS+RAKOIT:ETH&`

Response: <br>`MCU+PAS+RAKOIT:ETH:0&` Device not connected to LAN<br>`MCU+PAS+RAKOIT:ETH:1&` Device connected to LAN<br><br> 



### Get Status of Wireless Connection (WiFi Network)
> Get command format:

```html
MCU+PAS+RAKOIT:WIF&:
```

> Example Response:

```plaintext
MCU+PAS+RAKOIT:WIF:0& or MCU+PAS+RAKOIT:WIF:1&
```
This command will return the status of the device on the Wireless Local Area Network (WLAN).  

Command: `MCU+PAS+RAKOIT:ETH&`

Response: <br>`MCU+PAS+RAKOIT:WIF:0&` Device not connected to WLAN<br>`MCU+PAS+RAKOIT:WIF:1&` Device connected to WLAN<br> 


### Get Status of Internet Connection
> Get command format:

```html
MCU+PAS+RAKOIT:WWW&:
```

> Example Response:

```plaintext
MCU+PAS+RAKOIT:WWW:0& or MCU+PAS+RAKOIT:WWW:1&
```
This command will return the status of the device Internet Connection.  

Command: `MCU+PAS+RAKOIT:WWW&`

Response: <br>`MCU+PAS+RAKOIT:WWW:0&` Device not connected to Internet<br>`MCU+PAS+RAKOIT:WIF:1&` Device connected to Internet<br> 