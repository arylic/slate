### Playback

> Request format for sub commands: `play` | `playlist` | `hex_playlist` | `playLocalList` | `m3u:play`:

```html
GET /httpapi.asp?command=setPlayerCmd:play:<uri>
GET /httpapi.asp?command=setPlayerCmd:playlist:<uri>:<index>
GET /httpapi.asp?command=setPlayerCmd:hex_playlist:<uri>:<index>
GET /httpapi.asp?command=setPlayerCmd:playLocalList:<index>
GET /httpapi.asp?command=setPlayerCmd:m3u:play:<uri>
```

Sub-Command | Parameter | Description
---|---|---
`play` | `uri` | Play the `uri` immediately, it's normally used to play a radio link
`playLocalList` | `index` | Play the songs on USB pendrive start from <index>, and <index> start from 1
`m3u:play` | `uri` | 

M3U format private extension

To send a M3U link, and it will be then parsed and create a playlist for playback. supported M3U tags:

```plaintext
  #EXTM3U m3u header, must be in the first line
  #EXTURL:URL URL for coverart, placed before the music link
  #EXTINF:N,ARTIST - TITLE Meta info, placed before the music link
  URL music link, relative to m3u or absolute,
    example:
  #EXTM3U
  #EXTURL:http://192.168.0.2/test/cover.jpg
  #EXTINF:1,P!nk - Just give me a reason
    Just Give Me A Reason.mp3
```

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

Sub-Command | Parameter | Description
---|---|---
`prev` | | Play previous track
`next` | | Play next track
`seek` | `position` | Seconds to seek to, should be less than duration
`playindex` | `index` | play the selected track in current playlist, start from 1, and will play last track when `index` exceed the number of tracks. <br><aside class="notice"> Introduced in version 4.6.328252 </aside>

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
---|---|---
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
---|---|---
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
---|---|---
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
---|---
`getEqualizer` | Returns current EQ setting. The response value is one of the possible settings from command `setPlayerCmd:equalizer:<value>`

