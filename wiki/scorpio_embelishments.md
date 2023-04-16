## Embelishments
LaTeX is a well known system for typesetting mathematics. LaTeX uses commands that begin with '#Code(\)' to distinguish them from the text. I've added JaTeX which uses some of the same ideas. It can make complex 'text' on the labels. That text can become very like a diagram.

## Circuits
Here a JaTeX label with #Code(\transistor) in it is used for components of a circuit.

!!Scorpio
##TheStandardStyle
$$\resistor + \capacitor + \transistor
boxed: 65
:A: at: 60,15
!!Markdown
## Permutations
The #Code(\twisty) notation can be used to show permutations graphically.
!!Scorpio
##TheStandardStyle
boxed: 50
$$\twisty ijk \twisty jki \twisty kij \twisty kji \twisty jik \twisty ikj
:A: at: 60,15
!!Markdown
## DataScience
Here #Code(\tensor-sensor) is being used for a data science diagram. Drag the items to adjust the diagram.
!!Scorpio
##Annotated
boxed: 250
caption: Alex Net - First four layers
bounding_boxes: 
:A: $$ \mathitalsmall\straight #fdb { \tensor-sensor3 #ccb - - . \ \mbox{ Initial \ Image \paper-stack {\box #bbf \box #bfb \box #faa} \surround {224 \ px} \rot90 { } \rot90 {224 \ px} {} {RGB }} } \straight
:B: $$ \mathitalsmall\straight #fdb { \tensor-sensor3 #ccb 11 11 96 \  \stack{  \mbox{ Conv \ 11x11 }{ stride \ 4 }} \ \tensor-sensor3 54 54 96 \ + \ReLU} \straight
:C: $$ \mathitalsmall\straight #ccd { \tensor-sensor3 #ccb - - . \  \stack{ \mbox{ Pool \ 3x3 }{ stride \ 2 }} \ \ \ \ \ \tensor-sensor3 26 26 96 } \straight
:D: $$ \mathitalsmall\straight #fdb { \tensor-sensor3 #ccb 5 5 256 \  \stack{  \mbox{ Conv \ 5x5 }{ pad \ 2 }} \\\\ \tensor-sensor3 26 26 256 \ + \ReLU} \straight
:A: at: 85,5
:B: at: 85,63
:C: at: 85,121
:D: at: 85,179
!!Polyglot
## Angles
For geometry diagrams, Scorpio can draw a marker for an angle, if given three labels. 

Drag A, B and C and the angle marker will adjust to follow.
```
angle: A B C
```
!!Scorpio
##Geometry
boxed: 150
caption: A cute illustration of obtuseness
*:A: (A)
*:B: (B)
*:C: (C)
:A: at: 100,20
:B: at: 300,60
:C: at: 400,30
link: A B
link: B C
angle: C B A
!!Markdown