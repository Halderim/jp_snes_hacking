# jp_snes_hacking
Findings about code, data and many other things in Jurassic Park for the SNES

# ID Cards
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
In the ROM at Offset B617 the value 53 02 saved this the information what address should be used when picking up the card on the rooftop of the visitor center 
Usually this is the hammond card, changing that value to 55 02 would let you pick up the card of Ellie Sattler on the roof 

The Textbox does stay the same that you did find Hammonds ID
