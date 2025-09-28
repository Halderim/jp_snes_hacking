# Uncompressed data of interior levels of Jurassic Park
You will need to use a Hex Editor to look at the data

#### Some infos on items, the bahaviour and values:

Items in the levels can be found in the entities files

They are defined by multiple byte (13 bytes) values
examples

00 3E 00 00 00 00 00 00 00 EB 00 00 00 (Shotgun Ammo)

00 3E 00 00 00 01 00 00 00 EB 00 00 00 (Shotgun Ammo with one bullet left, only works with exchanged ammo)

01 48 00 00 00 00 00 00 00 00 01 00 00 (Bola Ammo)

FF 2A 00 00 00 00 00 00 00 00 01 00 00 (Bola Ammo picked up)

00 02 00 00 00 00 00 00 00 E8 00 10 00 (Ian Malcolm ID Card)


First byte visibility value 80 to FF is invisible, it does not remove the item its only invisible 
Second byte is the item type it tells the game what item is picked up
Sixth byte ammo count, 00 means full ammo pack, if ammo was exchanged this holds the value of the dropped ammo
Tenth and eleven byte is the sprite of the item EB 00 is the shotgun ammo sprite 00 01 is the Bola ammo sprite
Twelvth byte tells the game what ID card is picked up if the item is a ID card

Picking up a item that is not exhchanged sets the first byte to FF the second byte to 2A
FF 2A 00 00 00 00 00 00 00 EB 00 is picked up shotgun ammo 

Loading a floor of a building resets all items on the floor
Loading a floor happens during entering a building from the overworld or changing the floor with a elevator

ID cards are no exception to this but they are removed from their location when the player gets close to Card location

## Item Types
2A - Empty Item

04 - Chicken

08 - Medikit

3E - Shotgun Ammo

42 - Rocket Ammo

44 - NV Battery

48 - Bola Ammo

02 - ID Card

## Sprite Values
00 01 - Bolas

C9 00 - Medikit

CC 00 - Exit Sign

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
