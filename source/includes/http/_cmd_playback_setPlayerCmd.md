## Select Input Source

> Request format:

```html
GET /httpapi.asp?command=setPlayerCmd:switchmode:<player_mode>
```

> Example Response:

```plaintext
OK
```

Selects the Audio Source of the Device. The available audio sources for each device will depend on the installed hardware. 

Command: `setPlayerCmd:switchmode`

Parameter | Description
---|---
`player_mode` | The audio source that has to be switched<br>`wifi`: wifi mode<br>`line-in`: line analogue input<br>`bluetooth`: bluetooth mode<br>`optical`: optical digital input<br>`co-axial`: co-axial digital input<br>`line-in2`: line analogue input #2<br>`udisk`: UDisk mode<br>`PCUSB`: USBDAC mode

## Play a URL

> Request format 

```html
GET /httpapi.asp?command=setPlayerCmd:play:<url>
```

> Example response:

```plaintext
OK
```

Play Instruction for any valid audio file or stream specified as a `URL`. 

Command: `setPlayerCmd:play:<url>`

Parameter | Description
---|---
`url` | A complete `URL` for an audio source on the internet or addressable local device<br>`http://89.223.45.5:8000/progressive-flac` example audio file<br>`http://stream.live.vc.bbcmedia.co.uk/bbc_6music` example radio station file   


## Play a M3U File/Playlist

> Request format

```html
GET /httpapi.asp?command=setPlayerCmd:m3u:play:<url>
```

> Example response:

```plaintext
OK
```

Play Instruction for any valid `m3u` file or playlist specified as a `URL`. The M3U used [extended tags](#extended-m3u-tags) to support coverart URL, title and artist for the tracks.

Command: `setPlayerCmd:m3u:play:<url>`

Parameter | Description
---|---
`url` | A complete `URL` for an m3u file source on the internet or addressable local device<br>`http://nwt-stuff.com/Audio/playlists/ProgFLAC.m3u` example audio file<br>`http://nwt-stuff.com/Audio/playlists/bbc_6music.m3u8` example radio station file. The format of `m3u` files is not covered in this documentation. See <a href="https://docs.fileformat.com/audio/m3u/" target="_blank">further information on m3u file formats</a>.

## Play Selected Track 

> Request format:

```html
GET /httpapi.asp?command=setPlayerCmd:playindex:<index>
```

> Example response:

```plaintext
OK
```

The following commands will operate on the selected audio device.

Command: `setPlayerCmd:playindex:<index>`

Param | Description
---|---
`index` | play the selected track in current playlist, start from 1, and will play last track when `index` exceed the number of tracks. 

<aside class="notice"> Introduced in version 4.6.328252 </aside>

## Set Shuffle And Repeat Mode 

> Request format:

```html
GET /httpapi.asp?command=setPlayerCmd:loopmode:<mode>
```

> Example response:

```plaintext
OK
```

Command: `setPlayerCmd:loopmode:<mode>`

Parameter | Description
---|---
`mode` | Activates a combination of Shuffle and Repeat modes<br>`0`: Shuffle disabled, Repeat enabled - loop<br>`1`: Shuffle disabled, Repeat enabled - loop once<br>`2`: Shuffle enabled, Repeat enabled - loop<br>`3`: Shuffle enabled, Repeat disabled<br>`4`: Shuffle disabled, Repeat disabled<br>`5`: Shuffle enabled, Repeat enabled - loop once<br>

## Control The Playback 

> Request format 

```html
GET /httpapi.asp?command=setPlayerCmd:pause
GET /httpapi.asp?command=setPlayerCmd:resume
GET /httpapi.asp?command=setPlayerCmd:onepause
GET /httpapi.asp?command=setPlayerCmd:stop
GET /httpapi.asp?command=setPlayerCmd:prev
GET /httpapi.asp?command=setPlayerCmd:next
```

> Example response:

```plaintext
OK
```

Control the current playback 

Command: `setPlayerCmd:<control>`

Parameter | Description
---|---
`pause` | Pause playback
`resume` | Resume playback
`onepause` | Toggle Play/Pause
`stop` | Stop current playback and removes slected source from device
`prev` | Play previous song in playlist
`next` | Play next song in playlist
`pause` | Pause current playback
`resume` | Resume playback from last position, if it is paused

## Seeking

> Request format:

```html
GET /httpapi.asp?command=setPlayerCmd:seek:<position>
```

> Example response:

```plaintext
OK
```

Seek with seconds for current playback, have no use when playing radio link.

Command: `setPlayerCmd:seek:<position>`

Parameter | Description
---|---
`position` | Position to seek to in seconds

## Adjusting Volume

> Request format:

```html
GET /httpapi.asp?command=setPlayerCmd:vol:<volume>
```

> Example response:

```plaintext
OK
```

Set system volume

Command: `setPlayerCmd:vol:<volume>`

Parameter | Description
---|---
`volume` | Adjusts the volume of the current device.<br>Value range is from `0-100`.

## Mute and Unmute 

> Request format:

```html
GET /httpapi.asp?command=setPlayerCmd:mute:<mute>
```

> Example response:

```plaintext
OK
```

Toggle mute for the device

Command: `setPlayerCmd:mute:<mute>`

Parameter | Description
---|---
`mute` | Set the mute mode<br>`0`: Not muted<br>`1`: Muted

