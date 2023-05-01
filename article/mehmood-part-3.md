# Into code

This week how to use Compiler on your own programs - plus a demo game - all from **A Mehmood**  
([Popular Computing Weekly, 9 May–15 May 1985, p 24–25](https://archive.org/details/popular-computing-weekly-1985-05-09/page/n23/mode/1up))

Now you have typed in the compiler, you can use it on your own programs. To enter programs simply enter the listing of your Basic program to be compiled as you would enter a normal program, except the lowest line number you can use is 1000, because the compiler is stored in the lines 0–999.

Once you have entered your program you must take care of the following:

1. All *Gosub*s should be satisfied with *Return* statements.
2. To return back to Basic you must have a Return statement.
3. All machine code routines/sub routines called using the *Usr* statement must have a *Return* statement within them.
4. The *Stop* command will cause a direct return to *Basic*.

Now *merge* your program with *Compiler*. Once all the above has been done the program is ready to be compiled. To compile the program simply run the compiler by entering *Run*. The word *Compiler* will appear on the screen and there will be a slight pause, if the message ‘Check Sum error check Data...’ appears on the screen, it means that the data entered in Lines 980–984 is incorrect and therefore it should be checked very carefully and corrected. The compiler can then be run again. If all is well the compiler will begin to print out the Commands, Statements and Functions as they are being compiled.

Should there be an error in your Basic program the compiler will print a suitable error message, and tell on which line the error occurred so that it can be corrected and the compiler run again.

If no errors occurred through the whole program, the message ‘Compiled’ will appear on the screen together with another message telling you two addresses between which the machine code can be stored. A suitable address between the two addresses should be entered; it is advised to choose the lowest of the two addresses to store the code unless you have another machine could program stored there. Once you have entered the address you wish your code to be stored at there will be another pause (dependent on the size of the program, normally between 1 min–10 mins) after which the screen will be cleared and another two values will be printed. The first value will be the start address of your machine code and the second value will be the length of your machine code.

It is advised that you save both your Basic and machine code programs onto tape before you attempt to run the machine code program. It should be noted the machine code program will not run unless the first line of the compiler is in memory, ie, once a program has been compiled a *Line 0* will be created which must be present when running the machine code. Once the programs have saved, the machine code can be tested by using the *Usr* command as used in Sinclair Basic.

If the ‘*Out of Memory*’ error occurs whilst a program is being compiled it means the program you are compiling is too long and therefore it should be split up into subroutines and compiled subroutine at a time. The compiler, when run, erases every thing in the memory therefore if two subroutines are being tested both should be loaded in first then tested.

Now you are ready for the demo program. Type in the listing of the demo program—then merge with Compiler. Now simply type in *Run*.

The compiler will begin to print out the commands and statements as it compiles them. Once this has been done the compiler will ask you whether you want to store your compiled machine code. Enter a suitable address as told in the instructions of the compiler. There will now be a delay as the compiler loads the machine code into memory. (It will take approx 7½ mins.)

Once the code has been loaded into memory the compiler will print the address of where the code was stored and its length in bytes. You should now save the machine code as explained in the Spectrum Manual. You should also *Save* the compiler with your program.

If you *List* the compiler you will find a *Line 0* has appeared and an error will be printed. This is perfectly normal. To run any compiled programs Line Zero must be present in your programs, therefore it is a good idea to delete all the compiler and save Line Zero for later use by compiled programs. Once you have deleted all the compiler (except Line Zero) save the line as you would a normal Basic program. (This can now be used by all compiled programs that are to be run independently of the compiler.)

Although the compiled program will now run independently of the compiler (so long as Line Zero is present) it is a good idea to add a little Basic program to your machine code to improve it (you may wish to add instructions to your program or have a title page, etc).

A simple example of what I mean can be seen in Basic program that accompanies the demo program, listing two. If you type in *Goto 9999* the program will save itself together with the machine code and will auto run when loaded.

Note that the second *Save* instruction in Line 9999 is dependent on where you stored your code, so change this appropriately. Also when running compiled programs, before they have even been loaded you must clear a suitable address. If you do not know how to, type in *Clear 49999* as a direct command and then load in your program as normal.

*Compiler* is available on tape from me for £2.75 at 30 Webber House, North St, Barking, Essex.

Source of [demo](../src/demo.bas).