## Last Update

### CSR and stdlib are Out

In the last dev update, the C++ callback mechanism was not ready yet and I said I'd work on it.
Now it is done! Along with the libstdjasm, CSR can now do native callbacks. Notice that I said
native callbacks and not C++ callbacks. That's because as long as it is compatible with
C ABI, and you write necessary handlers/bindings for the functions, you can do callbacks
to any language! But as I said there are regulations. You should see CSR documentation if you
want to know more about them. Anyway. The memory mapping is still not ready but CSR is practically
now usable in projects. Well, I don't advise using a backend to make a project but hey, people used
assembly before the time began.

I have a couple of plans for CSR, like handling native memory instead of using a preallocated buffer
as a RAM for the VM. That'd increase the speed of the callbacks. And maybe increase the speed of the
bytecode alltogether. Oh, speaking of speed, I did some quick tests and scripts to compare Python, Lua
and JASM Bytecode. It's kinda unfair because JASM doesn't have a frontend yet so there isn't any 
syntactical sugar to be unpacked at runtime but anyway. Turns out JASM Bytecode is 4-5 times faster
than Python and 3-4 times slower than Lua when doing basic operations, such as input/output and
calculations. These include native callbacks too. With the same amount of IO operations, the
speed difference is around the numbers I gave. I take that as an accomplishment, even though it doesn't
mean a thing.

Anyway.

## History

- [CSR and stdlib are out](https://github.com/ysufender/ysufender/blob/master/updates/CSR_and_stdlib_are_out.md) - [22/07/2025]
- [JASM 0.1.0 Is Out](https://github.com/ysufender/ysufender/blob/master/updates/JASM_0_1_0_Is_Out.md) - [16/07/2025]
- [CSR Update](https://github.com/ysufender/ysufender/blob/master/updates/CSR_Update.md) - [25/05/2025]
- [CSR Communication Between Processes](https://github.com/ysufender/ysufender/blob/master/updates/CSR_Communication_Between_Processes.md) - [25/01/2025]
- [JASM Fixes and CSR](https://github.com/ysufender/ysufender/blob/master/updates/JASM_Fixes_and_CSR.md) - [23/01/2025]
- [Current State of CSR](https://github.com/ysufender/ysufender/blob/master/updates/Current_State_of_CSR.md) - [04.01.2025]
- [About JASM and CSR](https://github.com/ysufender/ysufender/blob/master/updates/About_JASM_and_CSR.md) - [10.12.2024]
- [Most Recent Update Is Now Shown On README](https://github.com/ysufender/ysufender/blob/master/updates/Most_Recent_Update_Is_Now_Shown_On_README.md) - [28.08.2024]
- [About CSLB](https://github.com/ysufender/ysufender/blob/master/updates/About_CSLB.md) - [28.08.2024]
- [Now With the Dates](https://github.com/ysufender/ysufender/blob/master/updates/Now_With_the_Dates.md) - [28.08.2024]
- [Initial Update and Updates Page](https://github.com/ysufender/ysufender/blob/master/updates/Initial_Update_and_Updates_Page.md)
