# REX 9628 Extern Kernel 8

![](https://github.com/DL2DW/REX_9628_Extern_Kernel_8/blob/main/Images/REX9628.jpg)



The former company Rex Datentechnik was a manufacturer of many hardware in the 80s. Especially for the Commodore 64 there was a rich offer of the most different expansions. One of these cards was the Rex 9628, a board for the expansion port of the C64. The card could hold two EPROMs from 8 to 64KByte. That alone was nothing special, there were already a countless number of them from the most different manufacturers at that time.

The practical thing about this card was that it could hold up to 8 kernel ROMs, up to 4 each in a 27C256 EPROM, and two of them could be plugged onto the board. For this the case of the C64 did not have to be opened. So it was possible to use another kernel externally without any intervention. There were many different kernels available in the 80's, for example SpeedDOS and JiffyDOS.



## Manual

EXTERNAL KERNAL 8 9628

On this board, "EXTERNAL KERNAL 8", can accommodate up to 8 kernals operated (2x8 to 32K Eproms). 100% compatible e.g. to all speeders like Speeddos, Rex-DOS, Prologic-DOS etc... Suitable for all 64's, also that of ALDI. Board is at the expansion port operated.

You can use 1 x 2764 or 27128 or 27256 per socket. From each EPROM is addressed in each case the corresponding 8K range.

About the two DIL switches, the respective eighth and slot 1 and 2 are addressed.

The 4-pin DIL switch:

```
Switch        1    2    3    4       Slot 1    Slot 2
======================================================
             on  off   on  off       2764       2764
             on  off   on  off      27128      27128
            off   on  off   on      27256      27256
             on  off  off   on     2764/128    27256
            off   on   on  off      27256     2764/128
```

The 10-pin DIL switch:

```
Switch (on)        slot   kernal number on EPROM
====================================================
                 1   1              1
               2-1   1              2
             3-2-1   1              3
           4-3-2-1   1              4
         5-4-3-2-1   2              1
       6-5-4-3-2-1   2              2
     7-6-5-4-3-2-1   2              3
   8-7-6-5-4-3-2-1   2              4

                 9 turns Game Stop on or off
                10 turns the card on or off
```

If nothing else is set, the card automatically jumps to the 1st kernal in the 1st slot.

If used EPROM is bigger than 8K, ie. 27128 or 27256, then kernals must be burned one after the other in 8K blocks each. See the following address table:

```
   Kernal         addresses 27128     addresses 27256
=====================================================
      1              0000 - 1FFF        0000 - 1FFF
      2              2000 - 3FFF        2000 - 3FFF
      3                                 4000 - 5FFF
      4                                 6000 - 7FFF
```

The EPROMs must match the notch of the socket when plugged in.

## BOM

The brands are only representative. Comparable components from other manufacturers can also be used.

| Quantity | Designator                  | Manufacturer 1     | Manufacturer  Part Number 1 | Description                                             |
| -------- | --------------------------- | ------------------ | --------------------------- | ------------------------------------------------------- |
| 7        | C1,  C2, C3, C4, C5, C6, C7 | Kemet              | C330C104J5R5TA              | Cap Ceramic 0.1uF 50V X7R 5% Radial 5.08mm 125C Bulk    |
| 1        | CN2                         | Sullins            | PRPC001SFAN-RC              | CONN  HEADER .100 SNGL STR 1POS                         |
| 2        | St.1,  St.2                 | STMicroelectronics | M27C256B-10F1               | IC  EPROM 256K PARALLEL 28CDIP                          |
| 1        | SW1                         | Wurth  Electronics | 418117270904                | SWITCH  SLIDE DIP SPST 25MA 24V                         |
| 1        | SW2                         | Wurth  Electronics | 418117270910                | SWITCH  SLIDE DIP SPST 25MA 24V                         |
| 1        | SW3                         | Wurth  Electronics | 430476085716                | Black  Button Tactile Switch, NO 50 mA 5mm Through Hole |
| 1        | U3                          | Texas  Instruments | SN74LS30N                   | IC  GATE NAND 1CH 8-INP 14DIP                           |
| 1        | U4                          | Texas  Instruments | SN74LS125AN                 | IC  BUS BUFF TRI-ST QD 14DIP                            |
| 1        | U5                          | Texas  Instruments | SN74LS04N                   | IC  HEX INVERTER 14-DIP                                 |
| 1        | U6                          | Texas  Instruments | SN74LS148NSR                | IC  PRIORITY ENCODER 8-3L 16SO                          |
| 1        | U7                          | Texas  Instruments | SN74LS00N                   | IC,  74LS, 74LS00, DIP14, 5.25V                         |



## PCB

The PCB can either be ordered directly from [PCBWay](https://www.pcbway.com/project/shareproject/REX_9628_Extern_Kernel_II_8.html), or you can create it yourself from the Gerber files available here.

[![PCBWay](https://www.pcbway.com/project/img/images/frompcbway.png)](https://www.pcbway.com/project/shareproject/REX_9628_Extern_Kernel_II_8.html)



If you liked my project, I would be very happy about a small coffee donation.

[![ko-fi](https://www.ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/R6R62T6RN)



# License

The contents of this repository, with the exception of the Docs and Software directories, are released under the following license:

- the "Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License" (CC BY-NC-SA 4.0) full text of this license is included in the [LICENSE.CC-NC-BY-SA-4.0](https://github.com/DL2DW/REX_9628_Extern_Kernel_8/blob/main/LICENSE.CC-NC-BY-SA) file and a copy can also be found at https://creativecommons.org/licenses/by-nc-sa/4.0/
