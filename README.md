# Vidyo WebRTC sample

# Build Docker container locally

    $ docker build -t my-image .

# Run Docker container from local image

The container exposes port 80, which needs to be mapped to a local port on the host (e.g. 8000).

You can run it on the foreground for quick tests (and kill it with Ctrl-C):

    $ docker run -ti -p 8000:80 my-image

On in the background (use `docker rm` to kill it):

    $ docker run -d -p 8000:80 my-image

# Run Docker container from published image

CI automation published a new image every time there is commit to this repository.

To start a Docker container based on the public image (in the background, exposing port 8000):

    $ docker run -d -p 8000:80 inclusivedesign/vidyo-webrtc-sample
