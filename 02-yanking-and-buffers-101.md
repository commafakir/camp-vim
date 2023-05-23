****************
** Copy/Paste **
****************

Vim freaks not talk about copying text.

They yank.

`yy` is the basic yank, that is line yank. Press `yy` here and then press `p`.

You have just yanked a line to register and pasted it in.

`dd` is "cut" which you can OFC paste as well.

Now we start to approach the real power of VIM. `dd` or `yy` is not the only thing you can do...

...you can attach `d` and `y` to _movements_.

Try `yw` or `dw` for an example! You can tie commands together in millions of ways! `d$` and `d^`.

Task: (Yank everything inside parenthesis) and leave this out. `f<char>` is probably the easiest movement.

Paste from file below `:r somejs.js` (tab completion should work).

***************
** Registers **
***************

VIM does not have clipboard, VIM has registers. Registers is a clipboard on steroids.

To yank something in different register start command with `"<char>` with char being the register name.

Then use `"<char>p` to paste that register out.

- default register is `"`, so `""` is kinda explicit
- List registers with just `"` (nvchad has a plugin for this), `:req <char>` shows you the contents in not nvchad config.
- `"_` is a black hole register
- learn how to use one additional register, the default and your favourite key, this way you can easily copy-paste on steroids
- number registers contains history

You can basically do for an example your own snippet collection with registers (there are better ways for snippets though).

Yank this into `f` and then you can paste new functions.

const x = () => {}

***************
** Repeating **
***************

The real power of Vim comes from repeating commands. Check the carbage that we have below, `dd` that stuff out!

wokcmworcimwc
wovmworivmwori
owirmvowrviwm
wroviwrovimwr
owirmowrmwr
owrmvoiwrmvo
owrimvworimworiv

Oh, `u` is undo. Now undo some of that carbage back. Place cursor on the first line of that carbage, then write `5dd` (5 can be how many lines there is).

Every single command can be repeated this way! I mean every. Try something like `10isomething<ESC>`. You can also jump 100 lines down with `100j`

Endless possibilities!

Repeating is the reason why VIM has relative line numbers. With relative line numbers, it's easy to see how far you have to go with repeats.

`.` is a cool repeat. It just repeats the last thing you did. Write something and repeat. You can repeat pretty much anything, but not bare movements.

Of yourse you can number repeat with dot.

For an example, do key strokes:

`owrite something<esc>`

(Start new line in INSERT mode, write something and back to NORMAL mode)

And then repeat that hundred times with `100.`

NEAT ISN'T IT!

When using repeats you have to design your movements. `o` is really different from `i` when repeated multiple times.

