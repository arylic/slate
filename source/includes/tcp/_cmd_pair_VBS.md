## Device Virtual Bass (On/Off)
### Get Virtual Bass Status (On/Off)

>Command:

```plaintext
MCU+PAS+RAKOIT:VBS&:
```

> Example Response:

```plaintext
MCU+PAS+VBS:0&                  // Virtual Bass Disabled
MCU+PAS+VBS:1&                  // Virtual Bass Enabled
```
This request will return a boolean state of the Virtual Bass Enable/Disable Function 

Command:   
`MCU+PAS+RAKOIT:VBS&`

Response:

Value | Description
---+---
`MCU+PAS+VBS:0&` | Virtual Bass Disabled
`MCU+PAS+VBS:1&` | Virtual Bass Enabled

### Set Virtual Bass Status (On/Off)

>Command:

```plaintext
MCU+PAS+RAKOIT:VBS:0&           // Disable Virtual Bass
MCU+PAS+RAKOIT:VBS:1&           // Enable Virtual Bass
MCU+PAS+RAKOIT:VBS:T&           // Toggle current Virtual Bass status
```

> Example Response:

```plaintext
MCU+PAS+VBS:0&                  // VBS Disabled
MCU+PAS+VBS:1&                  // VBS Enabled
```

Enables & Disables device Virtual Bass. 

Command:   
`MCU+PAS+RAKOIT:VBS:<bool_or_toggle>&`

Parameter | Description
---|---|---
`bool_or_toggle` | A boolean value or the character `T`<br>`1` Disable <br>`0` Enable<br>`T` Toggle between enable & disable   

Response:   

Value | Description
---+---
`MCU+PAS+VBS:0&` | Virtual Bass Disabled
`MCU+PAS+VBS:1&` | Virtual Bass Enabled