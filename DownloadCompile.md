# Getting the Source Code #

If you decided you want to build the application yourself, then you will first need to download the source code.  All of the source is kept in a SVN repository.  If you just want to anonymously check out the code then do the following:

svn checkout http://wildcat-cad.googlecode.com/svn/ wildcat-cad-read-only

If you are a project member and will be modifying the code then you need to authenticate your checkout.  Use the following command with your username instead of XXXX:

svn checkout https://wildcat-cad.googlecode.com/svn/ wildcat-cad --username XXXX

These instructions differ slightly from those listed on the Source page.  That page adds _trunk_ after /svn/.  I am currently getting errors when I use this command, but just /svn/ works just fine.  I will keep my eye on this issue and update the wiki as needed.


## Dependencies ##

For each different platform there are slightly different dependency libraries.  I have worked hard to limit the number of dependencies.  Included in the source code download are binary versions of all dependencies (for all required platforms) and the header files for those dependencies.  You should not have to download anything addition beyond that listed above.


# Compiling on Mac OS X #

**Required Development IDE: XCode 3.x**
**External Dependencies: xerces-c**

The current source code should work fine on 10.4+ of Mac OS X.  I have not tested it on Tiger, but I don't think that anything is Leopard dependent except for the use of XCode 3.x.  A little bit of time should yield a project for the 2.x verion of XCode.

There are a couple of extra steps to work around an issue with XCode.

  1. Download source code (see above)
  1. Open wildcat-cad/Projects/XCode3/Wildcat.xcodeproj


# Compiling on Windows XP #

**Required Development IDE: Visual Studio 2005 (VS8)**
**External Dependencies: xerces-c, libtiff, freetype, pthreads**

or see [CompilingVS2008Express](CompilingVS2008Express.md) page


# Compiling on Linux #

Currently Linux is not supported.  It should not be too difficult.  The initial Windows XP port took me about 5 days so to Linux should be pretty easy.