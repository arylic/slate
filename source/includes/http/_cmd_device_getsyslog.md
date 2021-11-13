## Get System Log

> Request format:

```html
GET /httpapi.asp?command=getsyslog
```

> Example response:

```html
<!doctype html>
<html>
	<head>
		<meta charset="utf-8">
	</head>
	<body>
		<DIV>
			<span id="dl">&nbsp;&nbsp;&nbsp;&nbsp;<a href=data/sys.log>download</a><hr></span>
		</DIV>
	</body>
</html>
```

To get current system log for debugging, the content is encryted. The response for this command is special, it will show a download link for user. And after clicked, will download the log file onto your computer. 

Command: `getsyslog`

