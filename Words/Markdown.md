This is an H1
=============
This is an H2
-------------
### This is an H3 ###
#### This is an H4 ######
###### THis is h6

## Blockquotes

> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
> consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
> Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
>
> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
> id sem consectetuer libero luctus adipiscing

### Put the > before the first line of a hard-wrapped paragraph

> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.

> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
id sem consectetuer libero luctus adipiscing.

### Blockquotes can be nested

> This is the first level of quoting.
>
> > This is nested blockquote.
>
> Back to the first level.

### Blockquotes can contain other Markdown elements

> ## This is a header.
>
> 1.   This is the first list item.
> 2.   This is the second list item.
>
> Here's some example code:
>
>     return shell_exec("echo $input | $markdown_script");

## Lists

*   Red
*   Green
*   Blue

+   Red
+   Green
+   Blue

-   Red
-   Green
-   Blue

### Ordered lists

1.  Bird
2.  McHale
3.  Parish

### The actual numbers you use to mark the list have no effect on the HTML output Markdown produces

1.  Bird
1.  McHale
1.  Parish

3. Bird
1. McHale
8. Parish

### You not need wrap items with hanging indents

*   Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi,
viverra nec, fringilla in, laoreet vitae, risus.
*   Donec sit amet nisl. Aliquam semper ipsum sit amet velit.
Suspendisse id sem consectetuer libero luctus adipiscing.

### If list items are separated by blank lines, Markdown will wrap the items in `<p>` tags in the HTML output

*   Bird

*   Magic

### List items may consist of multiple paragraphs,indents not need.

*   This is a list item with two paragraphs.

    This is the second paragraph in the list item. You're
only required to indent the first line. Lorem ipsum dolor
sit amet, consectetuer adipiscing elit.

*   Another item in the same list.

### To put a blockquote within a list item, the blockquote’s > delimiters need to be indented

*   A list item with a blockquote:

    > This is a blockquote
    > inside a list item.

### To put a code block within a list item, the code block needs to be indented twice — 8 spaces

*   A list item with a code block:

        <code goes here>

### You need backslash-escape the period

1986\. What a great season.

## Code Blocks

This is a normal paragraph:

    This is a code block.

### One level of indentation — 4 spaces or 1 tab — is removed from each line of the code block

Here is an example of AppleScript:

    tell application "Foo"
        beep
    end tell

### Within a code block, ampersands (&) and angle brackets (< and >) are automatically converted into HTML entities

    <div class="footer">
        &copy; 2004 Foo Corporation
    </div>

## Horizontal Rules

* * *

***

*****

- - -

---------------------------------------

## Span Elements

### Links

This is [an example](http://dvpr.xyz/ "Title") inline link.

[This link](http://example.me/) has no title attribute.

See my [About](/about/) page for details.

### Reference-style links use a second set of square brackets, inside which you place a label of your choosing to identify the link

This is [an example][id] reference-style link.

This is [an example] [id] reference-style link.

[id]: http://example.com/  "Optional Title Here"

That is:

- Square brackets containing the link identifier (optionally indented from the left margin using up to three spaces);
- followed by a colon;
- followed by one or more spaces (or tabs);
- followed by the URL for the link;
- optionally followed by a title attribute for the link, enclosed in double or single quotes, or enclosed in parentheses.

The following three link definitions are equivalent:

    [foo1]: http://example.com/  "Optional Title Here"
    [foo2]: http://example.com/  'Optional Title Here'
    [foo3]: http://example.com/  (Optional Title Here)

This is [an example foo1] [foo1] reference-style link.

This is [an example foo2] [foo2] reference-style link.

This is [an example foo3] [foo3] reference-style link.

[foo1]: http://example.com/  "Optional Title Here"
[foo2]: http://example.com/  'Optional Title Here'
[foo3]: http://example.com/  (Optional Title Here)

### Note: There is a known bug in Markdown.pl 1.0.1 which prevents single quotes from being used to delimit link titles.

###The link URL may, optionally, be surrounded by angle brackets:

```
[id]: <http://example.com/>  "Optional Title Here"
```

[id]: <http://example.com/>  "Optional Title Here"

### You can put the title attribute on the next line and use extra spaces or tabs for padding, which tends to look better with longer URLs

```
[id]: http://example.com/longish/path/to/resource/here
    "Optional Title Here"
```

[id]: http://example.com/longish/path/to/resource/here
    "Optional Title Here"

Link definitions are only used for creating links during Markdown processing, and are stripped from your document in the HTML output.

Link definition names may consist of letters, numbers, spaces, and punctuation — but they are not case sensitive. E.g. these two links:

```
[link text][a]
[link text][A]
```

[link text][a]
[link text][A]

[a]: http://dvpr.me "dvpr.me"

are equivalent.

### The implicit link name shortcut allows you to omit the name of the link

```
[dvpr][]
[dvpr]: http://dvpr.me "dvpr.me"
```

[dvpr][]
[dvpr]: http://dvpr.me "dvpr.me"

### Because link names may contain spaces, this shortcut even works for multiple words in the link text

```
[AppleStar dvpr][]
[AppleStar dvpr]: http://dvpr.me "dvpr.me"
```

[AppleStar dvpr][]
[AppleStar dvpr]: http://dvpr.me "dvpr.me"

## Emphasis

### Markdown treats asterisks (*) and underscores (_) as indicators of emphasis

*single asterisks*

_single underscores_

**double asterisks**

__double underscores__

## Code

Use the `printf()` function.

### To include a literal backtick character within a code span, you can use multiple backticks as the opening and closing delimiters

``There is a literal backtick (`) here.``

### The backtick delimiters surrounding a code span may include spaces — one after the opening, one before the closing

A single backtick in a code span: `` ` ``

A backtick-delimited string in a code span: `` `foo` ``

### With a code span, ampersands and angle brackets are encoded as HTML entities automatically

Please don't use any `<blink>` tags.

`&#8212;` is the decimal-encoded equivalent of `&mdash;`.

## Images

### Markdown uses an image syntax that is intended to resemble the syntax for links, allowing for two styles: inline and reference.

```
![Alt text](/path/to/img.jpg)

![Alt text](/path/to/img.jpg "Optional title")
```

That is:


- An exclamation mark: !;
- followed by a set of square brackets, containing the alt attribute text for the image;
- followed by a set of parentheses, containing the URL or path to the image, and an optional title attribute enclosed in double or single quotes.

### Reference-style image syntax looks like this

```
![Alt text][id]

[id]: url/to/image  "Optional title attribute"
```

As of this writing, Markdown has no syntax for specifying the dimensions of an image; if this is important to you, you can simply use regular HTML <img> tags.

## Miscellaneous

### Automatic Links

<http://dvpr.me/>

Automatic links for email addresses work similarly, except that Markdown will also perform a bit of randomized decimal and hex entity-encoding to help obscure your address from address-harvesting spambots

<x@dvpr.me>

## Backslash Escapes

### Markdown provides backslash escapes for the following characters:

\\literal backslash\\

\`literal backtick\`

\*literal asterisks\*

\_literal underscore\_

\{literal curly braces\}

\[literal square brackets\]

\(literal parentheses\)

\#literal hash mark\#

\+literal plus sign\+

\-literal minus sign (hyphen)\-

\.literal dot\.

\!literal exclamation mark\!