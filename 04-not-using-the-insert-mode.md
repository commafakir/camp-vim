# Sometimes you just don't want to go to INSERT mode 

In general you want to go to INSERT mode only when you are producing new text.

Let's say you need to capitalize two words in a sentance.

this is a sentance, and solita and vim needs to be capitalized.

- You can go to solita, enter INSERT mode, delete with backspace and rewrite SOLITA (this is not the VIM way) and do the same thing with vim part
- You can go to solita, then `gUw` and then go to vim (with `w` jump or even `fv`) and `gUw`
- uppercase the whole line with `gUU` and lowercase with `guu`
- remember `.`!!!! 
- You probably can do this with search as well and weird regex things
- There are LOTS of different things you can do, you just have to google and sometimes you learn new tricks by accident

Hello Hello
DEL this is some text
DEL more text
And here is an important message

`:g/DEL/d` deletes all lines that matches the regex.

# Ranges

You can apply something to a certain range with `:9,14d` (delete lines from 9-14).

# Indentation

```js
// Indent one line with >> and <<
console.log("Hello")

// Indent blocks with >% and <%
// Check ==, it works suprisingly well (like `4==`)
const fun = () => {
console.log("Fix my indentation");
console.log("Please");
console.log("Pretty please");
console.log("Pretty pretty please");
}
```

Lsps offer way better indentation support.

# Searching

- basic search with `/foo` <ENTER> and then `n` to next and `N` to previous
- it is a regex so you can do pretty crazy searches with that

# Search and Replace

- `s/needle/something/g`, this only matches to the current line
- `%s/needle/something/g` matches the whole document
- lsprename is usually more usable with code though

# I mean you can even edit the numbers without insert mode

You have 15 kittens. (press `<ctrl>a` or `<ctrl>x` before the number)

PRO-LEVEL KEY USAGE
*******************

Rename function to something else. 

fn foo()

maybe `dwi` (delete foo and go to INSERT mode). It's okay, BUT

`cw` saves you one key. After a while it starts to feel more natural and stroke count really matters.

God level would be `:s/foo/something/g` as it does not require placing the cursor.
