# empty\_msvc
A collection of "empty" MSVC projects (i.e. main() only consists of "return 0"), compiled using various version and configurations of Visual Studio.

## What is this good for?

The use case is probably quite special.
For us, this is used as groundtruth in binary code indexing / function similarity context.

## What's the folder structure / naming scheme?

So far, we used

  * Visual Studio 2005
  * Visual Studio 2008
  * Visual Studio 2010
  * Visual Studio 2012
  * Visual Studio 2013
  * Visual Studio 2015

and created an empty WIN32 console project each and compiled it

 * using Debug and Release mode
 * using the following linking
   * Multi-threaded - /MT (i.e. static linking)
   * Multi-threaded Debug /MTd
   * Multi-threaded DLL - /MD (i.e. linking against the respective MSVCRT)
   * Multi-threaded DLL debug - /MDd
* for a 32bit and 64bit target where possible

The folder structure we used is:
<visual\_studio\_version>/<build\_version>/<debug|release>/<visual\_studio\_version>\_<x86|x64>\_<debug|release>\_<mt|mtd|md|mdd>.<exe|pdb>

## How can I use it?

In any way you want. If you find this useful, credit is always appreciated. :)
