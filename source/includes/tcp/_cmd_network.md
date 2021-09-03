# Connection Status Commands

### Get Status of Ethernet Connection (RJ45 Network)

> Command:

```plaintext
MCU+PAS+RAKOIT:ETH&:
```

> Example Response:

```plaintext
MCU+PAS+RAKOIT:ETH:0&           // Device not connected to LAN
MCU+PAS+RAKOIT:ETH:1&           // Device connected to LAN
```
This command will return the status of the device on the Local Area Network (LAN).  

Command:   
`MCU+PAS+RAKOIT:ETH&`

Response:   

Response | Description
---+---
`MCU+PAS+RAKOIT:ETH:0&` | Device not connected to LAN
`MCU+PAS+RAKOIT:ETH:1&` | Device connected to LAN

<br><br><br> 

### Get Status of Wireless Connection (WiFi Network)

> Command:

```plaintext
MCU+PAS+RAKOIT:WIF&
```

> Example Response:

```plaintext
MCU+PAS+RAKOIT:WIF:0&           // Device not connected to WLAN
MCU+PAS+RAKOIT:WIF:1&           // Device connected to WLAN
```
This command will return the status of the device on the Wireless Local Area Network (WLAN).  

Command:   
`MCU+PAS+RAKOIT:WIF&`

Response:

Response | Description
---+---
`MCU+PAS+RAKOIT:WIF:0&` | Device not connected to WLAN
`MCU+PAS+RAKOIT:WIF:1&` | Device connected to WLAN

<br><br><br>

### Get Status of Internet Connection
> Command:

```plaintext
MCU+PAS+RAKOIT:WWW&
```

> Example Response:

```plaintext
MCU+PAS+RAKOIT:WWW:0&           // Device not connected to Internet
MCU+PAS+RAKOIT:WWW:1&           // Device connected to Internet
```
This command will return the status of the device Internet Connection.  

Command:   
`MCU+PAS+RAKOIT:WWW&`

Response:

Response | Description
---+---
`MCU+PAS+RAKOIT:WWW:0&` | Device not connected to Internet
`MCU+PAS+RAKOIT:WWW:1&` | Device connected to Internet
