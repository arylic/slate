## Set the Audio Channel (Left/Right/Stereo) for a Guest Device
> Request format:

```html
GET /httpapi.asp?command=multiroom:SlaveChannel:<ip_address>:<flag_channel>
```

> Example Response:

```plaintext
OK
```

This sub-command will set the audio channel for a Guest Devive in a Multiroom group.

Sub-Command: `SlaveChannel`



### Parameter Description

Parameter | Description
---|---
`ip_address` | The IP address of the Guest Device to control with this command
`flag_channel` | The channel that has to be switched<br>`0` - Stereo (both channels are on)<br>`1` - Left channel is on<br>`2` - Right channel is on


<aside class="notice">
The response isn't in JSON format. It is just plaintext.
</aside>