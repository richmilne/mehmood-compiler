# Mehmood ZX Spectrum BASIC Compiler

This document contains the source ([BASIC listings](src) and [instructions](article), [original](scans) and OCR'd) of a ZX Spectrum BASIC compiler, written by a certain A. Mehmood and published in Popular Computing Weekly magazine over the course of 3 weeks in April/May 1985.

As with so many type-ins from that era, this one doesn't work. Just trying to compile the line `1003 BORDER 7` leads to the output

``` 
BORDER IN 1000
ATN    IN 1000

Error in line 1000, statement 1
Invalid function
``` 

The reason the program doesn't work may be because of an error I made typing in the first few lines of the program (1–192). As you can see from the scans in this repo, these lines were printed in a very small font, as well as being slightly blurred

It also seems that the program was submitted in an incomplete state. There are several redundant commands (like two consecutive `LET R$=CHR$ PEEK P` on lines [50](src/compiler1.bas#L18) and [51](src/compiler1.bas#L18) and two 'invalid command' error messages on lines 270 and 299) and, as far as I can tell, several blocks of unreachable code (lines [299](src/compiler1.bas#L119), [450–462](src/compiler2.bas#L19-L21), [773–820](src/compiler2.bas#L63-L80)). This may be because of a typo made in the first few lines, where I perhaps mistyped the crucial target of a `GOTO` or `GOSUB`. Or it could be because the magazine made mistakes when laying-out the listing, leaving out and re-arranging lines.

The line numbers of the program are so close together, however, that this seems unlikely. Generally, though, the overall impression is that this version is unfinished or still a work in progress.

The author also offered to send a tape copy of the compiler for £2.75. It seems this tape copy did work, as the compiler was reviewed in [issue 19 of CRASH magazine](https://www.crashonline.org.uk/19/compilers.htm). To date, however, no copy of this tape has been found, and it's listed as "Missing in Action" at the [World of Spectrum](https://worldofspectrum.net/item/0011603) and other [Spectrum forums](https://spectrumcomputing.co.uk/index.php?cat=96&id=11603).

So this code repository has been put together as an appeal to the reader. If you happen to have a copy of the tape version lurking at home in the attic with the rest of your Speccy collection, OR you can spot the error in my OCR'd text, or otherwise get the compiler to work - please open a PR or otherwise get in touch so we can get a working version published.

Many thanks...