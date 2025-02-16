           TRACKS (FORENSIC)

"The Track Not Taken"

And we get file chall.zip

after i binwalk that file i can extract qrf.png 

![qrf](https://hackmd.io/_uploads/S1fQ8CRKkl.png)

frist i don't think there have flag.txt in binwalk so i scan it frist and see nothing

then, i use steg online anh choose Browse Bit Planes ![q1](https://hackmd.io/_uploads/By598RRtke.png)

**$st@cy*1245** may be this is the pass so i use binwalk again

and see flag.txt but binwalk not supported to unzip file with password 

and i use dd command 

**dd if=chall.mp4 bs=1 skip=7892907 count=227 of=flag.zip**


skip=7892907 the frist byte of flag.txt is start from there and end is ..2935 so count is to the end of the bytes we want

and yay we get flag.zip

unzip it!!

**(YB4R{x00zyh$bgcln7_f0p3yx_$n4ws})**

this is not a final we must decrypt it 

use caesar with dcode.fr and we get 

flag: 	**EH4X{d00fen$hmirt7_l0v3ed_$t4cy}**


            Retrieve the flag (MISC)

"Sit back , relax and enjoy this audio since you are going to have to decrypt a lot of things soon."

you will see there are a flag.zip and challage.wav

first challage.wav i use audacity choose stegogram and see this secret message : ":DE9:D4@CC64E"
![image](https://hackmd.io/_uploads/H1w_HN15ye.png)

use rot47 :  isthiscorrect (this is pass for unzip flag.zip)
![flag](https://hackmd.io/_uploads/SkzBHV1qJl.gif)


we will get flag.gif, it took me too long to slove the flag 
the isn't in the file gif, use "**strings flag.gif**" 

EHAX{WHERE_IS_THE_FLAS} this is the fake flag!

and you see the sign of the flag : 
**JMFC{qttpx@dtz##knsfqqd__ktzsi+_ymj%kqfl_tw_ini_dtz?}**

this is the real flag !!!

i use dcode.fr to identify cipher and use ROT cipher to decrypt it 

flag: ***EHAX{looks@you##finally__found+_the%flag_or_did_you?}***