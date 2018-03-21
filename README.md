# Shellcode

## Generating Shellcode from C

1. Run `gcc code.c -c`, using the -c flag to prevent linking.

2. Then run `objcopy -O binary -j .text shell.o shellcode` to create a binary file with the contents of .text

3. Use `od -An -t x1 shellcode | sed -e 's/ /\\x/g' > shellcode.txt` to dump the contents of "shellcode" and pipe them to sed to replace the spaces with \x so that it can be used in C code.


## The following C code can be used to execute your shellcode

    //run_shellcode.c
    
    unsigned char code[] = <shellcode goes here> // use char [] to prevent being placed in read-only section
    
    int main(int argc, char **argv) 
    {

      int (*foo)() = (int(*)())code;
      foo();

      return 0;
    }


- **This code must be compiled using the -z execstack flag in gcc**

