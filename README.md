```c
#include <complex.h>
#include <math.h>
#include <stdio.h>
#include <string.h>
#include <unistd.h>

int main() {for(double time=0;1;time+=0.016f){ puts("\e[2J\e[H");
for(int i=0;i<2048;i++){_Complex double z=0;_Complex double c=2j*
(double)(i/64)+i%64; double thing=cos(time)+1; c*=2*thing/64;c-=(
thing)+(thing)*1j+sqrt(2);int iter=0;while(cabs(z*z)<4.0&&++iter<
128){z=z*z+c;}putc(" .,:ilwW"[(iter!=128)*(iter%8)],stdout);if(!(
/*z=z*z+C;z=z*z+C;z=z*z+C;z=z*z+C;z=*/i%64)){putc('\n',stdout);}}

         char *_0 = "         Aidan Ocmer         \0";
         char *_1 = "     Computer Programmer     \0";
         char *_2 = " https://github.com/aidocmr  \0";
         char *_3 = "         z = z^2 + c         \0";

printf("\e[%luA\e[%luD",32/2,(64+strlen(_0))/2); puts(_0);printf(
"\e[%luC",(64-strlen(_1))/2);puts(_1);printf("\e[%luC",(64-strlen
(_2))/2);puts(_2);printf("\e[H\e[%luC",(64-strlen(_3))/2);puts(_3
/*z=z*z+C;z=z*z+C;z=z*z+C;z=z*z+C;z=*/);usleep(16000);}return 0;}
```
Compile with `$ gcc main.c -lm -o aidocmr`
