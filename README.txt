This is an work-in-progress for the code to run the AG-0 for a Raspberry Pi.

MAVSDK is required to run this system. It can be found here: https://mavsdk.mavlink.io/develop/en/getting_started/installation.html

The MAVLink_connection code will route the GPS lat/lon from a MAVLink message connected over USB to a serial output. This implementation is for an Arduino running the code in the AG-0_Arduino repo that is connected through the Pi's USB port. To run the program, navigate to the build directory and enter:

sudo -S ./MAVLink_connection serial:///dev/ttyACM0

Terminate the program with CTRL-C