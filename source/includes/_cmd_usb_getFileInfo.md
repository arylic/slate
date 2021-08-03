## Track Info from USB stick/disk

Allows to query file information on a connected USB stick or hard drive. Two parameters are passed. The first, the  `index` value, stands for "the number of files in the file system" from which the output should start. The second parameter `range` specifies how many files should be analyzed, starting with `index`. So, if `range` is larger than `1`, the response will give informations for multiple music files.

Command: `getFileInfo`

> Request format:

```html
GET /httpapi.asp?command=getFileInfo:<index>:<range>
```

> Example response for `range=1`:

```json
{
	"Album": "unknown",
	"Artist": "unknown",
	"Title": "unknown",
	"filename": "/media/sda1/avril lavigne – hush hush.mp3",
	"totlen": "0"
}
```

> Example response for `range=2`:

```json
{
	"num": "2",
	"infolist": [
		{
         "Album": "unknown",
         "Artist": "unknown",
         "Title": "unknown",
         "filename": "/ media / sda1 / avrilavigne - hush hush.mp3",
         "totlen": "0"
      },
      {
         "Album": "unknown",
         "Artist": "unknown",
         "Title": "unknown",
         "filename": "/ media / sda1 / avrilavigne - hush hush2.mp3",
         "totlen": "0"
      }
	]
}
```

### Parameter Description

Parameter | Description
-+-
`index` | The sequence number of the  USB stick/disk playlist
`range` | The number of files to be analized, starting an `index`


### Response Description

Key | Value-Description
-+-
`Album` | The album where this track is from.<br>If the info is available, the value is returned as `[hexed string]`, otherwise `UNKNOWN` in plaintext
`Artist` | The artist of that track.<br>If the info is available, the value is returned as `[hexed string]`, otherwise `UNKNOWN` in plaintext
`Title` | The title of that track.<br>If the info is available, the value is returned as `[hexed string]`, otherwise `UNKNOWN` in plaintext
`filename` | The filename as `[hexed string]`
`totlen` | Total playing time of that track (in ms)
