---
title: Arylic Audio HTTP API

# Languages must be one of: https://git.io/vQNgJ
language_tabs:

toc_footers:
  - v1.0.2<br>Made with ❤️ by<br><a href='https://woodbytes.me' target='_blank'>Woodbytes</a> and <a href="https://www.facebook.com/NWT.Stuff" target="_blank">NWT.Stuff</a> 
  
includes:
  - http/intro_welcome
  - http/intro_abstract
  
  # Networking
  - http/group_networking
  - http/cmd_networking_wlanGetApListEx
  - http/cmd_networking_wlanConnectApEx
  - http/cmd_networking_wlanConnectHideApEx
  - http/cmd_networking_wlanGetConnectState
  - http/cmd_networking_getStaticIP
  - http/cmd_networking_setStaticIP
  - http/cmd_networking_setDhcp

  # Device Informations
  - http/group_device
  - http/cmd_device_getStatusEx
  - http/cmd_device_getsyslog
  - http/cmd_device_redirect_ota
  - http/cmd_device_reboot

  # Playback control
  - http/group_playback
  - http/cmd_playback_getPlayerStatus
  - http/cmd_playback_setPlayerCmd
  - http/cmd_playback
  - http/cmd_playback_GetTrackNumber
  - http/cmd_playback_playPromptUrl

  # USB disk playback
  - http/group_usb
  - http/cmd_usb_getLocalPlayList
  - http/cmd_usb_playLocalList
  - http/cmd_usb_getFileInfo
  
  # Multiroom
  - http/group_multiroom
  - http/cmd_ConnectMasterAp_JoinGroupMaster
  - http/cmd_multiroom
  - http/cmd_multiroom_getSlaveList
  # - http/cmd_multiroom_SlaveChannel **KPW removed for now doesn't do anything !!
  # - http/cmd_multiroom_SlaveMask **KPW removed for now doesn't do anything !!
  - http/cmd_multiroom_SlaveMute
  # - http/cmd_multiroom_SlaveVolume **KPW removed for now as confusing can be acheieved with other commands !!
  - http/cmd_multiroom_SlaveKickout
  - http/cmd_multiroom_ungroup

  # Appendix
  - http/group_appendix
  - http/appendix_extended_m3u
  - http/appendix_hexed_string
  - http/appendix_changelog

search: true

code_clipboard: false
---
