## Device Bass Level
### Get Device Bass Level

>Command:

```plaintext
MCU+PAS+RAKOIT:BAS&
```

> Example Response:

```plaintext
MCU+PAS+RAKOIT:BAS:`<int_bass>`&
```

This request will return the current device bass level 

Command:   
`MCU+PAS+RAKOIT:BAS&`

Response:   
`MCU+PAS+RAKOIT:BAS<int_bass>&`

Value | Description
---+---
`<int_bass>` | Integer value of the bass level.<br>Value range is from `-10dB to 10dB`


### Set Device Bass Level

>Command:

```plaintext
MCU+PAS+RAKOIT:BAS`<int_bass>`&
```

> Example Response:

```plaintext
There is no Response for this command
```

Sets the Bass Level of the Device.

Command:   
`MCU+PAS+RAKOIT:BAS<int_bass>&`

Value | Description
---+---
`<int_bass>` | Integer value of the bass level.<br>Value range is from `-10dB to 10dB`

Response:   
There is no response for this command.