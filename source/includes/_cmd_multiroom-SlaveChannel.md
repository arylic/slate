## Set the Audio Channel of a Player

Allows dedicated switching on and off of an audio channel from a child player in a Multiroom group.

Sub-Command: `SlaveChannel`

> Request format:

```html
GET /httpapi.asp?command=multiroom:SlaveChannel:<ip_address>:<channel>
```

> Example Response:

```plaintext
OK
```

### Parameter Description

Parameter | Description
-+-
`ip_address` | The IP address of the child player whose audio channel has to be switched
`channel` | The channel that has to be switched<br>`0` - Stereo (both channels are on)<br>`1` - Left channel is on<br>`2` - Right channel is on


<aside class="notice">
The response isn't in JSON format. It is just plaintext.
</aside>
