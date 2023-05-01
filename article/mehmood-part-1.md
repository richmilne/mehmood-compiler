# Getting into top gear

Speed up your Basic programs using this Compiler for 48K Spectrum by **A Mehmood**  
([Popular Computing Weekly, 25 April–1 May 1985, p 24–25](https://archive.org/details/popular-computing-weekly-1985-04-25/page/n23/mode/1up))

One main draw-back of programs written in Basic is the speed they run at. You must have noticed that even some of the simplest of programs grams may be slow and sluggish. The only way to really overcome the problem of speed is to convert the programs into machine code. This may not be such a hard task for someone who is familiar with assembler but for someone who has no or very little such knowledge it becomes an almost impossible task. This is where many people can benefit by using a compiler.

This compiler interprets many (but not all) of the commands, functions and statements used in Basic to their machine code equivalents. When this code is run, you will find your program runs much faster than its Basic equivalent.

Commands, Functions and Statements supported are as follows:

|         |       |        |        |
| ------- | ----- | ------ | ------ |
| At      | Attr  | Beep   | Border |
| Chr$    | Cls   | Code   | Draw   |
| Flash   | Goto  | Gosub  | If     |
| In      | Ink   | Inkey$ | Int    |
| Inverse | Let   | Out    | Over   |
| Pause   | Peek  | Plot   | Point  |
| Poke    | Print | Rem    | Return |
| Rnd     | Stop  | Tab    | Then   |
| Usr     | Paper | Bright |        |

The following symbols (Punctuation/Arithmetic) are also supported:

|     |     |     |     |
| --- | --- | --- | --- |
| ,   | ;   | :   | (   |
| )   | /   | *   | +   |
| -   | =   | <   | >   |
| <=  | >=  | <>  | '   |

All the above Commands, Functions, Statements and Symbols can be used in exactly the same way as they are in standard Sinclair Basic, with the following exceptions.

**Inkeys** - To read a key, the *Inkey$* command must take up the following format: *If Code Inkey$ = x Then ...*, *x* being the character code of the key to be read. This can be found by looking in Chapter 26, appendix A of the Spectrum manual. Eg, five has the code of 53, nine has the code of 57, etc.

**Numbers** - All numbers used at any time in the program should be in the range of 0–65535. Any negative number will hold the value of *-65536-x*, *x* being the negative number. It should also be noted that only integers (whole numbers) are allowed or stored after calculation.

**Beep** - The *Beep* command has the format as in standard Sinclair Basic (eg, *Beep x,y*) except in that *x* holds the duration of the sound in micro seconds (approx) rather than holding the duration in seconds. Rather than *y* holding the value of the note to be played, *y* holds the result of the following equation: frequency * time (in seconds). Using this method more variety of sounds can be produced.

Next week, the remainder of the Basic Listing and how to compile your own programs ([Life in the fast lane](mehmood-part-2.md)).

Source of [part 1](../src/compiler1.bas).