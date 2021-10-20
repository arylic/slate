## Device Treble Level - Command Pair
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

Command:    `MCU+PAS+RAKOIT:TRE&`

Response:   `MCU+PAS+RAKOIT:TRE<int_treble>&`<br>
            `<int_treble>` Integer value of the treble level.  Value range is from `-10dB to 10dB`<br> 


### Select Device Treble Level
>Command:

```plaintext
MCU+PAS+RAKOIT:TRE`<int_Treble>`&:

There is no Response for this command:
```

Sets the treble Level of the Device.

Command:    `MCU+PAS+RAKOIT:TRE<int_Treble>&`  
            `<int_Treble>` Integer value of the treble level.  Value range is from `-10dB to 10dB`<br>

Response:    There is no response for this command.