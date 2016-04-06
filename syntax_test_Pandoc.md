<!-- SYNTAX TEST "Packages/PandocSyntax/PandocSyntax.sublime-syntax" -->

---
title: YAML Block
---

# Heading 1

## Heading 2

Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

This paragraph has text in **bold**, *italics*, a `code block`, and $$math$$.

- This is a list
- Item **2** of list

-   Still a list, but with multiple paragraphs in an item.

    Second paragraph.

    Third paragraph.

1. *Numbered list*
2. Numbered list

<!-- This text is part of a comment. -->

This paragraph contains a [link](/url). This is a [reference link][ref]. This
is an <inline link.html>. This is a [shortcut reference link]. With a
![Figure](/path). Lorem ipsum dolor sit amet, consectetur adipisicing elit,
sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit
esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat
non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

[ref]: /url

> A quote.
> 
> Next part of quote.

Lorem ipsum dolor sit amet,[^note ref] consectetur adipisicing elit, sed do
eiusmod tempor incididunt ut labore et dolore magna aliqua.^[Inline footnote]
Ut enim ad minim veniam,[@citation] quis nostrud exercitation ullamco laboris
nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in
reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia
deserunt mollit anim id est laborum.

[^note ref]: This is a footnote.

| A line block.
|   Which will preserve leading spaces.

~~~
And fenced code block.
~~~

Or just indent code:

    Like this.

