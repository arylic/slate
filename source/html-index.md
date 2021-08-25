---
title: Arylic Audio HTTP API

# Languages must be one of: https://git.io/vQNgJ
language_tabs:

toc_footers:
  - Documentation originally<br/>made with ❤️ by <a href='https://woodbytes.me' target='_blank'>Woodbytes</a>
  - "&nbsp;"
  - Based on firmware version<br><code>4.6.9724.26</code>
  
includes:
  - http/intro_welcome
  - http/intro_abstract
  
  # Networking
  - http/group_networking
  - http/cmd_networking_wlanGetApListEx
  - http/cmd_networking_wlanConnectApEx
  - http/cmd_networking_wlanConnectHideApEx
  - http/cmd_networking_wlanGetConnectState

  # Device Informations
  - http/group_device
  - http/cmd_device_getStatusEx

  # Playback control
  - http/group_playback
  - http/cmd_playback
  - http/cmd_playback_getPlayerStatus
  - http/cmd_playback_setPlayerCmd

  # USB disk playback
  - http/group_usb
  - http/cmd_usb_getLocalPlayList
  - http/cmd_usb_playLocalList
  - http/cmd_usb_getFileInfo
  
  # Multiroom
  - http/group_multiroom
  - http/cmd_multiroom
  - http/cmd_multiroom_getSlaveList
  - http/cmd_multiroom_SlaveChannel
  - http/cmd_multiroom_SlaveMask
  - http/cmd_multiroom_SlaveMute
  - http/cmd_multiroom_SlaveVolume
  - http/cmd_multiroom_SlaveKickout
  - http/cmd_multiroom_ungroup

  # Appendix
  - http/appendix_hexed_string

search: true

code_clipboard: false
---
