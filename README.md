#ScreenCap
![ScreenCap](https://raw.githubusercontent.com/active9/screencap/master/ScreenCap.png)

A Screen Capture (Image & Video) Library

##Introduction
ScreenCap is a screen capturing npm module that allows you to record your desktop to MP4 or animated GIF as well as take Desktop Screen Shots.

##Installing
Windows:
You will need to download and install the following:

 - http://www.microsoft.com/en-us/download/details.aspx?id=3138
 - http://sourceforge.net/projects/screencapturer/
 - http://ffmpeg.org/ *Optional

Using microsoft windows sdk 7 open the CMD Shell supplied with the SDK. Then type the following.
```bash
npm install screencap -g
```

Mac:
You will need to download and install the following:

 - http://brew.sh/

Using the terminal type in the following:
```bash
brew install ffmpeg
npm install screencap -g
```
LInux:

Using bash or the terminal type in the following:
```bash
sudo apt-get install ffmpeg x11grab
sudo npm install screencap -g
```

##USING

ScreenCap is best used stand-alone but may be incorporated into your projects. See the Incorporating section below to use ScreenCap in your own projects.

The stand alone version of ScreenCap is the easiest way to start. Now that you have ScreenCap installed you can record your current desktop by using any of the following methods:

Desktop Recording To MP4
```bash
screencap 5 screen_capture.mp4
```

The above command will execute ScreenCap and record your current desktop to screen_capture.mp4 for duration of 5 seconds. 

Desktop Recording To Animated GIF
```bash
screencap 5 screen_capture.gif
```

This will create a recording of your screen to a down sampled animated GIF image.


Desktop Recording To a PNG Image
```bash
screencap screen_capture.png
```

This will create a screen shot of your screen to a PNG image.
NOTE: Saving to PNG does not require a duration as it is unnecessary for a still image.

##Incorporating

You can use ScreenCap in your own software by including it as a dependency. The following example is a programatic way to take a screen shot using Screen Cap.
```javascript
var screencap = require('screencap');

var screen = screencap({
		videoCodec: "libx264",
		videoBitrate: "1000k",
		audioBitrate: "96k"
	},'test.mp4');
screen.capture('30');
```
The above example would take a Screen Recording of 30 second to an MP4 video.  Notice you may specify your own videoCodec and audio / video Bitrates. More examples are provided within the examples folder.

Piping can also be used to directly render a desktop through a response function such as express res. The most basic example is to pipe the screen to an express server.

```javascript

```

##CONTRIBUTING

We encourage forking. Feel free to fork & pull your new additions, or bug fixes.
