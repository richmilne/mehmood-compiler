# Life in the fast lane

Make your Basic programs run faster with Part Two of Compiler by **A. Mehmood**  
([Popular Computing Weekly, 2 May–8 May 1985, p 22–24](https://archive.org/details/popular-computing-weekly-1985-05-02/page/n21/mode/1up))

This week we present the remainder of the of the Basic listing and the explanation of the supported functions.

**Pause** - The *Pause* command works in a different way from the way it works in standard Sinclair Basic, in that the pause command in the compiler has the effect of *Pause 0*. The *Pause* command however uses the same format as it does in standard Sinclair Basic (eg, *Pause x*, *x* being any integer between 0-65535). It should be noted the value of *x* is not taken into account and is only used to overcome the standard Sinclair Basic syntax checking.

**Strings** - No Strings or String variables are supported, including string printing, or anything using double quotes.

**Rnd** - The *Rnd* command works in exactly the same way as it does in standard Sinclair Basic except that it produces a random number between 0–14 rather than 0–.99.

**Border** - The *Border* command works slightly differently from the Sinclair version. To get the required border colour the standard Sinclair Basic format should be used, (ie, *Border x*) where *x* has the result of the equation: *(y\*8)+z*. *y* is the colour of the border required and *z* is the ink colour of the lower half of the screen (bottom two lines), where all the error reports are produced.

**Variables** - Variables names can consist of any letter of the alphabet, and may be coupled with the number 1. This format allows a maximum of 52 variables. To assign a variable the standard Sinclair Basic format should be used.

**Arithmetic** - Any arithmetic using +, -, *, / can be performed. Brackets may be used. Although the compiler can handle fairly complicated arithmetic it is advised to keep equations short.

**Print** - The *Print* command works approximately as it does in standard Sinclair Basic, however it can *only* have the following formats:  
*Print At x,y;Chr$ z; Chr$ z...*, or  
*Print Tab y; Chr$ z;...*, or  
*Print Chr$ z; Chr$ z...*, or  
*Print...*  
This where *x* is the line number, *y* is the column number and *z* is the code of the character to be printed or any variable that exists within a program.

**Draw** - The *Draw* command uses a slightly different form from those used in standard Sinclair Basic, in that all negative numbers must hold the result of the following: (negative number required) - 1. The format of the command however is exactly the same as in standard Sinclair Basic, eg, *Draw x, y*.

All the above changes sometimes makes programs that are to be compiled incompatible with the way that standard Sinclair Basic works, however, this can be overcome by using commands which are compatible with both the Basic and the Compiler, changing commands before conversion or by simply omitting commands which are not compatible.

Type in the compiler as shown in the listing taking great care, especially with *Line 1* which should have at least 200 characters in it.

Next week, how to convert your own programs, plus a demo program for the Compiler. ([Into code...](mehmood-part-3.md)).

If you would like a tape copy of Compiler without typing it in, write to the author at 30 Webber House, North St, Barking, Essex, enclosing £2.75.

Source of [part 2](../src/compiler2.bas).