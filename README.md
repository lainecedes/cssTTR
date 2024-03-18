# Process Report - CSS to the Rescue
This is the repository for my individual assignment for the course CSS to the Rescue. In this assignment, I'm making a control panel in pure HTML/CSS (in my case, a dj controller) where the user can interact with the working panel itself. 
The rules are:
- No JavaScript, unless it's really needed (for range sliders)
- No classes and id's
- Experimenting with CSS techniques

Choose out the following 2 subjects:
- CSS nesting
- @layer
- Container queries
- Style queries

## Week 1 - 26 feb - 1 mar
- Presentations about chosen theme: team superheroes and layout
- Make sketches for my dj controller
- Additional ideas

This week, I made some sketches to see how my deck would look like in css:
-Sketch from Illustrator-

### Progress week 1
- showed my sketches, and made a start in html and css
I took concerts and stages as inspiration for the decoration of my background

## Week 2
I've made a to do list that I can check off: 
### Making the layout (with grid) ✅
I started with making the grid layout for the design that I made in Illustrator.
### Working on the jog wheel player ✅
I found out about different gradients such as the conic wheel gradient, and thought it was a fun look to style my jog wheels with. I played with monotone colors first but wasn't happy with it so I set crimson red and blue as default color:

<img src="/readme-images/jog-wheel.png" alt="Conic wheel gradient example" width="50%" height="auto">

### Add stage lights function for the checkboxes ✅
I've added stage light function for the first 4 checkboxes on the first half of the deck. I've also added stage lights outside of the deck, and their visibility is set to none. This means that if you select one or more checkboxes, the visibility for the selected stage light will change to visible. 

I've tried to do this as a simple thing with :checked pseudoclass, but it didn't work, and a lot of people advised me to use the :has() selector instead, and it worked:

<img src="/readme-images/has-selector.png" alt="Image of me using the :has() selector" width="50%" height="auto">

### Progress week 2
- Started with stage lights, added more modules to the deck, feedback from Sanne and others

## Week 3 
### Issues with the checkboxes ✅

### Container query for the deck (in progress, issues)

### Progress week 3
- Was sick so didn't attend class

## Week 4

### Restyling some parts
I've decided to restyle the cd wheel to make it more real. I've used the same conic gradient in the colors grey and white for a more lighter look, and added a label circle inside with a repeating linear gradient to make it look like it's a vinyl record being played

### Perfecting the stage light buttons ✅
I used the hsl example by Sanne to make the rainbow effect for my buttons, and I'm figuring out how to grey them in my off state. I added a white box shadow as :checked to simulate the midi buttons when pressed in real life to give it a glowy effect.
<img src="/readme-images/glowy.png" alt="Glowy midi button effect" width="50%" height="auto">

### Add mini equalizer animation on top of deck along with music playing ✅
I added a mini equalizer with animation in the top of the deck to make it seem like there's music playing, also while visualized! I got fed up with div's so I used unordered list items to make plain bars in a row:
<img src="/readme-images/list.png" alt="HTML view of a bunch of list items in an unordered list" width="50%" height="auto">

### On/off switch for deck + states
I've connected the rainbow lighting and the equalizer to the general off and on button. If the user selects the button in the middle, the deck "switches" on and a bunch of main features will start to work as an animation. I used the :has() selector in different ways to make this work, but have an issue with the equalizer color not turning on.


## Extra's
### Adding sound to the jog wheel player (in progress)
### Party blur background (in progress)



## Sources
[Responsive container query house to experiment as example](https://codepen.io/gayane-gasparyan/pen/yLqjVWb)
[Sanne's custom properties with hsl for rainbow inspiration](https://codepen.io/shooft/pen/OJoMVOK)
[Sanne's stage lights help](https://codepen.io/shooft/pen/LYvNPoo?editors=1100)
[Sanne's stage lights help](https://codepen.io/shooft/pen/LYvNPoo?editors=1100)
