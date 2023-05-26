********************************
** Movement                   **
********************************

VIM is a modal editor.

It means that it has multiple modes. In notepad you can write always. In VIM you can only write in INSERT mode (and REPLACE mode but that is another thing).

When you see NORMAL in bottom left corner, you are in NORMAL mode.

- Move cursor with arrow keys, of if you are leet use h,j,k,l.
- Jump to end of line with $ and to begingin with ^ (regexes!)

In NORMAL mode colon : is an important key. 

Press : and write 15 - your cursor should go to this line. Get it? The easiest way to jump to a certain line.

You can do lot's of things in NORMAL mode with :

Try:

:help (:q to exit)
:!ls -la (hot damn! Shell commands!)

Pressing arrow keys or hjkl is laborous.

- Jump faster down with ctl+d and up ctrl+u
- w jumps word and W (shift+w) jumps WORD, in normal text they work quite the same but really differently with code
- b and B jumps word and WORD backwards
- for advanced players, test `f+<char>` and `F+<char>` (jump to next/prev <char>) 

NOW MESS AROUND. Select a word with your eye and then try to reach it with cursor.

********************************
** Actually writing some text **
********************************

With `i` you enter INSERT mode. In INSERT mode you literally have notepad.

With <ESC> you exit INSERT mode back to NORMAL mode.

- note that the cursor pops before where the cursor is in NORMAL mode 
- try `a` and see the difference (i = insert, a = append) 
- now try `o`
- and `shift+i`, `shift+a`
- `shift+o` is really neat with code

No worries. You will not remember these now. It takes practice.

Now try to use jumping and switching to INSERT mode and back to NORMAL mode.

In NeoVim crtl+s saves the document. If you mess something up, delete lines by accident of whatever, just save the document and `:!git checkout -- .`

Of course `:w` saves (writes) the document as well as in normal vim.




