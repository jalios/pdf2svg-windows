# pdf2svg-windows
Compilation of pdf2SVG for windows

This repository provides windows version of pdf2svg tools provided in https://github.com/db9052/pdf2svg.

This version is compiled as described in http://www.cityinthesky.co.uk/opensource/pdf2svg/.

The platform used to do the cross compilation in a vanilla fedora 22 beta version to have latest version of poppler and cairo librairies. Version build from released version will be coming soon.

To cross compile for Windows under Linux, simply install the relevant cross-compiler packages (for Fedora this is mingw32-cairo and mingw32-poppler and their dependencies) and then replace “./configure” in the compilation instructions above with “mingw32-configure” or “mingw64-configure”.

Note : This build is provided AS IS and JALIOS SA will not do any support about that. 


Despite our efforts to recompile this program, it is still unstable (crashing with some files). We finally solved the problem by using a bash script (available at https://community.jalios.com/pdf2svg ) that iterates (each page) on "pdftocairo.exe" (from http://blog.alivate.com.au/poppler-windows/ ).
