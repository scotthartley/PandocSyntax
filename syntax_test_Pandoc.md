<!-- SYNTAX TEST "Packages/PandocSyntax/PandocSyntax.sublime-syntax" -->

---
title: YAML Block
---

# Heading 1 {#header_id}

## Heading 2 {-}

Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

### Heading 3

This paragraph has text in **bold**, *italics*, a `code block`, and an
equation: $x = y$. It also has text with sub~script~ and super^script^.
Pandoc-figref {#f:figlabel} and pandoc-chem-struct s:{CH2Cl2} are also
supported. Asterisks can be escaped \* to not interfere with *italics*.

#### Heading 4 {-}

- This is a list
- Item **2** of list

-   Still a list, but with multiple paragraphs in an item.

    Second paragraph.

    Third paragraph.

1. *Numbered list*
2. Numbered list

<!-- This text is part of a comment. -->

This paragraph contains a [link](\url). This is a [reference link][ref]. This
is an <inline link.html>. This is a [shortcut reference link].

![Figure](/path)

This inline ![Figure 2] has the path specified separately. Lorem ipsum dolor
sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut
labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud
exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis
aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu
fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in
culpa qui officia deserunt mollit anim id est laborum.

[ref]: \url

[shortcut reference link]: \url

[Figure 2]: /path

> A quote.
    That continues on the next line.
> 
> Next part of quote.

\LaTeX_command_brackets{option}
Lorem ipsum dolor sit amet,[^noteref1] consectetur adipisicing[^noteref2]
elit, sed do eiusmod tempor incididunt ut labore et dolore magna
aliqua.^[Inline footnote] Ut enim ad minim veniam,[@citation] quis nostrud
exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis
aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu
fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in
culpa qui officia deserunt mollit anim id est laborum. \LaTeX_command 

[^noteref]: This is a footnote.

| A line block.
|   Which will preserve leading spaces.

~~~
A fenced code block.
~~~

Or just indent code:

    Like this.

\begin{something}
Raw LaTeX.
\begin{something_else}
    More raw LaTeX.
\end{something_else}
\end{something}