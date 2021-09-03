## Device Main BEEP Tone (Enable/Disable)
### Get BEEP Tone Status (Enabled/Disabled)

> Command::

```plaintext
MCU+PAS+RAKOIT:BEP&
```

> Example Response:

```plaintext
MCU+PAS+RAKOIT:BEP:0&           // BEEP Disabled 
MCU+PAS+RAKOIT:BEP:1&           // BEEP Enabled
```
This request will return a boolean state of the BEEP Tone Enable/Disable Function 

Command:   
`MCU+PAS+RAKOIT:BEP&`

Response:

Response | Description
---|---
`MCU+PAS+RAKOIT:BEP:0&` | BEEP Tone Disabled
`MCU+PAS+RAKOIT:BEP:1&` | BEEP Tone Enabled

<br>

### Set BEEP Tone Status (Enable/Disable)

> Command:

```plaintext
MCU+PAS+RAKOIT:BEP:0&           // Disable BEEP Tone
MCU+PAS+RAKOIT:BEP:1&           // Enable BEEP Tone

```

> Example Response:

```plaintext
MCU+PAS+RAKOIT:BEP:0&           // BEEP Tone  Disabled 
MCU+PAS+RAKOIT:BEP:1&           // BEEP Tone Enabled
```

Enables & Disables device main BEEP Tone. 

Command:   
`MCU+PAS+RAKOIT:BEP:<bool>&`

Parameter | Description
---|---
`<bool>` | A boolean value <br>`0` Enable <br>`1` Disable

Response:

Response | Description
---|---
`MCU+PAS+RAKOIT:BEP:0&` | BEEP Tone Disabled
`MCU+PAS+RAKOIT:BEP:1&` | BEEP Tone Enabled

<br>
