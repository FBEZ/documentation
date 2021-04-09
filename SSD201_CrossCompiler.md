---
title: Cross compiler Setup
parent: IDO-SBC2D70
nav_order: 1
---

# Setup of the cross compiler

`tar -xvf gcc-arm-8.2-2018.08-x86_64-arm-linux-gnueabihf.tar.gz -C .`

`export PATH=/home/francesco/Projects/SoMCompiler/gcc-arm-8.2-2018.08-x86_64-arm-linux-gnueabihf/bin:$PATH`

## Create The file
```
#include <stdio.h>

int main(int argc, char* argv[])
{
    printf("Hello World!\n");
    return 0;
}
```
Save it as HelloWorld.c.

Compile the file with
`arm-linux-gnueabihf-gcc -C HelloWorld.c -o HelloWorld.o`

And upload it to the board via scp. 

## Reference
+ [Industio reference documentation](http://doc.industio.com/docs/ido-som2d01/som2d01-01)