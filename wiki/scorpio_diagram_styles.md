## Diagram Styles
There are several predefined types / styles for diagrams.  The styles affect the colouring, shapes and sizing.

The diagram type is the first line of the #NUTC(spec) for the diagram and starts with #Code(##) followed by the name for the style.  
#[You can see the spec by clicking and dragging slightly one of the labels on the diagram to move the label.  That is, start to modify the diagram and the spec will appear.
#]

You can find additional examples on the [More Examples](more_examples) page.

#Example(
* #Code(##MindMap) - Colourful.  Connecting lines vary in width.
* #Code(##Molecule) - Atoms and bonds.
* #Code(##LineArt) - Black and white style for figures.
* #Code(##GenericDiagram) - A more colourful version of LineArt.
* #Code(##Standard) - Colourful and 3d. This is the default.
* #Code(##Geometry) - For 'Euclid's elements'
* #Code(##FlowChart) - Rounded boxes
* #Code(##Annotation) - With translucency for an image overlay.
* #Code(##Rainbow) - Like MindMap, but over the top colourful.
* #Code(##SceneGraph) - Sombre black and blue two-tone, for serious projects.
* #Code(##StarMap) - A style with white lines, useful for star maps.
)End#


###Main diagram types
> #Code(##Mindmap) - A style with curved, tapered, colourful connection lines, and colourful labels, with 3D-bevel border.
!!Scorpio
##MindMap
boxed: 100
caption: My grand plans
:A: (💡New Ideas!)
*:B: Holidays!
**:C: <=Adventure<
**:D: <=Recharging<
*:E: (Customers!)
**:F: >Profit!=>
**:G: >Onwards=>
:A: at: 296,55
:B: at: 208,82
:C: at: 120,27
:D: at: 88,75
:E: at: 386,27
:F: at: 500,20
:G: at: 502,70
link: * *
bend: 20
!!Markdown
> #Code(##Molecule) - For molecular structures.  Atoms are shown as circular labels, with the colouring being letter-dependent.  The connections between the labels are dark single or double links. 
!!Scorpio
##Molecule
caption: Fun with Furans
:A: C
:B: C
:C: O
:D: C
:E: C
:A: at: 190,80
:B: at: 180,45
:C: at: 210,20
:D: at: 240,45
:E: at: 230,80
boxed: 100
link: A B
multiplicity: 2
link: B C
multiplicity: 1
link: C D
multiplicity: 1
link: D E
multiplicity: 2
link: E A
multiplicity: 1
!!Markdown

###Other diagram types
These are some more diagram types:
> #Code(##LineArt) - A black-on-white style suited for electronics and category theory diagrams.
!!Scorpio
##LineArt
caption: A push-me-pull-back
:A: (A)
:B: [B]
:C: (C)
boxed: 100
:A: at: 100,20
:B: at: 300,80
:C: at: 400,30
link: A B
link: B C
!!Markdown
> #Code(##GenericDiagram) - An alternative less fancy style than #Code(##MindMap).
!!Scorpio
##GenericDiagram
caption: An orange push-me-pull-back
:A: (A)
:B: [B]
:C: (C)
boxed: 100
:A: at: 100,20
:B: at: 300,80
:C: at: 400,30
link: A B ~~some text~~
link: B C ==something else==
!!Markdown


 #Button(scorpio_label_styles, Labels) - How to make labels in Scorpio