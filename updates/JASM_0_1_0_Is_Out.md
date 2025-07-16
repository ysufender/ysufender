### JASM 0.1.0 is Out

In the last dev update I stated that "CSR and JASM can be considered ready for usage".
However there were missing things like static and dynamic linking for the JASM linker.
I just updated the repo and added static linking support and made the repo public. That
means officially JASM 0.1.0 is out! I can't say it's 1.0.0 because it still lacks a couple
of things. I'll update the repo in the future and release 1.0.0. But I must say that this
won't be happening any soon because I'll focus on CSR to implement C++ callbacks and
memory mapping (because I just realized that concurrent processes using interrupts will
not work unless there is memory mapping).
