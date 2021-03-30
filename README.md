# Docker-Forth - Docker images for popular Forth systems

When you try to write portable Forth programs it is hard to verify
that your program is in deed compatible to a wide variety of 
Standard Forth systems. It would be ideal if you could test your 
program against many systems. With Forth systems in docker containers
you now can.

This repository provides Dockerfiles for a growing number of 
popular Forth systems, so it is getting easy to run them for a
test drive.

If you are not familiar with Docker, read about it at
[www.docker.com](https://www.docker.com/).

If you want to write Standard Forth programs and contribute
them to the community have a look at
[forth-standard.org](http://forth-standard.org/ "Forth standard web page")
and 
[theforth.net](https://theforth.net/ "The Forthnet")

## Supported Forth systems

- [cforth](./cforth)  
  Forth in C by Mitch Bradly, https://github.com/MitchBradley/cforth 

- [figforth32](./figforth32)  
  32 Bit FIG-Forth for Linux by Albert van der Horst, https://home.hccnet.nl/a.w.m.van.der.horst/figforth.html  

- [flk](./flk)  
  Optimizing native code compiler targeted for the Intel 386+ CPU by Lars Krueger, mirror at https://github.com/uho/flk

- [gforth](./gforth)  
  Gforth as installed in latest Debian, by Anton Ertl, Bernd Paysan, et.al,  https://www.gnu.org/software/gforth

- [gforth-current](./gforth-current)  
  A fairly up to date gforth development build, by Anton Ertl, Bernd Paysan, et.al, https://github.com/forthy42/gforth

- [gforth32](./gforth32)  
  32-Bit version of gforth 0.7.3, https://www.gnu.org/software/gforth

- [gforth32-0.6.2-7.3_libffcall1](./gforth32-0.6.2-7.3_libffcall1)  
  Ancient gforth version 0.6.2 (32 Bit) that some applications need, https://www.gnu.org/software/gforth

- [gforth64-0.6.2-7.3_libffcall1](./gforth64-0.6.2-7.3_libffcall1)  
  Ancient gforth version 0.6.2 as 64 Bit Forth, https://www.gnu.org/software/gforth 

- [kforth32](./kforth32)  
  Kforth, 32 Bit version by Krishna Myneni, https://github.com/mynenik/kForth-32

- [kforth64](./kforth64)  
  Kforth, 64 Bit version by Krishna Myneni, https://github.com/mynenik/kForth-64

- [lina32](./lina32)  
  ciForth 32 Bit Linux version by Albert van der Horst, http://home.hccnet.nl/a.w.m.van.der.horst

- [lina64](./lina64)  
  ciForth 64 Bit Linux version by Albert van der Horst, http://home.hccnet.nl/a.w.m.van.der.horst

- [mecrisp-stellaris](./mecrisp-stellaris)  
  Native Code ARM Forth by Matthias Koch, http://mecrisp.sourceforge.net 

- [minforth1.5](./minforth1.5)  
  Forth in C with transpiler early version by Andreas Kochenburger, mirror at https://github.com/andrewtholt/minforth

- [minforth3.4](./minforth3.4)  
  Forth in C with transpiler by Andreas Kochenburger, https://sourceforge.net/projects/minforth

- [muforth](./muforth)  
  Forth in C by David Frech, https://github.com/nimblemachines/muforth

- [pfe](./pfe)  
  Forth in C Portable Forth Environment by Dirk Zoller, Guido Draheim, et al., https://sourceforge.net/projects/pfe

- [pforth](./pforth)  
  Forth in C by Phil Burk, https://github.com/philburk/pforth 

- [sf-forth](./sf-forth)  
  ANS-Forth Compiler for Linux, by KTarasov, Andrey Filatkin, Aleksej Saushev, et. al. , http://downloads.sourceforge.net/spf

- [swiftforth](./swiftforth)  
  Commercial ANS Forth standard system by Forth, Inc., evaluation version, http://www.forth.com

- [ueforth](./ueforth)  
  Forth in C (also Basis of esp32Forth) by Brad Nelson, https://github.com/flagxor/eforth

- [vfxforth](./vfxforth)   
  Commercial ANS Forth standard system by MPE Ltd, evaluation version, https://www.mpeforth.com

## Try them

All free systems are also available as prebuilt images. To run them just run

    docker run -i -t --rm rundockerforth/SYSTEMNAME

where `SYSTEMNAME` is one of the above Forth system names.

## Contribute

If you want to improve the images (e.g. update them to a newer version, 
reduce the memory footprint, etc.) or contribute other systems,
I would be happy to accept your pull requests.

----

May the Forth be with you.

