# Capture-iOS-Simulator-video

how to control the Simulator with command line ?

 > see the built-in help to check what simctl can do
```
xcrun simctl
```

 > take a screenshot or record a video from a simulator using the following command line
 >  <br>```xcrun simctl io <device> <operation> <arguments> ```

 - take a screenshot

```
xcrun simctl io booted screenshot ~/Desktop/screenshot.png
```


 - start to record a video

```
xcrun simctl io booted recordVideo ~/Desktop/simulator.mov
```

 - end recording

```
control + c
```

> Convert the iPhone 6s screen shot into a gif:
```
ffmpeg -i ~/Desktop/simulator.mov -vf scale=320:-1 -r 6 -f gif -y ~/Desktop/simulator.gif
```
