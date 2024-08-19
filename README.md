# Gurumin Modding and Script Fixes
Repository for the original dialog/UI text of Gurumin: A Monstrous Adventure, as well as corrections for the PC version and some notes on my attempt at modding Gurumin. All files have been converted to txt via itmcnv.exe (or just renaming the file extension, in the case of the PSP scr .bin files).

The Western PC release of Gurumin, by Mastiff, contains some errors in dialogue such as typos, untranslated lines, and broken speech bubbles. This repository will host corrections to the script, as well as the original script files from all versions of Gurumin for reference and posterity.

The English PC map.itm is included with modified medal prices and all closet options revealed from "???" to their respective outfits (for trying to hack in the PSP costumes, no luck yet), and a WIP Google TL of the dev comments that are included.

[Steam thread with notes on my attempts at modding.](https://steamcommunity.com/app/322290/discussions/0/3431200155187214220/)

[Steam guide with notes on modding Gurumin (file types, tools used)](https://steamcommunity.com/sharedfiles/filedetails/?id=1555446052)

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
