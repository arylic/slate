## Device Treble Level
### Get Device Treble Level

>Command:

```plaintext
MCU+PAS+RAKOIT:TRE&
```

> Example Response:

```plaintext
MCU+PAS+RAKOIT:TRE:`<int_treble>`&
```

This request will return the current device treble level 

Command:   
`MCU+PAS+RAKOIT:TRE&`

Response:   
`MCU+PAS+RAKOIT:TRE<int_treble>&`

Value | Description
---+---
`<int_treble>` | Integer value of the treble level.<br>Value range is from `-10dB to 10dB`


### Select Device Treble Level

>Command:

```plaintext
MCU+PAS+RAKOIT:TRE`<int_Treble>`&
```

> Example Response:

```plaintext
There is no Response for this command
```

Sets the treble Level of the Device.

Command:   
`MCU+PAS+RAKOIT:TRE<int_Treble>&`

Value | Description
---+---
`<int_Treble>` | Integer value of the treble level.<br>Value range is from `-10dB to 10dB`

Response:   
There is no response for this command.