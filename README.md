# jp_snes_hacking
Findings about code, data and many other things in Jurassic Park for the SNES
(All values are in Hex)

## ID Cards
Most ID Cards are located inside building only the Card of John Hammond is located outside of a Building
When picking up a card the corresponding byte in WRAM is set 

The bytes are starting at address 253 of WRAM
If the value is greater 0 then the card is optained

253 / 254 Hammond\
255 / 256 Ellie Sattler\
257 / 258 Robert Muldoon\
259 / 25A Alan Grant\
25B / 25C Donald Gennaro\
25D / 25E Ray Arnold\
25F / 260 Dennis Nedry\
261 / 262 Dr Wu\
263 / 264 Ian Malcolm

Usually the Cards have a index value to them, Ellie Sattlers Card has the index value 02 Ian Malcolm has the 10
During the pickup of a card the index is added to the address 253 and the bytes are set to FF 
Hammonds card works a bit different 
In the ROM at Offset B617 the value 53 02 is saved this is the information what address should be used when picking up the card on the rooftop of the visitor center 
Usually this is the hammond card, changing that value to 55 02 would let you pick up the card of Ellie Sattler


The Textbox does stay the same that you did find Hammonds ID

## Loading level data

### Elevator transitions
During a elevator ride the new level data is read from RNC data blocks
The subroutine to load the item data is located at $124CC0 (Exectution breakpoint in Mesen Emulator)

In this subroutine there are two instructions that read data from a specific address 
LDA $A50003,X reads the offset for the RNC block 
LDA $A50005,X reads the bank 

The Raptor Pen Sub Level 1 Items for example are located at A5BC0E
The first LDA instructions reads $BC0E from the address A5850F
The second LDA reads $19A5 from the address A58511

At $134224 (Exectution breakpoint in Mesen Emulator) the subroutine for the RNC unpack starts 
LDA [$20] then starts to read byte after byte of the RNC block the RNC magic happens and the data is written into WRAM

Changing the values for the offset and bank loads data from a different location then the original one 

If the rom is extended and level data is injected into the start of the new free space changing those two values would load from the new data

This way new level data for items could be packed from a uncompressed binary inserted into the extended rom and loaded during a level transition via elevator
