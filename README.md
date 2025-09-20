# RISC-V-SoC-Tapeout---WEEK-0

For First Week, we have an introduction to SoC Design Flow and installation of tools like Yosys, iverilog and gtkwave.

# SoC Design Flow Overview

This flow explains how a System-on-Chip (SoC) moves from specifications to real-world applications:

- Chip Modeling (O1):- Define specs in a C model with C-based testbenches for functional verification.
- RTL Design (O2):– Describe the hardware using RTL (Verilog), covering processors, peripherals, and IPs.
- SoC Integration (O3):– Combine gate-level netlists, synthesized macros, analog IPs, and GPIOs into a unified SoC.
- Final Chip (O4):– The integrated design runs at real operating frequencies (e.g., 100–130 MHz) and is verified again with C-based testbenches.

After ASIC synthesis and RTL-to-GDSII (RTL2GDS) flow—which includes floorplanning, placement, clock tree synthesis, routing, and DRC/LVS checks—the final GDSII is sent for fabrication.
The end result is silicon chips powering real products like iWatches, Arduino boards, TV panels, and AC controllers.

# Tool Installations

1) Yosys:- Yosys is an open-source logic synthesis tool used mainly in digital hardware design. Its purpose is to take a Register Transfer Level (RTL) description (usually written in Verilog) and translate it into a gate-level netlist that can be mapped to standard cell libraries, FPGAs, or other target technologies. Basically it is used for synthesis.

The following commands are used to instal Yosys in linus terminal environment

,,,

$ sudo apt-get update
$ git clone https://github.com/YosysHQ/yosys.git
$ cd yosys
$ sudo apt install make (If make is not installed please install it)
$ sudo apt-get install build-essential clang bison flex \
libreadline-dev gawk tcl-dev libffi-dev git \
graphviz xdot pkg-config python3 libboost-system-dev \
libboost-python-dev libboost-filesystem-dev zlib1g-dev
$ make config-gcc
$ make
$ sudo make install
,,,
