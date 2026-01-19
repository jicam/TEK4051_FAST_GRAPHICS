# TEK4051 – Fast Graphics
Jean CAMPIONI

## YouTube Clip
This folder contains the files used or associated with the following YouTube clip:
https://www.youtube.com/watch?v=vJw_ju_zLXM

---

## ZIP Archives

### 4050files.zip
This archive must be unzipped before use.

It contains all drawings dated **January 19, 2026**.  
These files can be copied (all or partially) into a new folder (with a name of your choice),
created on the SD card used by the Flash Drive connected to the **Tektronix 4051**
via the **IEEE-488 bus**.

### File sequence list

| SEQ | TYPE | DESCRIPTION |
|----:|------|-------------|
| 1 | PROG | Not used |
| 9–11 | DATA | TOPOLINO |
| 12–14 | DATA | VW1200 |
| 15–17 | DATA | PORSCHE_AV |
| 18–20 | DATA | PORSCHE_AR |
| 21–27 | DATA | EINSTEIN_2 |
| 29–33 | DATA | EINSTEIN_TIME |
| 34–41 | DATA | JEAN00 |
| 42–46 | DATA | JEEP |
| 47–52 | DATA | JFK_NEW |
| 53–61 | DATA | MONTY_FATHER |
| 62–66 | DATA | MONTY_HEAD |
| 67–73 | DATA | 492P |
| 74–85 | DATA | COWS |
| 86–100 | DATA | MBK |
| 101–104 | DATA | GRINCH |
| 105–116 | DATA | XFMR4051 |
| 117–118 | DATA | F35_ISRAEL |
| 119–123 | DATA | HELICO_H145 |
| 124–130 | DATA | LEOPARD |
| 131–135 | DATA | JEAN_ABL |
| 136–138 | DATA | RAFALE |
| 139–141 | DATA | A400M |
| 142–148 | DATA | MMONROE |
| 149–154 | DATA | LUCKY_LUKE |
| 200 | PROG | To be loaded with `FIND@5:200` & `OLD@5:` |

### Display only GRINCH and LUCKY_LUKE

After loading the BASIC program on the 4051, modify:

- Line 112: `W = 1`
- Line 900: `DATA 101,104`
- Line 910: `DATA 149,154`

---

### Archive_190126_072409.zip
This file is intended for the **Tektronix 4051 simulator**.

It must be loaded (in *zapped mode*) using: 
STORAGE / IMPORT / Storage Archive

Select the file location and load it.  
When the BASIC program appears, close the window by clicking **CANCEL**, then type:
FIND@5:200
OLD@5:

After a few seconds, the cursor appears and the BASIC program is loaded.

If you wish to display only one or a few drawings, apply the same method described above
for `4050files.zip`.

The file numbers associated with each drawing are identical.  
The filename format `DDMMYY_Time` avoids confusion with other versions.

---

### lucky_luke_seq.zip
This archive must be unzipped.

It contains an **11-step sequence** showing the evolution of a drawing,
from its initial **DXF state** (created with *Inkscape*)
to the final image displayed on the **Tektronix 4051 simulator**.

The example used is **LUCKY_LUKE**, but the same process applies to all other drawings.

These sequences represent successive processing stages using various **Python programs**
running on an **iMac**.

---

## Notes
Additional technical notes and documentation may be added later.


