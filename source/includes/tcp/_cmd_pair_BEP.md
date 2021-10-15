## Device Main BEEP Tone (Enable/Disable) Command Pair `BEP`

### Get BEEP Tone Status (Enabled/Disbled)
> Get Request format:

```html
MCU+PAS+RAKOIT:BEP&:
```

> Example Response:

```plaintext
MCU+PAS+BEP:0& or MCU+PAS+BEP:1&
```
This request will return a boolean state of the BEEP Tone Enable/Disable Function 

Command: `MCU+PAS+RAKOIT:BEP&`

Response: <br>`MCU+PAS+BEP:0&` BEEP Tone Disabled<br>`MCU+PAS+BEP:1&` BEEP Tone Enabled




### Set BEEP Tone Status (Enabled/Disbled)
> Set Request format:

```html
MCU+PAS+RAKOIT:BEP:1& or MCU+PAS+RAKOIT:BEP:0&
```

> Example Response:

```plaintext
MCU+PAS+BEP:0&
MCU+PAS+BEP:1&
```

Enables & Disables device main BEEP Tone. 

Command: `MCU+PAS+RAKOIT:BEP:<bool_or_toggle>&`

Parameter | Description
---|---|---
`bool_or_toggle` | A boolean value <br>`1` Disable <br>`0` Enable<br>

Response: <br>`MCU+PAS+BEP:0&` BEEP Tone Disabled<br>`MCU+PAS+BEP:1&` BEEP Tone Enabled
