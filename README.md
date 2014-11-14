Autoboat
========
_Autonomous boat base station setup_

For use with autonomous (Pixhawk) MOKAI jetboat performing waypoint navigation.

Setup
-----
Initialize the QGroundControl (QGC) and MavLink submodules:

```bash
git submodule update --init --recursive
```

The following are the minimal necessary steps required to get QGC set up in
Ubuntu. For full instructions, see the [official
readme](https://github.com/mavlink/qgroundcontrol#build-on-linux).

```bash
sudo apt-get install qtcreator qttools5-dev qtbase5-dev qt5-default qtdeclarative5-dev libqt5serialport5-dev libqt5svg5-dev libqt5webkit5-dev libsdl1.2-dev build-essential libudev-dev
cd qgroundcontrol
qmake
make
```

If anything goes wrong, refer to the [build
notes](https://github.com/mavlink/qgroundcontrol#additional-build-notes-for-all-supported-os).

Boat
----
For now, this is meant to control an autonomous (modified) MOKAI jetboat
capable of:

  * TODO: Manual and automatic (watchdog) kill
  * TODO: Remote start/stop
  * TODO: Operation with radio dropouts

The boat will be controlled by a Pixhawk with a Digi XTend radio link.
Potential expansion to Iridium satellite link in the future.

Off-the-shelf, the MOKAI boat is drive-by-wire. Once the boat arrives, we will
need to splice the Pixhawk into the control electronics.


Base
----
QGroundcontrol, usage TBD.
