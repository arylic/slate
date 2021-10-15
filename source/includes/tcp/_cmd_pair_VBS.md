## Device Virtual Bass (Enable/Disable) Command Pair `VBS`
### Get Virtual Bass Status (Enabled/Disbled)
> Get Request format:

```html
MCU+PAS+RAKOIT:VBS&:
```

> Example Response:

```plaintext
MCU+PAS+VBS:0& or MCU+PAS+VBS:1&
```
This request will return a boolean state of the Virtual Bass Enable/Disable Function 

Command: `MCU+PAS+RAKOIT:VBS&`

Response: <br>`MCU+PAS+VBS:0&` Virtual Bass Disabled<br>`MCU+PAS+VBS:1&` Virtual Bass Enabled<br>

### Set Virtual Bass Status (Enabled/Disbled)
> Set Request format:

```html
MCU+PAS+RAKOIT:VBS:1& or MCU+PAS+RAKOIT:VBS:0& or MCU+PAS+RAKOIT:VBS:T&
```

> Example Response:

```plaintext
MCU+PAS+VBS:0&
MCU+PAS+VBS:1&
```

Enables & Disables device Virtual Bass. 

Command: `MCU+PAS+RAKOIT:VBS:<bool_or_toggle>&`

Parameter | Description
---|---|---
`bool_or_toggle` | A boolean value or the character `T`<br>`1` Disable <br>`0` Enable<br>`T` Toggle between enable & disable   

Response: <br>`MCU+PAS+VBS:0&` Virtual Bass Disabled<br>`MCU+PAS+VBS:1&` Virtual Bass Enabled