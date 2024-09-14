# Galaksija PLUS FPGA core for NeptUNO+ (ported from Poseidon-EP4CGX150 (WIP))
# Thanks to @turri21

This port has been made thanks to the following sources: 

It is mainly based on the corresponding core for MiST created by [Gehstock](https://github.com/Gehstock/Mist_FPGA/tree/master/Computer_MiST/Galaksija_MiST).

Several elements such as the keyboard handling have been added from [hrvach](https://github.com/MiSTer-devel/Galaksija_MiSTer)'s port to MiSTer.

The ROM D addition is based on [GALe - Galaksija Emulator](https://galaksija.net/)*

Finally, several improvements have been migrated from the respective port for the [Senhor](https://github.com/turri21/Senhor) board (MiSTer clone).

---

Port to Poseidon-EP4CGX150 and Senhor by [turri21](https://github.com/turri21) 

Additional help by [CoreRasurae](https://github.com/CoreRasurae). 

-- The Senhor team -- 

---

## Galaksija first model.

It is possible to disable the ROM C (PLUS model) and ROM D by entering the following command in BASIC:
A=USR(&1000)

## ROM D info

The core boots straight into PLUS mode, in other words it loads all 4 roms automatically. Therefore, you do not have to type anything in basic to enable them, but for the record I will list these commands here: 

Enables ROM C: A=USR(&E000)

Enables ROM D: A=USR(&F000)

---

To use the monitor (RAM dump) you have to type in BASIC the following command:

*A &STARTING_ADDRESS &ENDING_ADDRESS

Example:
*A &F00 &FFF

or simply
*A &F00

and then ESC to break it 

To use the disassembler you have to type in BASIC the following command:
*D &STARTING_ADDRESS &ENDING_ADDRESS

Example: 
*D &F00 &FFF

or simply
*D &F00

and then ESC to break it

## TODO

Tape loading 

Audio

Saving

Graphics mode 

## License

This project is licensed under the MIT License.

## Acknowledgments

* Gehstock
* Damir
* Voja Antonic - Creator of Galaksija - Author of ROM A, B and D.
* ROM C Authors - Nenad Balint, Nenad Dunjic and Milan Tadic
* Dejan Ristanovic - In December 1983 he wrote a special edition of Galaksija called "Computers in Your Home" (Računari u vašoj kući), the first computer magazine in former Yugoslavia. This issue featured entire schematic diagrams guides on how to build computer Galaksija, created by Voja Antonić.
* *GALe - Galaksija Emulator - Copyright © 2022-2023 Dragoljub B. Obradović. All rights reserved.
