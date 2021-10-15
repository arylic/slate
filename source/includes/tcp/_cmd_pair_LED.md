## Device Main LED (Enable/Disable) Command Pair `LED`
### Get LED Status (Enabled/Disbled)
> Get Request format:

```html
MCU+PAS+RAKOIT:LED&:
```

> Example Response:

```plaintext
MCU+PAS+LED:0& or MCU+PAS+LED:1&
```
This request will return a boolean state of the LED Enable/Disable Function 

Command: `MCU+PAS+RAKOIT:LED&`

Response: <br>`MCU+PAS+LED:0&` LED Disabled<br>`MCU+PAS+LED:1&` LED Enabled<br>

### Set LED Status (Enabled/Disbled)
> Set Request format:

```html
MCU+PAS+RAKOIT:LED:1& or MCU+PAS+RAKOIT:LED:0& or MCU+PAS+RAKOIT:LED:T&
```

> Example Response:

```plaintext
MCU+PAS+LED:0&
MCU+PAS+LED:1&
```

Enables & Disables device main LED. 

Command: `MCU+PAS+RAKOIT:LED:<bool_or_toggle>&`

Parameter | Description
---|---|---
`bool_or_toggle` | A boolean value or the character `T`<br>`1` Disable <br>`0` Enable<br>`T` Toggle between enable & disable   

Response: <br>`MCU+PAS+LED:0&` LED Disabled<br>`MCU+PAS+LED:1&` LED Enabled
