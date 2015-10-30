# Logging #


During flight two log files are created
  * data log file - containing navigation and attitude data
  * kml log file - containing data about flight path and waypoints

Files are saved in the GCS application "data" folder

![http://ardupilotgcs.googlecode.com/svn/images/GCSloggingExpl.jpg](http://ardupilotgcs.googlecode.com/svn/images/GCSloggingExpl.jpg)

For both files, all data is logged as is received. During the flight kml file will be called APflight.kml, however after GCS exits, it will be renamed "APflight\_year\_month\_day\_hour\_minute\_sec.kml" . For example "APflight\_2010\_05\_07\_23\_29\_47.kml" was created on May 7th, 2010 at 11:29:47 pm.

Same file naming scheme goes for data log file - "ArduPilot\_DataLog\_2010\_05\_07\_23\_28\_54.txt".

## Data Log File ##

Data log file will log navigational and attitude data as is received. Since those two data sets arrive at different intervals, only data from the received set is logged, and other columns are left blank.

All data is defined by and passed from ArduPilot, with exception of "t(ms)". Time in milliseconds or "t(ms)" is time when GCS received given data set. Although not accurate to millisecond when on-board ArduPilot processed it, it is still useful as a diagnostics and informational tool since time differences between data sets can be discerned. Time starts to tick when GCS is launched.

It is worth mentioning that if IMU is present fields with IMU data will be populated, otherwise they will be logged with 0

Data is logged as tab delimated ASCII text. Example data log file:

```
t[ms]	ASP	THH	RLL	PCH	CRS (IMU)	IMU	ch3_in	LAT	LON	SPD	CRT	ALT	ALH	CRS	BER	WPN	DST	BTV	RSP
...

39048	30	50	10	10	5	80	3500													
39141	30	50	10	10	5	80	3500													
39397	30	50	10	10	5	80	3500													
39669	30	50	10	10	5	80	3500													
39941								37632200	-122491200	20	100	20	30	5	120	1	100	7	100
40211	30	50	10	10	5	80	3500													
40483	30	50	10	10	5	80	3500													
40738	30	50	10	10	5	80	3500													
41009	30	50	10	10	5	80	3500													
41281								37632210	-122491200	20	100	20	30	5	120	1	100	7	100
41552	30	50	10	10	5	80	3500													
41824	30	50	10	10	5	80	3500

...

```


## KML Log File ##

During ArduPilot power-up, if any waypoints are stored in memory, it will be transmitted to GCS and logged (as well as displayed on the Google Earth Map). (**Note:** since you should not have your Xbee telemetry wireless modules connected to ArduPilot on power up, if you want the GCS to capture these waypoints, press the ArduPilot reset button after powerful to restart the autopilot and retransmit the waypoint data.) During flight, data will be logged as is received. After the flight this file can be viewed in any application that supports kml viewing (ex. Google Earth) - no more post processing ( now you quickly upload your flight for others to see).

Example of (simulated) flight displayed in GE:

![http://ardupilotgcs.googlecode.com/svn/images/LoggingGE1.jpg](http://ardupilotgcs.googlecode.com/svn/images/LoggingGE1.jpg)



You can also change view to see flight path - yellow bars indicate where location data is received. Hint: you can have same view in real time while  GCS is running if you adjust controls in the "Setup" Tab

![http://ardupilotgcs.googlecode.com/svn/images/LoggingGE2.jpg](http://ardupilotgcs.googlecode.com/svn/images/LoggingGE2.jpg)