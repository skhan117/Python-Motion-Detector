# OpenCV Live Feed Application

This application pulls a live feed from a user's webcam, draws red squares around any moving body parts in-frame, then tunnels this image stream to the public web via ngrok.

## Installation

First, ensure that python3, virtualenv, and git are installed on your machine.

Make a new directory for the project and cd into it.

```mkdir MyLiveFeed```

```cd MyLiveFeed```

Start a virtual environment for this project named "venv". A virtual environment (or virtualenv) allows an application to have its own set of installed packages that are independent of your machine.
```virtuelenv venv```

Now activate the virtual environment.
```source venv/bin/activate```

Now clone this git repository into your application directory.
```git clone https://github.com/skhan117/OpenCV-Live-Feed```

cd into the directory.
```cd OpenCV-Live-Feed```

Now we need to install the proper libraries in the application's virtual environment. The libraries needed are listed in requirements.txt, so we just pip3 this text file.
```pip3 install -r requirements.txt```