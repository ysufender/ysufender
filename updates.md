## Last Update

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

## History

- [JASM Fixes and CSR](https://github.com/The2ndSlimShady/The2ndSlimShady/blob/master/updates/JASM_Fixes_and_CSR.md) - [23/01/2025]
- [Current State of CSR](https://github.com/The2ndSlimShady/The2ndSlimShady/blob/master/updates/Current_State_of_CSR.md) - [04.01.2025]
- [About JASM and CSR](https://github.com/The2ndSlimShady/The2ndSlimShady/blob/master/updates/About_JASM_and_CSR.md) - [10.12.2024]
- [Most Recent Update Is Now Shown On README](https://github.com/The2ndSlimShady/The2ndSlimShady/blob/master/updates/Most_Recent_Update_Is_Now_Shown_On_README.md) - [28.08.2024]
- [About CSLB](https://github.com/The2ndSlimShady/The2ndSlimShady/blob/master/updates/About_CSLB.md) - [28.08.2024]
- [Now With the Dates](https://github.com/The2ndSlimShady/The2ndSlimShady/blob/master/updates/Now_With_the_Dates.md) - [28.08.2024]
- [Initial Update and Updates Page](https://github.com/The2ndSlimShady/The2ndSlimShady/blob/master/updates/Initial_Update_and_Updates_Page.md)
