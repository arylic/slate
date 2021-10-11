### Request Volume Level
> Request format:

```html
"MCU+PAS+RAKOIT:VOL&:
```

> Example Response:

```plaintext
AXX+VOL+23
```

Requests the Current Volume. 

Command: `MCU+PAS+RAKOIT:SRC:`

The Value returned is an Integer  


### Set Volume Level
> Request format for command:

```html
MCU+PAS+RAKOIT:VOL:<int_volume>&
```

> There is No Response to this command:

Set the required volume level `0-100` 

Command: `MCU+PAS+RAKOIT:PST:`

Parameter | Description
---|---|---
`int_volume` | Integer value for the required Volume<br>Value range is from `0 - 100`   


### Mute Device
> Request format:

```html
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
