# Scorpio Links
## Links and how to style them

You create a link between two named labels with the #Code(:link:) command. You can also create a link implicitly by placing the labels in a [hierarchy](scorpio_connections).  

### Wide and narrow lines

If you don't specify any style for a link, Scorpio will use a default style:
!!Raw
link: A B
!!Scorpio
##Geometry
:A: A
:B: B
link: A B
boxed: plain
:A: at: 100,27
:B: at: 300,27
!!Polyglot

Scorpio has #Code(:Wide:) lines and #Code(:Narrow:) lines. They behave very similarly#Footnote(1).

Click on any example to edit.  You can try out adding arrow heads and other effects.

### Links with default styling

When you create a link between two labels with the #Code(:link:) command, and no additional styling for that link, the result might look like this:

!!Raw
link: A B
!!Scorpio
##LineArt
:A: A
:B: B
link: A B
boxed: plain
:A: at: 100,27
:B: at: 300,27
!!Markdown

### Change the appearance
At the same time as adding the link, you can style it.  Here is how to style it as an arrow:
!!Raw
link: A B -->
!!Scorpio
##LineArt
caption: Example
boxed: plain
:A: A
:B: B
:A: at: 75,35
:B: at: 410,20
link: A B -->
!!Markdown
### Bending a line
Here's how to bend a line:
!!Raw
link: A B -->
bend: 15
!!Scorpio
##LineArt
caption: Example
boxed: plain
:A: A
:B: B
:A: at: 70,40
:B: at: 410,20
link: A B -->
bend: 15
!!Markdown
The bending also works for the more colourful wide lines:
!!Raw
link: A B --
bend: 15
!!Scorpio
##MindMap
caption: Example
boxed: plain
***:A: A
***:B: B
:A: at: 67,35
:B: at: 421,35
link: A B --
bend: 15
!!Markdown
Positive values bend in one direction, negative in the other.

### Styling the Line
When you make a link, you can choose what line style it should have.
#Example(
> &nbsp;&ndash;&ndash; &nbsp; An ordinary single link<br> ~~ &nbsp; A squiggly link<br> == &nbsp; A double link  
)End#

!!Raw
link: A B ==
!!Scorpio
##LineArt
caption: Example
boxed: plain
:A: A
:B: B
:A: at: 75,35
:B: at: 410,20
link: A B ==
!!Markdown
Here in the wide style. The #Code([]) are for square ends. Without them the ends would be round:
!!Raw
link: A B [==]
!!Scorpio
##MindMap
caption: Example
boxed: 80
:A: A
:B: B
:A: at: 75,35
:B: at: 410,20
link: A B [==]
!!Markdown

### End shapes and Text
As in the previous example, you can control the end shapes on a link much the same way you control the end shapes on a label. You can also place text on the link, and it becomes a label.

!!Raw
link: A B [~~Text on the arrow~~>
!!Scorpio
##LineArt
caption: Example
boxed: plain
:A: A
:B: B
:A: at: 75,35
:B: at: 410,20
link: A B [~~Text on the arrow~~>
!!Markdown

You can control the end shapes on the label.  End shapes placed around the label affect the label. The end shapes at the ends affect the link.

The labels on a link behave very similarly to labels that aren't. 

* The quoting of text and the use of #Code(\n) for a line break are the same.
* Styling for their end shapes - Many of the directives such as #Code(:Height:) work for both stand alone labels and labels on links.
* Styling for the diagram as a whole affects both stand alone labels and labels on links.

The main difference between a label that is positioned on a link and a label on its own is that the label on a link will change its slope to follow the line of the link.  Text on the other labels stays horizontal.  

The text on a link is usually a smaller font than the text on a label.

The next three examples demonstrate the single, squiggly and double line styles for links. They also have text labels on the line and they have various end shapes for the line and for the label.

!!Raw
 --single line-->
!!Scorpio
##LineArt
:A: A
:B: B
:A: at: 75,35
:B: at: 410,20
link: A B --single line-->
boxed: plain
!!Raw
 >>~~>squiggly line>~~=>
!!Scorpio
##LineArt
:A: A
:B: B
:A: at: 75,35
:B: at: 410,20
link: A B >>~~>squiggly line>~~=>
boxed: plain
!!Raw
/==[double line]==)+(
!!Scorpio
##LineArt
:A: A
:B: B
:A: at: 75,35
:B: at: 410,20
link: A B /==[double line]==)+(
boxed: plain
!!Markdown
In the simple case where you don't want text on the link nor an arrow, leave both out:

!!Raw
link: A B ~~
!!Scorpio
##LineArt
:A: A
:B: B
link: A B ~~
boxed: plain
:A: at: 75,35
:B: at: 410,20
!!Markdown

### Text Positioning

The examples with text so far have shown text placed directly on the line. If you have an even number of text lines, Scorpio will position half the lines above and half below:
!!Raw
 ~~Text above\nand below the line~~
!!Scorpio
##LineArt
:A: ~~Text above\nand below the line~~
boxed: plain
:A: at: 200,27
!!Markdown
You can use \n as a line break, and so get two lines, one of which is blank. As shown below you can position the text above or below the line by adding the blank line. Use #Code("") around your text, so that Scorpio knows that \n is part of the text.
!!Raw
 ~~"Text above the line\n"~~
!!Scorpio
##LineArt
:A: ~~"Text above the line\n"~~
boxed: plain
:A: at: 200,27
!!Raw
 ~~"\nText below the line"~~
!!Scorpio
##LineArt
:A: ~~"\nText below the line"~~
boxed: plain
:A: at: 200,27
!!Polyglot
----
### Footnotes

#FootnoteRef(1) Wide lines can have outlines and can vary in width. Narrow lines are a fixed width. When you use custom end shapes and have multiple lines, the narrow lines add one end shape in total, whereas the wide lines add one end shape for each line.

