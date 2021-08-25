## Adjust Volume of a Player
Allows you to adjust the volume of each player in a group. The request must be sent to the host of the group. When a player is removed from the group (command `multiroom:SlaveKickout`), this setting is lost, and the player gets its previous volume.

Sub-Command: `SlaveVolume`

> Request format:

```html
GET /httpapi.asp?command=multiroom:SlaveVolume:<ip_address>:<volume>
```

> Example Response:

```plaintext
OK
```

### Parameter Description

Parameter | Description
---|---
`ip_address` | The IP address of the child player to be removed from the group
`volume` | The volume to be set. Numeric value ranges from `0-100`


<aside class="notice">
The response isn't in JSON format. It is just plaintext.
</aside>
