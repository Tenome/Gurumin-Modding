# Gurumin Modding and Script Fixes
Repository for the original dialog/UI text of Gurumin: A Monstrous Adventure, as well as corrections for the PC version and some notes on my attempt at modding Gurumin. All files have been converted to txt via itmcnv.exe (or just renaming the file extension, in the case of the PSP scr .bin files).

The Western PC release of Gurumin, by Mastiff, contains some errors in dialogue such as typos, untranslated lines, and broken speech bubbles. This repository will host corrections to the script, as well as the original script files from all versions of Gurumin for reference and posterity. Before installing, backup map.itm in your bin folder and all .itm files in your 3dData folder.

The English PC map.itm is included with modified medal prices and all closet options revealed from "???" to their respective outfits (for trying to hack in the PSP costumes, no luck yet), and a WIP Google TL of the dev comments that are included.

[Steam thread with notes on my attempts at modding.](https://steamcommunity.com/app/322290/discussions/0/3431200155187214220/)

[Steam guide with notes on modding Gurumin (file types, tools used)](https://steamcommunity.com/sharedfiles/filedetails/?id=1555446052)

I'm going over the PSP vs. PC differences again to see if there are any lines I might've missed. If someone wants to help me, that'd be nice. It's a wall of text. In this zip, you'll find the PC and PSP scripts dumped into their own txt files, and then a diff txt file that I generated with a Python script that should contain all the lines that are in the PSP txt, but not the PC txt. A lot of them aren't actually missing lines, though, but got marked because the pointer or some other number in the line is different in the PSP version. You can help by reading the English lines in the diff.txt, and then checking against the PC.txt to see if the line is in there, or if it's different. Sometimes lines got a better translation in the PSP version, etc.

mediafire.com/file/uhuwb7f44bqiouc/ 

## PSP
### Japanese:
The Japanese PSP release contains 75 loose txt files in *3dData* which encompass both text and code, and 4 loose txt files in *map*. In addition, *binc* contains more dialogue/UI text in 824 scr*.bin files (which seem to just be txt files), and some code for things such as the new costumes. scr0867.bin in the PSP version contains the code for the bonus outfits.

### English:
The English PSP release contains 75 loose txt files in *3dData* which encompass both text and code, and 4 loose txt files in *map*. In addition, *binc* contains more dialogue/UI text in 826 scr*.bin files (which seem to just be txt files), and some code for things such as the new costumes. scr0867.bin in the PSP version contains the code for the bonus outfits. The English release contains two extra src bin files which don't seem to do anything (scr4094 and scr4095). The code inside says 

```
int main()
{
	// 家具テストでムービー再生
	KaguTest(70001,0);
	Black(0,0,30);
}
```

## PC
### Japanese:
The Japanese PC release (DLSite) contains 75 .itm files in *3dData* which encompass both text and code (not including the BMP files that make up the rest of the 236 .itm files), and 1 map.itm file in *map*.

### English:
The English PC release contains 75 .itm files in *3dData* which encompass both text and code (not including the BMP files that make up the rest of the 238 .itm files), and 1 map.itm file in *map*.
