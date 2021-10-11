### Get the Current Device Status
> Request format:

```html
"MCU+PAS+RAKOIT:STA&"
```

> Example Response:

```plaintext
MCU+PAS+STA:NET,0,60,0,0,0,1,1,1,0&
```

This command provides useful device status information.  

Command: `MCU+PAS+RAKOIT:STA&`

Response: `MCU+PAS+STA:{str_source},{bool_mute},{int_volume},{int_treble},{int_bass},{bool_net},{bool_internet},{bool_playing},{bool_led},{bool_upgrading}`

### Description of response values

Key | Value Description
---|---
`str_source` | Playback mode<br>`0` - `PLAYER_MODE_NONE`
`int_volume` | Current volume<br>The integer range is from `0 - 100`. So can be considered a linear percentage (`0% to 100%`)
`int_treble` | Current treble level<br> The integer range is from `-10 - 10`.  This corresponds to `-10dB` & `+10dB`  
`int_bass` | Current bass level<br> The integer range is from `-10 - 10`.  This corresponds to `-10dB` & `+10dB`
`bool_net` | A boolean value indicating current device local network status<br>'0' Not on local network<br>`1` Device on local network.
`bool_internet` | A boolean value indicating current device internet connection status<br>'0' No internet connection<br>`1` Internet connection active  
`bool_playing` | A boolean value indicating if playback is active<br>'0' Playback not active<br>`1` Playback active 
`bool_led`  | A boolean value indicating if main LED light is enabled or disabled<br>'0' LED disabled<br>`1` LED enabled
`bool_upgrading`  | A boolean value indicating if a device firmware upgrade is in progress<br>'0' No firmware upgrade in progress<br>`1` upgrading firmware

