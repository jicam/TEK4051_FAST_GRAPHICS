# Vector Drawings for the TEK 4051

This repository contains a collection of vector drawings for the Tektronix 4051, generated using a workflow that combines 
### ChatGPT, Inkscape, Python, and Fast Graphics.

# Drawing Creation Workflow
The drawings are produced using the following processing pipeline:

## 1. Initial drawing generation
A source photograph is selected.
ChatGPT is used to generate a technical drawing–style version of the image, on a white background, while preserving the original X/Y proportions.

## 2. Vectorization
The generated image is imported into Inkscape.
It is then converted into a DXF vector file.

## 3. Vector optimization
The DXF file is processed by a Python program that:
minimizes the total number of vectors,
merges compatible segments into 
   ### polylines / polygons.

## 4. Data cleanup
A second set of Python scripts:
removes all non-essential DXF data,
keeps only the X and Y coordinate information.

## 5. Scaling and segmentation
The drawing is scaled to match the TEK 4051 display dimensions.
It is then split into 8100-byte blocks, since the maximum size for a binary block is 8192 bytes.

## 6. Fast Graphics compression
Each block is compressed using the Fast Graphics format, which encodes:
two floating-point coordinates
into three ASCII bytes
📖 Reference: Fast Drawing and Refreshed Graphics from: 
### 4050 Series Graphics Enhancement ROM Pack TEKniques, Vol. 7, No. 3, p. 5

## 7. FlashDrive header formatting
File names are adjusted to strictly follow the FlashDrive header structure:

- **1–7** File number
- **8–15** ASCII/BINARY
- **16–20** PROG/DATA
- **21–36** COMMENT / Name
- **38** File size (automatic)
   
## Note: The maximum number of files in a single directory is limited to 250.

# Viewing the drawings (TEK 4051 simulator)

The first program in the folder is a BASIC program that automatically displays all drawings contained in the directory.

Example: loading  
### VECTOR1.zip

## Steps:
## 1- Launch the simulator by opening:,

  ### Tektronix4051.html
located in the 4051 Emulator directory.

## 2- If you do not already have the emulator, download it here: 
👉 https://github.com/mmcgraw74/Tektronix-4051-Emulator

## 3- In the simulator:
Click MUTE Then: 

- **START**
- **STORAGE**

## 4- In the dialog window:
Change Single File to Storage Archive
Click IMPORT
Select VECTOR1.zip

## 5- The BASIC program listing at position 1 will appear.
Click CANCEL to close the window.
Then click AUTO LOAD

## 6- The simulator displays: 
  - **FIND@5:1**
  - **OLD@5**
  
## 7- The images are then displayed automatically, one after another, until the last one.

## Viewing another archive

   Once VECTOR1 has finished, you can load 
   ### VECTOR2 by repositioning at point 4.


# Using the files on a real TEK 4051 / 4052 / 4054

If, in addition to the 4050 Series Emulator, you are fortunate enough to own a real, operational TEK 4051, 4052, or 4054, and you also have a FlashDrive, you can place these files onto an SD card (up to 256 GB if you wish).

In that case, once the emulator has been loaded with one of the ARCHIVEx.ZIP files, it can be used to automatically create one or more directories on your SD card.

## Procedure

- ***Your drawings are loaded into the emulator using the XXX.ZIP archive.***

- ***Click STORAGE.***

- ***In the small window to the right of IMPORT, select FLASH DRIVE FILES.***
  
- ***Click EXPORT.***
  
- ***The emulator will create a zipped file.***
  
- ***Simply unzip it and copy/paste the contents onto your SD card.***

### Do not forget to reset the FlashDrive microcontroller if you remove and reinsert the SD card.




