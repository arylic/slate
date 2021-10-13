# Device Status Command Pair `SRC`

These commands share a common parameter table

Parameter | Description
---|---
`str_player_mode` | The audio source that has to be switched<br>`NET`: wifi mode<br>`LINE-IN`: line analogue input<br>`BT`: bluetooth mode<br>`OPT`: optical digital input<br>`???`: RCA Analogue input<br>`COAX`: co-axial digital input<br>`LINE-IN2`: line analogue input #2

### Get Device Audio Source
> Request format:

```html
"MCU+PAS+RAKOIT:SRC&:
```

> Example Response:

```plaintext
MCU+PAS+SRC:NET&
```

This request will return the current audio source 

Command: `MCU+PAS+RAKOIT:SRC&`

Response: `MCU+PAS+RAKOIT:SRC{str_player_mode}&`


### Select Device Audio Source
> Request format:

```html
"MCU+PAS+RAKOIT:SRC:<str_player_mode>&:"
```

> Example Response:

```plaintext
NET = AXX+MEA+RDY AXX+PLY+000
USB = AXX+MEA+RDY AXX+MEA+RDY AXX+PLY+PLA AXX+PLY+000 AXX+PLY+001
```

Selects the Audio Source of the Device. The available audio sources for each device will depend on the installed hardware. 

Command: `MCU+PAS+RAKOIT:SRC:`

Response | Description
---|---
`AXX+MEA+RDY AXX+PLY+000` |  Example reply 
`MCU+PAS+ERR:UNSUPPORTED&` |  Check with FZ
`MCU+PAS+ERR:SRC&` | Check with FZ