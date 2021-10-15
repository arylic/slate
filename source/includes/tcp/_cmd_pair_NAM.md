## Device Name (Command Pair Get & Set)

### Get Device Name
> Get command format:

```html
MCU+PAS+RAKOIT:NAM&:
```

> Example Response:

```plaintext
MCU+PAS+RAKOIT:NAM:4E4F42425920424F58&
```
This command will return the current device name.  

Command: `MCU+PAS+RAKOIT:NAM&`

Response: Is a hexadecimal string  

<aside class="notice">
Note after a firmware upgrade the name of the device will be extended to '<ascii_str_name>' and `_XXXX` so '<ascii_str_name>_XXXX`.  XXXX correponds to the last two hexadecimal pairs of the device MAC address.
</aside>

### Set Device Name
> Set command format:

```html
MCU+PAS+RAKOIT:NAM:<hex_str_name>&
```

> Example Response:

```plaintext
AXX+NAM+RAKOIT:<ascii_str_name>&
```

Sets the device name. 

Command: `MCU+PAS+RAKOIT:NAM:<hex_str_name>&`

Parameter | Description
---|---|---
`hex_str_name` | Device name string (hexadecimal)    
`ascii_str_name` | Device name string (ascii characeters) 

Response: <br>`MCU+PAS+RAKOIT:<hex_str_name>&`

<aside class="notice">
When setting the Device name current playback will stop 
</aside>