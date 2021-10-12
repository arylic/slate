## Extended M3U Tags

> Example M3U file with extended tags and relative URL

```text
#EXTM3U
#EXTURL:http://192.168.0.2/test/cover.jpg
#EXTINF:1,P!nk - Just give me a reason
Just Give Me A Reason.mp3
```

> Example M3U file with extended tags and absolute URL

```text
#EXTM3U
#EXTURL:http://192.168.0.2/test/cover.jpg
#EXTINF:1,P!nk - Just give me a reason
http://192.168.0.2/test/Just%20Give%20Me%20A%02Reason.mp3
```

Standard M3U does not define tags for coverart and title, artist. There's a extended tag to append an image data for coverart, but it's not suitable for streaming device. So we defined a private tag `EXTURL` for the URL of covert. And also referenced the `EXTINF` tag to include the title and artist. With the extra meta data, the playing state on 4STREAM APP would be more friendly. 

Tag | Description
---|---
`EXTURL` | The URL will be appended after the tag and `:`. It will be used as coverart of the track, and need to be absolute URL.
`EXTINF` | Information will be appended after the tag and `:`. It is in format `N,ARTIST - TITLE`<br>`N` is track index but it's not used.<br> `ARTIST` and `TITLE` is seperated by ` - `, better to remove the `-` in title or artist. 
