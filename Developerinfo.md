# AutohotkeyCE - Developerinfo

## Autohotkey build for CE devices - Infos about the solution

### Projects of the solution: The solution contains the projects:

* Aut2Exe_VC8: the compiler
* AutohotkeyCE: Autohotkey and the self executing exe
* lib_pcre: regular expression
* libCE: Autohotkey is using a closed source lib. The compiler is using the library to append the script to the self executing exe. The self executing exe is using the lib to read the script from itself. This libaray is used for wince.
If you build a win32 exe, the ahk-library is used.
* AutohotkeyCE: Setup for wince (create a cab for installing).

### Build types

There are debug and release configurations for win32 and pocketPC platforms. Autohotkey and the compiler are using these settings.

HotkeySC is the configuration for the self executing exe for both platforms.

With these configurations you can build

* debug win32 autohotkey
* release win32 autohotkey
* debug pocketpc autohotkey
* release pocketpc autohotkey

* win32 self executing exe
* pocketpc self executing exe

* debug win32 compiler
* release win32 compiler 
* debug pocketpc compiler
* release&nbsp;pocketpc compiler

If you want to compile a script on your computer and transfer the exe to your pocketpc you need an extra build type.

The compiler must run on your computer but has to use the special library to append the script in the same way the self executing exe is using&nbsp;to extract.

There's another build type deb_win32CE. That can be used to create a compiler for that case.

Last change: 13-06-09
