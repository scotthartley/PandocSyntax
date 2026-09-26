<!-- SYNTAX TEST "Packages/PandocSyntax/PandocSyntax.sublime-syntax" -->

---
title: YAML Block
<!-- <- markup.raw.block.markdown source.yaml -->
---
<!-- <- comment -->

# Heading 1 {#header_id}
<!-- <- comment - markup.heading -->
<!-- ^^^^^^ markup.heading.1.markdown - comment -->
<!--        ^^^^^^^^^^^^ comment -->

## Heading 2 {-}
<!-- ^^^^^^^ markup.heading.2.markdown -->
<!--         ^^^ comment - markup.bold -->

###### Heading 6 with *emphasis* and closing hashes ######
<!--   ^^^^^^^^^ markup.heading.6.markdown -->
<!--                   ^^^^^^^^ markup.heading.6.markdown markup.italic.markdown -->
<!--                                                ^^^^^^ comment -->

####### Seven hashes is not a heading
<!--    ^^^^^ - markup.heading -->

Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
<!-- ^^^ - markup -->

### Heading 3
<!-- ^^^^^^^^ markup.heading.3.markdown -->

This paragraph has text in **bold**, *italics*, a `code block`, and an
<!--                       ^^ comment -->
<!--                         ^^^^ markup.bold.markdown - comment -->
<!--                                  ^^^^^^^ markup.italic.markdown - comment -->
<!--                                               ^^^^^^^^^^ markup.raw.inline.markdown - comment -->
<!--                                                          ^^^^^^^^ - markup -->
equation: $x = y$. It also has text with sub~script~ and super^script^.
<!--      ^ comment -->
<!--       ^^^^^ markup.raw.block.markdown -->
<!--                                        ^ comment -->
<!--                                         ^^^^^^ - comment -->
<!--                                                          ^ comment -->
<!--                                                           ^^^^^^ - comment -->
Pandoc-figref {#f:figlabel} and pandoc-chem-struct s:{CH2Cl2} are also
<!--          ^^^^ comment -->
<!--              ^^^^^^^^ constant.other.reference.link.markdown -->
<!--                                               ^^^ comment -->
<!--                                                  ^^^^^^ - comment - markup.bold -->
supported. Asterisks can be escaped \* to not interfere with *italics*.
<!--                                ^^ - comment -->
<!--                                   ^^^^^^ - markup.italic -->
<!--                                                          ^^^^^^^ markup.italic.markdown -->

#### Heading 4 {-}
<!-- ^^^^^^^^^ markup.heading.4.markdown -->

- This is a list
<!-- <- markup.list.unnumbered.markdown -->
<!-- ^^^^ markup.list.unnumbered.markdown -->
- Item **2** of list
<!--     ^ markup.list.unnumbered.markdown markup.bold.markdown -->

-   Still a list, but with multiple paragraphs in an item.
<!-- ^^^^ markup.list.unnumbered.markdown -->

    Second paragraph with *italics*.
    <!-- ^^^^^^^^^^^ markup.list.unnumbered.markdown - markup.raw -->
    <!--                   ^^^^^^^ markup.list.unnumbered.markdown markup.italic.markdown -->

    Third paragraph.
    <!--  ^^^^^^^^^ markup.list.unnumbered.markdown - markup.raw -->

1. *Numbered list*
<!-- <- markup.list.numbered.markdown -->
<!-- ^^^^^^^^^^^^ markup.list.numbered.markdown markup.italic.markdown -->
2. Numbered list
    - Nested item
<!--  ^^^^^^ markup.list -->

<!-- This text is part of a comment. -->
<!-- ^^^^^^^^^ comment - markup.list -->

This paragraph contains a [link](\url). This is a [reference link][ref]. This
<!--                       ^^^^ string.other.link.title.markdown -->
<!--                           ^^ comment -->
<!--                             ^^^^ markup.underline.link.markdown -->
<!--                                               ^^^^^^^^^^^^^^ string.other.link.title.markdown -->
<!--                                                             ^^ comment -->
<!--                                                               ^^^ constant.other.reference.link.markdown -->
is an <inline link.html>. This is a [shortcut reference link].
<!--  ^ comment -->
<!--   ^^^^^^^^^^^^^^^^ string.other.link.title.markdown -->
<!--                                 ^^^^^^^^^^^^^^^^^^^^^^^ string.other.link.title.markdown -->

![Figure](/path)
<!-- <- comment -->
<!-- ^^^ string.other.link.description.markdown -->
<!--      ^^^^^ markup.underline.link.markdown -->

![A *caption* with [@cite] and a [link](url)](img.png){#fig:x width=50%}
<!-- ^^^^^^^ string.other.link.description.markdown markup.italic.markdown -->
<!--                ^^^^^ string.other.link.description.markdown constant.other.reference.link.markdown -->
<!--                              ^^^^ string.other.link.description.markdown string.other.link.title.markdown -->
<!--                                          ^^^^^^^ markup.underline.link.markdown -->
<!--                                                  ^^^^^^^^^^^^^^^^^^ comment - constant - string -->

This inline ![Figure 2] has the path specified separately. Lorem ipsum dolor
<!--          ^^^^^^^^ string.other.link.description.markdown -->
<!--                    ^^^^^^^ - string -->
sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut
labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud
exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis
aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu
fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in
culpa qui officia deserunt mollit anim id est laborum.

[ref]: \url
<!--   ^^^^ markup.underline.link.markdown -->

[shortcut reference link]: \url
<!-- ^^^^^^^^^^^^^^^^^^^ constant.other.reference.link.markdown -->
<!--                    ^^ comment -->

[Figure 2]: /path {width=50%}
<!--        ^^^^^ markup.underline.link.markdown -->
<!--              ^^^^^^^^^^^ comment -->
[another]: http://example.com
<!-- ^^^ constant.other.reference.link.markdown -->
<!--       ^^^^^^^^^^^^^^^^^^ markup.underline.link.markdown -->

> A quote.
<!-- <- markup.quote.markdown comment -->
    That continues on the next line.
<!--     ^^^^^^^^^ markup.quote.markdown - markup.raw -->
>
> Next part of quote with a [@citation].
<!--                         ^^^^^^^^^ markup.quote.markdown constant.other.reference.link.markdown -->

Not a quote.
<!-- ^^^^^^ - markup.quote -->

\LaTeX_command_brackets{option} Lorem ipsum dolor sit amet,[^noteref1]
<!-- <- comment -->
<!--                   ^^^^^^^^ comment -->
<!--                                                         ^^^^^^^^ constant.other.reference.link.markdown -->
<!--                                                       ^^ comment -->
consectetur adipisicing[^noteref2] elit, sed do eiusmod tempor incididunt ut
labore et dolore magna aliqua.^[Inline footnote] Ut enim ad minim
<!--                          ^^ comment -->
<!--                            ^^^^^^^^^^^^^^^ string.other.link.description.markdown -->
<!--                                             ^^^^^^^ - string -->
veniam,[@citation; @citation] quis nostrud exercitation ullamco [@more_complex
<!--    ^^^^^^^^^^^^^^^^^^^^ constant.other.reference.link.markdown -->
<!--                          ^^^^ - constant -->
<!--                                                              ^^^^^^^^^^^^ constant.other.reference.link.markdown -->
[p. 30]; @citation [p. 20]] laboris nisi ut aliquip ex ea commodo consequat.
<!--     ^^^^^^^^^^^^^^^^^^ constant.other.reference.link.markdown -->
<!--                        ^^^^^^^ - constant -->
Duis aute irure dolor in @inline_citation [p. 55--60] reprehenderit in
<!--                     ^^^^^^^^^^^^^^^^ constant.other.reference.link.markdown -->
<!--                                      ^ comment -->
<!--                                       ^^^^^^^^^ constant.other.reference.link.markdown -->
<!--                                                  ^^^^^^^^^^^^^ - constant -->
voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint
occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit
anim id est laborum. \LaTeX_command
<!--                 ^^^^^^^^^^^^^^ comment -->

[^noteref]: This is a footnote with *emphasis*.
<!-- ^^^^ constant.other.reference.link.markdown -->
<!--     ^^ string.other.link.description.markdown comment -->
<!--        ^^^^^^^ string.other.link.description.markdown -->
<!--                                 ^^^^^^^^ string.other.link.description.markdown markup.italic.markdown -->

    A second paragraph of the footnote with a [link](url).
    <!-- ^^^ string.other.link.description.markdown - markup.raw -->
    <!--                                       ^^^^ string.other.link.description.markdown string.other.link.title.markdown -->

Not part of the footnote.
<!-- ^^^ - string -->

Spans can contain [1 submitted [@Raji:2025ab] and 1 more in preparation]{.mark}
<!--              ^ comment -->
<!--                            ^^^^^^^^^^^^ constant.other.reference.link.markdown -->
<!--                                                                   ^^^^^^^^ comment - markup.bold -->
and [nested [links](\url) too]{.underline}.
<!--         ^^^^^ string.other.link.title.markdown -->
<!--                ^^^^ markup.underline.link.markdown -->
<!--                      ^^^ - string - markup.underline -->
<!--                         ^^^^^^^^^^^^^ comment - markup.bold -->

| A line block.
<!-- <- markup.quote.markdown comment -->
|   Which will preserve leading spaces.
<!-- ^^^^ markup.quote.markdown -->

~~~
A fenced code block with **no** markup.
<!--                       ^^ markup.raw.block.markdown - markup.bold -->
```python
<!-- <- markup.raw.block.markdown - source.python -->
~~~
<!-- <- comment -->

```python
def f(x):
    return x ** 2
<!-- <- markup.raw.block.markdown source.python -->
```
<!-- <- comment - source.python -->

~~~~ {.r .numberLines}
x <- c(1, 2)
<!-- <- markup.raw.block.markdown source.r -->
~~~
<!-- <- markup.raw.block.markdown source.r -->
~~~~
<!-- <- comment - source.r -->

```
Unknown or missing language is raw: **not bold**
<!--                                  ^^^^^^^^ markup.raw.block.markdown - markup.bold -->
```

Or just indent code:

    Like this.
    And a *second* line.
<!--       ^^^^^^ markup.raw.block.markdown - markup.italic -->

\begin{something}
<!-- <- comment -->
Raw LaTeX with **no markdown**.
<!--             ^^^^^^^^^^^ markup.raw.block.markdown text.tex.latex - markup.bold -->
\begin{something_else}
    More raw LaTeX.
\end{something_else}
<!-- <- markup.raw.block.markdown -->
\end{something}
<!-- <- comment - markup.raw -->
Text after the environment.
<!-- ^^^^^ - markup.raw -->

{{< shortcode param="value" >}}
<!-- <- constant.other.reference.link.markdown comment -->
<!-- ^^^^^^^^ constant.other.reference.link.markdown -->

{{< figure src="/img/photo.jpg"
    alt="A photo"
<!-- ^^^^^^^^^^^^ constant.other.reference.link.markdown -->
    caption="My caption" >}}
<!--                     ^^^ comment -->

{{< figure >}}
Some content inside a paired shortcode.
<!-- ^^^^^^^ - constant -->
{{< /figure >}}

{{% notice %}}
<!-- ^^^^^ constant.other.reference.link.markdown -->

[hugo-ref]: {{< ref "docs/page" >}}
<!--        ^^^ comment -->
<!--            ^^^^^^^^^^^^^^^ constant.other.reference.link.markdown -->
<!--                            ^^^ comment -->

<!-- ===== Regression tests for the audit findings ===== -->

An unmatched a*b and **kwargs stay inside this paragraph.

This paragraph is not italic or bold.
<!-- ^^^^^^^^^ - markup.italic - markup.bold -->

Some ***bold italic*** text, then **bold *nested italic*** and *ital **nested bold***.
<!--    ^^^^^^^^^^^ markup.bold.markdown markup.italic.markdown -->
<!--                   ^^^^^^^^^^ - markup.bold - markup.italic -->
<!--                                      ^^^^^^^^^^^^^ markup.bold.markdown markup.italic.markdown -->
<!--                                                   ^^^ comment -->
<!--                                                       ^^^ - markup.bold - markup.italic -->
<!--                                                            ^^^^ markup.italic.markdown - markup.bold -->
<!--                                                                   ^^^^^^^^^^^ markup.italic.markdown markup.bold.markdown -->
<!--                                                                                 ^ - markup.bold - markup.italic -->

[Ac + F -> Ac^*]{.chem} and then [a *b]{.c} end.
<!--          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ - markup.italic -->
<!--           ^^^^^^^^ comment -->
<!--                                  ^^^^^ comment -->

Some ___both___, __bold _ital___, (__paren__), snake_case_name, _word_? ok.
<!--    ^^^^ markup.bold.markdown markup.italic.markdown -->
<!--                     ^^^^ markup.bold.markdown markup.italic.markdown -->
<!--                                 ^^^^^ markup.bold.markdown -->
<!--                                           ^^^^^^^^^^^^^^^ - markup.italic -->
<!--                                                             ^^^^ markup.italic.markdown -->
<!--                                                                  ^^^^ - markup.italic -->

Code ``with `backticks` inside`` and `**not bold** $x$ [no]` ok.
<!--   ^^^^^^^^^^^^^^^^^^^^^^^ markup.raw.inline.markdown -->
<!--                          ^^ comment -->
<!--                                  ^^^^^^^^^^^^^^^^^^^^^ markup.raw.inline.markdown - markup.bold - comment -->
<!--                                                         ^^ - markup.raw -->
Code with attributes `print(1)`{.python} and a span [x]{.class}.
<!--                           ^^^^^^^^^ comment - markup.bold -->
<!--                                                   ^^^^^^^^ comment - markup.bold -->

Compounds {1a} and {2,3-dimethyl} are bold; {=latex} and {-} are not.
<!--       ^^ markup.bold.markdown -->
<!--                ^^^^^^^^^^^^ markup.bold.markdown -->
<!--                                        ^^^^^^^^ - markup.bold -->
<!--                                                     ^^^ - markup.bold -->

Fig. 3 shows that lettered lists need a single letter.
<!-- <- - markup.list -->

Dr. Smith is not a list.
<!-- <- - markup.list -->

1.5 million is not a list.
<!-- <- - markup.list -->

A. Smith is not a list either.
<!-- <- - markup.list -->

a. Lettered item
<!-- <- markup.list.numbered.markdown -->

iv. Roman item
<!-- <- markup.list.numbered.markdown -->

(b) Parenthesized item
<!-- <- markup.list.numbered.markdown -->

#. Auto-numbered item
<!-- <- markup.list.numbered.markdown - markup.heading -->

   - [x] Done task
<!-- ^ markup.list.unnumbered.markdown comment -->
<!--  ^ markup.list.unnumbered.markdown markup.bold.markdown -->
<!--   ^ markup.list.unnumbered.markdown comment -->
   - [ ] Open task
<!--   ^ comment -->

- item

Paragraph after a list.
<!-- <- - markup.list -->

* * *
<!-- <- comment - markup.list -->

***
<!-- <- comment - markup.bold - markup.italic -->

Links: (<http://example.com>) and <user@example.com>.
<!--   ^ - comment -->
<!--    ^ comment -->
<!--     ^^^^^^^^^^^^^^^^^^ string.other.link.title.markdown -->
<!--                               ^^^^^^^^^^^^^^^^ string.other.link.title.markdown -->

Paths like ~/a and ~/b are not subscripts; H~2~O and 2^10^ are.
<!--       ^^^^^^^^^^^ - comment -->
<!--                                        ^ comment -->
<!--                                         ^ - comment -->
<!--                                                  ^ comment -->
<!--                                                   ^^ - comment -->
Strike ~~this out~~ now.
<!--     ^^^^^^^^ invalid -->
<!--   ^^ comment -->

Escaped \$5 and $6 are not math, nor is $20,000 and $30,000.
<!--      ^^^^^^^^ - markup.raw - comment -->
<!--                                     ^^^^^^^^^^^^^^^^^^ - markup.raw - comment -->
Inline display $$x^2$$ {#eq:sq} too.
<!--             ^^^ markup.raw.block.markdown -->
<!--                   ^^^^^^^^ comment -->

$$
<!-- <- comment -->
E = mc^2
<!-- <- markup.raw.block.markdown -->
$$ {#eq:energy}
<!-- <- comment -->
<!-- ^^^^^^^^^^ comment -->

Email me [mail a@b.com] or see [-@doe, p. 3] and @roe.
<!--      ^^^^^^^^^^^^ - constant.other.reference -->
<!--                            ^^^^^^^^^^^ constant.other.reference.link.markdown -->
<!--                                             ^^^^ constant.other.reference.link.markdown -->

See {#fig:results} and {#tbl:data} and {#eq:1}.
<!-- ^^^^^ comment -->
<!--      ^^^^^^^ constant.other.reference.link.markdown -->
<!--                         ^^^^ constant.other.reference.link.markdown -->
<!--                                   ^^^^^ comment -->

!(chapters/intro.md)
<!-- ^^^^^^^^^^^^^^ markup.underline.link.markdown -->

| A | B       |
|---|:-------:|
| 1 | **2** $x$ |
<!-- <- comment -->
<!--    ^ markup.bold.markdown -->
<!--         ^ markup.raw.block.markdown -->

: Results table {#tbl:results}
<!-- <- comment -->
<!-- ^^^^^^^^^^ string.other.link.description.markdown -->
<!--            ^^^^^^^^^^^^^^ comment -->

Table: Another caption.
<!-- <- comment -->
<!--   ^^^^^^^^^^^^^^^ string.other.link.description.markdown -->

::: {.note}
<!-- <- comment -->
Div content with *italic*.
<!--              ^^^^^^ markup.italic.markdown -->
:::
<!-- <- comment -->

Text [[Wiki Link]] here.
<!--   ^^^^^^^^^ constant.other.reference.link.markdown -->
<!-- ^^ comment -->
