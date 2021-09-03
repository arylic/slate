## Track Info from USB stick/disk
> Request format:

```html
GET /httpapi.asp?command=getFileInfo:<num_file_index_start>:<num_range>
```

> Example response for `range=1`:

```json
{
   "filename":"2F6D656469612F736461312F52656164696E672032303136202D20466F616C732E6D7033",<br> 
   "totlen":"00:00:00",<br> 
   "Title":"52656164696E672032303136202D20466F616C732E6D7033",<br>
   "Artist":"756E6B6E6F776E",<br> 
   "Album":"756E6B6E6F776E"
}

```

> Example response for `range=2`:

```json
{
	"num": "2",
	"infolist": [
		{
         "filename":"2F6D656469612F736461312F52656164696E672032303136202D20466F616C732E6D7033", 
         "totlen":"00:00:00", 
         "Title":"52656164696E672032303136202D20466F616C732E6D7033", 
         "Artist":"756E6B6E6F776E", 
         "Album":"756E6B6E6F776E"},
      {
         "filename":"2F6D656469612F736461312F52656164696E672032303136202D20466F616C732E6D7033", 
         "totlen":"00:00:00", 
         "Title":"52656164696E672032303136202D20466F616C732E6D7033", 
         "Artist":"756E6B6E6F776E", 
         "Album":"756E6B6E6F776E"},
      }
	]
}
```

Allows to query file information on a connected USB stick or hard drive. Two parameters are passed. The first, the  `index` value, stands for "the number of files in the file system" from which the output should start. The second parameter `range` specifies how many files should be analyzed, starting with `index`. So, if `range` is larger than `1`, the response will give informations for multiple music files.

Command: `getFileInfo`

### Parameter Description

Parameter | Description
---|---
`num_file_index_start` | Start Position - the numerical position of an audio file in the USB file index.<br>Value range is from `1-1024`.
`num_range` | The quantity of files to be analysed, starting from the `num_file_index_start` value


### Response Description

Key | Value-Description
---|---
`filename` | The filename as `[hexed string]`
`totlen` | Total playing time of that track (in ms)
`Title` | The title of that track.<br>If the info is available, the value is returned as `[hexed string]`, otherwise `UNKNOWN` in plaintext
`Artist` | The artist of that track.<br>If the info is available, the value is returned as `[hexed string]`, otherwise `UNKNOWN` in plaintext
`Album` | The album where this track is from.<br>If the info is available, the value is returned as `[hexed string]`, otherwise `UNKNOWN` in plaintext

<aside class="notice">
The treatment of hexed data is covered in a seperate section.  
</aside>


