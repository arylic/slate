# Arylic API Documentation

This is a fork of the [Slate project](https://github.com/slatedocs/slate). To study its original documentation please visit their [Wiki](https://github.com/slatedocs/slate/wiki).

## How it works

Arylic boards provides three different API's which are accessible via:

* HTTP
* TCP and
* UPnP

The documentation is written in pure [Markdown](https://www.markdownguide.org/basic-syntax/), and all documentation files are placed in their API specific directories:

* `source/includes/http/` for HTTP API
* `source/includes/tcp/` for TCP API, and
* `source/includes/upnp/` for UPnP API

When you edit the documentation, you usually do this by running the `./slate.sh serve` command side-by-side to be able to see live your changes in the browser. Using this command without any additional parameter will serve the HTML documentation by default.

If you want to see live changes for the TCP documentation, then you have to use the `-t` or `--target` parameter, setting by one of three possible targets:

* `html` (in this case the target parameter can also be omitted)
* `tcp`, or
* `upnp`

This will result in a command like:

```
./slate.sh -t tcp serve
```

for watching live changes of your TCP documentation.

To get it work properly, besides the documentation files in `source/includes/$TARGET` there are three Markdown index files:

* `html-index.md`
* `tcp-index.md`, and
* `upnp-index.md`

These files contains the final structure of the generated static documentation. By running the `serve`, `build` or `deploy` command, the index file in question will be copied to `index.html.md` which will be used by Slate finally.