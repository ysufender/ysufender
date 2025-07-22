### CSR and stdlib are Out

In the last dev update, the C++ callback mechanism was not ready yet and I said I'd work on it.
Now it is done! Along with the libstdjasm, CSR can now do native callbacks. Notice that I said
"native callbacks" and not "C++ callbacks". That's because as long as it is compatible with
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
