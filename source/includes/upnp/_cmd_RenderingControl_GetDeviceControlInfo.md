## RenderingControl.GetDeviceControlInfo

```html
GET Onit 
```

> Example response:

```json
{ 
	"uuid": "FF31F09E1A5020113B0A3918", 
	"DeviceName": "PRO", 
	"GroupName": "PRO", 
	"ssid": "PRO_D4AD", 
	"language": "en_us", 
	"firmware": "4.6.328252", 
	"hardware": "A31", 
	"build": "release", 
	"project": "UP2STREAM_PRO_V3", 
	"priv_prj": "UP2STREAM_PRO_V3", 
	"project_build_name": "a31rakoit", 
	"Release": "20210903", 
	"temp_uuid": "A7A50887ACBC9B36", 
	"hideSSID": "1", 
	"SSIDStrategy": "2", 
	"branch": "A31_stable_4.6", 
	"group": "0", 
	"wmrm_version": "4.2", 
	"internet": "1", 
	"MAC": "00:22:6C:33:D4:AD", 
	"STA_MAC": "00:00:00:00:00:00", 
	"CountryCode": "CN", 
	"CountryRegion": "1", 
	"netstat": "0", 
	"essid": "", 
	"apcli0": "", 
	"eth2": "192.168.167.74", 
	"ra0": "10.10.10.254", 
	"eth_dhcp": "0",
	"eth_static_ip": "192.168.167.74", 
	"eth_static_mask": "255.255.255.0", 
	"eth_static_gateway": "192.168.167.1", 
	"eth_static_dns1": "194.168.4.100", 
	"eth_static_dns2": "194.168.8.100",
	"VersionUpdate": "0", 
	"NewVer": "0", 
	"mcu_ver": "28", 
	"mcu_ver_new": "0", 
	"dsp_ver": "", 
	"dsp_ver_new": "0", 
	"date": "2021:09:27", 
	"time": "13:25:17", 
	"tz": "0.0000", 
	"dst_enable": "1", 
	"region": "unknown", 
	"prompt_status": "1", 
	"iot_ver": "1.0.0", 
	"upnp_version": "1005", 
	"cap1": "0x305200", 
	"capability": "0x28e90b80", 
	"languages": "0x6", 
	"streams_all": "0x7bff7ffe", 
	"streams": "0x7b9831fe", 
	"external": "0x0", 
	"plm_support": "0x6", 
	"preset_key": "10", 
	"spotify_active": "1", 
	"lbc_support": "0", 
	"privacy_mode": "0", 
	"WifiChannel": "11", 
	"RSSI": "0", 
	"BSSID": "", 
	"battery": "0", 
	"battery_percent": "0", 
	"securemode": "1", 
	"auth": "WPAPSKWPA2PSK", 
	"encry": "AES", 
	"upnp_uuid": "uuid:FF31F09E-1A50-2011-3B0A-3918FF31F09E", 
	"uart_pass_port": "8899", 
	"communication_port": "8819", 
	"web_firmware_update_hide": "0", 
	"ignore_talkstart": "0", 
	"web_login_result": "-1", 
	"silenceOTATime": "", 
	"ignore_silenceOTATime": "1", 
	"new_tunein_preset_and_alarm": "1", 
	"iheartradio_new": "1", 
	"new_iheart_podcast": "1", 
	"tidal_version": "2.0", 
	"service_version": "1.0", 
	"security": "https\/2.0", 
	"security_version": "2.0" 
}
```

Retrieves detailed informations about a connected device.

Command: `getStatusEx`

### Description of response values

Key | Value Description
---|---
`uuid` | Device permanent UUID (will remain after device reboot)
`DeviceName` | The device UPnP and Airplay friendly name
`GroupName` | You can guess what it means, but:<br>*!! DOCUMENTATION IN PROGRESS !!*
`ssid` | Device's own `SSID` when in WiFi pairing mode or when device's WiFi hotspot is active
`language` | The language
`firmware` | Current firmware version
`hardware` | Hardware model
`build` | Possible values: `release`, `debug`, `backup`<br>`release`: this is a release version<br>`debug`: this is a debug version<br>`backup`: this is a backup version
`project` | The project name
`priv_prj` | *!! DOCUMENTATION IN PROGRESS !!*
`project_build_name` | *!! DOCUMENTATION IN PROGRESS !!*
`Release` | Firmware build date<br>Format: `YYYYMMDD`
`temp_uuid` | Temporary UUID (will change after device reboot)
`hideSSID` | When the device is operating as a WiFi hotspot, this flag determines whether its SSID should be hidden or visible<br>`0`: `ssid` is visible<br>`1`: `ssid` is hidden
`SSIDStrategy` | *!! DOCUMENTATION IN PROGRESS !!*
`branch` | *!! DOCUMENTATION IN PROGRESS !!*
`group` | *!! DOCUMENTATION IN PROGRESS !!*
`wmrm_version` | *!! DOCUMENTATION IN PROGRESS !!*
`internet` | Current status of internet access:<br>`0`: not ready<br>`1`: ready
`MAC` | MAC address of the active network connection 
`STA_MAC` | MAC address of the `STA` = STATION 
`CountryCode` | *!! DOCUMENTATION IN PROGRESS !!*
`CountryRegion` | *!! DOCUMENTATION IN PROGRESS !!*
`netstat` | WiFi connect state:<br>`0`: no connection<br>`1`: connecting<br>`2`: connected
`essid` | SSID of the WiFi the device is connected to<br>`[hexed string]`
`apcli0` | Device's IP address over WiFi
`eth2` | Device's IP address when it's connected to ethernet
`ra0` | WiFi AP IP address, normally it is `10.10.10.254`
`eth_dhcp` | Flag for DHCP or Static IP Address <br>`0`: Static IP<br>`1`: IP Address provided by LAN/WLAN DHCP Server
`eth_static_ip` | Device's Static IP address (If `eth_dhcp=0`) 
`eth_static_mask` | Device's Network Mask (If `eth_dhcp=0`)
`eth_static_gateway` | Device's IP Gateway (If `eth_dhcp=0`)
`eth_static_dns1` | Device's Primary DNS Server (If `eth_dhcp=0`)
`eth_static_dns2` | Device's Secondary DNS Server (If `eth_dhcp=0`)
`VersionUpdate` | Flag that determines, if there is a new firmware version available or not.<br>`0`: no new firmware<br>`1`: new firmware available
`NewVer` | If there is a new firmware available (in case of `VersionUpdate` is set to `1`), this is the new version number
`mcu_ver` | *!! DOCUMENTATION IN PROGRESS !!*<br>But I guess: Version of MCU
`mcu_ver_new` | *!! DOCUMENTATION IN PROGRESS !!*<br>But I guess:<br>Flag that indicates, if there is a newer version of MCU available<br>`0`: No<br>`1`: Yes
`dsp_ver` | *!! DOCUMENTATION IN PROGRESS !!*
`dsp_ver_new` | *!! DOCUMENTATION IN PROGRESS !!*
`date` | Current Date
`time` | Current Time
`tz` | *!! DOCUMENTATION IN PROGRESS !!*
`dst_enable` | *!! DOCUMENTATION IN PROGRESS !!*
`region` | *!! DOCUMENTATION IN PROGRESS !!*
`prompt_status` | It seems to relate to the commands `PromptEnable` and 
`iot_ver` | *!! DOCUMENTATION IN PROGRESS !!*
`upnp_version` | UPnP Device Architecture Version
`cap1` | *!! DOCUMENTATION IN PROGRESS !!*
`capability` | This is a bit mask:<br>`0`: has airplay support<br>`1`: has ethernet support<br>`2`: has USB disk support<br>`3`: has WPS button support<br>`4`: has battery support<br>`5`: has preset key support<br>`6`: has I2S in support
`languages` | *!! DOCUMENTATION IN PROGRESS !!*
`streams_all` | *!! DOCUMENTATION IN PROGRESS !!*
`streams` | This is a bit mask:<br>`0`: If Airplay is enabled<br>`1`: If DLNA is enabled<br>`2`: Has TTPod support<br>`3`: Has TuneIn support<br>`4`: Has Pandora support<br>`5`: Has DoubanFM support<br>!! DOCUMENTATION IN PROGRESS !!*
`external` | hexadecimal value<br>*!! DOCUMENTATION IN PROGRESS !!*
`plm_support` | This is a bit mask:<br>`0`: LineIn (Aux support)<br>`1`: Bluetooth support<br>`2`: Optical support 
`preset_key` | Quantity of presets available:<br>
`spotify_active` | *!! DOCUMENTATION IN PROGRESS !!*<br>But I guess:<br>Flag that indicates if Spotify is currently playing on the device (via Spotify Connect?)<br>`0`: Spotify is not playing<br>`1`: Spotify is playing
`lbc_support` | *!! DOCUMENTATION IN PROGRESS !!*
`privacy_mode` | *!! DOCUMENTATION IN PROGRESS !!*
`WifiChannel` | The current connected WiFi channel
`RSSI` | [RSSI Level](https://en.wikipedia.org/wiki/Received_signal_strength_indication) of used WiFi<br>Value ranges from `0 - 100`. `100` means best signal strength.
`BSSID` | The Basic Service Set Identifiers : In most cases this will be the MAC Address of the Wireless Acces Point Used (e.g. Router)
`battery` | `0`: battery is not charging<br>`1`: battery is charging
`battery_percent` | Battery charge level<br>Value ranges from `0 - 100`
`securemode` | *!! DOCUMENTATION IN PROGRESS !!*
`auth` | Type of WiFi Protected Access used (Authentication Key). 
`encry` | Type of WiFi Protected Access used (Encryption Protocol).
`upnp_uuid` | The UPnP UUID
`uart_pass_port` | Port used for TCP/IP Communcations/Socket Connections
`communication_port` | *!! DOCUMENTATION IN PROGRESS !!*
`web_firmware_update_hide` | *!! DOCUMENTATION IN PROGRESS !!*
`ignore_talkstart` | *!! DOCUMENTATION IN PROGRESS !!*
`silenceOTATime` | *!! DOCUMENTATION IN PROGRESS !!*
`ignore_silenceOTATime` | *!! DOCUMENTATION IN PROGRESS !!*
`new_tunein_preset_and_alarm` | *!! DOCUMENTATION IN PROGRESS !!*
`iheartradio_new` | *!! DOCUMENTATION IN PROGRESS !!*
`new_iheart_podcast` | *!! DOCUMENTATION IN PROGRESS !!*
`tidal_version` | *!! DOCUMENTATION IN PROGRESS !!*
`service_version` | *!! DOCUMENTATION IN PROGRESS !!*
`security` | *!! DOCUMENTATION IN PROGRESS !!*
`security_version` | *!! DOCUMENTATION IN PROGRESS !!*

<aside class="warning">
There are <strong>LOTS</strong> of keys in the example response which don't have any description yet!
</aside>
