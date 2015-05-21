# OpenWebRTC fork of cerbero

## Changes by AlertMe are located on branch 'custom'

To use just do 'git checkout custom' then follow the build instructions

## How to make changes in projects that cerbero builds?

Checkout the project (for example https://github.com/AlertMe/openwebrtc).
Make your change and commit it locally.
Then edit the recipe file for the project (for example recipes/openwebrtc.recipe) and modify the Recipe class so that your local copy of the project is used

```python
class Recipe(recipe.Recipe):
     name = 'openwebrtc'
     version = '0.1'
     _api_version = '0.1'
     stype = SourceType.GIT
     licenses = [License.BSD_like]
     remotes = {
     # Custom repo on GitHub 'AlertMe/openwebrtc'
     #'origin': 'https://github.com/AlertMe/openwebrtc.git'
     # For development one can use a local revision
      'origin': '<path_to>/openwebrtc'
     }
     # Which commit to be picked up from local/remote repo
     commit = '3b8d84c4415907ef363618ace0ff9a637862cc01'
}
```

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
