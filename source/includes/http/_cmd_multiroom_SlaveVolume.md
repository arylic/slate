## Adjust Volume of a Guest Device
> Request format:

```html
GET /httpapi.asp?command=multiroom:SlaveVolume:<ip_address>:<num_volume>
```

> Example Response:

```plaintext
OK
```

Allows you to adjust the volume of each Guest Device in a group. The request must be sent to the Host Device of the group. When a Guest Device is removed from the group (command `multiroom:SlaveKickout`), this volume level is overwritten an the Guest Device will return to its previous independent volume.

Sub-Command: `SlaveVolume`


### Parameter Description

Parameter | Description
---|---
`ip_address` | The IP address of the child/slave media player to be removed from the group
`num_volume` | Volume level requested. Numeric value ranges from `0-100`


<aside class="notice">
The response isn't in JSON format. It is just plaintext.
</aside>
