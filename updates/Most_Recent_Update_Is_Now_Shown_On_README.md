### The Lates Dev Update Will Now Be Shown On README.md

Because why not? Besides I'm on something like a hiatus with JASM. So I had to do
something to keep me busy.

#### A Couple of Problems With The Script

For some reason (the reason being shitty design of SlimScript), when reading the
`README.md`, the script loses every single quote symbol. I'll try to track the bug down
but not any time soon.

#### Additions to the Script

Now the script has the new argument `recent`. It prints the most recent entry under
`updates/` directory.

Usage: `SlimScript update.sscript %p recent`
