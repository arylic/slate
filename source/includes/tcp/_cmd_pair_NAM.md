## Device Name

### Get Device Name

> Command:

```plaintext
MCU+PAS+RAKOIT:NAM&:
```

> Example Response:

```plaintext
MCU+PAS+RAKOIT:NAM:4E4F42425920424F58&
```

This command will return the current device name.  
Response: Is a hexadecimal string  

<br><br>
<aside class="notice">
Note after a firmware upgrade the name of the device will be extended to '<ascii_str_name>' and `_XXXX` so '<ascii_str_name>_XXXX`.  XXXX correponds to the last two hexadecimal pairs of the device MAC address.
</aside>

<br><br><br><br>

### Set Device Name

> Command:

```plaintext
MCU+PAS+RAKOIT:NAM:<hex_str_name>&
```

> Example Response:

```plaintext
AXX+NAM+RAKOIT:<ascii_str_name>&
```

Sets the device name. 

Parameter | Description
---|---|---
`hex_str_name` | Device name string (hexadecimal)    
`ascii_str_name` | Device name string (ascii characeters) 

Response: <br>`MCU+PAS+RAKOIT:<hex_str_name>&`

<aside class="notice">
When setting the Device name current playback will stop 
</aside>