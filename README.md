# Process Report - CSS to the Rescue
This is the repository for my individual assignment for the course CSS to the Rescue. In this assignment, I'm making a control panel in pure HTML/CSS (in my case, a dj controller) where the user can interact with the working panel itself. 
The rules are:
- No JavaScript, unless it's really needed (for range sliders)
- No classes and id's
- Experimenting with CSS techniques

I chose the 2 following subjects to focus on, that fits my case:
- CSS nesting
- Container queries

## Week 1 - 26 feb - 1 mar
- Presentations about chosen theme: team superheroes and layout
- Make sketches for my dj controller
- Additional ideas

This week, I made some sketches to see how my deck would look like in css:
-Sketch from Illustrator-
- Nintendo Switch and Dj deck

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

<img src="/readme-images/has-selector.png" alt="Image of me using the :has() selector" height="auto">

### Progress week 2
- Started with stage lights,
- added more modules to the deck, 
- feedback: Go with the dj deck, you can add more functionality than the Nintendo Switch
- feedback: maybe add music, Ali had a jog wheel design that he made and showed

## Week 3 
### Issues with the checkboxes ✅

### Container query for the deck (in progress, issues)
I made a container query for my dj controller to make it responsive. I used an inline size container type and gave it a simple name: deck. With this. I could style the container based on how big the container is, and not the viewport. So I made it so that if I resized it smaller, the grid columns would change.

I ran into some issues where my container query wasn't even triggering at all. Apparently, this is because I had to make an additional wrapper for my dj controller itself, so that that could be considered the parent query, and the items being my controller itself that I could style. It works now, by resizing the container horizontally!

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

### Title neon light effect

### Party blur background (in progress)
I changed the party blur background into a 3 color linear gradient show

### Progress week 4
I did a extra progress conversation to make up for week 3. I had some issues while using the container query and my centering using position absolute, such as the left value not working. Apparently CSS skipped that because my container query styling was above the normal styling, and I had to place it below. But it wasn't necessary anyways because I could center my grid items using justify and align-items/self or using just one rule: place-items/self.


## Extra's
### Adding sound to the jog wheel player
Maybe another time?
### Make the slider design and let it work
Made the design but due to time and no inspiration,  I. didn't make it work



## Sources
- [Responsive container query house to experiment as example](https://codepen.io/gayane-gasparyan/pen/yLqjVWb)
- [Sanne's custom properties with hsl for rainbow inspiration](https://codepen.io/shooft/pen/OJoMVOK)
- [Sanne's stage lights help](https://codepen.io/shooft/pen/LYvNPoo?editors=1100)
- ChatGPT for minor issues and troubleshooting prompts
- [The Noun Project - Off/On icon](https://thenounproject.com/icon/power-3821211/)
- [Container queries - MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_containment/Container_queries) 
- [Nesting css - MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/Nesting_selector)