### Get Audio Channel Information (Mono/Stereo)

> Command:

```plaintext
MCU+PAS+RAKOIT:CHN&
```

> Example Response:

```plaintext
MCU+PAS+CHN:S&                  // Device output is Stereo
MCU+PAS+CHN:L&                  // Device output is Mono - Left Channel
MCU+PAS+CHN:R&                  // Device output is Mono - Right Channel
```
This request will return a string which will indicate stereo active or mono active (including channel left or right) 

Command:   
`MCU+PAS+RAKOIT:CHN&`

Response:

Response | Description
---+---
`MCU+PAS+RAKOIT:CHN:S&` | Device output is Stereo
`MCU+PAS+RAKOIT:CHN:L&` | Device output is Mono - Left Channel
`MCU+PAS+RAKOIT:CHN:R&` | Device output is Mono - Right Channel
