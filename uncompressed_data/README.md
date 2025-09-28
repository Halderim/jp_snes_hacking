# Uncompressed data of interior levels of Jurassic Park
You will need to use a Hex Editor to look at the data

#### Some infos on items, the bahaviour and values:

Items have 2 or more values saved in the data, one value is for the item type the other value is the sprite that is used.
Ammo has at least 3 values ammo type, sprite and ammo count, ammo count seems to be 00 initially, which gives a full stack of ammo 
If the ammo was picked up and exchanged with a different type of ammo the ammo counter holds the amount of ammo left 
Loading a floor of a building resets all pickups, only exception are ID cards
Loading a floor happens during entering a building from the overworld or changing the floor with a elevator

## Sprite Values
E8 - ID Card

E9 - Chicken

EA - Gas Granate

EB - Shotgun Ammo

EC - Darts

ED - Rocket Ammo

EE - Battery

EF - Gas Canister


## Items found so far in the data, 

### Raptor Pen

#### Entry Level (RaptorPen_EntryLevel_Entities.bin) Offset + initial value
- 3A4 3E Itemtype Shotgun Ammo
- 3A8 00 Ammo count
- 3AC EB Itemsprite Shotgun Ammo

#### Upper Level (RaptorPen_UpperLevel_Entities.bin)
- 226 3E Itemtype Shotgun Ammo
- 22E EB Itemsprite Shotgun Ammo

- 66E E8 Itemsprite ID Card
- 670 10 ID Card Ian Malcolm

#### SubLevel1 (RaptorPen_SubLevel1_Entities.bin)
- 2AF2 E8 Itemsprite ID Card
- 2AF4 04 ID Card Robert Muldoon
