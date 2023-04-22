!!Polyglot
##Connections
###Things Connected to Things
Scorpio is well suited for diagrams of 'things connected to things'. In these 'things connected to things' diagrams you can drag the things about and they stay connected.

A range of shapes for the things and for their connections gives a lot of flexibility in what Scorpio diagrams can show.  You can use the 'connections diagrams' for:

* Mind maps
* Flowcharts
* Annotations to diagrams
* Chemical structures

##Labels and Links
Scorpio has Labels and Links. 
* Labels are the things that you place and can move around.
* Links are the connections betwen them.

A text specification#Footnote(1) tells Scorpio what the labels are, how they are connected to each other, how to position things and how the diagram, labels and links are styled.

Scorpio will give letters A to Z#Footnote(2) to the labels. When you drag labels around on the diagram, Scorpio will update the text specification to match. If you delete or add labels, Scorpio will update the letters and numbers so that the right things stay linked.

## Mind Maps
Many layouts have a hierarchical tree like structure.  You can specify a tree structure by listing the items.  Here's an example of a list that has different foods grouped together to make a hierarchy.
!!Raw
* Foods
** High Fat
*** Pizza
*** Burger
** High Carb
*** Potatoes
*** Rice
*** Bread
** High Sugar
*** Toffee
*** Honey
*** Chocolate
!!Polyglot
Scorpio will add letters in for the labels when you drag one of them on the diagram.
!!Markdown
The diagram below is in the '#Code(##MindMap)' style#Footnote(3):

> #Code(##MindMap) - A colourful style for mind-map trees. 

Here's that list presented as a tree-like MindMap diagram.  This diagram is specified by the list above.  The list specifies the labels and their links. You then drag the labels into position.  
!!Scorpio
##MindMap
caption: Essential food groups 😄
*:A: Foods
**:B: High Fat
***:C: Pizza
***:D: Burger
**:E: High Carb
***:F: Potatoes
***:G: Rice
***:H: Bread
**:I: High Sugar
***:J: Toffee
***:K: Honey
***:L: Chocolate
:A: at: 342,72
:B: at: 240,164
:C: at: 176,108
:D: at: 218,257
:E: at: 436,251
:F: at: 470,333
:G: at: 542,310
:H: at: 404,312
:I: at: 478,140
:J: at: 530,201
:K: at: 602,129
:L: at: 498,64
link: * *
bend: 30
!!Polyglot

> [!info]- Try it Out
## Positioning the Items
Drag the labels into new positions.  

Notice that the text updates to show the new position information.  The positions are the lines with 'at' and then coordinates in them.  If you delete those 'at' lines from the text, Scorpio will make a guess as to where to place the items.
```Raw
**Link to previous diagram!**
*:A: Foods
**:B: High Fat
***:C: Pizza
***:D: Burger
**:E: High Carb
***:F: Potatoes
***:G: Rice
***:H: Bread
**:I: High Sugar
***:J: Toffee
***:K: Honey
***:L: Chocolate
:A: at: 342,72
:B: at: 240,164
:C: at: 176,108
:D: at: 218,257
:E: at: 436,251
:F: at: 470,333
:G: at: 542,310
:H: at: 404,312
:I: at: 478,140
:J: at: 530,201
:K: at: 602,129
:L: at: 498,64
```)
> [!info]- Adding a Link
You can add in additional links, using the #Code(link:) command.

###Add more links
Add a link between #Code(D) (burger#) and #Code(H) (bread#) like so:
```Raw
**Link to previous diagram!**
link: D H
```
You should place this at the end of the spec.  You can place it earlier, so long as the labels #Code(D) and #Code(H) have already been defined.  Scorpio though will rearrange the spec as soon as you move any of the labels. )

Other diagrams also use connections. With different styling for the diagram you get different results.

## Flow Charts
!!Markdown
> #Code(##Flowchart) - Has more pastel colours than #Code(##MindMap).  Label boxes are enlarged to 'standard sizes' (multiples of 50 pixels) so that more often boxes' dimensions will match nicely.  Rectangular boxes have their corners slightly chamfered.
!!Scorpio
##Flowchart
caption: Rossum's universal flow charts
:A: :Height3:(Start)
:B: [Do The Thing]
*:C: :Height3:(Finish)
boxed: 100
:A: at: 100,40
:B: at: 253,60
:C: at: 439,64
link: A B
!!Markdown


## Annotated Diagrams
!!Markdown
> #Code(##Annotated) - For marking up an existing image with labels. 
!!Scorpio
##Annotated
caption: Femur
:A: Head
*:B: ""
:C: Greater\nTrochanter
*:D: " "
:E: Lesser\nTrochanter
*:F: " "
:G: Condyles
*:H: " "
*:I: " "
boxed: 150
:A: at: 22,40
:B: at: 99,44
:C: at: 41,108
:D: at: 120,107
:E: at: 239,17
:F: at: 167,73
:G: at: 524,80
:H: at: 461,107
:I: at: 459,54
background: Gray252.png
:info:
card:
##Femur
The illustration of the femur is from the 1918 edition of Gray's anatomy, and is in the public domain.
!!Markdown

## Chemical Structures

> #Code(##Molecule) - For molecular structures.
!!Polyglot
> For chemistry, Scorpio also has the beginnings of support for SMILES#Footnote(4), a standard concise method for specifying chemical structure.  SMILES is a shorter way for specifying molecules.
!!Markdown
In the diagram below, each label and each link is specified in the Scorpio spec.  The colouring and styling is automatic, once '#Code(##Molecule)' has been specified.

The Scorpio spec is more longwinded than the SMILES spec would be, but can handle a wider range of 'things connected to things' diagrams.
!!Scorpio
##Molecule
compound: CC(=O)NCCC1=CNC2=C1C=C(OC)C=C2
caption: Melatonin
:A: at: 121,117
:B: at: 168,116
:C: at: 181,163
:D: at: 190,70
:E: at: 238,60
:F: at: 283,73
:G: at: 289,121
:H: at: 253,153
:I: at: 275,201
:J: at: 324,186
:K: at: 324,140
:L: at: 360,118
:M: at: 400,144
:N: at: 435,117
:O: at: 474,146
:P: at: 399,183
:Q: at: 365,209
boxed: 250
!!Polyglot
----

#FootnoteRef(1) You can see and then edit the text specification by draging on one of the labels to move the label. The spec will then appear.

#FootnoteRef(2) When Scorpio runs out of letters A to Z, it moves on to AA, BA, CA and so on.

#FootnoteRef(3) Other styles can be found [here](scorpio_diagram_styles).

#FootnoteRef(4) Proper support for SMILES is a feature under development. You can find out more about progress on it by following the link below to the development documentation.
#Right(\Rock [SMILES](scorpio_dev;dev_smiles))

#FootnoteEnd
&nbsp;