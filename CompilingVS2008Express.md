I used Windows XP.

Get Microsoft Visual C++ 2008 Express Edition and install it ( it's free, but almost 1GB ).

Download the wxWidgets source code from here.
http://prdownloads.sourceforge.net/wxwindows/wxMSW-2.8.8-Setup.exe

Set an environment variable called WXWIN to be C:\wxWidgets-2.8.8 or whereever wxWidgets installed to. ( to set an evironment variable go to Control Panel, then System, then Advanced tab, then press "Environment Variables" button, then press "New" ).

Edit C:\wxWidgets-2.8.8\include\wx\msw\setup.h changing "#define wxUSE\_GLCANVAS 0" to "#define wxUSE\_GLCANVAS 1" and changing "#define wxUSE\_ODBC 0" to "#define wxUSE\_ODBC 1"

Open and build C:\wxWidgets-2.8.8\build\msw\wx\_dll.dsw ( let VC2008 convert the projects )
Change the configuration to "DLL Unicode Release" or to "DLL Unicode Debug" if you will be building Wildcat in Debug mode.

Copy 4 of the dlls that get made from C:\wxWidgets-2.8.8\lib\vc\_dll to wildcat-cad\trunk\Build\wxWin32

They are:
  * xmsw28u\_aui\_vc\_custom.dll
  * xmsw28u\_core\_vc\_custom.dll
  * xmsw28u\_gl\_vc\_custom.dll
  * xbase28u\_vc\_custom.dll

or, if you are doing the debug mode

  * xmsw28ud\_aui\_vc\_custom.dll
  * xmsw28ud\_core\_vc\_custom.dll
  * xmsw28ud\_gl\_vc\_custom.dll
  * xbase28ud\_vc\_custom.dll


Open "wildcat-cad\trunk\Projects\wxVC9\Wildcat.sln", it should open with Visual C++ 2008 Express.

Choose "Release" configuration or "Debug".

Press "Build Solution"

If it builds OK, press "Start Debugging" to run it, or go to Windows Explorer and double-click on

Wildcat.exe in wildcat-cad\trunk\Build\wxWin32


If you have a problem, look at the forum and post a question for me.   Dan Heeks.