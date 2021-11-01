# UPnP/DLNA API

Welcome to Arylic's UPnP/DLNA API developer documentation.  

The objective of this documentation is not to replicate previous documentation from https://www.dlna.org/ but to show how the DLNA platform can be used to control Arylic Devices with practical examples and table data. DLNA is a standard which is very complex and a subset of UPnP (Link and bit of very small blah blah blah about UPnP) 

We assume that you are exploring this functionality because you are familiar with UPnP & DLNA. If you are not you should first familiarise yourself with the DLNA documentation, particularly with regard to the key terminology used in these standards.

SOURCE = The physical location where music is being played from (e.g. URL Stream, MP3 file on a disk, Bluetooth from your phone etc. etc.)
SINK = The physical location where music is being played to (e.g. Your Arylic Device, TV, DLNA Friendly Stuff etc. etc.)
CONTROL POINT = How you select the content, change volume, mute etc. etc. (Phone, Tablet, Laptop etc. etc.)

Arylic Devices deliver the following DLNA Services by default:-
- AVTransport
- ConnectionManager
- RenderingControl
- PlayQueue (Frank Z what is this used for ?)
- QPLAY is a upnp extension for chinese music service QQMusic

Arylic Devices are principally "DLNA Renderers" which require a minumum of
- AVTransport
- ConnectionManager
- RenderingControl

To Control and Interrogate the Arylic Devices we only need to consider the following Services
- AVTransport
- RenderingControl

Our instructions for Arylic Deveoplers we will only document DLNA commands that have a relevance to the Arylic Product Range. If you refer to https://developer.arylic.com/docs/ you will see a useful table for funcionality related to the various Interface platforms.

The UPNP/DLNA Interface can be used for the following Functional Requirements:-
    - Playback Control
    - Title and artist
    - Coverart and playlist    

So the documentation is organised by these Functional Requirements and not the Services Provided (AVTransport & Rendering Control) 