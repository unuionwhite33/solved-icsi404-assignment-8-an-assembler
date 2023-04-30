Download Link: https://assignmentchef.com/product/solved-icsi404-assignment-8-an-assembler
<br>
In the last assignment, testing was done by creating strings of bits (0101010 style) and pre-populating memory. This is a very tedious way to write programs. Nearly as soon as we had computers, their designers realized that programming using bits was too error prone and difficult. Kathleen Booth, in 1947, invented the first assembler.

An assembler is a program that takes text as input and outputs bits that correspond to that text. As you can imagine, writing move R1 -1 is much easier than writing 0001 0001 1111 1111

To create an assembler, we will create a new class, Assembler. It will have one public method: public static string[]  assemble (string[]). We will pass into that method a series of strings, like “move R1 -1” and it will return the bit patterns that are represented by that command. A simple approach is to use the split method on string to break an input line up into tokens (remember this from ICSI311?).

A more complete, robust implementation would be to build a lexical analyzer. This would loop over each character. When a space is found, it would decide whether this is a number, a register (R1, for example) or a keyword (like “move”).

You could use a case statement to decide what to do based on the first token (the assembly command). Note that there will be lots of cases of repeated functionality – you must create helper methods. One example of this is converting a register name (like R1) to a bit pattern (0001). While we are working on low level code, we should not forgo good code quality.

Like lexical analysis, there is a more complete, robust solution available – a recursive descent parser.

These were covered in ICSI311, but Wikipedia has some good explanation: https://en.wikipedia.org/wiki/Recursive_descent_parser

You must create a new test class (assembler_test) that sends assembly language into the assembler and confirms that the  bit patterns created are correct.