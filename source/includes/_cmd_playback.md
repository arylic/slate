Command: `setPlayerCmd`  

The command `setPlayerCmd` is just an abstract command, it needs a sub command to work as expected. See the list of current available sub commands.

### Playback Sub-Commands

Sub-Command | Parameters | Description
-+-+-
`play` | | Play an URI<br>`uri` could be a direct URL to a web radio stream (must be URL encoded)
`playlist` | `uri`, `index` | Play an URI<br>`uri` is an M3U playlist<br>`index` is the start index
`hex_playlist` | `uri`, `index` | Play an URI<br>`uri` is an M3U playlist<br>`index` is the start index<br>The `uri` value must be a `[hexed string]`
`playLocalList` | `index` | Play from USB disk<br>`index` is the start index

### Player Control Sub-Commands

Sub-Command | Description
-+-
`pause` | Pause current playback
`resume` | Resume playback from last position, if it is paused
`onepause` | Toggle Play/Pause
`stop` | Stop current playback (play position will be reset to `0`)
