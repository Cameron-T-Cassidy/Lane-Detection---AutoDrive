
The majority of this code came from https://github.com/tomazas/opencv-lane-vehicle-track
However, I've made the following imrpovements:
	-Updated the 2012 MIT Haar classifer to a better one from CalTech
	-Increased sensitivity in greyscale, to detect yellow lanes
	-Removed noisy lanes
	- Shortened response time between lane curvature and projected lanes. 
	-rejoined cropped lane detection images. 
PreRequs:
	-Reinstall/test OpenCV, and dependencies: https://www.learnopencv.com/install-opencv3-on-ubuntu/
	-Install XMing, if using an emulator. 
Local Comannd Line variables:
	*these must be done every time the terminal is opened*
	-Set Display out: export DISPLAY=:0
	-Disable bus security policies: sudo ln /dev/null /dev/raw1394
Compile:
	-g++ `pkg-config --cflags opencv` main.cpp `pkg-config --libs opencv` -o a
Run:
	./a
Options:
	I've disabled the greyscale and binary image video feeds, To turn them one, uncomment them in 
	main() at line ~620.
	
	



 
