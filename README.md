# OpenWebRTC fork of cerbero

## How do I use this?

[Using this cerbero fork to build OpenWebRTC](https://github.com/EricssonResearch/openwebrtc/wiki/Building-OpenWebRTC)

## What is cerbero?

[cerbero](http://cgit.freedesktop.org/gstreamer/cerbero/) is a build system
written by GStreamer developers to build all GStreamer dependencies, GStreamer
itself and package it up into nice platform-specific SDK-like binary files.

## Why a fork?

OpenWebRTC needs some extra dependencies that are not desirable to have in
upstream cerbero. OpenWebRTC also needs some bits and pieces built in specific
ways to meet our needs.

We like collaboration and hope the use of cerbero to build OpenWebRTC will be
mutually beneficial. *All real cerbero changes are being submitted upstream!*

## Branches

`master` - Contains upstream's master branch.

`ZOO-10288-update-custom_ice_compat` - Contains upstream's master branch changes as of February 2016 with our custom fixes and modifications for libnice and OpenWebRTC itself.

`blank_frame_fixes` - OBSOLETE. Attempts to fix the flickering.

`custom_ice_compat` - Added Google ICE compatibility mode.

`custom` - Using custom libnice and OpenWebRTC forks. Probably obsolete.

