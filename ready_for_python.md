# 准备Python环境

树莓派的Linux系统默认已经安装好Python环境。我们可以执行以下指令安装MegaPi和OpenCV相关的支持。
```
sudo pip install megapi
sudo apt-get update && sudo apt-get install git python-opencv python-all-dev libopencv-dev
```
用户可以访问```https://github.com/makeblock-official/PythonForMegaPi``` 找到MegaPi相关源代码。


### Python 接口

 * 开始
 	* **MegaPi**()
 	* **start**()
 	
 * 通用输入输出
 	* **digitalWrite**( pin, level )
 	* **pwmWrite**( pin, pwm )
 	* **digitalRead**( pin, **def** onResult )
 	* **analogRead**( pin, **def** onResult )
 	
 * 运动类
	* 直流电机
	  * **dcMotorRun**( port, speed )
	* 舵机
	  * **servoRun**( port, slot, angle )
	  * **servoPinRun**( pin, angle )
	* 编码电机
	  * **encoderMotorRun**( port, speed )
	  * **encoderMotorMove**( port, speed, distance, **def** onFinish )
	  * **encoderMotorMoveTo**( port, speed, position, **def** onFinish )
	* Stepper Motor
	  * **stepperMotorSetting**( port, microsteps, acceleration )
	  * **stepperMotorRun**( port, speed )
	  * **stepperMotorMove**( port, speed, distance, **def** onFinish )
	  * **stepperMotorMoveTo**( port, speed, position, **def** onFinish )
	  
 * Sensors
 	* Ultrasonic Sensor
 	  * **ultrasonicSensorRead** ( port, **def** onResult ) 
 	* LineFollow Sensor
 	  * **lineFollowerRead** ( port, **def** onResult ) 
 	* Light Sensor
 	  * **lightSensorRead** ( port, **def** onResult ) 
 	* Sound Sensor
 	  * **soundSensorRead** ( port, **def** onResult ) 
 	* Temperature Sensor
 	  * **temperatureRead** ( port, **def** onResult ) 
 	* PIR Motion Sensor
 	  * **pirMotionSensorRead** ( port, **def** onResult ) 
 	* Touch Sensor
 	  * **touchSensorRead** ( port, **def** onResult ) 
 	* LimitSwitch
 	  * **limitSwitchRead** ( port, slot, **def** onResult ) 
 	* Humiture Sensor
 	  * **humitureSensorRead** ( port, type, **def** onResult ) 
 	* Gas Sensor
 	  * **gasSensorRead** ( port, **def** onResult )
 	* Flame Sensor
 	  * **flameSensorRead** ( port, **def** onResult ) 
 	* Button
 	  * **buttonRead** ( port, **def** onResult ) 
 	* Potentiometer
 	  * **potentiometerRead** ( port, **def** onResult )
 	* Joystick
 	  * **joystickRead** ( port, axis, **def** onResult )
 	* 3-Axis Accelerometer and Gyro Sensor
 	  * **gyroRead** ( axis, **def** onResult )
 	* Compass
 	  * **compassRead** ( **def** onResult )
 	
 * Display
 	* RGB Led
 	  * **rgbLedSetColor** ( port, slot, index, r, g, b )
 	  * **rgbLedShow** ( port, slot )
 	  * **rgbLedDisplay** ( port, slot, index, r, g, b )
 	* 7-segment Display
 	  * **sevenSegmentDisplay** ( port, value )
 	* Led Matrix Display
 	  * **ledMatrixDisplayMessage** ( port, x, y, msg )
 	  * **ledMatrixDisplayRaw** ( port, buffer )
 	* Serial LCD Display
 	  * **lcdDisplay** ( string )
 	  
 * Others
 	* DSLR Shutter
	  * **shutterOn** ( port )
	  * **shutterOff** ( port )
	  * **focusOn** ( port )
	  * **focusOff** ( port )
