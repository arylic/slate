## Current Player status

Command: `getPlayerStatus`

> Request format:

```html
GET /httpapi.asp?command=getPlayerStatus
```

> Example response:

```json
{
	"Album": "556E6B6E6F776E",
	"Artist": "556E6B6E6F776E",
	"Title": "556E6B6E6F776E",
	"alarmflag": "0",
	"ch": "0",
	"curpos": "89872",
	"eq": "0",
	"loop": "3",
	"mode": "31",
	"mute": "0",
	"offset_pts": "4843754",
	"plicount": "0",
	"plicurr": "0",
	"status": "play",
	"totlen": "219806",
	"type": "0",
	"vol": "16"
}
```

### Description of response values

Key | Value Description
---|---
`Album` | `[hexed string]` of the album
`Artist` | `[hexed string]` of the artist
`Title` | `[hexed string]` of the track title
`alarmflag` | *!! Documentation is MISSING !!*
`ch` | Active channel(s)<br>`0`: Stereo<br>`1`: Left<br>`2`: Right
`curpos` | Current playing position (in ms)
`eq` | The current Equalizer setting
`loop` | Loop mode<br>`0`: Sequence, no loop<br>`1`: Single loop<br>`2`: Shuffle all<br>`3`:loop all
`mode` | Playback mode<br>`0` - `PLAYER_MODE_NONE`<br>`1` - `PLAYER_MODE_AIRPLAY`<br>`2` - `PLAYER_MODE_DLNA`<br>`10` - `PLAYER_MODE_WIIMU`<br>`11` - `PLAYER_MODE_WIIMU_LOCAL`<br>`12` - `PLAYER_MODE_WIIMU_STATION`<br>`13` - `PLAYER_MODE_WIIMU_RADIO`<br>`14` - `PLAYER_MODE_WIIMU_SONGLIST`<br>`19` - `PLAYER_MODE_WIIMU_MAX`<br>`20` - `PLAYER_MODE_HTTP`<br>`21` - `PLAYER_MODE_HTTP_LOCAL`<br>`29` - `PLAYER_MODE_HTTP_MAX`<br>`30` - `PLAYER_MODE_ALARM`<br>`40` - `PLAYER_MODE_LINEIN`<br>`41` - `PLAYER_MODE_BT`<br>`42` - `PLAYER_MODE_EXT_LOCAL`<br>`43` - `PLAYER_MODE_OPTICAL`<br>`49` - `PLAYER_MODE_LINEIN_MAX`<br>`50` - `PLAYER_MODE_MIRROR`<br>`60` - `PLAYER_MODE_TALK`<br>`99` - `PLAYER_MODE_CHILD`<br><br><aside class="warning">@Arylic: Documentation is MISSING! Please review and give feedback.</aside>
`mute` | The mute status<br>`0`: Not muted<br>`1`: Muted
`offset_pts` | *!! DOCUMENTATION IS MISSING !!*
`plicount` | The total number of tracks in the playlist
`plicurr` | Index of current track in playlist
`status` | Player status<br>`0`: stop<br>`1`: play<br>`2`: load<br>`3`: pause<br><br>**NOTE: This documentation describes number values for the key. However, the example response from my device returns the text representations instead!**
`totlen` | Current track length (in ms)
`type` | `0`: Main or standalone device<br>`1`: Child
`vol` | Current volume<br>Value ranges from `0 - 100`<br>`0` means off


