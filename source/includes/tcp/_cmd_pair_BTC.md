## Device Bluetooth Connection
### Get Bluetooth Connection Status 

> Command:

```plaintext
MCU+PAS+RAKOIT:BTC&
```

> Example Response:

```plaintext
MCU+PAS+BTC:0&                  // Bluetooth connection not active 
MCU+PAS+BTC:1&                  // Bluetooth connection active
```
This request will return the boolean state of the Bluetooth connection,   

Command:   
`MCU+PAS+RAKOIT:BTC&`

Response:

Response | Description
---+---
`MCU+PAS+BTC:0&` | Bluetooth connection not active
`MCU+PAS+BTC:1&` | Bluetooth connection active

<aside class="notice">
If the Device is not in Bluetooth player mode then the reply will always be <code>MCU+PAS+BTC:0&</code>.
</aside>

### Reconnect last active Bluetooth connection

> Command:

```plaintext
MCU+PAS+RAKOIT:BTC:0&           // Disconnect current Bluetooth connection 
MCU+PAS+RAKOIT:BTC:1&           // Reconnect to a last active Bluetooth connection
```

> Example Response:

```plaintext
MCU+PAS+BTC:0&                  // Bluetooh disconnected
MCU+PAS+BTC:1&                  // Bluetooth connected
MCU+PAS+RAKOIT:ERR:INVALID&     // Device is not in Bluetooth player mode
```

Connects and disconnects Bluetooth active connection when the player mode is Bluetooth. 

Command:   
`MCU+PAS+RAKOIT:BTC:<bool>&`

Parameter | Description
---|---
`<bool>` | A boolean value<br>`0` Disconnect Bluetooth<br>`1` Connect Bluetooth   

Response:

Response | Description
---+---
`MCU+PAS+VBS:0&` | Bluetooh disconnected
`MCU+PAS+VBS:1&` | Bluetooth connected
`MCU+PAS+RAKOIT:ERR:INVALID&` | Device is not in Bluetooth player mode