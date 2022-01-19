This Brainfuck interpreter is written in Python, and it is compatible with all programs written for other versions of the interpreter. It has the classic rules of the Brainfuck language, supports standard commands and a special mode of operation of cells.
<h1> Short Guide </h1>

Here is an example of starting a programm from file brain.txt: <br>
**pybrainfuck brain.txt <cells_mode>**<br>
<br>
<h2> Cells Controll </h2>
'cells_mode' argument can take two values: -dynamic and -fixed_cells_num <num> <br>
<br>
Program, that running in dynamic mode, will automatically create new cells, if you're moving to them.<br>
<br>
However,program with fixed number of cells will create them before starting the interpretation process.  If you exceed the number of allowed cells while the program is running, it will not work. <br>
<br>
Dynamic mode can help when you working with big amount of cells, but this mode requires more RAM. On the other hand, fixed cells mode allows you to controll resources and allows you to fix the limit, but you need to strictly control the number of transition operations in the source code. <br>
That is all you need to know about cells modes
  
  <h1> Issues </h1>
  If your program finds errors that violate the general concepts of the Brainfuck language, it will not run until you fix it.<br>
  Below is a complete list of errors that you may encounter: <br>
  * Error: row x does not exist! - this error may encounter if you using fixed_cells_num, or trying to move to cells with negative index. Try to switch into -dynamic or search for error in your source code. Also remember, that in pybrainfuck program starts on cell with index 1.<br>
  *Error: No mode is set for rows. Use -dynamic or -fixed_cells_num <num> - the error speaks for itself. Probably, you forgot the argument, that tells program cells mode.
List may extend with further updates. If you encounter an error that is not described in this guide, please send a bug report to the issues section.
  
