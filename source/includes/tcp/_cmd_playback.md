# Playback Commands

### Play Preset Content
>Command:

```plaintext
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

### Mute Device
>Command:

```plaintext
"MCU+PAS+RAKOIT:MUT:1& or MCU+PAS+RAKOIT:MUT:0& or MCU+PAS+RAKOIT:MUT:T&"
```

> Example Response:

```plaintext
MCU+PAS+MUT:0&
MCU+PAS+MUT:1&
```

Mute and Unmute device. 

Command: `MCU+PAS+RAKOIT:MUT:<bool_or_toggle>&`

Parameter | Description
---|---|---
`bool_or_toggle` | A boolean value or the charater `T`<br>`1` mute <br>`0` unmute<br>'T' Toggle between mute and unmute   
