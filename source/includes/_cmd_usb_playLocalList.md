## Play from USB stick/disk

Based on the return value of `getLocalPlayList` this command can be used to selectively play individual tracks on a connected USB stick/hard disk. The parameter <index> specifies the position of the track within the array returned by `getLocalPlayList`.

Command: `playLocalList`

> Request format:

```html
GET /httpapi.asp?command=playLocalList:<index>
```

This request produces no response.