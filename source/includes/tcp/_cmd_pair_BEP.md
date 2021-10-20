## Device Main BEEP Tone (Enable/Disable) - Command Pair
### Get BEEP Tone Status (Enabled/Disbled)
> Command::

```plaintext
MCU+PAS+RAKOIT:BEP&:
```

> Example Response:

```plaintext
MCU+PAS+RAKOIT:BEP:0&           // BEEP Disabled 
MCU+PAS+RAKOIT:BEP:1&           // BEEP Enabled
```
This request will return a boolean state of the BEEP Tone Enable/Disable Function 

Command: `MCU+PAS+RAKOIT:BEP&`

Response: <br>`MCU+PAS+RAKOIT:BEP:0&` BEEP Tone Disabled<br>`MCU+PAS+RAKOIT:BEP:1&` BEEP Tone Enabled

<br><br><br>

### Set BEEP Tone Status (Enabled/Disbled)
> Command:

```plaintext
MCU+PAS+RAKOIT:BEP:0&      // Disable BEEP Tone
MCU+PAS+RAKOIT:BEP:1&      // Enable BEEP Tone

```

> Example Response:

```plaintext
MCU+PAS+RAKOIT:BEP:0&           // BEEP Tone  Disabled 
MCU+PAS+RAKOIT:BEP:1&           // BEEP Tone Enabled
```

Enables & Disables device main BEEP Tone. 

Command: `MCU+PAS+RAKOIT:BEP:<bool>&`

Parameter | Description
---|---|---
`<bool>` | A boolean value <br>`0` Enable <br>`1` Disable<br>

Response: <br>
`MCU+PAS+RAKOIT:BEP:0&` BEEP Tone Disabled<br>
`MCU+PAS+RAKOIT:BEP:1&` BEEP Tone Enabled

Parameter | Description
---|---|---
`0` | Disable
`1` | Enable
