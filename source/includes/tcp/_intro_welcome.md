# TCP API

Welcome to Arylic's TCP API developer documentation.  

The Query and Control Interface is supported by standard TCP/IP Sockets.  So unique socket identification on the LAN/WLAN is the pair of the Arylic Device IP Address and the Communication Port. The creation and management of TCP/IP Sockets is no covered in the Scope of this document as this can found in many places on the Internet and in books. 

It is a strong recommendation to familise yourself with the Arylic "Web Management Interface".  This will enable you to configure the IP address of your Arylic Device and also configure the communications Port for the TCP/IP Socket if required.

Arylic provide a simple development Tool for Windows.   

The "root" of these commands is:   
`MCU+PAS+RAKOIT:`	

All commands are terminated with the special character `&`.

Some Commands are Command Pairs where the same 3 character code `ABC` can be used for query/read or control/write:

* `MCU+PAS+RAKOIT:ABC&` - Query or Read Values
* `MCU+PAS+RAKOIT:ABC:{parameter}&` - Control Functions or Write Values 

The Command Pairs (Read & Write) are the following:
    
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
  