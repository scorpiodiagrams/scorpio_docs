!!Polyglot
!+[[./images/UfoBlueprint.png]]
 #Caption Blueprint for a UFO.
# Plans and Blueprints 
```Key to Plans
🛸 - far future plans. 
🚀 - for future plans that will arrive sooner.
⛵️ - old code that needs to be made seaworthy again
```
## Scorpio Features Mind Map
This mind-map shows how closely the various features of Scorpio are *or will be* related to each other. My idea is to make things be of the same kind, so that they become more composable. I reduce the amount of code I write and diagrams become easier to make.

Hover over the items to find out more about each.
!!Scorpio
# ScorpioGuide
!!Raw
Graphs - are things connected to things
  General Graphs - there are no restrictions on what's connected
  Trees - there are no loops in the connections
  Lines - there is a sequence, maybe A to B to C.
Fields - have a value for every point on their image
Shape Modifiers - modify the outlines of shapes
!!Markdown

### Graphical Elements
I am writing code to unify different kinds of graphical element. For example chemical structures initially in SMILES format (a standard concise format for molecules used by chemists) become general graphs. Atoms connected by bonds *are* the same thing as labels connected by links. At least - as far as diagrams are concerned. Code to edit labels and links becomes able to edit molecules.

Menus, that is the commands found in the 'top bar' of a progam, are commands organised as a tree. If I have a display format for labels that makes them look like menu items, the software to edit trees can edit menus.

Shape modifiers are a particular kind of graphical element. If you can modify the shape of a label by adding a modifier, the same system ought to let you modify serifs on a font.

### Diagram Styling

At the moment the diagram style applies to the whole diagram, and you then override colours and shapes per item. A future plan is to allow mixing of styles on the same diagram.

### Label Styling

The label end-styles are accomplished using SVG snippets. I would like to expose this system to the end user, so that users can define new end shapes.

### Link Styling

Scorpio diagrams aims to work with large complex diagrams, not just the small hand crafted ones.  Currently the system for selecting and styling lines is too labour intensive for larger diagrams.

> #UFO(I plan that in a future Scorpio you will be able to style lines based on what they represent.  So for example you'll be able to dynamically highlight a particular path through a large network.  That's future work and needs more design.)
