# SYSTEM COMMANDS

The following commands are all "system" commands 'SYS'

Command: `MCU+PAS+RAKOIT:SYS:<str_command>`

### Factory Reset
> Request format: ```html
MCU+PAS+RAKOIT:SYS:RESET&
```
> Example Response:

```plaintext
PLY+000 AXX+PMT+000 AXX+FACTORY AXX+DEV+RST
```

This will stop playback and reset the device to factory settings.  

Command: `MCU+PAS+RAKOIT:SYS:RESET&`

The response string will confirm that the command has been accepted 
`PLY+000 AXX+PMT+000 AXX+FACTORY AXX+DEV+RST`

<aside class="notice">
If playback is active before reboot, playback and current settings are retained.
</aside>

### System Reboot
> Request format: 
```html
MCU+PAS+RAKOIT:SYS:REBOOT&
```

> No Response:

This will stop playback immediately and will reboot the device.  Playback is resumed after reboot has been completed.

Command: `MCU+PAS+RAKOIT:SYS:REBOOT&`

This command will reboot the whole device including the base board and the wifi module.

<aside class="notice">
If playback is active before reboot, playback and current settings are retained.
</aside>

### System Standby
> Request format:

```html
"MCU+PAS+RAKOIT:SYS:STANDBY&"
```

> No Response:

This will stop playback immediately and power off the device.

Command: `MCU+PAS+RAKOIT:SYS:STANDBY&`

<aside class="notice">
Input Power will need to be cycled to switch on / power up the device
</aside>



