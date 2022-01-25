# This is a public script and a work in progress. 
# A RPi project to control the antique Technic Lego Crane, built from the 8094 set with PWM, the aim is to estimate the slew position, the lift and the extend, by setting initial conditions and logging the duty cycle, frequency, time and polarity of the signal through the H Bridge.  

STAR Python Control Script

SITUATION:- Plugged in model crane into the Raspberry Pi via the H-Bridge and when the power was turned on the crane slewed continously with no command from the Python script, writing a line to force all the GPIO outputs to go to ground worked however the crane would still slew on power up and only stopped when the script was run.

The TASK was to prevent this from occuring.

ACTION:- The config file was edited sudo nano/boot/config and added GPIO.op.dl to the end of the file.

RESULT:- Changing the boot parameters in this way prevented movement of the motors during power up.
