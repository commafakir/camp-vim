# Macros

Macros is the thing tha blew my mind.

Macro is basically just a series of keystrokes.

Let's do something funny. Yank the following line with `"ayy`

:%s/funny/horrible/g

And then press `@a`

What you have just done is that you have evaluated the register as a macro. Macro is nothing but keys in register which are evaluated as a macro. For funny things, yank a paragraph into a register and evaluate it as a macro. `u` is undo.

Of course this is not the way macros are usually used. Instead you start recoding a macro with `q<char>` with <char> being the register used. Then do your thing and stop recording with `q`.

Make a macro that writes your name and replay it.

Well this is quite the same than registers in general, but you can add jumps and what not to your macros.

Let's try easyish codemod macro.

1. Make a macro that adds ; to the end of line
2. Make a macro that adds ; to each line AND uppercases the parameter

HINT: `u` is undo so use that if you mess up. `gUw` for uppercasing a word `f<char>` to jump to next <char>.
HINT: The placement of cursor is essential. Start by placing the cursor to a known place.

```js
console.log("hello")
console.log("world")
console.log("wooo")
console.log("coo")
console.log("dadjac")
console.log("sajcjasc")
console.log("19403")
console.log("di2e2e")
console.log("hello")
console.log("hello")
console.log("hello")
```

Hot damn! That clojure jeebie forgot to add commas in the array. Fix it with macro or regex.

```js
const values = [1 2 3 4 5 6 7 8 9 10 12 13 14 15 16];
```

Bonus: increment all the values in the array above with one! (Or even five!)

Some Rust fun. In Rust you make a variable size string from literal string with `String::from("My value")`. And some Juho has made literal strings when we need String instead of &str. Do a codemod!

```rust
// This needs to be do_something(String::from("foo"));

do_something("foo");
do_something("bar");
do_something("juho");
do_something("hahah they can contain whitespaces");
do_something("ping");
do_something("pong pang");
do_something("foo foo foo");
do_something("foo");
```

Now let's try something harder. Following YAML is incorrect, as `harrastukset` needs to be an array!

Write a macro that changes each `harrastukset` into

```
harrastukset:
    - <harrastus>
```

```yaml
things:
    - name: Seppo
      harrastukset: kokkailu
    - name: Juho
      harrastukset: vimittely
    - name: Mirja
      harrastukset: marjastus
    - name: Liisa
      harrastukset: fysiikka
    - name: Kimmo
      harrastukset: pesäpallo
    - name: Jack
      harrastukset: liitohommat
    - name: Ville
      harrastukset: syöminen
    - name: Kerppa
      harrastukset: juominen
    - name: Tarmo
      harrastukset: räppääminen
```

You can edit all the lines separately, but try to record a macro that does it and apply it to each row. Cursor placement is essential!

- think that macro can be repeatable (start with search or cursor placement to known location)

This is not an easy task.



```ts
const things = [
    foo(13),
    foo(13),
    foo(52),
    foo(14),
    foo(1),
    foo(51),
    foo(51),
    foo(1),
    foo(1),
    foo(3),
    foo(1),
];

// Hot damn, all of these need foo(Some.Constant, 5, "abba") 
```

# Applying macro to ALL matching lines

`:g/SEARCH/norm! @a`

Uppercase all first letters in name but nothing else. `gUl` uppercases a single character, (why?).

Name: marko
Position: developer

Name: kalle 
Position: developer

Name: tilpertti
Position: developer

Name: lillukka
Position: developer

