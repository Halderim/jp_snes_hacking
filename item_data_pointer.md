# Item Data pointer

Each level has a RNC Data block containing all the enteties of a loaded level 
the game loads this block during a transition unpacks the data and places it in wram
in the game data there are 24bit pointers to find the right data to load

| Level | Hi | Lo | Bank | Original Pointer |
|-------|----|----|------|------------------|
| Beach Ground | A583C2 | A583C3 | A583C4 | AC EA A1 |
| Beach Sub | A58389 | A5838A | A5838B | 71 DC A1 |
| North Ground | A583F1 | A583F2 | A583F3 | 51 BB A0 |
| North Sub | A58425 | A58426 | A58427 | 0C F1 A5 |
| Nublar Ground | A58341 | A58342 | A58343 | 74 C2 A1 |
| Nublar Sub | A58308 | A58309 | A5830A | A4 CF A1 |
| Raptorn Nest | A5805F | A58060 | A58061 | ED 88 A5 |
| Raptorn Pen Entry | A58454 | A58455 | A58456 | 63 FB B6 |
| Raptorn Pen Upper | A5847E | A5847F | A58480 | 07 FA A1 |
| Raptorn Pen Ground | A584BC | A584BD | A584BE | A2 EB B5 |
| Raptorn Pen Sub1 | A5850F | A58510 | A58511 | 0E BC A5 |
| Raptorn Pen Sub2 | A5855D | A5855E | A5855F | 49 D8 A5 |
| Secret Level | A58037 | A58038 | A58039 | B4 F4 B7 |
| Ship Ground | A58073 | A58074 | A58075 | 04 82 A0 |
| Ship Sub1 | A5809D | A5809E | A5809F | AB AF A5 |
| Ship Sub2 | A580D1 | A580D2 | A580D3 | 33 A0 A0 |
| Ship Sub3 | A5813D | A5813E | A5813F | FC DD A6 |
| Ship Sub4 | A58176 | A58177 | A58178 | BE DC A0 |
| Visitor Center Ground | A581C8 | A581C9 | A581CA | 42 CA A0 |
| Visitor Center Floor 1 | A58234 | A58235 | A58236 | 94 CA A6 |
| Visitor Center Roof | A58286 | A58287 | A58288 | 71 FB BF |
| Visitor Center Sub1 | A582B0 | A582B1 | A582B2 | 17 EE A0 |
