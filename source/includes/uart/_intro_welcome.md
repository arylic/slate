# UART API

Welcome to Arylic's UART API developer documentation.  

**Playback related commands:**

  * `SRC` - Device Source
  * `VOL` - Device Volume
  * `TRE` - Equaliser Treble Level
  * `BAS` - Equaliser Bass Level
  * `VBS` - Virtual Bass
  * `LPM` - Loop and Repeat Modes

**Hardware configuration commands:**

  * `NAM` - Device Name
  * `LED` - Main Device LED  
  * `BEP` - Device Beep

**Connection configuration commands:**

  * `BTC` - BT connection blah blah
  

In the following table:

* Content between `[]` means optional. And normally function without param means to query current state, function with param means to change current state. And `[]` itself is not meant to be sent.

* Content between `{}` is variable name, you need to replace with the real content, and `{}` itself is not meant to be sent.

Function | Version | Description
---|---|---
VER | 3 | version
STA | 3 | device status summary
SYS:{cmd} | 3 | system operations
WWW | 3 | internet status
AUD[:{onoff}] | 3 | audio output
SRC[:{source}] | 3 | input source
VOL[:{volume}] | 3 | master volume
MUT[:{onoff}] | 3 | mute
BAS[:{bass}] | 3 | bass tone
TRE[:{treble}] | 3 | treble tone
MID[:{middle}] | 6 | middle tone
POP | 3 | play or pause
STP | 3 | stop
NXT | 3 | next
PRE | 3 | previous
BTC[:{onoff}] | 3 | bluetooth connection
PLA | 3 | playback status
CHN | 3 | audio channel
MRM | 3 | multiroom status
LED[:{onoff}] | 3 | led or display
BEP[:{beep}] | 3 | beep sound 
PST:{preset} | 3 | preset
VBS[:{onoff}] | 3 | virtual bass
WRS | 3 | wifi reset
LPM[:{loopmode}] | 3 | loop and shuffle mode
NAM[:{name}] | 3 | device name
ETH | 3 | ethernet status
WIF | 3 | wifi status
PMT | 4 | [:{onoff}] | prompt voice
PRG[:{onoff}] | 4 | pregain
DLY[:{mute_delay}] | 4 | delay of auto mute
MXV[:{max_vol}] | 4 | max volume
ASW[:{auto_swith}] | 4 | auto switch mode
POM[:{source}] | 4 | power on mode
TIT | 4 |
ART | 4 |
ALB | 4 |
VND | 4 |
ELP | 4 |
PLI | 4 |
VOS | 4 |
BAL | 5 |
VOF | 5 |
APL | 5 |
WSS | 6 |
IPA | 6 |
TME | 6 |
BSS | 6 |
VOG | 6 |
VST | 6 |
PEQ | 6 |
EQS[:{eq_group}] | 6 |
DEF | 6 |
ZON:{zone}:{msg} | 7 | zone
IDS | 7 |
BTM | 7 |
LST | 7 |
CEQ | 7 |
EQE | 7 |
CFS | 7 | 
CFE | 7 | 
CFF | 7 | 
SOP | 7 |
BTS | 7 |
DSK | 7 |
COE | 8 |
COD | 8 |
MMC | 8 |
ARC | 8 |

Default Function | Description
---|---
LTP | 
NAM |
FXN |
VOL |
VBS |
PMT |
SEN |
POM |
VOS |
BEP |
MDL |
VST |
SAV |
