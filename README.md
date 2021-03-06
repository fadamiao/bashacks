# bashacks

 1. What is it?
 2. Requirements
 3. Installation
 4. Documentation
 5. ChangeLog
 6. Bugs


## 1. What is it?

 bashacks is an open source (GPL) set of bash functions
 probably useful for programmers, security analysts and general
 users that need to do some low level type of operation.

 In fact, there is nothing really new in bashacks since
 all functions are written using exiting software in GNU/Linux
 distributions. But you still can have advantage in use short
 commands to run tasks that commonly will require a lot of lines
 to be done.

 !!! IMPORTANT !!!

 There is no error handling in bashacks. That's a job
 for bash, called programs and your responsibility. :)


## 2. Requirements

 * linux
 * bash >= 4
 * bc
 * wget - and internet access
 * hexdump
 * grep
 * objdump
 * base64
 * md5sum
 * cut
 * gdb
 * rev
 * html2text
 * tee
 * udcli e udis86 - for sc2asm() only
 * nasm - for asm2sc() only
 * awk
 * iw


## 3. Installation

 Put bashacks.sh in some directory and 'source' it to your
 shell using .bashrc for example:

    $ sudo mv bashacks.sh /opt
    $ echo "source /opt/bashacks.sh" >> $HOME/.bashrc
    $ source /opt/bashacks.sh

 And that's all. You can now call the available functions from bash.

 Additionally you need to install libudis86 to use sc2asm function. Go
 to http://udis86.sourceforge.net, download the latest version and run:

    $ tar xf udis86-*.tar.gz
    $ cd udis86-*
    $ ./configure
    $ make
    # make install
    $ cd udcli
    $ make
    # make install


## 4. Documentation

 See bh-referencia.html file (only in Portuguese, sorry).


## 5. ChangeLog

 * bashacks 1.5 - ?
  * new name: bashacks
  + new function: asminfo() - details an Assembly x86 (Intel) instruction.
  + new function: dumpheap() - dump the process heap content.
  + new function: dumpstack() - dump a process stack content,
  + new function: str2hexr() - converts string to reversed hexa bytes.
  + new function: asm2sc() - creates a payload from assembly instructions.
  + new function: sc2asm() - disassembles a payload.
  + caching in $HOME/.hf/cache to speed up things!

 * hack-functions 1.4 - Feb, 27 2012
  + new function: charcalc() - do character calculation.
  + new function: intel() - set Intel syntax for disassembling.
  + new function: rotall() - simultaneous ROT for strings
    (thanks to @laerciomasalla for suggesting it).
  + created reference guide in Portuguese.
  * hexcalc() now supports the four basic math operations and the result is
    prefixed with '0x'.
  * str2hex() and hex2str() now support the prefixes '0x', '\x', with or
    without spaces and C-array notation.

 * hack-functions 1.2 - Feb, 24 2012
  + new functions: bin2dec() and asc2hex().
  + added Intel syntax by default for gdb and objdump.
  * curl gets replaced by wget in unmd5().
  * code optimization in many functions.

 * hack-functions 1.0 - Feb, 24 2012
  - first public release with 20 functions.


## 6. Bugs

 If you think you find a bug, please fill it through
 https://github.com/merces/bashacks/issues
