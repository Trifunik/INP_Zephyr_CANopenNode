
Zephyr OS - CANopenNode Sample for Industrial Network Playground
================================================================

This is a copy of, and adaptation of, the Zephyr OS CANopen node example for my hobby project, `Industrial Network Playground <https://hackaday.io/project/193862-industrial-network-playground>`_

The original code can be found here: `canopennode <https://github.com/zephyrproject-rtos/zephyr/tree/main/samples/modules/canopennode>`_ The original README can also be found in this repository (`README_original.rst <https://github.com/Trifunik/INP_Zephyr_CANopenNode/README_original.rst>`_) and should be read to understand this example.

The following information refers to my changes and adaptations.

Done
****
- Added devicetree overlay for CAN (TWAI) for M5Stack Atom Lite target.


NOTE - Modifying the Object Dictionary
**************************************
The version of the EDS editor that is currently used in the CANopen implementation of Zeyphr has a small bug.
The define CO_NO_TIME is written as CO_NO_TS. As suggested in `issue #33149 <https://github.com/zephyrproject-rtos/zephyr/issues/33149>`_, I have added zephyr_compile_definitions(CO_NO_TIME=CO_NO_TS) to the CMakeLists.txt.



Todo
****
- Enable LSS
- Create a I2C slave on the Raspi and build a sensor simulator
- Read out the simulated sensor
