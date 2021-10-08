### Device Audio Source
> Request format:

```html
"MCU+PAS+RAKOIT:SRC:<str_player_mode>&:
```

> Example Response:

```plaintext
OK
```

Selects the Audio Source of the Device. The available audio sources for each device will depend on the installed hardware. 

Command: `MCU+PAS+RAKOIT:SRC:`

Parameter | Description
---|---
`str_player_mode` | The audio source that has to be switched<br>`NET`: wifi mode<br>`LINE-IN`: line analogue input<br>`BT`: bluetooth mode<br>`OPT`: optical digital input<br>`???`: RCA Analogue input<br>`COAX`: co-axial digital input<br>`LINE-IN2`: line analogue input #2


### Play Preset Content
> Request format for command:

```html
MCU+PAS+RAKOIT:PST:<num_preset>&
```

> Example response:

```plaintext
AXX+MEA+RDY
```
Play Instruction for one of the Programmable Presets (maximum 10) 

Command: `MCU+PAS+RAKOIT:PST:`

Parameter | Description
---|---|---
`num_value` | The numeric value of the required Preset<br>Value range is from `0 - 10`   

