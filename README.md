# Finally learning to program at age 40

My first computer when growing up in the 1980s was an odd beast called an [ADAM](https://en.wikipedia.org/wiki/Coleco_Adam#/media/File:Coleco_Adam_(adjusted_version).jpg), a sort of hybrid of personal computer, COLECOVISION gaming system, and a typewriter. The computer itself is as you can see in the image, with two tape drives in place of a disk drive, an actual TV instead of a monitor, and an interesting printer that had a switch on it that let you turn it into a full-blown typewriter. A lot of other ADAM computer users had actual disk drives but we didn't, and I remember my dad doing a lot of tape recording in the basement when we first got it, but wasn't sure why it resulted in getting so many games out of it. (My favourite was called [Gateway to Apshai](https://en.wikipedia.org/wiki/Gateway_to_Apshai) I asked him about it a few months ago, and it turned out that he used Forth to make it happen:

>I used Forth a bit when we had the Coleco Adam computer which had a Zilog Z80 CPU. Not sure if you remember but I ordered a tape from the U.S. (for the tape drive) that came with several hacker programs and a manual called The Hackers Guide to the Adam which allowed us to download ColecoVision cartridge games to blank tapes so we got a ton of games. I didn't write any programs myself but the programs on the tape came with the source code so you could follow the logic. In some cases I needed to tweak the parameters and re-save in order to optimize whatever needed to be hacked. It was interesting and fun to do.

He showed me something called BASIC that at the time I assumed was the only programming language in the world. I took to it and followed along with [books like this one called the Mystery of Silver Mountain](https://archive.org/details/the-mystery-of-silver-mountain/mode/2up) and [Hunt the Wumpus](https://en.wikipedia.org/wiki/Hunt_the_Wumpus), and pretty soon had picked up how to program and began making my own small RPGs based on [Steve Jackson's Sorcery! books](https://en.wikipedia.org/wiki/Steve_Jackson%27s_Sorcery!).

```basic
10 INPUT "What is your name: "; U$
20 PRINT "Hello "; U$
30 INPUT "How many stars do you want: "; N
40 S$ = ""
50 FOR I = 1 TO N
60 S$ = S$ + "*"
70 NEXT I
80 PRINT S$
90 INPUT "Do you want more stars? "; A$
100 IF LEN(A$) = 0 THEN GOTO 90
110 A$ = LEFT$(A$, 1)
120 IF A$ = "Y" OR A$ = "y" THEN GOTO 30
130 PRINT "Goodbye "; U$
140 END
```
