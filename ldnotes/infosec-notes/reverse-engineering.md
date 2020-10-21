# Reverse Engineering

## Initial Information Gathering

`strings <file>`  
`hexdump -C <file>`  
open in `vim`  
`objdump -d <file>` = disassemble

  
`objdump -x <file>` = all headers, pipe into less  
    -- looking at header permissions \(rwx\)  
    -- Idx Name ==&gt; .text \(start location 0x4004d0, size\)  
                     ==&gt; .rodata \(read only data\)

execute program with `strace` or `ltrace`  
`strace ./<file>`  


  


## GDB + pwndbg

### Common Binary Info

`cmp` = compare  
`jne`= jump not equal  


`printf` = prints string  
`puts` = prints info  
`strcmp` = string compare - returns 0 if the same  


### Interacting with GDB

`run <optional agrument>` = starts executing a new instance of program  
`gdb <filename>` = start debugger  
`disassemble main` = all c has main, outputs code  
`break *main` = puts breakpoint at start of main function  
`info reg` = shows registers  
`si` = step one instruction  
`continue`= run normally until next breakpoint  
`set $eax=0` = set a variable \($eax or other\) to a value

`rip` = instruction pointer

### Basic GDB commands.

#### Break points:

```text
b F                     Set a break-point at function F.
b *A                    Set a break-point at absolute address A
b N                     Set a break-point at line number N.
b N:F                   Set a break-point at line number N at file F.


info b                  Lists break-points.
cond B cond             Set a condition to a break-point B.
cond B                  Remove the condition of a break-point B.
delete B                Delete a break-point B.
```

#### Stepping:

```text
stepi or si             Execute one machine instruction (follows a call).
step or s               Execute one C-program statement (steps into functions).
stepi N                 Do N machine instructions.
nexti or ni             Same as si but execute calls as one instructions.
next or n               Same as ni but execute functions as one statement.
bt                      Show names of the stack frames.
up                      Go up one stack frame.
down                    Go down one stack frame.
```

#### Examining:

```text
info reg                List contents of registers.
p V                     Print contents of a variable V.
x /CT A                 Examining memory where:
                        C   number of units to display. 
                        T   x hex integer.
                            d dec integer.
                            u unsigned dec integer.
                            o octal integer.
                            c character.
                            s null terminated string.
                            i as machine instruction.
                        A   an absolute address or 
                            $reg pointed by some register.
```

## Other Tools

Hopper  
radare  
ida pro/free  


