# Docker image for transmission torrent client

A Docker image for Transmission torrent client based on Debian Jessie.

The web interface:

* User: `transmission`
* Password: `secret`
* Url: `http://<host>:9091/transmission/web/`

## Build

`docker build -t transmission .`

## Run

`docker run -d --name transmission -p 6669:6669 -p 6669:6669/udp -p 9091:9091 -v /torrent/downloads/:/downloads -v /torrent/incomplete/:/incomplete transmission`
