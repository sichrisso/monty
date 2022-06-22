# 0x19. C Stacks, Queues, LIFO, FIFO.
=
     C low-level programming language
=======================================================================

## Installation

- compile with

    gcc -Wall -Werror -Wextra -pedantic *.c -o monty
    
 ## Description:

# The Monty language

   Monty 0.98 is a scripting language that is first compiled into Monty byte codes (Just like Python). It relies on a unique stack, with specific instructions to manipulate it. The goal of this project is to create an interpreter for Monty ByteCodes files.

# Monty byte code files

   Files containing Monty byte codes usually have the .m extension. Most of the industry uses this standard but it is not required by the specification of the language. There is not more than one instruction per line. There can be any number of spaces before or after the opcode and its argument:

     julien@ubuntu:~/monty$ cat -e bytecodes/000.m
     push 0$
     push 1$
     push 2$
       push 3$
                   pall    $
      push 4$
      push 5    $
      push    6        $
      pall$
      julien@ubuntu:~/monty$

Monty byte code files can contain blank lines (empty or made of spaces only, and any additional text after the opcode or its required argument is not taken into account:

      julien@ubuntu:~/monty$ cat -e bytecodes/001.m
	       push 0 Push 0 onto the stack$
     push 1 Push 1 onto the stack$
     $
	push 2$
     push 3$
                   pall    $
		   $
	$
                           $
			   push 4$
     $
	    push 5    $
          push    6        $
      $
	pall This is the end of our program. Monty is awesome!$
     julien@ubuntu:~/monty$
