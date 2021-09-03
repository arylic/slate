### Current Device - Play status

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
`mode` | Playback mode<br>`0` - `PLAYER_MODE_NONE`<br>`1` - `PLAYER_MODE_AIRPLAY`<br>`2` - `PLAYER_MODE_DLNA`<br>`10` - `PLAYER_MODE_WIIMU` e.g. vTuner, Home Media Share, Amazon Music, Deezer<br>`11` - `PLAYER_MODE_WIIMU_LOCAL` e.g. UDISK(Local USB disk on Arylic Device)<br>`12` - `PLAYER_MODE_WIIMU_STATION`<br>`13` - `PLAYER_MODE_WIIMU_RADIO`<br>`14` - `PLAYER_MODE_WIIMU_SONGLIST`<br>`19` - `PLAYER_MODE_WIIMU_MAX`<br>`20` - `PLAYER_MODE_HTTP`<br>`21` - `PLAYER_MODE_HTTP_LOCAL`<br>`29` - `PLAYER_MODE_HTTP_MAX`<br>`30` - `PLAYER_MODE_ALARM`<br>`31` - `PLAYER_MODE_SPOTIFY`<br>`40` - `PLAYER_MODE_LINEIN`<br>`41` - `PLAYER_MODE_BT`<br>`42` - `PLAYER_MODE_EXT_LOCAL`<br>`43` - `PLAYER_MODE_OPTICAL`<br>`49` - `PLAYER_MODE_LINEIN_MAX`<br>`50` - `PLAYER_MODE_MIRROR`<br>`60` - `PLAYER_MODE_TALK`<br>`99` - `PLAYER_MODE_CHILD` The Device is a Guest in a Multiroom Zone<br><br><aside class="warning">@Arylic: Documentation is MISSING! Please review and give feedback.</aside>
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









