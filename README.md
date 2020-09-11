# OpenCV Live Feed Application

This application pulls a live feed from a user's webcam, draws red squares around any moving body parts in-frame, then tunnels this image stream to the public web via ngrok.

## Installation

First, ensure that python3 and virtualenv are installed on your machine.

Make a new directory for the project and cd into it.

```mkdir MyLiveFeed```
```cd MyLiveFeed```

Start a virtualenv for this project named "venv".
```virtuelenv venv```
```source venv/bin/activate```


