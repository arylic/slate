# UART API

Welcome to Arylic's UART API developer documentation. 

These messages are mainly defined to get current system status and control the deivce via the UART pins on some DIY boards of Arylic, eg: Up2Stream PRO. And the product models MA400/HA400 which support RS232 serial port, support to control with this API. These messages are also used to extend the TCP API, so you could send and receive message via network.

> UART parameters

```plaintext
115200/8/n/1
no flow control
```

## Basic Rules

* messages are defined in 3 characters, and will use `:` to seperate the different part. 
* messages sent over UART need to be terminated with `;`
* messages might be received without query when state changed.
* Content between `{}` is variable name, you need to replace with the real content, and `{}` itself is not meant to be sent.
* Content between `[]` means optional, and `[]` itself is not meant to be sent.
* messages sent by host without param means to query current state, and messages with param means to change current state. 
* messages received normally with param, and means current state.

# State And Control

## Device 

### Summary

Command | Ver | Response | Ctrl 
---|---|---|---
STA | 3 | STA:{states}  
SYS:{cmd} | 3 | | * 
WWW | 3 | WWW:{onoff} | 
NAM[:{hextext}] | 3 | NAM:{hextext} | * 
ETH | 3 | ETH:{onoff} | 
WIF | 3 | WIF:{onoff} | 
WRS | 3 | | * 
WSS | 6 | WSS:{rssi} | 
BSS | 6 | BSS:{rssi} | 
IPA | 6 | IPA:{ip} | 
TME | 6 | TME:{time} | 
COE[:{onoff}] | 8 | COE:{onoff} | * 
COD[:{pin}] | 8 | COD:{pin} | * 

> STA response sample

```
NET,0,33,-2,0,1,1,1,1,0
```

### STA

Device status summary, and the response message `{states}` will consist with: current source,mute,volume,treble,bass,net,internet,playing,led,upgrading.

> reset factory 

```
SYS:RESET
```

### SYS:{cmd}

system operations 

{cmd} | description
--|--
`REBOOT` | reboot device
`STANDBY` | enter standby. Not well considered, and can't wake up via UART for some models. 
`RESET` | reset factory


> message received when device connected to internet

```
WWW:1
```

### WWW 

get internet status, message would be sent when state changed

> change device name to Backyard

```
NAM:4261636B79617264
```

### NAM[:{hextext}] 

set or get device name, and the string is encoded with hex value in UTF-8 encoding. eg: `4261636B79617264` for `Backyard`

> message received when device connected to ethernet

```
ETH:1
```

### ETH 

get ethernet status, message would be sent when state changed

> message received when device connected to WIFI AP

```
WIF:1
```

### WIF 

get wifi status, wether connected to AP. message would be sent when state changed

### WRS

trigger the WIFI setup, device will enter WIFI configuration mode and waiting for setup in APP

> message received when query WIFI signal strength

```
WSS:-49
```

### WSS 

get WIFI signal strength, host need to query this value proactively.

### BSS 

get Bluetooth signal strengh, not working in all models and host need to query this value proactively.

> message received when query IP

```
IPA:192.168.0.105
```

### IPA

get device IP address, message would be sent when state changed. 

> message received when query current time

```
TME:2024-06-11 09:14:00 (+8)
```

### TME 

get local time, host need to query this value proactively.

> query if pin code activated

```
COE
```

### COE[:{onoff}] 

turn on/off pin code for bluetooth connection, device will reboot when execute this command

>  set connection code to 1234

```
COD:1234
```

### COD[:{pin}] 

set/get pin code for bluetooth connection, default `0000`

## Playback

### Summary

Command | Ver | Response | Ctrl 
---|---|---|---
SRC[:{source}] | 3 | SRC:{source} | *
POP | 3 | | * 
STP | 3 | | * 
NXT | 3 | | *
PRE | 3 | | *
PST:{preset} | 3 | | * 
LPM[:{loopmode}] | 3 | LPM[:{loopmode}] | * 
BTC[:{onoff}] | 3 | | * 
PLA | 3 | PLA:{onoff} | 
CHN | 3 | CHN:{channel} | 
MRM | 3 | MRM:{mrmmode} |
TIT | 4 | TIT:{hextext} |
ART | 4 | ART:{hextext} |
ALB | 4 | ALB:{hextext} |
VND | 4 | VND:{vendor} |
ELP | 4 | ELP:{elapsed} |
PLI | 4 | PLI:{playlist_info} | 
APL[:{onoff}] | 5 | APL:{onoff} | * 

> switch source to bluetooth

```
SRC:BT
```

### SRC[:{source}] | 3 | SRC:{source} | * | select input source

get or set input source of device

{source} | description 
--|--
`NET` | network
`BT` | bluetooth
`USBDAC` | USB DAC
`LINE-IN` | line-in
`OPT` | Optical
`COAX` | Coaxial
`LINE-IN2` | extra line-in
`OPT2` | extra Optical 
`COAX2` | extra Coaxial
`HDMI` | HDMI ARC

### POP

play or pause, available in network playback and bluetooth

### STP

stop, available only in network playback

> next track

```
NXT
```

### NXT

next track, available in network playback and bluetooth

### PRE

previous track, available in network playback and bluetooth

> play preset #1

```
PST:1
```

### PST:{preset}

start to play preset playlist

### LPM[:{loopmode}] 

set/get loop and shuffle mode, available in network playback. 

{loopmode} | description
--|--
`REPEATALL` | repeat all in playlist
`REPEATONE` | repeat track
`REPEATSHUFFLE` | repeat all and shuffle
`SHUFFLE` | shuffle and stop when all tracks played
`SEQUENCE` | stop when reach end of playlist

> close current bluetooth connection

```
BTC:0
```

### BTC[:{onoff}] 

disconnect/reconnect bluetooth

### PLA 

network playing state

### CHN 

query multiroom channel status, does not support to set from API

{channel} | description
--|--
`S` | stereo mode
`L` | left channel
`R` | right channel

### MRM

query multiroom mode, does not support to set from API

{mrmmode} | description
--|--
`S` | multiroom slave
`M` | multiroom master
`N` | normal mode

### TIT 

notification messages for song metadata title. (not work when sent in TCP)

### ART 

notification messages for song metadata artist. (not work when sent in TCP)

### ALB 

notification messages for song metadata album. (not work when sent in TCP)

### VND

notification messages for song metadata vendor. (not work when sent in TCP)

{vendor} will have the following value:

`spotify`
`qplay`
`dlna`
`airplay`
`upnp`
`phone`
`usb`
`tidal`
`napster`
`qobuz`
`amazon`
`tunein`
`iheart`
`vtuner`
`http`
`other`

### ELP 

notification messages for elapsed and duration of current track. {elapsed} will have unit ms, and a sample: `31251/212000`

(not work when sent in TCP)

> message received when query playlist info

```
PLI:1/23
```

### PLI

query current track index and number of playlist, {playlist_info} will be in this format index/count, and index is start from 1. eg: `1/23` means now playing the first song in playlist contains 23 songs in total.

### APL[:{onoff}]

set/get autoplay feature. When enabled, the device will try to play last playlist on boot. 

## Audio

### Summary

Command | Ver | Response | Ctrl 
---|---|---|---
AUD[:{onoff}] | 3 | AUD:{onoff} | * 
VOL[:{volume}] | 3 | VOL:{volume} | *
MUT[:{onoff}] | 3 | MUT:{onoff} | * 
BAS[:{tone}] | 3 | BAS:{tone} | * 
TRE[:{tone}] | 3 | TRE:{tone} | * 
MID[:{tone}] | 6 | MID:{tone} | * 
VBS[:{onoff}] | 3 | VBS:{onoff} | * 
BAL[:{balance}] | 5 | BAL:{balance} | * 
VOF[:{volume}] | 5 | VOF:{volume} | * 
VOG[:{volume}] | 6 | VOG:{volume} | * 
PEQ | 6 | PEQ:{eqlist} |  
EQS[:{eqidx}] | 6 | EQS:{eqidx} | * 
VST[:{step}] | 6 | VST:{step} | * 
EQE[:{onoff}] | 7 | EQE:{onoff} | * 
CFE[:{onoff}] | 7 | CFE:{onoff} | * 
CFF[:{cffreq}] | 7 | CFF:{cffreq} | * 

### AUD[:{onoff}]

set/get audio output

> set system volume to 50

```
VOL:50
```

### VOL[:{volume}] 

set/get master volume

### MUT[:{onoff}] 

set/get mute

> set bass to +2

```
BAS:2
```

### BAS[:{tone}] 

set/get bass tone, and {tone} ranges [-10,10], unit dB

### TRE[:{tone}] 

set/get treble tone

### MID[:{tone}] 

set/get middle tone

> enable virtual bass

```
VBS:1
```

### VBS[:{onoff}] 

set/get virtual bass

> set the sound balance to the right side

```
BAL:50
```

### BAL[:{balance}]

set/get audio output balance, the {balance} ranges [-100,100], available only when output mode is stereo. Will attenuate the left channel output when {balance} is greater than 0, and attenuate the right channel output when {balance} is less than 0.

### VOF[:{volume}] 

set/get fixed volume output, the {volume} ranges [0,100], and will be disabled when set to `0`. And if set to non zero value, the system will have fixed output level, and can't be adjusted by volume control.

### VOG[:{volume}]

set volume of grouped playback (multiroom)

> the query result of EQ groups

```
PEQ:0@Flat,1@Classical,2@Pop,3@Jazz,4@Rock,5@Vocal
```

### PEQ 

query system EQ group list, the format of {eqlist} will be index@name, and seperated by `,`.

> select EQ group #1

```
EQS:1
```

### EQS[:{eqidx}] 

get/set EQ group

### VST[:{step}]

set/get volume step, {step} ranges [0,10]. It will affect the volume value changes when press once vol+ or vol- button.

### EQE[:{onoff}] 

enable/disable EQ

### CFE[:{onoff}]

enable/disable crossfilter, when activated the stereo output will have a high-pass filter. and the DAC-X output will have a low-pass filter.

### CFF[:{cffreq}]

set/get crossfilter frequency point, {cffreq} ranges [50,300]

## Misc

### Summary

Command | Ver | Response | Ctrl
---|---|---|---
VER | 3 | VER:{version} | 
LED[:{onoff}] | 3 | LED:{onoff} | * 
BEP[:{onoff}] | 3 | BEP:{onoff} | * 
PMT[:{onoff}] | 4 | PMT:{onoff} | * 
DLY[:{mute_delay}] | 4 | DLY:{mute_delay} | * 
MXV[:{volume}] | 4 | MXV:{volume} | * 
ASW[:{onoff}] | 4 | ASW:{onoff} | * 
POM[:{source}] | 4 | POM:{source} | * 
VOS:{onoff} | 4 | VOS:{onoff} | * 
LST | 7 | LST:{sources} | 
SOP:{onoff} | 7 | SOP:{onoff} | * 

> response of current version

```
VER:44-c7c30da5-8
```

### VER 

firmware version, and the {version} will contain the version number, short git commit, and API level, connected with `-`.

> turn off beep sound

```
BEP:0
```

### BEP[:{onoff}] 

Query or turn on/off beep sound for key press

### LED[:{onoff}] 

Query or turn on/off led or display

### PMT[:{onoff}] 

Query or turn on/off the prompt voice, device will reboot on this command

### ASW[:{onoff}] 

Query or turn on/off auto switch mode. When enabled, will try return previous input source when connection lost. eg: will switch to previous input when plug-out detected in AUX mode.

### VOS:{onoff} 

Query or turn on/off volume sync feature. When enabled, and adjusting volume on master device (multiroom group) with remote or button, will sync the changes to slave devices. 

### SOP:{onoff} 

Query or turn on/off standby on power. When enabled, device will enter standby mode on power supplied.

> set max volume to 80

```
MXV:80
```

### MXV[:{max_volume}] 

set/get max volume, {max_volume} ranges [30,100]

### DLY[:{mute_delay}] 

set/get delay time to auto mute when detected no audio input. {mute_delay} ranges [0,32767]

> supported input sources of Up2Stream Pro

```
LST:NET,BT,LINE-IN,USBDAC
```
### LST 

query system available input sources

### POM[:{source}] 

set/get power on mode, when set an available source, the device will select the specified source on power up.

# 4 Zone Model

We've produced 4 models with 4 zone, MA400/HA400, and M400/H400 which without contain internal amplifier. There's a master MCU to manage the 4 zones on these models. And the RS232 port is connect to this master MCU, and it could transfer commands to specific zone. We defined a special command `ZON` to redirect commands sent to specific zones. Each zone has an id which is used to identify zone physically. The param used to `ZON` is logic zone id. The logic zone id is by default the same with physical zone id, and could be changed with command `IDS`. 

This RS232 managing port support to connect in casacading, that means you could use a host to control 2 or more MA400s. And before connect together, you need to assign different logic zone id first. So you're able to identify each zone.

## zone manage

> set volume of zone 1 to 50

```
ZON:1:VOL:50;
```

### ZON:{logiczoneid}:{msg} 

Redirect {msg} to specific zone with {logiczoneidx}, {msg} is the UART command and parameter defined previously. And response will also be redirected in the same format. 


> set logic id of zone 1 to 5

```
IDS:1:5;
```

> IDS query result

```
IDS:5,2,3,4;
```

### IDS[:{zoneid}:{logiczoneid}]

query or set/get logic zone id, the query response will contain the logic zone id of all zones. The logic zone id ranges [1,127].

# Default Configuration 

For the Up2Stream series, users are building various products based on it. So we defined a set of API to set the default settings of these boards. eg: default device name, disable the beep sound by default, etc.

> example of set default volume to 30

```
DEF:VOL:30
```

The default configuration will be sent as param of API `DEF`, and is defined as sub level API.

## Sub API

All sub APIs is supposed to send with `DEF`.

### Summary 

Command | Ver | Response | 
--|--|--|--
LTP[:{led_type}] | 6 | LTP:{led_type}
NAM[:{hextext}] | 6 | NAM:{hextext}
FXN[:{onoff}] | 6 | FXN:{onoff} 
VOL[:{volume}] | 6 | VOL:{volume} 
VBS[:{onoff}] | 6 | VBS:{onoff}
PMT[:{onoff}] | 6 | PMT:{onoff}
VOS[:{onoff}] | 6 | VOS:{onoff}
BEP[:{onoff}] | 6 | BEP:{onoff}
MDL[:{hextext}] | 6 | MDL:{hextext}
VST[:{step}] | 6 | VST:{step}
SAV | 6 | SAV:1
SEN[:{source}={onoff}] | 7 | SEN:{sources} on query, SEN:1 on set
POM[:{source}] | 7 | POM:{source}
MXV[:{max_volume}] | 7 | MXV:{max_volume}
COE[:{onoff}] | 8 | COE:{onoff}
COD[:{pin}] | 8 | COD:{pin}
LAP[:{onoff}] | 8 | LAP:{onoff}

> set to use single PIN to drive LED

```
DEF:LTP:PIN
```

### LTP[:{led_type}]

Change LED driving method, availabe only on model Up2Stream PRO and AMP2.0. 

{led_type} | desc
--|--
`UND` | firmware default
`RGB` | working in RGB mode
`PIN` | driven with single PIN, and some modes are sharing PIN.

### NAM[:{hextext}]

Set default device name

### FXN[:{onoff}]

Set whether to restore the default device name when do factory reset. It's off by default

### VOL[:{volume}]

Set default volume level 

> turn on virtual bass by default

```
DEF:VBS:1
```

### VBS[:{onoff}]

Set default virtual bass state, default off.

### PMT[:{onoff}]

Set default prompting voice state, default on.

### VOS[:{onoff}]

Set default volume sync state, default off.

### BEP[:{onoff}]

Set default beep sound state, default on.

### MDL[:{hextext}]

Set model name, it's not used in device actually, could be used to identify your model.

### VST[:{step}]

Set default volume step, default 3.

### SAV

Save the settings. And this messages has to be sent in the last to make sure the changes will take effect. And after configured, you need to restore factory default to verify.

> disable LINE-IN input

```
DEF:SEN:LINE-IN=0
```

> SEN query response

```
DEF:SEN:NET,BT,USBDAC
```

### SEN[:{source}={onoff}]

Disable/enable some input modes. You could only enable the existing input modes supported by model.

And this command is a bit special, it will just save and restore factory default when settings updated.

### POM[:{source}]

Set the default input mehtod when power on.

### MXV[:{max_volume}]

Set the default max volume, default 100.

### COE[:{onoff}]

Set the default bluetooth pin code protection state, default off.

### COD[:{pin}]

Set the default bluetooth pin code, default 0000.

### LAP[:{onoff}]

Set the default auto play feature of AXX module, defaut off.

