# Setting Up and Using Ground Control Station #

Make sure that you installed and configured hardware per [ArduPilot Instructions](http://code.google.com/p/ardupilot/wiki/IntroductionPage).
Don't power-up ArduPilot yet.

Start GCS by clicking on the application.

http://ardupilotgcs.googlecode.com/svn/images/GCSwinexplorer2.JPG


Ground Control Station application and Google Earth will load and you should see screen like the following:


![http://ardupilotgcs.googlecode.com/svn/images/GCS1.jpg](http://ardupilotgcs.googlecode.com/svn/images/GCS1.jpg)




Click on **Setup Tab**


Choose _COM Port_ and _Baud Rate_ ( red arrows ) where ArduPilot will connect to. Press _Connect_ ( although ArduPilot is not powered-up GCS will "listen and wait" on that port for it).

Note that _Boaud Rate_ has helpful hints dor identifications of EM 406 and uBlox GPS-es. Also next time you start GCS it will "remember" these settings and automatically connect to them. If your ArduPilot settings have changed, just set them again on this screen

![http://ardupilotgcs.googlecode.com/svn/images/GCS2.jpg](http://ardupilotgcs.googlecode.com/svn/images/GCS2.jpg)


Power-up ArduPilot. When connection is made with GCS _Communication Status_ indicator in the upper right corner will turn from red to green and you will also see "GCS Port Set" message ( red arrows). Click back to the _Main_ tab to see ArduPilot data displayed.

If you had waypoints "pre-loaded" in the ArduPilot they will be displayed on the Google Earth map - "balloon" with waypoint number next to it ( green arrows). As plane icon moves on the map you will be able to see it's path traced in yellow.

![http://ardupilotgcs.googlecode.com/svn/images/GCS3.jpg](http://ardupilotgcs.googlecode.com/svn/images/GCS3.jpg)

That's it - enjoy the flight ! ( or check out some of the [GCS Features](GCSfeatures.md) )