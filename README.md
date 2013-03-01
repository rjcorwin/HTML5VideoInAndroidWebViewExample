HTML5VideoInAndroidWebViewExample
=================================

Here's an example app that, on the loadRemoteFileFromHTTP branch, successfully loads a video file in a webview from a remote location. On the loadLocalFileUsingFileReader branch, the test.m4v file exists on the SD Card of he the device by being referenced as file:///mnt/sdcard/external_sd/test.m4v. The gotcha is when you trying to include the video file in your App. There's no way to use the file:/// protocol to reference something in your App and you cannot use relative URLs for referencing videos in a WebView. In other words, if you have your video file in your assets/www directory and you set src to "nameOfVideo.mp4", it plain won't work :(. See the loadLocalFileUsingRelativeURL branch for an example.
