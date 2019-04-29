# empty\_msvc
A collection of "empty" MSVC projects (i.e. main() only consists of "return 0"), compiled using various versions and configurations of Visual Studio along their respective PDB files.

## What is this good for?

The use case is probably quite special.
For us, this is used as groundtruth in binary code indexing / function similarity context.

## What's the folder structure / naming scheme?

So far, we used

  * MSVC++ 6.0   MSC_VER 1200 (Visual Studio 6.0 Standard)
  * MSVC++ 7.1   MSC_VER == 1310 (Visual Studio .NET 2003 v7.1 Standard)
  * MSVC++ 8.0   MSC_VER == 1400 (Visual Studio 2005 Express)
  * MSVC++ 9.0   MSC_VER == 1500 (Visual Studio 2008 Express)
  * MSVC++ 10.0  MSC_VER == 1600 (Visual Studio 2010 Express)
  * MSVC++ 11.0  MSC_VER == 1700 (Visual Studio 2012 Express)
  * MSVC++ 12.0  MSC_VER == 1800 (Visual Studio 2013 Community)
  * MSVC++ 14.0  MSC_VER == 1900 (Visual Studio 2015 Community)
  * MSVC++ 14.16 MSC_VER == 1916 (Visual Studio 2017 Community v15.9)
  * MSVC++ 14.2  MSC_VER == 1920 (Visual Studio 2019 Community v16.0.2)

and created an empty WIN32 console project each and compiled it

  * using Debug and Release mode
  * using the following linking configuration
    * Multi-threaded - /MT (i.e. static linking)
    * Multi-threaded Debug /MTd
    * Multi-threaded DLL - /MD (i.e. linking against the respective MSVCRT)
    * Multi-threaded DLL debug - /MDd
    * Single-threaded - /ML
    * Single-threaded Debug - /MLd
  * for a 32bit and 64bit target where possible

The folder structure we used is:
<visual\_studio\_version>/<build\_version>/<debug|release>/<visual\_studio\_version>\_<x86|x64>\_<debug|release>\_<mt|mtd|md|mdd|ml|mld>.<exe|pdb>

## How can I use it?

In any way you want. If you find this useful, credit is always appreciated. :)

## How can I help?

The above list of versions is not complete yet. 
Should you have access to one of the missing versions, feel free to compile an empty WIN32 console project in the same way as provided above and create a pull request.

## Changes

* 2019-04-29 added VS6, 2003, 2017, and 2019
* 2019-04-26 initial commit with VS 2005, 2008, 2010, 2012, 2013, 2015
