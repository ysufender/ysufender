### ShakeCpeare

A couple of days ago I was wandering around in my old projects and stumbled
upon [SlimScript](https://github.com/ysufender/SlimScript), which I use
to automate this mini devlog using the [update.sscript](../update.sscript)
script.

Anyway, I took a quick look at the update script I use, which I wrote a long
time ago and forgot how it works. A couple lines caught my attention, such as:

```
set cmd to index 0 of os.args
```

and

```
foreach line in updateContents begin
    append line to newMainContent
end
```

I like the way how it is just plain spoken language, it makes it feel like...
a script.

After that I remembered that I added 1-to-1 token macros in the form of
`@macro <token_to_replace> <token_to_place>`. For some reason I didn't
add it to the documentation but whatever. The thing is, it is possible to
change the whole look of the language using said macros, for example:

```
where damaged one be
there's vigor that's the health of one
now the health of one is less vigor sadly
poor one
here

where South be place that looks heavenly also beautiful here
there's player that's from South
announce the name of player
now player is truly damaged player
```

I used a macro set that would turn this seemingly prose text into
a valid SlimScript script. It prints "Jack" by the way.

But since SlimScript is insanely slow, and the macro system is limited, I thought
maybe it is possible to do such thing in another language. Then I decided to turn
C into a full spoken language programming language.

And then, [ShakeCpeare](https://github.com/ysufender/ShakeCpeare) was born.

You can do fun things like:

```
the status main function is an action
with the body that is this program
there is this individual that is a man
known as "Jack" by some
print that man line at once
the program should end now
```

And it is a completely valid C program. How cool is that?
