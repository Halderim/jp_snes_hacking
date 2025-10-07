# Item Data pointer

Each level has a RNC Data block containing all the enteties of a loaded level 
the game loads this block during a transition unpacks the data and places it in wram
in the game data there are 24bit pointers to find the right data to load

| Level | Hi | Lo | Bank | Original Pointer |
|-------|----|----|------|------------------|
| Raptorn Pen Entry | A58454 | A58455 | A58456 | 63 FB B6 |
| Raptorn Pen Upper | A5847E | A5847F | A58480 | 07 FA A1 |
| Raptorn Pen Ground | A584BC | A584BD | A584BE | A2 EB B5 |
| Raptorn Pen Sub1 | A5850F | A58510 | A58511 | 0E BC A5 |
| Raptorn Pen Sub2 | A5855D | A5855E | A5855F | 49 D8 A5 |
| Visitor Center Ground | A581C8 | A581C9 | A581CA | 42 CA A0 |
| Visitor Center Floor 1 | A58234 | A58235 | A58236 | 94 CA A6 |
| Visitor Center Roof | A58286 | A58287 | A58288 | 71 FB BF |
