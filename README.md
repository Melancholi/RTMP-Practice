# RTMP-Practice

Quick demo to work on RMTP protocol using docker and OBS studio

## 1. Setup (Docker)

Simply run

`bash
docker compose up -d
`
*
This simply boots up your rtpm server on **locahost:1935**

## 2. Setup (OBS)

On OBS studio, you have to create a custom connection that will stream to your RTMP Server

Go to **File > Settings > Stream > Custom Service**

For the server, just fill it with the protocol and your ip:host

In this case it would be **rtmp://localhost:1935/live** (live is the name of the application defined in the nginx.conf)

The stream key is used to identify your stream and make it accessible.

Click apply and OK, then you can start streaming

### Accessing your stream

Pretty simple, either use a media player like VLS to access the rtmp server

Go to **Media > Open Network Stream > Enter a network URL:**

Then from there enter the stream URL you used for OBS + **the stream key** it should be something similar to this:

rtmp://localhost:1935/live/test
