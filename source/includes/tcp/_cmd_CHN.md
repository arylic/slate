### Get Audio Channel Information (Mono/Stereo)
>Command:

```plaintext
MCU+PAS+RAKOIT:CHN&
```

> Example Response:

```plaintext
MCU+PAS+CHN:S& or MCU+PAS+CHN:L& or MCU+PAS+CHN:R&
```
This request will return a string which will indicate stereo active or mono active (including channel left or right) 

Command: `MCU+PAS+RAKOIT:CHN&`

Response: <br>
`MCU+PAS+RAKOIT:CHN:S&` Device output is Stereo <br>
`MCU+PAS+RAKOIT:CHN:L&` Device output is Mono - Left Channel<br>
`MCU+PAS+RAKOIT:CHN:R&` Device output is Mono - Right Channel<br>
