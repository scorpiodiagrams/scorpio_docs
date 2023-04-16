!!Polyglot
## Overview of Markdown

Scorpio diagrams are embedded in a fairly standard markdown processing system. 

The markdown used is broadly compatible with Obsidian. The diagrams are included into the markdown. The Markdown is also used within [info cards](scorpio_cards) to specify the text on the cards.

Many extension commands start with #Hash.

I'm using the #``` syntax for GeSHi islands. These islands do not give syntax colour highlighting. They just show raw monospaced text. However Scheme GeSHI islands have an auto-formatting feature. Click the scheme button to toggle auto formatting.
```Scheme
(down 
  ( ( (partial 0) H) 
    (up t (up x y) (down p_x p_y))) 
  (down 
    ( ( (partial 1 0) H) 
      (up t (up x y) (down p_x p_y))) 
    ( ( (partial 1 1) H) 
      (up t (up x y) (down p_x p_y)))) 
  (up 
    ( ( (partial 2 0) H) 
      (up t (up x y) (down p_x p_y))) 
    ( ( (partial 2 1) H) 
      (up t (up x y) (down p_x p_y))))) 
```

I'm using Obsidian's #Code(> [!info]) syntax for drop downs. Like this:

> [!info]- More info
I'm not yet supporting the full gamut of symbols and styles for these drop downs. For my needs, one version is enough.)

I can do 'quote boxes' both left using #Code(>) and right using #Code(<). The idea is to make showing conversations easier.

> This is a left quote box.
< And this is a right quote box.

## Sidebar
The sidebar is 'just' a specially named markdown file, #Code(sidebar.md).

A typical item in the sidebar looks like this:
```
#Jump( more_label_styles \Diamond  More Labels
# \Diamond More Labels
Additional label styles, beyond the basics.)
```
The above is providing a link to the file more_label_styles.md, with text with a blue diamond to the left. When you hover, the longer message appears.

## Book Features
To format mathematical textbooks I trap some headings and hyperlinks and treat them specially.
* #Hash#Hash#Hash Exercise gets an anchor as an exercise that can be linked to
* #Hash Footnote(number) will link to a later #Hash FootnoteRef(number)
* The \tag{number} within a KaTeX equation is used to detect numbered equations, which can be linked to using #Eqn

## Diagrams
Diagrams are included by first providing a line !!Scorpio. The next lines can be the full diagram spec, or a link to the diagram spec.
