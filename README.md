# OpenCV Live Feed Application

This application pulls a live feed from a user's webcam, draws red squares around any moving body parts in-frame, then makes this video feed accessible to the public web via ngrok.

## Installation

First, ensure that python3, virtualenv, and git are installed on your machine.

Enter Terminal on Mac or the command line on Windows. Navigate to your home directory. Now, make a new directory for the project and cd into it.

```mkdir MyLiveFeed```

```cd MyLiveFeed```

Start a virtual environment for this project named "venv". A virtual environment (or virtualenv) allows an application to have its own set of installed packages that are independent of those on your machine.

```virtuelenv venv```

Activate the virtual environment.

```source venv/bin/activate```

Clone this git repository into your application directory.

```git clone https://github.com/skhan117/OpenCV-Live-Feed```

cd into the directory.

```cd OpenCV-Live-Feed```

We need to install the proper libraries in the application's virtual environment. The libraries needed are listed in requirements.txt, so we just pip3 this text file.

```pip3 install -r requirements.txt```

Get the application up and running on your machine with the following command. The application will be accessible on your machine on port 8004.

```python3 webstreaming.py -i 0.0.0.0 --port 8004```

Now open a web browser and enter "http://localhost:8004" into your search bar. You should be able to see a live video feed being pulled from your webcam. While you're in view of the video frame, move your arms to confirm that the application detects motions and superimposes red squares onto moving body parts. 

To exit the app, hit Control-C. 

We now have an application that can run on our local machine, but we need to be able to serve this video feed onto the public web. There are different ways to do this, but for this project we'll use the free ngrok service, which allows public web traffic to be "tunneled" to the application's port while it's running on your machine.

First, navigate to ngrok.com, sign up for the free service, and download ngrok to your machine.

If it isn't alraedy, get the application up and running on port 8004. 

```python3 webstreaming.py -i 0.0.0.0 --port 8004```

Now open a new Terminal or command line window. Navigate into the ngrok directory, the type in the following command to open an HTTP tunnel to your local port 8004, where the video feed application is accessible.

```./ngrok http 8004```

Ngrok will generate a publicly accessible IP address where you can see your feed. Navigate to this address with your browser, and you should be able to see your live feed running on the public web. 

When you're done using the Video Feed App and the NGrok service, terminate them by typing in Control-C. 