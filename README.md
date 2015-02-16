Autoboat
========
_Autonomous boat base station setup_

For use with autonomous (Pixhawk) MOKAI jetboat performing waypoint navigation.

Setup
-----
Initialize the APM Planner and MavLink submodules:

```bash
git submodule update --init --recursive
```

The following are the minimal necessary steps required to get APM Planner set up in
Ubuntu. For full instructions, see the [official
readme](https://github.com/diydrones/apm_planner#linux-).

```bash
sudo apt-get update
sudo apt-get install git qt5-qmake qt5-default \
       qtscript5-dev libqt5webkit5-dev libqt5serialport5-dev \
       libqt5svg5-dev libsdl1.2-dev  libsndfile-dev \
       flite1-dev libssl-dev libudev-dev libsdl2-dev

cd apm_planner
qmake qgroundcontrol.pro
make
```

Run APM Planner:

```bash
./release/apmplanner2
```


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
APM Planner, usage TBD.
