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
	  * **servoRunAtPin**( pin, angle )
	* 编码电机
	  * **encoderMotorRun**( port, speed )
	  * **encoderMotorMove**( port, speed, distance, **def** onFinish )
	  * **encoderMotorMoveTo**( port, speed, position, **def** onFinish )
	* 步进电机
	  * **stepperMotorSetting**( port, microsteps, acceleration )
	  * **stepperMotorRun**( port, speed )
	  * **stepperMotorMove**( port, speed, distance, **def** onFinish )
	  * **stepperMotorMoveTo**( port, speed, position, **def** onFinish )
	  
 * 传感器类
 	* 超声波测距传感器
 	  * **ultrasonicSensorRead** ( port, **def** onResult ) 
 	* 巡线传感器
 	  * **lineFollowerRead** ( port, **def** onResult ) 
 	* 光线传感器
 	  * **lightSensorRead** ( port, **def** onResult ) 
 	* 声音传感器
 	  * **soundSensorRead** ( port, **def** onResult ) 
 	* 温度传感器
 	  * **temperatureRead** ( port, **def** onResult ) 
 	* 人体热释电传感器
 	  * **pirMotionSensorRead** ( port, **def** onResult ) 
 	* 触摸传感器
 	  * **touchSensorRead** ( port, **def** onResult ) 
 	* 限位开关
 	  * **limitSwitchRead** ( port, slot, **def** onResult ) 
 	* 湿度传感器
 	  * **humitureSensorRead** ( port, type, **def** onResult ) 
 	* 瓦斯传感器
 	  * **gasSensorRead** ( port, **def** onResult )
 	* 火焰传感器
 	  * **flameSensorRead** ( port, **def** onResult ) 
 	* 按钮
 	  * **buttonRead** ( port, **def** onResult ) 
 	* 电位器
 	  * **potentiometerRead** ( port, **def** onResult )
 	* 角度传感器
 	  * **angularSensorRead** ( port, slot, **def** onResult )
 	* 摇杆
 	  * **joystickRead** ( port, axis, **def** onResult )
 	* 3轴加速度计和陀螺仪
 	  * **gyroRead** ( axis, **def** onResult )
 	* 指南针
 	  * **compassRead** ( **def** onResult )
 	
 * 显示类
 	* RGB Led
 	  * **rgbLedDisplay** ( port, slot, index, r, g, b )
 	  * **rgbLedShow** ( port, slot )
 	* 数码管
 	  * **sevenSegmentDisplay** ( port, value )
 	* Led矩阵屏
 	  * **ledMatrixDisplayMessage** ( port, x, y, msg )
 	  * **ledMatrixDisplayRaw** ( port, buffer )
 	* 串口液晶屏
 	  * **lcdDisplay** ( string )
 	  
 * 其它
 	* 快门控制器
	  * **shutterOn** ( port )
	  * **shutterOff** ( port )
	  * **focusOn** ( port )
	  * **focusOff** ( port )
