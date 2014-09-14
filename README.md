
TAKE-5
======

**BeBoPr expansion board for 5 axes.**

![](http://imagizer.imageshack.us/v2/800x600q90/661/V9qlAy.jpg)
*Fully populated Take-5 carrier*

# Introduction

The **TAKE-5 module carrier** is designed as **low cost expansion board** for the **BeBoPr**. It connects to the external stepper driver connector (J5) present on all BeBoPrs, and offers an extra socket for a fifth stepper driver module.

The four stepper modules that were plugged into the BeBoPr move to the corresponding sockets on the **TAKE-5** carrier and only one extra module is needed to **upgrade a BeBoPr to control five axes**.

The TAKE-5 carrier is compatible with the PEPPER and **two TAKE-5** carriers combined with a **DECAMUX** can be used to control a total of **10 axes**.

## The PCB

The board is **easy to assemble** as it holds no SMD parts, but **only through hole components**. All components are placed on the top side of the board. Besides the connectors, three electrolytic capacitors, a single blade fuse socket and six resistors are used.

![](http://imagizer.imageshack.us/v2/640x480q90/537/U1XOKa.png)
*PCB Top view*

### PCB Status

At the time of this writing, the first **PCBs are being manufactured**. This first prototype should be ready for testing before the end of September.

![](http://www.oshwa.org/wp-content/uploads/2014/03/oshw-logo-100-px.png)

The **PCB will be Open Source Hardware** and made available for ordering via **OSH Park**, Gerbers and a BOM will follow after successful testing.

## Configuration

Each stepper driver seat has three jumpers to set the microstepping. These jumpers replace the DIP switches that are present on the BeBoPr boards and are easier to obtain (and cheaper too).

An optional jumper field is for setting the decay mode. If PanuCatt SD8825 SureStepr modules are used, a driver's decay mode can be configured with this jumper. 

## Compatibility

The **Take-5** carrier has the same footprint as a **PEPPER** board. The carrier will work with the **BeBoPr++**, the **BeBoPr++** and a **BeBoPr + R1 Bridge**. The R0 bridge is not supported as some of the signals for the 5th stepper are not present.

Stepper power is applied via the same type of connector as used on the BeBoPrs. The Molex KK stepper motor connectors are also the same as used on the BeBopr and PEPPER boards. Of course, any connector that fits on the board could be used. For the blade fuse, either one of two different sizes of sockets can be mounted. 

## SureStepr SD8825

Besides sockets for the standard 16-pin stepper modules, optionally receptacles for the three extra signals from the **PanuCatt SD8825** driver modules can be installed. This allows to set the decay mode (fast, slow or mixed) with a jumper on the carrier (instead of soldering wires to the SD8825).

## Expanding to 10 axes

Just like the [**PEPPER**](https://github.com/modmaker/BeBoPr-plus-plus/wiki/PEPPER-Intro), this board can be used in combination with the [**DECAMUX**](https://github.com/modmaker/DECAMUX) to expand to number of axes to 10. Any combination of PEPPER and TAKE-5 boards can be used on the DECAMUX. But of course, **only the PEPPER has full software control** over the driver settings and allows to **run motors at the full 2.5 Ampere** driver current.
