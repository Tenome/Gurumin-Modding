# Gurumin Modding and Script Fixes
Repository for the original dialog/UI text of Gurumin: A Monstrous Adventure, as well as corrections for the PC version and some notes on my attempt at modding Gurumin. All files have been converted to txt via itmcnv.exe (or just renaming the file extension, in the case of the PSP scr .bin files).

The Western PC release of Gurumin, by Mastiff, contains some errors in dialogue such as typos, untranslated lines, and broken speech bubbles. This repository will host corrections to the script, as well as the original script files from all versions of Gurumin for reference and posterity. Before installing, backup map.itm in your bin folder and all .itm files in your 3dData folder.

The English PC map.itm is included with modified medal prices and all closet options revealed from "???" to their respective outfits (for trying to hack in the PSP costumes, no luck yet), and a WIP Google TL of the dev comments that are included.

[Steam thread with notes on my attempts at modding.](https://steamcommunity.com/app/322290/discussions/0/3431200155187214220/)

[Steam guide with notes on modding Gurumin (file types, tools used)](https://steamcommunity.com/sharedfiles/filedetails/?id=1555446052)

Other mods and misc.:

[Mediafire folder](https://www.mediafire.com/folder/3xd1misdnh92q/Gurumin)

[Mute the dodge and jump sound effects, which might be annoying for some (especially speedrunners).](https://www.mediafire.com/file/3tyjbftzwagm3ig/)

[Japanese dub](https://www.mediafire.com/file/ct9xica21v77bi0/)

[Japanese text](https://www.mediafire.com/file/amfm3jp4t3fy8iq/%2521Japanese_text.zip/file)

[PSP outfit files (I haven't been able to mod them back in)](https://www.mediafire.com/file/d7yfgf0p6m4gxy8/)

[Quieter movement](https://www.mediafire.com/file/3srcmanhd9o9cdo/)

[Panty shot unlock, normally unlocked after getting to Crazy Mode (virtually impossible to see anyway, you have to do specific moves for a single frame's view)](https://www.mediafire.com/file/5ssau7biacbspu6/)

[Archived interview with JP voice cast](https://www.mediafire.com/file/8dgvbcgocpr1oog/Japanese_Interview_with_Dubbing_Cast.zip/file) If I figure out how to do speech bubble checks, maybe I can insert this interview into the Boss Rush room?

[Cream's doppelganger recolor](https://www.mediafire.com/file/5fm5nqhr24as982/)

![](https://i.imgur.com/GLV7Djc.jpeg)

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

## Changelog
* Misc. typos, fixed speech bubble code, and general proofreading before I made this repository, need to go back and do a comparison for a detailed changelog
* Renamed "Maid Outfit" to its original JP name, Gothic Lolita Outfit.
* Added a line that wasn't translated during the Radish Woods boss cutscene (同じ手には… -> I'm not falling for that again...)
* Renamed "A Boring Class" to "Really Boring Class" so the secret makes sense (big oversight by Mastiff imo).
* The password to the Boss Rush room supports lowercase, Sentence case, and FULL CAPS now.
* Restored dialogue about Dad's book on the shelf
* Restored dialogue about Dad's photos on the wall (turned into a speech bubble rather than a thought so it smoothly transitions between lines). Thought bubbles/system prompts use different code, and I'm not sure if it supports multiple sequential bubbles. I have to look into it more.
* Fixed typo on password door
* At the end of some prompts (the ones that aren't speech bubbles) is a delay Wait(10); which causes the slight pause after you receive objects, examine objects, etc. I've commented out a few that seemed safe to remove the delay from, since the delay doesn't seem to serve any purpose.
* Restored Pamela to her JP name, "Plane," in keeping with the mathematics-themed names of the rest of the townspeople.
* Restored missing partial line after you beat the Astrals
* Fixed other typo on password door (had to compare it to JP)
* Added an additional missing prompt to the password door that was added in the PSP version. I'm not sure how to trigger it, though. I had to edit the code to make it say the alternate dialogue, but it's just "Please speak the password." I started a clear file on Crazy Mode, but I got the usual dialogue. It seems to be based on a flag that tracks progress?

Boss Rush room:
* Added Tokaron's dialogue from the PSP version
* Slightly adjusted Prince's dialogue to match PSP/PC JP
* Added Giga's dialogue from PSP version, but you can't actually speak to him. Parin makes a joke about the collision being different in the PC version, so that seems to be the real reason (in the PSP version, you have to talk to him at an angle, so the collision probably is janky/not working on PC). Not sure if this can be fixed, since of course no one knows how to edit collision yet (probably something to do with the .exe)... Here's the dialogue.

> 	"Giiiiigaaaa."
> 	"That's strange...","You couldn't talk in the original PC version.","Maybe the collision detection is different..."
> 	"Giga giga..."
> 	"Poor thing.","You can only talk in one place,","and that's all you get to say..."
> 	""You called，master?""
> 	"That was your line，right?"
> 	"Giga giga..."

* Changed Roger's name to his JP name, Lassi (ラッシー)
* Changed Lassi's "We love Gurumin" dialogue (made up by Mastiff because the original PC dialogue was about the video card the devs used) to the PSP dialogue
* * Fixed a misplaced line when giving the Old Scroll back to Rocko
* Added the "Change outfits?" prompt from the PSP version, but changed it to "What should I wear?" to match the JP version
* Adjusted a line about Puchi barking to closer match the JP/PSP version
* Adjusted a line by Pierre where he calls Parin a courageous Mademoiselle, to be more in line with the JP/PSP scripts.
* Restored another partial line when you lose at Hoccer
* Restored another partial line when you lose at Hoccer
* Fixed incomplete sentence when Disk thanks you for putting up ads, and adjusted second line to be more in line with JP
* Adjusted Doug's dialogue when first meeting you to more closely match the JP line
* Adjusted Doug's dialogue about accepting the job request to more closely match the JP line, by adding an additional speech bubble
* Corrected Poco being referred to as her instead of him in one line.
* Added an extra line from the English PSP version for when you give Chucky his umbrella stand.
* Fixed an incorrect sentence when Pierre wants a couch
* Changed one of Cylinder's sales pitches to match PSP ("Want to see some drill parts?")
* Minor correction to Fan's "Anyway, can I help you?" line
* Minor adjustment to Pierre's "Bonjour, my pretty Mademoiselle!" line
* Renamed Gothic Lolita Outfit to Gothic Lolita Maid. It's a bit conflicting, because the code says "meido," and the description is about maids, but the JP outfit name is Gothic Lolita. So, a compromise.
* Added some lines after you exchange for medals from the PSP version. I haven't tested them nor do I remember what the dialogue is usually like, but for whatever reason Hyperbolic will put the clothes in your dresser for you.
* Minor adjustment to Cylinder's Alchemy Book dialogue
* Fixed error in Puku's dialogue when asking you to find Pino and Poko
* Changed the password to Eggplant Caverns - Ruby Cave to match either SentenceCase, lowercase, or UPPERCASE. The password fields don't support the space key so I can't split it.
* Fixed typos while working at Fan's shop (comming -> coming, … -> ...)
* Fixed an incorrect bubble from Chucky when you give him the scroll
* Fan's work minigame: Changed all orders to lowercase (IceCream -> icecream etc.) I dont' have a save file at this spot so I can't test if I can put in multiple correct answers for different cases. If you have a save file that can play this game, please upload it so I can test.
* Added a missing "Can I help you?" bubble when talking to Fan after the cake thefts
* Changed "Ok, we got a deal" to "We got a deal!" from the PSP script when exchanging for bronze or silver medals
* Revised + fixed a missing partial line when you beat the Motoro Astrals to closer match the JP dialogue
* Fixed a missing line from Fan about prices being high
* Adjusted Motoro's introduction when meeting him in his home to match JP dialogue more closely
* Adjusted a couple of Peke's lines when doin the laser experiment
* Fixed a typo when Fan comments on your outfit
* Fixed a typo when Cylinder is asking you out for a cup of tea
* Fixed a missing partial Fan line about prices going up
* Fixed a missing partial Fan line about not being able to lower prices
* Restored Parin's comment about the books being boring if you choose not to read the shelf
* Fixed a typo when Pierre is asking you to return Francois
* Fixed an incorrect line in the "where does my brother reside" riddle
* Changed the description of the afro to match JP (it's a reference to the Japanese wrestler, Muhammad Yone AKA Mr. Afro). New line is  :Long Live Mr. Afro!, Original JP is ミスターアフロ、万歳! original English is: Makes the wearer very...funky.
* Changed description of sombrero to match JP. New line is: From today on, you, too, can be Mexican!, Original JP is 今日からあなたもメキシカン。Original EN is : Yo quiero Gurumin!

* There is some dummied out dialogue  after giving Motoro a platinum medal that makes it clear that Motoro was talking to Grandpa about you earlier (after you show Grandpa a platinum medal), but this dialogue was left out by Falcom since it contradicts the ending where Motoro states that only children can see them (and also since Motoro was already leaving hints on signs for you)

>なるほど。彼の言っていた女の子は君の事だったであるか……
>なんのこと？彼って…？
>"な、なんでも無いのである。気にしないでほしいのである

* There is some dummied out dialogue that seems to be by Hyperbolic when you show him a platinum medal for the first time. He's much more excited and tells you find a collector who is obsessed with them, whereas the current dialogue is rather muted but still tells you to find a collector (same way in JP). However, I'm confused because the code is in the block where you give Motoro the medals, which would imply that it's Motoro getting excited (which doesn't make sense, since the dialogue tells you to give it to a "real collector" who is worthy of it, like what Hyperbolic says.) If the dialogue is supposed to be by Hyperbolic, though, it doesn't make sense continuity-wise either since Hyperbolic gives you your first Platinum Medal and would have no reason to react like this. So both of these points tell me this was dummied out earlier in development. Since I don't know how to cleanly insert it in a way that makes sense, I'll just paste it here.

>そ、そ、そ、それは！！！
>どうしたの？
>"プ、プ、プ、プラチナメダルじゃないか！
>長年メダルを集めてきたのじゃが","プラチナメダルを見るのは","初めてじゃわい"
>へ～そんなに珍しいメダルなんだ
>わしが手にするにはあまりにも勿体ないわい
>世界にはわしよりもさらにメダルマニアな男が五万といるらしい
>そのメダルをあげるのならそういう男達にあげると良いじゃろう
>わかったわ。もしそんな変な人を見かけたらその人にあげることにするわ

* Boss room:
* Bobo:  Replaced lines about the original JP PC release's benchmark tool, since  the benchmark tool doesn't come with Steam/GOG and thus it doesn't make much sense to leave it. Replaced with PSP's dialogue. If I can figure out how to give them multiple speech bubbles depending on whether you talked to them or not, I can add both.
* Imported a feature from the PSP version that lets you select the difficulty level of the buss rush. It seems to work, but let me know if the bosses have the wrong HP/damage or something.
