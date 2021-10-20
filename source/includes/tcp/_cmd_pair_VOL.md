## Device Volume

### Get Device Volume

>Command:

```plaintext
MCU+PAS+RAKOIT:VOL&:
```

> Example Response:

```plaintext
MCU+PAS+VOL:`<int_volume>`&
```

This request will return the current device volume level 

Command:   
`MCU+PAS+RAKOIT:VOL&`

Response:   
`MCU+PAS+RAKOIT:VOL<int_volume>&`

Parameter | Description
---+---
`<int_volume>` | Integer value of the volume level.<br>Value range is from `0 - 100`


### Select Device Volume
>Command:

```plaintext
MCU+PAS+RAKOIT:VOL`<int_volume>`&:
```

> Example Response:

```plaintext
There is no Response for this command
```

Sets the Volume of the Device.

Command:   
`MCU+PAS+RAKOIT:VOL<int_volume>&`

Parameter | Description
---+---
`<int_volume>` | Integer value of the volume level.<br>Value range is from `0 - 100`

Response:   
There is no response for this command.