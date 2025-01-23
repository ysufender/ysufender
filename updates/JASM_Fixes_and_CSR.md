### JASM Fixes and CSR

The endianness caused problems while working on CSR::Board class. I had to go back
to JASM and change the endianness, as well as add some new lines to CMakeLists.txt 
and the build script for it to support mingw-w64 on Linux machines. Now it looks like
everything is okay, projects use big endian (if I remember correctly) to write/read 
binary files.

The build scripts (build.sh ones, I didn't work on build.ps1 files) now support 
windows targeted builds via mingw-w64. One little problem is that there was no 
implicit conversation from std::filesystem::path to std::string so I had to manually
convert while passing. So the project source code has been changed a tiny bit.
