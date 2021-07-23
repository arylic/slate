## USB stick/disk playback

Command: `getLocalPlayList`

> Request format:

```html
GET /httpapi.asp?command=getLocalPlayList
```

> Example response when a stick/disk is connected and files where found:

```json
{
   "num": "2",
   "locallist": [
      {
         "file": "/media/sda1/avril lavigne - tik tok.mp3"
      },
      {
         "file": "/media/sda1/avril lavigne – hush hush.mp3"
      }
   ]
}
```

> Example response when no stick/disk is connected or no files where found:

```
no music file
```

Key | Value-Description
-+-
`num` | Number of returned files
`locallist` | The key to get the file an array of file
`file` | Key to get the filepath



