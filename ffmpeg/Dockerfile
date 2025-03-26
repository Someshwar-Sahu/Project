FROM ubuntu:24.04

RUN apt update
RUN apt install -y ffmpeg

WORKDIR /media
COPY 12.mp4 .

# Define the entry point
ENTRYPOINT ffmpeg -re -i 12.mp4 -c:v libx264 -c:a aac -f flv rtmp://nginx-c/hls/my-video
