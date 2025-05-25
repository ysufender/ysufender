### CSR: Update

As for today, CSR and JASM can be considered ready for usage. Sure they can't do IO
operations because C++ callback system is not ready yet but if you say "I can just 
read the ROM, RAM and registers manually" then you can technically use it.

Basic arithmetic operations, conditionals, callstacks, parameter and return values are
supported so it can do pretty much everything on paper. Oh, heap allocations are also
present, though I forgot to add a deallocate instruciton, will do that soon.

Below, is a program that finds factorials, the stack is limited to 84 because I didn't
want to see pages of stack values printed on my terminal. So this code can just calculate
factorials of numbers up to 5 (included). But you can just increase the stack size so
no problem at all?

```
.prep
    org main
    sts 84
    sth 0
.body
    fact:
        stc %i 2
        cmp %i %geq
        pop %i
        cnd rec 
            pop %i
            stc %i 1
            mov 4 &bl
            ret
        rec:
            dup %i 
            dcr %i 1
            mov 4 &bl
            cal fact
            swp %i
            pop %i
            mul %i
            mov 4 &bl
            ret
             
    main:
        stc %i 5
        mov 4 &bl
        cal fact
        swp %i
        pop %i
        mov &eax
.end
```

It's recursive because I wanted to test the callstack creation and destruction, and
parameter/return value passing.

Next, I'll implement the C++ callback system, and improved communication between
processes for asynchronous execution.
