# Quadcopter
***
##The Command type:

Notice:The capital letters and small letters  represent different command type.

Case 'a':
		stop all motors(Set all motors speed to 0)

Case 'b':<br>
		type1(now using):<br>
		Increase all motors speed;<br>
		type2(developing):<br>
		Increase the Height(by change the Set_point of height);<br>
		
Case 'c':<br>
		type1(now using):<br>
		Decrease all motors speed;<br>
		type2(developing):<br>
		Decrease the Height(by change the Set_point of height);<br>
		
Case 'd':
		no-use command<br>

Case 'e':
		This command is used to turn the mode to physical controller.<br>

***
Notice!!!
		
How to determine left,right,front and back?

Belowing are OUR definations  

	+Y:front(M3) 
	-Y:back (M1) 
	+X:right(M4) 
	-X:left (M2) 
		
Case 'f':
		This command is used to make the quadcopter move left.(with a MAX_ANGLE == 40).
		
Case 'h':
		This command is used to make the quadcopter move right.(with a MAX_ANGLE == 40).

Case 't':
		This command is used to make the quadcopter move forward.(with a MAX_ANGLE == 40).
		
Case 'g':
		This command is used to make the quadcopter move backward.(with a MAX_ANGLE == 40).

Case 'v':
		This command is used to make the quadcopter stay horizonal.(setpoint_x = 0;setpoint_y = 0;).
		

***		
Belowing are some commands of turing PID,you must type "#define turning_pid" to enable the following commands.
Case 'p': Change the tuning mode to tuning Kp.

Case 'i': 
		Change the tuning mode to tuning Ki.

Case 'o': 
		Change the tuning mode to tuning Kd.

Turning Scale setting: <br>
The default values of Tuning scale are: 2% , 1%  and 0.5% , you can change the value by modify the following code: <br>
	 
	#define scale_large 0.02
	#define scale_mid 0.01  
	#define scale_small 0.005 
	

		
Case 'q':
		Set the tuning_scale to Large(Default is 2%)

Case 'r':
		Set the tuning_scale to Middle(Default is 1%)

Case 's':
		Set the tuning_scale to Small(Default is 0.5%)


Case 'x':Decrease the coeffcient of pid_x by the setting before.(tuning scale and tuning mode). 

Case 'X':Increase the coeffcient of pid_x by the setting before.(tuning scale and tuning mode). 

Case 'y':Decrease the coeffcient of pid_y by the setting before.(tuning scale and tuning mode). 

Case 'Y':Increase the coeffcient of pid_y by the setting before.(tuning scale and tuning mode). 
***

Belowing are some commands of the EEPROM operation

Case '@':Save the pid coeffcients (IN THE MEMORY OR REGISTER!!!!) into EEPROM.

Case '!':Show the pid coeffcients in the EEPROM.

Case '#':Show the pid coeffcients (IN THE MEMORY OR REGISTER!!!!) on the screen

Case '$':Reload the pid coeffcients from EEPROM to MEMORY OR REGISTER.
