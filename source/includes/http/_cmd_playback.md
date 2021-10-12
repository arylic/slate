### Device Audio Source
> Request format:

```html
GET /httpapi.asp?command=switchmode:<player_mode>
```

> Example Response:

```plaintext
OK
```

Selects the Audio Source of the Device. The available audio sources for each device will depend on the installed hardware. 

Sub-Command: `switchmode`

Parameter | Description
---|---
`player_mode` | The audio source that has to be switched<br>`0`: wifi mode<br>`40`: line analogue input<br>`41`: bluetooth mode<br>`43`: optical digital input<br>`44`: RCA Analogue input<br>`45`: co-axial digital input<br>`47`: line analogue input #2


### Play Preset Content
> Request format

```html
GET /httpapi.asp?command=MCUKeyShortClick:<num_value>
```

> Example response:

```plaintext
OK
```

Play Instruction for one of the Programmable Presets (maximum 10) 

Command: `MCUKeyShortClick`

Parameter | Description
---|---|---
`num_value` | The numeric value of the required Preset<br>Value range is from `0 - 10`   

