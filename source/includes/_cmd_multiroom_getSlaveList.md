## Get a list of child players

Sub-Command: `getSlaveList`

> Request format:

```html
GET /httpapi.asp?command=multiroom:getSlaveList
```

> Example response:

```json
{
   "slaves": 1,
   "wmrm_version": "4.2",
   "slave_list": [
      {
			"name": "Wohnzimmer",
			"uuid": "FF31F09EFFF1D2BB4FDE2B3F",
			"ip": "10.213.69.106",
			"version": "4.2",
			"type": "WiiMu-A31",
			"channel": 0,
			"volume": 63,
			"mute": 0,
			"battery_percent": 0,
			"battery_charging": 0
		}
   ]
}
```

> Example response when there are no child players where found:

```json
{
   "slaves": 0,
   "wmrm_version": "4.2"
}
```

### Response Description

Key | Value-Description
---|---
`slaves` | The number of child players to this player. Numeric value.
`wmrm_version` | *!! Documentation is MISSING !!*
`slave_list` | Key to get the array of child players.

Child Player Item

Key | Value-Description
---|---
`name` | The name of the player
`uuid` | UUI of the player
`ip` | Player's IP address
`version` | *!! Documentation is MISSING !!*
`type` | Board type (I guess)<br>*!! Documentation is MISSING !!*
`channel` | Active audio channel<br>`0` - Stereo<br>`1` - Left channel<br>`2` - Right channel
`volume` | Current volume. Value ranges from `0 - 100`
`mute` | Mute status:<br>`0` - Device is unmuted<br>`1` - Device is muted
`battery_percent` | Battery level (if battery is present). Value ranges from `0 - 100`
`battery_charging` | Flag that indicates whether the battery is currently charging or not.<br>`0` - Battery not charging<br>`1` - Battery is charging
