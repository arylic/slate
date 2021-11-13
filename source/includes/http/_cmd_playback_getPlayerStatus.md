## Playback Status

Command: `getPlayerStatus`

> Request format:

```html
GET /httpapi.asp?command=getPlayerStatus
```

> Example response:

```json

{
	"type":"0",
	"ch":"0",
	"mode":"10",
	"loop":"3",
	"eq":"0",
	"status":"play",
	"curpos":"11",
	"offset_pts":"11",
	"totlen":"170653",
	"Title":"596F752661706F733B766520476F7420746865204C6F7665205B2A5D",
	"Artist":"466C6F72656E636520616E6420746865204D616368696E65",
	"Album":"4C756E6773205B31362F34345D",
	"alarmflag":"0",
	"plicount":"11",
	"plicurr":"9",
	"vol":"47",
	"mute":"0
}

```

### Description of response values

Key | Value Description
---|---
`type` | `0`: Main or standalone device<br>`1`: Device is a Multiroom Guest 
`ch` | Active channel(s)<br>`0`: Stereo<br>`1`: Left<br>`2`: Right
`mode` | Playback mode<br>`0`: Idling <br>`1`: airplay streaming<br>`2`: DLNA streaming<br>`10`: Playing network content, e.g. vTuner, Home Media Share, Amazon Music, Deezer, etc.<br>`11`: playing UDISK(Local USB disk on Arylic Device)<br>`20`: playback start by HTTPAPI<br>`31`: Spotify Connect streaming<br>`40`: Line-In input mode<br>`41`: Bluetooth input mode<br>`43`: Optical input mode<br>`47`: Line-In #2 input mode<br>`51`: USBDAC input mode<br>`99`: The Device is a Guest in a Multiroom Zone<br>
`loop` | Is a Combination of `SHUFFLE` and `REPEAT` modes<br>`0`: `SHUFFLE:` disabled  `REPEAT:` enabled - loop<br>`1`: `SHUFFLE:` disabled  `REPEAT:` enabled - loop once<br>`2`: `SHUFFLE:` enabled  `REPEAT:` enabled - loop<br>`3`: `SHUFFLE:` enabled  `REPEAT:` disabled<br>`4`: `SHUFFLE:` disabled `REPEAT:` disabled<br>`5`: `SHUFFLE:` enabled  `REPEAT:` enabled - loop once<br>   
`eq` | The current Equalizer setting
`status` | Device status<br>`stop`: no audio selected<br>`play`: playing audio<br>`load`: load **??**<br>`pause`: audio paused
`curpos` | Current playing position (in ms)
`offset_pts` | *!! DOCUMENTATION IN PROGRESS !!*
`totlen` | Current track length (in ms)
`Title` | `[hexed string]` of the track title
`Artist` | `[hexed string]` of the artist
`Album` | `[hexed string]` of the album
`alarmflag` | *!! DOCUMENTATION IN PROGRESS !!*
`plicount` | The total number of tracks in the playlist
`plicurr` | Index of current track in playlist
`vol` | Current volume<br>Value range is from `0 - 100`. So can be considered a linear percentage (`0% to 100%`)
`mute` | The mute status<br>`0`: Not muted<br>`1`: Muted









