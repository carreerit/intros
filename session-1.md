Linux is command line. 

Intro command to get h/w and s/w info.
-> Check whether the machine which you login is linux or something else??
    Run the command : `uname`

-> Check your machine is 32 bit or 64 bit

   If the answer comes as 
        x86/ i386/ i586/ i686 -> 32 bit
        x86_64  -> 64 bit
       
   Command: `uname -p`
    
-> Which Operating System you are using ??

    Run the command : `cat /etc/*release`
    
-> What is the processor.

    Command: `cat /proc/cpuinfo`
    
-> What is the RAM/Memory Size??

    Command: `cat /proc/meminfo`
    
-> Check the Disk Size

    Command: `sudo fdisk -l`
