# drew

Homebrew like tool for running Docker images that wrap a binary with local directory access.

## demo

```
$ drew install youtube-dl
vimagick/youtube-dl A small command-line program to download videos from YouTube.com and a few more sites. 12 [OK]

Found 'vimagick/youtube-dl' from the registry, use that? (Y/n): y
Using default tag: latest
latest: Pulling from vimagick/youtube-dl

Digest: sha256:24a24cbddbfc695f210bbf21769c60eea9626cf90fad4f3f9b41279a0bfd22e7
Status: Image is up to date for vimagick/youtube-dl:latest

$ youtube-dl https://www.youtube.com/watch\?v\=AIiW8VllwSg
[youtube] AIiW8VllwSg: Downloading webpage
[youtube] AIiW8VllwSg: Downloading video info webpage
[youtube] AIiW8VllwSg: Extracting video information
[youtube] AIiW8VllwSg: Downloading MPD manifest
[download] Destination: akumusa.swf-AIiW8VllwSg.f133.mp4
[download] 100% of 3.55MiB in 00:02
[download] Destination: akumusa.swf-AIiW8VllwSg.f171.webm
[download] 100% of 2.00MiB in 00:01
[ffmpeg] Merging formats into "akumusa.swf-AIiW8VllwSg.mkv"

$ open akumusa.swf-AIiW8VllwSg.mkv
```

## install

```
git clone https://github.com/matti/drew.git
cd drew
ln -s $(pwd)/bin/drew /usr/local/bin/drew
```

## usage

```
$ drew
   _
 _| |___ ___ _ _ _
| . |  _| -_| | | |
|___|_| |___|_____|

Usage:

drew install {youtube-dl,ffmpeg,...}    # Searches for matches and installs the command
drew install -y youtube-dl              # Uses the first match
drew install -f youtube-dl              # Always overwrites /usr/local/bin/youtube-dl
drew install -yf youtube-dl             # Uses first match, always overwrites
```
