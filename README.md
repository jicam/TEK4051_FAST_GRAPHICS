# TEK4051_FAST_GRAPHICS

TEK4051 – Fast Graphics – Jean CAMPIONI
# YouTube Clip – TEK4051 Fast Graphics

This folder contains the files used or associated with the following YouTube clip:  
https://www.youtube.com/watch?v=vJw_ju_zLXM

## File Description

### ZIP Archives

#### 4050files.zip

This file must be **unzipped** before use.

It contains all drawings dated **January 19, 2026**.  
These files can be copied (all or partially) into a new folder  
(with a name of your choice), created on the **SD card** used by the  
**Flash Drive** connected to the **Tektronix 4051** via the **IEEE-488 bus**.

The list of files and their sequence numbers is as follows:

SEQ. TYPE DESCRIPTION
1 		    PROG Not used 
9–11 		  DATA TOPOLINO 
12–14 		DATA VW1200 
15–17 		DATA PORSCHE_AV 
18–20 		DATA PORSCHE_AR 
21–27 		DATA EINSTEIN_2 
29–33 		DATA EINSTEIN_TIME 
34–41 		DATA JEAN00 
42–46 		DATA JEEP 
47–52 		DATA JFK_NEW 
53–61 		DATA MONTY_FATHER 
62–66 		DATA MONTY_HEAD 
67–73 		DATA 492P 
74–85 		DATA COWS 
86–100 	  DATA MBK 
101–104 	DATA GRINCH 
105–116 	DATA XFMR4051 
117–118 	DATA F35_ISRAEL 
119–123 	DATA HELICO_H145 
124–130 	DATA LEOPARD 
131–135 	DATA JEAN_ABL 
136–138 	DATA RAFALE 
139–141 	DATA A400M 
142–148 	DATA MMONROE 
149–154 	DATA LUCKY_LUKE 
200 		PROG To be loaded with FIND@5:200 & OLD@5:

If you want to display only the **GRINCH** and **LUCKY_LUKE** drawings:
After loading the BASIC program on the 4051, simply modify:
      - line **112**: `W=1`
      - line **900**: `DATA 101,104`
      - line **910**: `DATA 149,154`
---

#### Archive_190126_072409.zip

This file is intended for the **Tektronix 4051 simulator**.
It must be loaded (in *zapped* mode) using:  
**STORAGE / IMPORT / Storage Archive**,  
and selecting the location where the file is stored.
Once loaded, the BASIC program appears in a window.  
Close this window by clicking **CANCEL**.
Then type:
        FIND@5:200
        OLD@5:
After a few seconds, the cursor appears and the BASIC program is loaded.
If you wish to display only one or a few drawings, apply the same method described above for **4050files.zip**.  
The file numbers associated with each drawing are identical to those listed earlier.
The filename uses the format **DDMMYY_Time** to avoid confusion with other versions.
---

#### lucky_luke_seq.zip

This file must be **unzipped**.

It contains an **11-step sequence** showing the evolution of a drawing,  
from its initial **DXF state** (created with **Inkscape**) to the final image displayed on 
the **Tektronix 4051 simulator**.

The example used is **LUCKY_LUKE**, but the same process applies to all other drawings.
These sequences represent successive stages processed by various **Python programs**, running on my **iMac**.
---

## Notes
