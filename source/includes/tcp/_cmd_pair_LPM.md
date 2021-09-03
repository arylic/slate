## Device Repeat & Shuffle playback

These commands share a common parameter table

Parameter | Description
---|---
`<str_shuffle_repeat>` | Activates a combination of Shuffle and Repeat modes<br>`REPEATALL`: Shuffle disabled, Repeat enabled - loop<br>`REPEATONE`: Shuffle disabled, Repeat enabled - loop once<br>`REPEATSHUFFLE`: Shuffle enabled, Repeat enabled - loop<br>`SHUFFLE`: Shuffle enabled, Repeat disabled<br>`SEQUENCE`: Shuffle disabled, Repeat disabled<br>`REPEATALL`: Shuffle enabled, Repeat enabled - loop once<br>

<aside class="notice">
The command <code>REPEATALL</code> appears twice in the table.  Arylic are checking this ! 
</aside>

### Get Device Repeat & Shuffle Modes

>Command:

```plaintext
"MCU+PAS+RAKOIT:LPM&:
```

> Example Response:

```plaintext
MCU+PAS+RAKOIT+SRC:LPM&
```

This request will return a combination of the current shuffle & repeat mode status.

Command:   
`MCU+PAS+RAKOIT:LPM&`

Response:

Response | Description
---|---
`MCU+PAS+RAKOIT:LPM<str_shuffle_repeat>&` | See parameter table above.


### Set Device Repeat & Shuffle Modes

>Command:

```plaintext
MCU+PAS+RAKOIT:SRC:`<str_shuffle_repeat>`&:
```

> Example Responses:

```plaintext
AXX+PLP+000                 // REPEATALL
AXX+PLP+001                 // REPEATONE
AXX+PLP+002                 // REPEATSHUFFLE - REPEAT ALL & SHUFFLE
AXX+PLP+003                 // SHUFFLE
AXX+PLP+004                 // NO SHUFFLE NO REPEAT
```

Selects the desired combination of shuffle and repeat functions. 

Command:   
`MCU+PAS+RAKOIT::`

Value | Description
---|---
`mode` | Playback mode<br>`PLAYER_MODE_NONE`<br>`NET`: NET Blah Blah Blah<br>`USB`: USB disk pen drive connected to  device)<br>`USBDAC`: USB DAC e.g. Fromlap to connected with USB lead<br>`BT`:  Bluetooth Input<br>`LINE-IN`: Analogue Line in<br>`LINE-IN2`: `PLAYER_MODE_LINEIN2`<br>`OPT`: `PLAYER_MODE_OPTICAL`<br>`COAX`: `PLAYER_MODE_COAXIAL`<br>`I2S`: `PLAYER_MODE_I2S`<br>`HSMI`: HDMI IN`<br>


NET/USB/USBDAC/LINE-IN/LINE-IN2/BT/OPT/COAX/I2S/HDMI

Response | Description
```
`AXX+MEA+RDY AXX+PLY+000` |  Example reply 
`MCU+PAS+ERR:UNSUPPORTED&` |  Check with FZ
`MCU+PAS+ERR:SRC&` | Check with FZ
```