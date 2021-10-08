## Request a list of Guest Devices in a Multiroom Group
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

> Example response when there are no Guest Devices connected e.g. This Device is in standalone mode:

```json
{
   "slaves": 0,
   "wmrm_version": "4.2"
}
```

Sub-Command: `getSlaveList`

This sub-command requests a list of Guest Devices in the Multiroom Group.  A `JSON` table with information about the Guest Devices is returned.

### Response Description (JSON Table)

Key | Value-Description
---|---
`slaves` | The number of Guest Devices connected to this Host Device. Numeric value.
`wmrm_version` | *!! DOCUMENTATION IN PROGRESS  Windows Media Rights Management ? !!*
`slave_list` | Identifier for the array of Guest Devices.

Guest Device Information

Key | Value-Description
---|---
`name` | The name of the Guest Device
`uuid` | UUI of the Guest Device
`ip` | Guest Device's IP address
`version` | *!! DOCUMENTATION IN PROGRESS !!*
`type` | Audio Module type  <br>`WiiMu-A31`: LinkPlay A31 (used for A50, PRO, MINI, S50+ AMP)
`channel` | Active audio channel<br>`0`: Stereo<br>`1`: Left channel<br>`2`: Right channel
`volume` | Current volume.<br>Value range is from `0 - 100`.<br>So can be considered a linear percentage (0% to 100%)
`mute` | Mute status:<br>`0`: Guest Device is unmuted<br>`1`: Guest Device is muted
`battery_percent` | Battery level (if battery is present).<br>Value ranges from `0 - 100`.<br>So can be considered a linear percentage (0% to 100%) 
`battery_charging` | Flag that indicates whether the battery is currently charging or not.<br>`0`: Battery not charging<br>`1`: Battery is charging
