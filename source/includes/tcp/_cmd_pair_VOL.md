## Device Volume Command Pair

### Get Device Volume
> Get command format:

```html
"MCU+PAS+RAKOIT:VOL&:
```

> Example Response:

```plaintext
MCU+PAS+VOL:`<int_volume>`&
```

This request will return the current device volume level 

Command:    `MCU+PAS+RAKOIT:VOL&`

Response:   `MCU+PAS+RAKOIT:VOL<int_volume>&`  
            `<int_volume>` Integer value of the volume level.  Value range is from `0 - 100`<br> 


### Select Device Volume
> Set command format:

```html
MCU+PAS+RAKOIT:VOL`<int_volume>`&:

There is no Response for this command:
```

Sets the Volume of the Device.

Command:    `MCU+PAS+RAKOIT:VOL<int_volume>&`  
            `<int_volume>` Integer value of the volume level.  Value range is from `0 - 100`<br>

Response    There is no response for this command.