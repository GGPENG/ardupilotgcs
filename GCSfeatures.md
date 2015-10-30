# GCS Features #

Main feature differences from earlier version:
  * log file - navigation and attitude data
  * kml log file - kml data showing flight path and waypoints
  * voice synthesis


> ## General ##

![http://ardupilotgcs.googlecode.com/svn/images/GCSfgeneral.jpg](http://ardupilotgcs.googlecode.com/svn/images/GCSfgeneral.jpg)

  1. STOP button - use to exit GCS application.
  1. Communication Status - indicates if GCS can communicate with ArduPilot. Red means no communication; Green - communication established
  1. Message Box 1 - various status messages
  1. Tabs - click on them to access various ArduPilot data or GCS settings
  1. Battery, Throttle, and IMU health indicators. IMU health indicator is based on 0-100% scale, and it's data will be displayed if IMU is present on the system, otherwise it will display N/A
  1. Climb Rate
  1. Message Box 2 - various information ( flight mode, etc.)
  1. Navigation Display - waypoint, distance to waypoint, and plane's latitude and longitude information
  1. Google Earth map - displays map with plane location and flight path


## Main Tab ##

![http://ardupilotgcs.googlecode.com/svn/images/GCSfmainTab.jpg](http://ardupilotgcs.googlecode.com/svn/images/GCSfmainTab.jpg)

  1. Altimeter - indicates current altitude and altitude hold
  1. Artificial Horizon - indicates roll and pitch
  1. Speedometer - indicates air speed and ground speed
  1. Course and Bearing indicator


## Setup Tab ##

![http://ardupilotgcs.googlecode.com/svn/images/GCSfsetupTab.jpg](http://ardupilotgcs.googlecode.com/svn/images/GCSfsetupTab.jpg)

  1. Communication Settings - Select port and baud rate to communicate with ArduPilot
  1. Announcement Interval - selects interval for voice synthesis rate of announcements ( default is every 30 seconds). Spoken message will convey waypoint, altitude and ground speed - ex: "En route to waypoint 2, altitude 50 meters, ground speed is 30 meters per second". Mute your speakers if you do not wish to hear audio messages.
  1. kml update interval - set how often to update kml ( Google Earth) display. Note that this des not affect how ofthen to log data, since all of the data will be logged as it arrives, but rather this setting dictates how often to update display.
  1. Google Earth Controls - Control display of Google Earth view via zoom, pan and tilt. Since kml data will show flight path as it is generated, changing the view angles may provide for some interesting visualization.



## IMU Tab ##

![http://ardupilotgcs.googlecode.com/svn/images/GCSfimuTab.jpg](http://ardupilotgcs.googlecode.com/svn/images/GCSfimuTab.jpg)

  1. IMU data - If IMU is present, IMU data as provided by ArduPilot, will be sisplayed
  1. IMU health - unscaled numerical value of IMU health variable


## Debug Tab ##

![http://ardupilotgcs.googlecode.com/svn/images/GCSfdebugTab.jpg](http://ardupilotgcs.googlecode.com/svn/images/GCSfdebugTab.jpg)

  1. Raw Data set - current data as received by the ArduPilot
  1. Debug/ Non Telemetry data - cumulative debug or non telemetry data received during flight