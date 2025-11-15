### Working On A Compiler

#### About CSR

So CSR is done. There is a C callback system that you can find in the repo, but it's
bound to be changed sometime. And it executes pretty well. I'll add some new instructions
to the JASM and then to CSR. Currently CSR only supports flat mode, that is one execution
per invokation. So for every ".jef" file you wan't to execute one instance of CSR
should be executed. But anyway.

#### About the Compiler

I started writing a compiler in [Effekt research language](https://effekt-lang.org/). The
compiler will emit JASM IL and then assemble it to bytecode using the embedded version
of JASM. The lanugage looks like Zig, feels like Zig (maybe also C3) and so on and so forth.
It is both an assignment of sorts and also writing JASM IL by hand is getting tiresome.
Plus I need to build some real project using JASM IL to prove it can technically be used,
and I don't want to write a whole project in the IL. The language won't have crazy optimizaitons
so that I can start working on JASM assembler optimizations and start seeing results directly. Also
if I ever add native assembling to JASM, the language will then be able to call C functions
and such easily so I might have a scripting/programming language of sorts.

Also since I'm so bad at finding names I named the language JASL. Take a wild guess about
what it stands for.

##### A Snippet of JASL (Can Change in the Future)

```rust
// all files must start with a module directive, not necessarily unique.
// think of them as namespaces.
module string

/*
    /* Layouts
        They're basically structs without alignment. Tightly packed. I don't want OOP.
    */

    /* Wrapper
        'wrapper' means that it wraps whatever inside so kind of a type alias. No one
        can access the insides except the type itself in certain scenarios.
    */

    /* Type Names
        Every custom type (String is a semi-built-in custom type) must start with an uppercase
        letter. Built-ins may start with lowercase letters.
    */

    /* Yeah also nested comments */
*/
wrapper layout String { 
    data: ptr; // ptr is the same as void*. just syntax sugar.
}

// you can access this function from some other module using the full qualified name
// like string::unpack()
//
//          this is not a tuple, it's just multiple returns
//                              |
//                              |
pub fn String::unpack() -> (u32, i8*) {
    // immutable variables by default. use 'mut' after 'let' to make them mutable.

    // type annotation is mandatory.
    let size: u32 = ptrcast(this.data).get() // ptrcast and get are built-in
    let str: i8* = ptrcast(this.data.offset(4)) // offset is also built-in. No overloaded '+'

    return size, str; // you can also wrap them in parentheses
}

// This is nearly the same as above but in this case 'this' can't access
// to 'data' because the function is not defined on type String.
// pub fn unpack(this: String) -> (u32, i8*)
```

Additionally circular dependencies are alright, you don't have to define functions and types
before use, you don't have to include explicitly to use something from some other file given
that compiler detects that file is already included in the include hierarchy, you can extend
modules by "module <the_same_name>" at the start of the file, and you don't need to feed the
compiler all the files you wish to compile it detects used files from includes and compiles
them all.

There are probably more features to come, but I can't remember right now.
