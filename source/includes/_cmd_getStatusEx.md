# API Command Overview
## Device Informations

Retrieves informations about a device.

Command: `getStatusEx`

> Request format:

```html
GET /httpapi.asp?command=getStatusEx
```

> Example response:

```json
{
   "uuid": "FF31F09E501F2B0089EE7709",
   "DeviceName": "Büro",
   "GroupName": "Büro",
   "ssid": "SoundSystem_1689",
   "language": "en_us",
   "firmware": "4.6.9724",
   "hardware": "A31",
   "build": "release",
   "project": "UP2STREAM_AMP_V4",
   "priv_prj": "UP2STREAM_AMP_V4",
   "project_build_name": "a31rakoit",
   "Release": "20210624",
   "temp_uuid": "F4F82885209537F1",
   "hideSSID": "1",
   "SSIDStrategy": "2",
   "branch": "A31_stable_4.6",
   "group": "0",
   "wmrm_version": "4.2",
   "internet": "1",
   "MAC": "00:22:6C:2D:16:89",
   "STA_MAC": "00:22:6C:2D:16:8B",
   "CountryCode": "CN",
   "CountryRegion": "1",
   "netstat": "2",
   "essid": "57696E6B656C6761737365",
   "apcli0": "10.213.69.116",
   "eth2": "",
   "ra0": "10.10.10.254",
   "eth_dhcp": "1",
   "VersionUpdate": "0",
   "NewVer": "0",
   "mcu_ver": "26",
   "mcu_ver_new": "0",
   "dsp_ver": "0",
   "dsp_ver_new": "0",
   "date": "2021:07:23",
   "time": "13:56:44",
   "tz": "1.0000",
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
   "spotify_active": "0",
   "lbc_support": "0",
   "privacy_mode": "0",
   "WifiChannel": "11",
   "RSSI": "-76",
   "BSSID": "B4:FB:E4:F4:73:81",
   "battery": "0",
   "battery_percent": "0",
   "securemode": "1",
   "auth": "WPAPSKWPA2PSK",
   "encry": "AES",
   "upnp_uuid": "uuid:FF31F09E-501F-2B00-89EE-7709FF31F09E",
   "uart_pass_port": "8899",
   "communication_port": "8819",
   "web_firmware_update_hide": "0",
   "ignore_talkstart": "0",
   "silenceOTATime": "",
   "ignore_silenceOTATime": "1",
   "new_tunein_preset_and_alarm": "1",
   "iheartradio_new": "1",
   "new_iheart_podcast": "1",
   "tidal_version": "2.0",
   "service_version": "1.0",
   "security": "https/2.0",
   "security_version": "2.0"
}
```

### Description of response values

Key | Value Description
-+-
`language` | The language
`ssid` | Device's own `SSID` when in WiFi pairing mode
`firmware` | Current firmware version
`build` | Possible values: `release`, `debug`, `backup`<br>`release`: this is a release version<br>`debug`: this is a debug version<br>`backup`: this is a backup version
`Release` | Firmware build date<br>Format: `YYYYMMDD`
`group` | *!! Documentation is MISSING !!*
`expired` | `1` means the firmware has expired<br>*This key isn't found in the current example response. Unsure if it's still in use.*
`internet` | Internet access:<br>`0`: not ready<br>`1`: ready
`uuid` | Device permanent UUID (will remain after device reboot)
`netstat` | WiFi connect state:<br>`0`: no connection<br>`1`: connecting<br>`2`: connected<br>
`essid` | SSID of the WiFi the device is connected to<br>`[hexed string]`
`apcli0` | Device's IP address over WiFi
`ra0` | WiFi AP IP address, normally it is `10.10.10.254`
`eth2` | Device's IP address when it's connected to ethernet
`hardware` | Hardware model
`project` | The project name
`VersionUpdate` | Flag that determines, if there is a new firmware version available or not.<br>`0`: no new firmware<br>`1`: new firmware available
`NewVer` | If there is a new firmware available (in case of `VersionUpdate` is set to `1`), this is the new version number
`DeviceName` | The device UPnP and Airplay friendly name
`temp_uuid` | Temporary UUID (will change after device reboot)
`capability` | This is a bit mask:<br>`0`: has airplay support<br>`1`: has ethernet support<br>`2`: has USB disk support<br>`3`: has WPS button support<br>`4`: has battery support<br>`5`: has preset key support<br>`6`: has I2S in support
`streams` | This is a bit mask:<br>`0`: if airplay is enabled<br>`1`: if DLNA is enabled<br>`2`: has TTPod support<br>`3`: has TuneIn support<br>`4`: has Pandora support<br>`5`: has DoubanFM support
`external` | hexadecimal value<br>*!! Documentation is MISSING !!*
`preset_key` | presets key number
`plm_support` | This is a bit mask:<br>`0`: LineIn (Aux support)<br>`1`: Bluetooth support<br>`2`: Optical support
`WifiChannel` | The current connected WiFi channel
`AP_clients` | AP client number
`RSSI` | RSSI Level of used WiFi<br>Value ranges from `0 - 100`. `100` means best signal strength.
`TxQuality` | Tx quality<br>*This key isn't found in the current example response. Unsure if it's still in use.*
`RxQuality` | Rx quality<br>*This key isn't found in the current example response. Unsure if it's still in use.*
`battery` | `0`: battery is not charging<br>`1`: battery is charging
`battery_percent` | Battery charge level (`0 - 100`)
`securemode` | WiFi secure or not
`psk` | If WiFi is in secure, the password<br>*This key isn't found in the current example response. Unsure if it's still in use.*
`usb_storagesize` | USB disk storage size
`usb_freesize` | USB disk available free space
`part1_storage` | User1 part in ROM, storage size
`part1_free` | User1 part in ROM, free size
`part2_storage` | User2 part in ROM, storage size
`part2_free` | User2 part in ROM, free size

<aside class="warning">
There are <strong>LOTS</strong> of keys in the example response which don't have any description yet!
</aside>
