## Add Guest Device to Multiroom Group (Router Mode)

This command will add/join a Guest Device to the Host Device or an existing Multiroom Group (which is assigned to the host device).  The command is sent to the Guest Device and the IP Address of Host Device needs to be added to the command as shown below.

Command: `ConnectMasterAp:JoinGroupMaster`:

> Request format:

```html
GET /httpapi.asp?command=ConnectMasterAp:JoinGroupMaster:eth<ip_address>:wifi0.0.0.0
```

> Example Response:

```plaintext
OK
```

### Parameter Description

Parameter | Description
---|---
`ip_address` | The IP address of the host device to be removed from the group


<aside class="notice">
The response isn't in JSON format. It is just plaintext.
</aside>
