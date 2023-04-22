## More Link Styles

The default #Code(##MindMap) [diagram style](scorpio_diagram_styles) has colourful lines that vary in width.  A link between labels A and B could look like this:
!!Scorpio
##MindMap
*:A: A
**:B: B
boxed: plain
:A: at: 100,27
:B: at: 300,27
!!Markdown


### Change the appearance
These links can be styled.  Here is how to style the link as a curved snake with text on it:
!!Raw
link: A B :snake_tail:-->"I am a snake!">--:snake_head:
bend: 15
!!Scorpio
##Sankey
boxed: 200
caption: Example
*:A: A
**:B: B
:A: at: 82,157
:B: at: 422,83
link: A B :snake_tail:-->"I am a snake!">--:snake_head:
bend: 15
!!Markdown
All the usual end shapes work for the ends of the link. 


One problem with #Code(##MindMap) is that the ends like #Code(:chevron:) and #Code(:straight:), or their short equivalents #Code(>) and #Code([), are mostly obscured by the label.

In the above example I'm using the #Code(##Sankey) style which has faint labels that almost vanish, so that you can see the end shapes.

### Hiding labels
An alternative to #Code(##Sankey)'s near invisible labels is to use the #Code(hide:) command to hide labels.  Here's an arrow, done with #Code(##MindMap) style and hiding both of the labels.

!!Raw
link: A B >=-->"An arrow">--=>
bend: 15
:A:B:
hide:
!!Scorpio
##MindMap
boxed: 200
caption: Example
**:A: A
***:B: B
:A: at: 82,157
:B: at: 422,83
link: A B >=-->"An arrow">--=>
bend: 15
:A:B:
hide:
!!Markdown
### More styling commands

Whilst #Code(~) and #Code(==) are convenient for wiggly and doubled links, they aren't very flexible. The texty versions give more control: 
#Example(
>  multiplicity: 3 - to set 3 (or some other number) of links<br> wiggle: 7 3     - to set amplitude 7 and wavelength 3
)End# 
Here's an example with #Code(bend), #Code(multiplicity) and #Code(wiggle)

!!Raw
link: A B --
bend: 15
multiplicity: 3
wiggle: 7 3
!!Scorpio
##MindMap
boxed: 100
caption: Example
**:A: A
***:B: B
:A: at: 80,80
:B: at: 413,17
link: A B ~~
bend: 15
multiplicity: 3
!!Markdown


### Size and Colour
Each diagram style has default size and colour for each level in the hirearchy. That is why the colourful lines in #Code(#MindMap) style vary in colour and width.

Size of a label can be changed using the #Code(size:) command and colour using the #Code(level:) command. These are applied to the labels.

!!Raw
:A: A
:B: B
:A: at: 82,157
size: 5
hide:
level: 5
:B: at: 422,83
size: 20
hide:
level: 3
link: A B >=-->"An arrow">--=>
bend: 15
!!Scorpio
##MindMap
boxed: 200
caption: Example
:A: A
:B: B
:A: at: 82,157
size: 5
hide:
level: 5
:B: at: 422,83
size: 20
hide:
level: 3
link: A B >=-->"An arrow">--=>
bend: 15
!!Markdown
