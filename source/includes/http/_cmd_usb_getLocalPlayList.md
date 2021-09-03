## Get content list from USB stick/disk
> Request format:

```html
GET /httpapi.asp?command=getLocalPlayList
```

> Example response when a stick/disk is connected and files where found:

```json
{
   "num":"3", 
   "locallist":[
      {
         "file":"2F6D656469612F736461312F52656164696E672032303136202D20466F616C732E6D7033"
      },
      {
         "file":"2F6D656469612F736461312F52656164696E672032303136202D20524843502E6D7033"
      },
      {
         "file":"2F6D656469612F736461312F52656164696E672032303136202D20426966667920436C79726F2E6D7033"
      }
   ]
}
```

> Example response when no stick/disk is connected or no files where found:

```
no music file
```

Returns a list of music files on an attached USB stick or hard drive (connected with a USB Adaptor)

Command: `getLocalPlayList`


Key | Value-Description
---|---
`num` | Number of valid audio files.<br>Value range is from `1-124`.
`locallist` | The array containing the filenames  
`file` | A single string of path, filename & file extension. Note the string returned is a `[hexed string]`.

<aside class="notice">
The treatment of hexed data is covered in a seperate section.  
</aside>
