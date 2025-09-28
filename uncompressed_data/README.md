# Uncompressed data of interior levels of Jurassic Park
You will need to use a Hex Editor to look at the data

#### Some infos on items, the bahaviour and values:

Items have 2 or more values saved in the data, one value is for the item type the other value is the sprite that is used.
Ammo has at least 3 values ammo type, sprite and ammo count, ammo count seems to be 00 initially, which gives a full stack of ammo 
If the ammo was picked up and exchanged with a different type of ammo the ammo counter holds the amount of ammo left 
Loading a floor of a building resets all pickups, only exception are ID cards
Loading a floor happens during entering a building from the overworld or changing the floor with a elevator

## Sprite Values
00 01 - Bolas

C9 00 - Medikit

E8 00 - ID Card

E9 00 - Chicken

EA 00 - Gas Granate

EB 00 - Shotgun Ammo

EC 00 - Darts

ED 00 - Rocket Ammo

EE 00 - Battery

EF 00 - Gas Canister


## Items found so far in the data, 

### Raptor Pen

#### Entry Level (RaptorPen_EntryLevel_Entities.bin) Offset + initial value
- 3A4 3E Itemtype Shotgun Ammo, 3A8 00 Ammo count, 3AC EB 00 Itemsprite Shotgun Ammo

#### Upper Level (RaptorPen_UpperLevel_Entities.bin)
- 226 3E Itemtype Shotgun Ammo, 22E EB 00 Itemsprite Shotgun Ammo
- 66E E8 00 Itemsprite ID Card, 670 10 ID Card Ian Malcolm

#### Ground Level (RaptorPen_GroundLevel_Entities.bin)
- 847 00 Visibility Medikit, 848 08 Medikit Type, 850 C9 00 Medikit Sprite
- 3FD 01 Visibility Bola Ammo, 3FE 48 Bola Ammo Type, 406 00 01 Bola Sprite
- 1273 00 Visibility Chicken, 1274 04 Chicken Type, 127C E9 00 Chicken Sprite

#### SubLevel1 (RaptorPen_SubLevel1_Entities.bin)
- 2AF2 E8 00 Itemsprite ID Card, 2AF4 04 ID Card Robert Muldoon
