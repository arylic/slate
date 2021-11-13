## Play from USB stick/disk
> Request format:

```html
GET /httpapi.asp?command=setPlayerCmd:playLocalList:<num_file_index>
```

> Example response:

```plaintext
OK
```

Based on the return value of `getLocalPlayList` this command can be used to selectively play individual tracks on a connected USB stick/hard disk. The parameter <index> specifies the position of the track within the array returned by `getLocalPlayList`.

Sub-command: `playLocalList`

Parameter | Description
---|---|---
`num_file_index` | The numerical position of an audio file in the USB file index.<br>Value range is from `1-124`.
