## Playback

Command: `setPlayerCmd`  

### Playback

> Request format for sub commands: `play` | `playlist` | `hex_playlist` | `playLocalList`:

```html
GET /httpapi.asp?command=setPlayerCmd:play:<uri>
GET /httpapi.asp?command=setPlayerCmd:playlist:<uri>:<index>
GET /httpapi.asp?command=setPlayerCmd:hex_playlist:<uri>:<index>
GET /httpapi.asp?command=setPlayerCmd:playLocalList:<index>
```

Sub-Command | Parameters | Description
-+-+-
`play` | | Play an URI<br>`uri` could be a direct URL to a web radio stream (must be URL encoded)
`playlist` | `uri`, `index` | Play an URI<br>`uri` is an M3U playlist<br>`index` is the start index
`hex_playlist` | `uri`, `index` | Play an URI<br>`uri` is an M3U playlist<br>`index` is the start index<br>The `uri` value must be a `[hexed string]`
`playLocalList` | `index` | Play from USB disk<br>`index` is the start index

### Player Control

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

Sub-Command | Description
-+-
`pause` | Pause current playback
`resume` | Resume playback from last position, if it is paused
`onepause` | Toggle Play/Pause
`stop` | Stop current playback (play position will be reset to `0`)

### Track Selection

> Request format for sub commands: `prev` | `next` | `seek`:

```html
GET /httpapi.asp?command=setPlayerCmd:prev
GET /httpapi.asp?command=setPlayerCmd:next
GET /httpapi.asp?command=setPlayerCmd:seek:<position>
```

> Example response:

```plaintext
OK
```

Sub-Command | Parameter | Description
-+-+-
`prev` | | Play previous track
`next` | | Play next track
`seek` | `position` | Seek in current track (fast forward and rewind) to `position`

### Adjusting Volume, Mute the Player

> Request format for sub command: `vol` | `mute`

```html
GEt /httpapi.asp?command=setPlayerCmd:vol:<value>
GEt /httpapi.asp?command=setPlayerCmd:mute:<value>
```

> Example response:

```plaintext
OK
```

Sub-Command | Parameter | Description
-+-+-
`vol` | `value` | Adjusts the volume of the current device. The value ranges from `0-100`.
`mute` | `value` | Set the mute mode<br>`0` - Not muted<br>`1` - Muted

### Playback Mode

> Request format for sub command: `loopmode`

```html
SET /httpapi.asp?command=setPlayerCmd:loopmode:<value>
```

> Example response:

```plaintext
OK
```

Sub-Command | Parameter | Description
-+-+-
`loopmode` | `value` | Starts different playback modes<br>`0` - Sequential playback, no loop<br>`1` - Loops over the current track<br>`2` - Shuffle playback<br>`-1` - Playlist loop

### Adjust the Equalizer

> Request format for sub command: `equalizer`

```html
SET /httpapi.asp?command=setPlayerCmd:equalizer:<value>
```

> Example response:

```plaintext
OK
```

Sub-Command | Parameter | Description
-+-+-
`equalizer` | `value` | Adjusts the built in equalizer. Available values are:<br>`0` - Disables EQ<br>`1` - Classic<br>`2` - Popular<br>`3` - Jazz<br>`4` - Vocal<br><br>**NOTE: Not all device supports an equalizer.**

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
-+-
`getEqualizer` | Returns current EQ setting. The response value is one of the possible settings from command `setPlayerCmd:equalizer:<value>`

