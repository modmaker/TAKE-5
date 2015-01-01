
TAKE-5
======

Last changed: 2015-01-01 - Introduction deal has ended.

## Special deal

While stock lasts, and if bought together with a BeBoPr++, the TAKE-5 kit can be bought at the very special price of only EUR 15.00 for the complete kit. The kit contents is shown on the picture below.

The TAKE-5 kit contains all the parts you need to assemble the board. It also contains the ribbon cable _and_ the female connector should you want to attach the board directly onto the BeBoPr. This is a special introduction deal, that's why the price is so low.

If you want to use the board with Panucatt stepper drivers and the extra decay jumper, you do need to add these (optional) parts yourself (see the BOM).

After assembly this allows you to use the BeBoPr++ for 5 axes, or up to 10 after adding a DECAMUX and a second driver board (either PEPPER, TAKE-5 or XTRUDR).

|![](http://imagizer.imageshack.us/v2/640x480q90/673/pXguZY.jpg)|
|:-:|
|*Take-5 DIY kit contents*|

[Click here](http://imageshack.com/a/img907/6414/52fuZa.gif) for the order of assembly. This is the version that uses the ribbon cable to connect to the BeBoPr. By mounting the female 16 pin connector is mounted to the bottom side of the PCB (instead of the header on the top side), a board is created that plugs directly onto the BeBoPr. Two of the mounting holes of the BeBoPr align with those of the TAKE-5 and with two long screws and a couple of spacers, a rigid construction can be made. 

### **BeBoPr add-on board for 5 axes.**

|![](http://imagizer.imageshack.us/v2/640x480q90/538/Bi6xLJ.jpg)|
|:-:|
|*Take-5 carrier populated with 5 stepper driver modules*|


# Introduction

The **TAKE-5 module carrier** is designed as **low cost expansion board** for the **BeBoPr**. It connects to the external stepper driver connector (**J5**), present on all BeBoPrs, and offers an extra socket for a fifth stepper driver module.

The four stepper modules that were plugged into the BeBoPr migrate to the corresponding sockets on the **TAKE-5** carrier and only one extra module is needed to **upgrade a BeBoPr to control five axes**.

|![](http://imagizer.imageshack.us/v2/320x480q90/908/uwIyx3.jpg)|![](http://imagizer.imageshack.us/v2/320x480q90/661/DefH18.jpg)|
|:-:|:-:|
|*Side view bare board*|*Side view with driver modules plugged in*|

The TAKE-5 carrier is compatible with the **DECAMUX**, **PEPPER** and **XTRUDR**. Use a **DECAMUX** and two expansion boards to control up to **10 axes**.


## How to buy / build

|![](http://www.oshwa.org/wp-content/uploads/2014/03/oshw-logo-100-px.png)|![](http://imagizer.imageshack.us/v2/480x360q90/537/U1XOKa.png)|
|:-:|:-:|
||*PCB Top view*|

The [TAKE-5 board design](https://github.com/modmaker/TAKE-5/blob/master/pcb/TAKE-5_schematics.pdf) is available as **Open Source Hardware**. Only basic soldering skills are needed since the board uses leaded components only.

The PCB design is open hardware and available as shared project at **OSH Park**. A set of 3 PCBs can be [ordered directly from OSH Park](https://oshpark.com/shared_projects/5rlN100P) for around $40 including shipping. The [BOM cost](https://github.com/modmaker/TAKE-5/blob/master/pcb/TAKE-5_BOM.pdf) is around EUR 11 (EU|Farnell), or $16(US|Newark).

## Configuration

Each stepper driver seat has three jumpers to set the microstepping mode. These jumpers replace the DIP switches that are present on the BeBoPr boards and are easier to obtain (and cheaper too).

An optional jumper field is for setting the decay mode. If PanuCatt SD8825 SureStepr modules are used, the driver's decay mode can be configured with this jumper (see below).

|![](http://imagizer.imageshack.us/v2/640x480q90/674/Rl3ZNS.jpg)|
|:-:|
|*Normal board population, without the optional decay mode jumpers*|

## Compatibility

### Mechanical

The **Take-5** carrier has the same footprint and mounting holes as the **PEPPER** board. The carrier will work with the **BeBoPr++**, the **BeBoPr++** and a **BeBoPr + R1 Bridge**. The R0 version bridge is not supported as some of the signals for the 5th stepper are not present.

### Connectors

- A 16-wire flat-cable connects the TAKE-5 to the BeBoPr. A boxed header prevents accidental cable reversal.
- Stepper power is applied via the same type of connector as used on the BeBoPr.
- The stepper motor connectors (Molex KK) are the same as used on the BeBopr and PEPPER boards.

Of course, any connector that fits on the board could be used if it's properly dimensioned for the currents used.

### Fuse

The board is designed to mount an automotive blade fuse that protects the stepper power. Either a complete (isolated) socket, or dual clips can be mounted to hold the fuse.

The board can be assembled to accept either a standard, a mini, or a low profile fuse, depending on the kind of socket mounted:


| Part Type | For Fuse Type | Part No.        | Count |
|:----------|:-------------:|:----------------|:-----:|
| CLIP      | ALL           | KEYSTONE 3557   |   2   |
| SOCKET    | STANDARD      | KEYSTONE 3557-2 |   1   |
| SOCKET    | MINI          | KEYSTONE 3568   |   1   |

## SureStepr SD8825

Besides sockets for the standard 16-pin stepper modules, optionally receptacles for the three extra signals from the **PanuCatt SD8825** driver modules can be installed. This allows to set the decay mode (fast, slow or mixed) with a jumper on the carrier (instead of soldering wires to the SD8825).

|![](http://imagizer.imageshack.us/v2/320x240q90/674/8UVIwY.jpg	)|![](http://imagizer.imageshack.us/v2/320x240q90/673/IAYnDh.jpg)|
|:-:|:-:|
| *Extra pins for the SD8825*| *Bottom view with extra pins* |

|![](http://imagizer.imageshack.us/v2/640x480q90/911/ueRcPR.jpg)|
|:-:|
|*Fully populated board with decay mode jumpers for SD8825*|


## Expanding to up to 10 axes

Just like the [**PEPPER**](https://github.com/modmaker/BeBoPr-plus-plus/wiki/PEPPER-Intro), this board can be used in combination with the [**DECAMUX**](https://github.com/modmaker/DECAMUX) to expand to number of axes. Any combination of PEPPER and/or TAKE-5 boards can be used on the DECAMUX. But **only the PEPPER gives full software control** over the driver settings and allows to **run motors at the full 2.5 Ampere** driver current.
