## Get Device Metadata

Retrieves detailed informations about a connected device.

Command: `getStatusEx`

> Request format:

```html
GET /httpapi.asp?command=getStatusEx
```

> Example response:

```json
{
	"BSSID": "B4:FB:E4:F4:73:81",
	"CountryCode": "CN",
	"CountryRegion": "1",
	"DeviceName": "Büro",
	"GroupName": "Büro",
	"MAC": "00:22:6C:2D:16:89",
	"NewVer": "0",
	"RSSI": "-76",
	"Release": "20210624",
	"SSIDStrategy": "2",
	"STA_MAC": "00:22:6C:2D:16:8B",
	"VersionUpdate": "0",
	"WifiChannel": "11",
	"apcli0": "10.213.69.116",
	"auth": "WPAPSKWPA2PSK",
	"battery": "0",
	"battery_percent": "0",
	"branch": "A31_stable_4.6",
	"build": "release",
	"cap1": "0x305200",
	"capability": "0x28e90b80",
	"communication_port": "8819",
	"date": "2021:07:23",
	"dsp_ver": "0",
	"dsp_ver_new": "0",
	"dst_enable": "1",
	"encry": "AES",
	"essid": "57696E6B656C6761737365",
	"eth2": "",
	"eth_dhcp": "1",
	"external": "0x0",
	"firmware": "4.6.9724",
	"group": "0",
	"hardware": "A31",
	"hideSSID": "1",
	"ignore_silenceOTATime": "1",
	"ignore_talkstart": "0",
	"iheartradio_new": "1",
	"internet": "1",
	"iot_ver": "1.0.0",
	"language": "en_us",
	"languages": "0x6",
	"lbc_support": "0",
	"mcu_ver": "26",
	"mcu_ver_new": "0",
	"netstat": "2",
	"new_iheart_podcast": "1",
	"new_tunein_preset_and_alarm": "1",
	"plm_support": "0x6",
	"preset_key": "10",
	"priv_prj": "UP2STREAM_AMP_V4",
	"privacy_mode": "0",
	"project": "UP2STREAM_AMP_V4",
	"project_build_name": "a31rakoit",
	"prompt_status": "1",
	"ra0": "10.10.10.254",
	"region": "unknown",
	"securemode": "1",
	"security": "https/2.0",
	"security_version": "2.0",
	"service_version": "1.0",
	"silenceOTATime": "",
	"spotify_active": "0",
	"ssid": "SoundSystem_1689",
	"streams": "0x7b9831fe",
	"streams_all": "0x7bff7ffe",
	"temp_uuid": "F4F82885209537F1",
	"tidal_version": "2.0",
	"time": "13:56:44",
	"tz": "1.0000",
	"uart_pass_port": "8899",
	"upnp_uuid": "uuid:FF31F09E-501F-2B00-89EE-7709FF31F09E",
	"upnp_version": "1005",
	"uuid": "FF31F09E501F2B0089EE7709",
	"web_firmware_update_hide": "0",
	"wmrm_version": "4.2"
}
```

### Description of response values

Key | Value Description
-+-
`BSSID` | *!! DOCUMENTATION IS MISSING !!*
`CountryCode` | *!! DOCUMENTATION IS MISSING !!*
`CountryRegion` | *!! DOCUMENTATION IS MISSING !!*
`DeviceName` | The device UPnP and Airplay friendly name
`GroupName` | You can guess what it means, but:<br>*!! DOCUMENTATION IS MISSING !!*
`MAC` | MAC address of the device
`NewVer` | If there is a new firmware available (in case of `VersionUpdate` is set to `1`), this is the new version number
`RSSI` | [RSSI Level](https://en.wikipedia.org/wiki/Received_signal_strength_indication) of used WiFi<br>Value ranges from `0 - 100`. `100` means best signal strength.
`Release` | Firmware build date<br>Format: `YYYYMMDD`
`SSIDStrategy` | *!! DOCUMENTATION IS MISSING !!*
`STA_MAC` | *!! DOCUMENTATION IS MISSING !!*
`VersionUpdate` | Flag that determines, if there is a new firmware version available or not.<br>`0`: no new firmware<br>`1`: new firmware available
`WifiChannel` | The current connected WiFi channel
`apcli0` | Device's IP address over WiFi
`auth` | *!! DOCUMENTATION IS MISSING !!*
`battery` | `0`: battery is not charging<br>`1`: battery is charging
`battery_percent` | Battery charge level (`0 - 100`)
`branch` | *!! DOCUMENTATION IS MISSING !!*
`build` | Possible values: `release`, `debug`, `backup`<br>`release`: this is a release version<br>`debug`: this is a debug version<br>`backup`: this is a backup version
`cap1` | *!! DOCUMENTATION IS MISSING !!*
`capability` | This is a bit mask:<br>`0`: has airplay support<br>`1`: has ethernet support<br>`2`: has USB disk support<br>`3`: has WPS button support<br>`4`: has battery support<br>`5`: has preset key support<br>`6`: has I2S in support
`communication_port` | *!! DOCUMENTATION IS MISSING !!*
`date` | *!! DOCUMENTATION IS MISSING !!*
`dsp_ver` | *!! DOCUMENTATION IS MISSING !!*
`dsp_ver_new` | *!! DOCUMENTATION IS MISSING !!*
`dst_enable` | *!! DOCUMENTATION IS MISSING !!*
`encry` | *!! DOCUMENTATION IS MISSING !!*
`essid` | SSID of the WiFi the device is connected to<br>`[hexed string]`
`eth2` | Device's IP address when it's connected to ethernet
`eth_dhcp` | *!! DOCUMENTATION IS MISSING !!*
`external` | hexadecimal value<br>*!! DOCUMENTATION IS MISSING !!*
`firmware` | Current firmware version
`group` | *!! DOCUMENTATION IS MISSING !!*
`hardware` | Hardware model
`hideSSID` | When the device is operating as a WiFi hotspot, this flag determines whether its SSID should be hidden or visible<br>`0` - `ssid` is visible<br>`1` - `ssid` is hidden
`ignore_silenceOTATime` | *!! DOCUMENTATION IS MISSING !!*
`ignore_talkstart` | *!! DOCUMENTATION IS MISSING !!*
`iheartradio_new` | *!! DOCUMENTATION IS MISSING !!*
`internet` | Curremt status of internet access:<br>`0`: not ready<br>`1`: ready
`iot_ver` | *!! DOCUMENTATION IS MISSING !!*
`language` | The language
`languages` | *!! DOCUMENTATION IS MISSING !!*
`lbc_support` | *!! DOCUMENTATION IS MISSING !!*
`mcu_ver` | *!! DOCUMENTATION IS MISSING !!*<br>But I guess: Version of MCU
`mcu_ver_new` | *!! DOCUMENTATION IS MISSING !!*<br>But I guess:<br>Flag that indicates, if there is a newer version of MCU available<br>`0` - No new version<br>`1` - New version available
`netstat` | WiFi connect state:<br>`0`: no connection<br>`1`: connecting<br>`2`: connected
`new_iheart_podcast` | *!! DOCUMENTATION IS MISSING !!*
`new_tunein_preset_and_alarm` | *!! DOCUMENTATION IS MISSING !!*
`plm_support` | This is a bit mask:<br>`0`: LineIn (Aux support)<br>`1`: Bluetooth support<br>`2`: Optical support
`preset_key` | Presets key number. But in detail:<br>*!! DOCUMENTATION IS MISSING !!*
`priv_prj` | *!! DOCUMENTATION IS MISSING !!*
`privacy_mode` | *!! DOCUMENTATION IS MISSING !!*
`project` | The project name
`project_build_name` | *!! DOCUMENTATION IS MISSING !!*
`prompt_status` | It seems to relate to the commands `PromptEnable` and `PromptDisable`, but:<br>*!! DOCUMENTATION IS MISSING !!*
`ra0` | WiFi AP IP address, normally it is `10.10.10.254`
`region` | *!! DOCUMENTATION IS MISSING !!*
`securemode` | *!! DOCUMENTATION IS MISSING !!*
`security` | *!! DOCUMENTATION IS MISSING !!*
`security_version` | *!! DOCUMENTATION IS MISSING !!*
`service_version` | *!! DOCUMENTATION IS MISSING !!*
`silenceOTATime` | *!! DOCUMENTATION IS MISSING !!*
`spotify_active` | *!! DOCUMENTATION IS MISSING !!*<br>But I guess:<br>Flag that indicates if Spotify is currently playing on the device (via Spotify Connect?)<br>`0` - Spotify is not playing<br>`1` - Spotify is playing
`ssid` | Device's own `SSID` when in WiFi pairing mode or when device's WiFi hotspot is active
`streams` | This is a bit mask:<br>`0`: If Airplay is enabled<br>`1`: If DLNA is enabled<br>`2`: Has TTPod support<br>`3`: Has TuneIn support<br>`4`: Has Pandora support<br>`5`: Has DoubanFM support<br>!! DOCUMENTATION IS MISSING !!*
`streams_all` | *!! DOCUMENTATION IS MISSING !!*
`temp_uuid` | Temporary UUID (will change after device reboot)
`tidal_version` | *!! DOCUMENTATION IS MISSING !!*
`time` | *!! DOCUMENTATION IS MISSING !!*
`tz` | *!! DOCUMENTATION IS MISSING !!*
`uart_pass_port` | *!! DOCUMENTATION IS MISSING !!*
`upnp_uuid` | The UPnP UUID
`upnp_version` | *!! DOCUMENTATION IS MISSING !!*
`usb_freesize` | USB disk available free space
`usb_storagesize` | USB disk storage size
`uuid` | Device permanent UUID (will remain after device reboot)
`web_firmware_update_hide` | *!! DOCUMENTATION IS MISSING !!*
`wmrm_version` | *!! DOCUMENTATION IS MISSING !!*

<aside class="warning">
There are <strong>LOTS</strong> of keys in the example response which don't have any description yet!
</aside>
