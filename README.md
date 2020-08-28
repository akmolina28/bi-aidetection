# ** New Features in this Fork **
Added a camera setting which optionally saves relevant images to a pre-configured network path. The images are given the same name as the camera and they overwrite each time a new relevant alert is processed.

This can be used to generate a static image camera in Home Assistant. For example:
1. Designate a shared folder on the Home Assistant machine for alert images
2. Set up the shared folder as a network drive on the Blue Iris host, save the credentials permanently
3. Configure the network drive in the new setting in the AI Tools UI
4. Check the box for each camera in AI Tools which should generate alert images into the network path
5. Add camera integrations for the static images in HA:

```
camera:
- platform: generic
  still_image_url: 'http://127.0.0.1:8123/local/images/ai_alerts/Driveway Car.jpg'
  name: Driveway Car Alert
```

# AI Detection for Blue Iris
Alarm system for Blue Iris based on Artificial Intellience. Can send alerts to Telegram.

### Download
https://github.com/gentlepumpkin/bi-aidetection/releases
Click "> Assets" to find the .zip file.

### Install guide and discussion
https://ipcamtalk.com/threads/tool-tutorial-free-ai-person-detection-for-blue-iris.37330/

### Key Features
- analyze Blue Iris motion alerts using Artificial Intelligence and sort out false alerts
- detect humans and selected objects
- send alert images to Telegram using a bot (optional)
- one alert image per event
- statistics and individual configuration for every camera

### Screenshot
![Screenshot](https://ipcamtalk.com/attachments/processing1-53-png.44807/)

### How to contribute
1. install Visual Studio
2. download project as .zip and unpack somewhere
3. go to ./src/ and open bi-aidetection.sln with Visual Studio.

Using the Github extension for Visual Studio:
1. install Visual Studio
1. install Github Extension from here https://visualstudio.github.com/
2. Click the green button "clone or download" above this text
3. Select "Open in Visual Studio"
