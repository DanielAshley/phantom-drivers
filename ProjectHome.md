This project aims to create open source drivers for the [SensAble PHANTOM haptic devices](http://www.sensable.com/products-haptic-devices.htm). Currently the proprietary drivers are not stable enough and unusable for our experiments.

The aims are to fully implement drivers for the PHANTOM Omni device and:
  * prevent crashes of time (stability)
  * allow to control multiple devices connected to one host
  * eventually add other PHANTOM devices to the project (_which we do not have in our possession, so we can use any help from other developers!_)

Currently the status of this project is somewhat less immature: by adding traces to [libraw1394](http://sourceforge.net/projects/libraw1394/), we managed to create an application which drives two (but we think multiple) PHANTOM Omni devices. The positions, forces, buttons and some other status parts can be read/written correctly. This test application is also able to handle bus resets and continue to run when one was issued.

Now a library part is being build (slowely) using the proofs of principle of the test application. The idea is to have a low-level platform specific part (ie libraw1394 and other firewire libraries) to make it (more) OS independent. Currently, the plan in to support Linux and MacOS. The high(er)-level part is to support the PHANTOM devices, depending on our needs it might be possible that we also create an even higher-level part with all kind of matrix, angle, etc calculation functionalities.

This library now is able to communicate with the PHANTOM Omni devices and start/stop isochronous communication with them (ie receive and send the coordinates, button information, forces, etc). Isochronous communication is yet working for the Mac OS layer.

If you feel like to help with this project please let us know! Any help is welcome.

<font size='1'>We are part of the <a href='http://www.ce.utwente.nl/'>Robotics and Mechatronics</a> chair which belongs to the <a href='http://www.utwente.nl/'>University of Twente</a>.</font>