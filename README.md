# JTAG-HS2-SMT2

## Designed by ThinkerMaker

- [Thinkermaker Bilibili](https://space.bilibili.com/11945069)
- [Thinkermaker Github](https://github.com/LiveQiu)
- [Thinkermaker website](https://thinkermaker.xyz)

## About Project

- I drew on a lot of open source schematics to draw on the schematic of JTAG-SMT2.
- I used it on the board and it worked fine and the download speed was at 30M.
- All interfaces have added ESD chips, but USB I didn't add separately, you may be able to add it.

## Run step

- 1.Design and make your board.
- 2.Connect your board to your PC.
- 3.Perhaps you need to install the FT232 driver first(FT232HL-drive folder).
- 4.Use FT232HL-Download-tool/EEPROM.exe automatic programming of chips(ft232).
- 5.Have fun!

## Software package

- Windows 10 21H2
- Visual Studio 2022

## Note

- I compiled the latest release version software using Visual-Studio-2022.
- This version of the firmware should be the JTAG-HS2 version.
- FT232HL-Download-tool/Eep.bin is FT232 firmware, if you have newer firmware,you should rename file as Eep.bin

## Hardware view

- My JTAG-SMT2 Schematic

  ![Image text](https://raw.githubusercontent.com/LiveQiu/JTAG-HS2-SMT2/main/JTAG-SMT2-img/Schematic_Xilinx_jtag_smt2.png)

- My JTAG-SMT2 PCB(two-layer board)

  <img src="https://raw.githubusercontent.com/LiveQiu/JTAG-HS2-SMT2/main/JTAG-SMT2-img/JTAG-SMT2-PCB.png" width="250px"/>
  <img src="https://raw.githubusercontent.com/LiveQiu/JTAG-HS2-SMT2/main/JTAG-SMT2-img/JTAG-SMT2-PCB1.png" width="250px"/>

- My JTAG-SMT2 Hardware(two-layer board)

  <img src="https://raw.githubusercontent.com/LiveQiu/JTAG-HS2-SMT2/main/JTAG-SMT2-img/JTAG-SMT2.jpg"/>

- On-board test

  <img src="https://raw.githubusercontent.com/LiveQiu/JTAG-HS2-SMT2/main/JTAG-SMT2-img/JTAG-SMT-USE.jpg" width="500px"/>

## Reference project

- In this project, you need to customize the shape of the board. [JTAG-SMT2 Reference project](https://oshwhub.com/peyo/Xilinx_jtag_smt2_nc)
- Note: I only used a two-layer board to complete his design, and I realized the design of JTAG-SMT2 at a very low cost, and it can work stably, using components packaged in 0603, making it friendly.JLC can use the hole breaking process, which is friendly to production and does not require manual cutting of the board.

## Project structure

- Run command to build the project structure. (tree >list.txt /F /A)

```text
+---
|   README.md
|
+---FT232HL-Download-tool
|   |   Eep.bin
|   |   EEPROM.exe
|   |   EEPROM.pdb
|   |   FTD2XX_NET.dll
|   |   FTD2XX_NET.xml
|   |
|   \---src
|       |   EEPROM.csproj
|       |   EEPROM.sln
|       |   FTD2XX_NET.dll
|       |   FTD2XX_NET.XML
|       |   Program.cs
|       |
|       \---Properties
|               AssemblyInfo.cs
|
+---FT232HL-drive
|       CDM v2.12.28 WHQL Certified.rar
|
+---Hardware-Ref
|       XM-JLINK-V1.0.0.PcbDoc
|       XM-JLINK-V1.0.0.pdf
|       XM-JLINK-V1.0.0.PrjPcb
|       XM-JLINK-V1.0.0.SchDoc
|
\---JTAG-SMT2-img
```
