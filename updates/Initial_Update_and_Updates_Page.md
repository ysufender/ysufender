### What is This Updates Thing?

I decided to make something like a devlog or a mini blog-ish. 
And I'm too lazy to do it properly so I made the 
[`update_update.sscript`](https://github.com/The2ndSlimShady/The2ndSlimShady/blob/master/update_update.sscript) 
script to update the [`updates.md`](https://github.com/The2ndSlimShady/The2ndSlimShady/blob/master/updates.md) 
accordingly with the markdown file I specify from command line residing at 
[`updates`](https://github.com/The2ndSlimShady/The2ndSlimShady/blob/master/updates) 
directory. The script sets the `Last Update` and updates the `History` list. 
And that's it. Yeah.

To show that it works as I intended, I'll first push the `updates.md` empty, then
update it using the script.

### Usage

I made the script in my own scripting language because why not? Plus it's a proof
that even though the language is ugly as hell, it can still get some job done.

`SlimScript update.sscipt`           -> Prints help
`SlimScript update.sscipt %p help`   -> Prints help
`SlimScript update.sscipt %p list`   -> Lists all available updates under `updates` directory 
`SlimScript update.sscipt %p <name>` -> Applies the given update 
