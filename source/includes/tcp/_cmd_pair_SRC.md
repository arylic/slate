## Device Status

These commands share a common parameter table composed of strings.

Parameter | Description
---|---
`str_player_mode` | The audio source that has to be switched<br>`NET`: wifi mode<br>`LINE-IN`: line analogue input<br>`BT`: bluetooth mode<br>`OPT`: optical digital input<br>`???`: RCA Analogue input<br>`COAX`: co-axial digital input<br>`LINE-IN2`: line analogue input #2

### Get Device Audio Source

> Command:

```plaintext
MCU+PAS+RAKOIT:SRC&
```

> Example Response:

```plaintext
MCU+PAS+RAKOIT:SRC`<str_player_mode>`&
```

This request will return the current player mode / audio source 

Command:   
`MCU+PAS+RAKOIT:SRC&`

Response:   
`MCU+PAS+RAKOIT:SRC<str_player_mode>&`

<br><br><br>

### Select Device Audio Source

> Command:

```plaintext
MCU+PAS+RAKOIT:SRC:`<str_player_mode>`&:
```

> Example Response:

```plaintext
NET                         // AXX+MEA+RDY AXX+PLY+000
USB                         // AXX+MEA+RDY AXX+MEA+RDY AXX+PLY+PLA AXX+PLY+000 AXX+PLY+001
BT                          // AXX+MEA+RDY AXX+MEA+RDY AXX+PLY+PLA
```

Selects the Audio Source of the Device. The available audio sources for each device will depend on the installed hardware. 

Command:   
`MCU+PAS+RAKOIT:SRC:<str_player_mode>&`

Response:

Parameter | Description
---+---
`AXX+MEA+RDY AXX+PLY+000` | Example reply 
`MCU+PAS+ERR:UNSUPPORTED&` | Check with FZ
`MCU+PAS+ERR:SRC&` | Check with FZ

<aside class="notice">
The RAKOIT command sent changes the audio source but the reply format is using the LinkPlay command set. Arylic are checking if this is correct!
</aside>

