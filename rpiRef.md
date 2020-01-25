# Quick References For Raspberry Pi

## Using RPi.GPIO library

some common methods 
```python
import RPi.GPIO as GPIO
import time

# Define which type of numbering we will be using is the physical numbering
GPIO.setmode(GPIO.BOARD)

## OR USE THE OTHER MODE

# Define which type of numbering we will be using is the one defined by the Broadcom SOC channel
GPIO.setmode(GPIO.BCM)

# Use variables to access pin values
pin1 = 11

# Configure GPIO pins as input or Output pins
GPIO.setup(pin1,GPIO.OUT)

# Set (Turn ON) respective GPIO pin
GPIO.output(pin1,True)
time.sleep(1)

# Reset (Turn OFF) respective GPIO pin
GPIO.output(pin1,False)

# clean up (Reset) all the ports you’ve used
GPIO.cleanup()
```

