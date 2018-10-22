**Read IOT data from Raspberry Pi**

About: 

	- This is a sample program written in Python that is executable in Raspberry.

	- Basically we read the Pressure, Temperature and Humidity data from the SenseHat in the raspberry PI.
	
Data Collection:

	- We are using the Sense Hat with the Raspberry PI. For now, we are just using it to measure Pressure, Temperature and Humidity
	- Readings are take every hour and is stored in memory. Every 24 hours i.e at the end of the day the readings are then transfered to a physical file. 
	- Separate files are created for Pressure, Temperature and Humidity.
	- On each day a new file is created so we have 3 files each day, each with 24 readings.
	
Data Correction with Temperature Sensor

	- The Sense hat goes right above the Raspberry. As a consequence, the CPU temperature of the Raspberry itself causes the Sense hat data to be incorrect.
	- We had to introduce certain correction factors.
	  The corrected temperature was calculated with relation as:
			t_corr = t - ((t_cpu - t) / 1.5)


	Where, t_corr = Corrected temperature, t is the average of temperature computed from humidity and temperature computed from pressure and t_cpu is the CPU temperature. Though the temperature readings are better but not completely accurate.
	
	
Steps to run:
	- Run CreateData.py
	- 
Note: Intro.py is optional, we just added it for cool effects in the SenseHat LED. 