### Playback

Command: `setPlayerCmd`  

The command `setPlayerCmd` is the main command, it needs a sub command to execute an action. See the list of current available sub commands.


### Play Sub-command
> Request format for sub command: `play`

```html
SET /httpapi.asp?command=setPlayerCmd:play:<url>
```

> Example response:

```plaintext
OK
```

Play Instruction for any valid audio file or stream specified as a `URL`. 

Sub-Command: `play`

Parameter | Description
---|---|---
`url` | A complete `URL` for an audio source on the internet or addressable local device<br>`http://89.223.45.5:8000/progressive-flac` example audio file<br>`http://stream.live.vc.bbcmedia.co.uk/bbc_6music` example radio station file   


### M3U File/Playlist Sub-command
> Request format for sub command: `m3u:playlist`

```html
SET /httpapi.asp?command=setPlayerCmd:m3u:play:<url><index>
```

> Example response:

```plaintext
OK
```

Play Instruction for any valid `m3u` file or playlist specified as a `URL`. 

Sub-Command: `m3u:play`

Parameter | Description
---|---|---
`url` | A complete `URL` for an m3u file source on the internet or addressable local device<br>`http://nwt-stuff.com/Audio/playlists/ProgFLAC.m3u` example audio file<br>`http://nwt-stuff.com/Audio/playlists/bbc_6music.m3u8` example radio station file   

<aside class="notice">
The format of `m3u` files is not covered in this documentation. See <a href="https://docs.fileformat.com/audio/m3u/" target="_blank">further information on m3u file formats</a>.
</aside>


### Other Playback Sub-Commands
*!! DOCUMENTATION IN PROGRESS !!*

Sub-Command | Parameters | Description
---|---|---
`hex_playlist` | `uri`, `index` | Play an URI<br>`uri` is an M3U playlist<br>`index` is the start index<br>The `uri` value must be a `[hexed string]`


### Playback Control Sub-Commands
> Request format for sub commands: `pause` | `resume` | `onepause` | `stop`:

```html
GET /httpapi.asp?command=setPlayerCmd:pause
GET /httpapi.asp?command=setPlayerCmd:resume
GET /httpapi.asp?command=setPlayerCmd:onepause
GET /httpapi.asp?command=setPlayerCmd:stop
```

> Example response:

```plaintext
OK
```

The following commands will operate on the selected audio device.  

Sub-Command | Description
---|---
`pause` | Pause current playback
`resume` | Resume playback from last position, if it is paused
`onepause` | Toggle Play/Pause
`stop` | Stop current playback and removes slected source from device


### Track Selection
> Request format for sub commands: `prev` | `next` | `seek`:

```html
GET /httpapi.asp?command=setPlayerCmd:prev
GET /httpapi.asp?command=setPlayerCmd:next
GET /httpapi.asp?command=setPlayerCmd:seek:<position>
GET /httpapi.asp?command=setPlayerCmd:playindex:<index>
```

> Example response:

```plaintext
OK
```
The following commands will operate on the selected audio device.

Sub-Command | Parameter | Description
---|---|---
`prev` | | Play previous track
`next` | | Play next track
`seek` | `position` | Seconds to seek to, should be less than duration
`playindex` | `index` | play the selected track in current playlist, start from 1, and will play last track when `index` exceed the number of tracks. <br><aside class="notice"> Introduced in version 4.6.328252 </aside>

### Adjusting Volume, Mute the Player

> Request format for sub command: `vol` | `mute`

```html
GEt /httpapi.asp?command=setPlayerCmd:vol:<num_value>
GEt /httpapi.asp?command=setPlayerCmd:mute:<flag_value>
```

> Example response:

```plaintext
OK
```

Sub-Command | Parameter | Description
---|---|---
`vol` | `num_value` | Adjusts the volume of the current device.<br>Value range is from `0-100`.
`mute` | `flag_value` | Set the mute mode<br>`0`: Not muted<br>`1`: Muted

### Playback SHUFFLE and REPEAT Mode 
> Request format for sub command: `loopmode`

```html
SET /httpapi.asp?command=setPlayerCmd:loopmode:<flag_value>
```

> Example response:

```plaintext
OK
```

Sub-Command | Parameter | Description
---|---|---
`loopmode` | `flag_value` | Activates a combination of Shuffle and Repeat modes<br>`0`: Shuffle disabled, Repeat enabled - loop<br>`1`: Shuffle disabled, Repeat enabled - loop once<br>`2`: Shuffle enabled, Repeat enabled - loop<br>`3`: Shuffle enabled, Repeat disabled<br>`4`: Shuffle disabled, Repeat disabled<br>`5`: Shuffle enabled, Repeat enabled - loop once<br>

### Adjust the Equalizer
> Request format for sub command: `equalizer`

```html
SET /httpapi.asp?command=setPlayerCmd:equalizer:<flag_value>
```

> Example response:

```plaintext
OK
```

Sub-Command | Parameter | Description
---|---|---
`equalizer` | `flag_value` | Adjusts the built in equalizer. Available values are:<br>`0`: Disables EQ<br>`1`: Classic<br>`2`: Popular<br>`3`: Jazz<br>`4`: Vocal<br><br>**NOTE: Not all device supports an equalizer.**

### Get Equalizer Settings
> Request format for sub command: `getEqualizer`

```html
GET /httpapi.asp?command=setPlayerCmd:getEqualizer
```

> Example response (when EQ is set to Jazz):

```plaintext
3
```

Sub-Command | Description
---|---
`getEqualizer` | Returns current EQ setting. The response value is one of the possible settings from command `setPlayerCmd:equalizer:<value>`

