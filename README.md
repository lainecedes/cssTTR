# Process Report - CSS to the Rescue
This is the repository for my individual assignment for the course CSS to the Rescue. In this assignment, I'm making a control panel in pure HTML/CSS (in my case, a dj controller) where the user can interact with the working panel itself. 
The rules are:
- No JavaScript, unless it's really needed (for range sliders)
- No classes and id's
- Experimenting with CSS techniques

I chose the 2 following subjects to focus on, that fits my case:
- CSS nesting
- Container queries

## General progress
- Presentations about chosen theme: team superheroes and layout
- Make sketches for my ideas
- Additional ideas

In the first week, we did some presentations about our chosen CSS theme (I got layout and did something with popovers and anchor positioning) and I made some idea's and sketches:

<img src="/readme-images/djcontroller.png" alt="DJ deck illustrator sketches" width="50%" height="auto">

I sketched the first concept: A dj controller with buttons, switches, wheels and sliders that does.. something with music or a live event

<img src="/readme-images/switch.png" alt="Switch illustrator sketches" width="50%" height="auto">

And the last concept: Building a Nintendo Switch where I make the controller and interface, and could scroll between my animated game covers with a hover event.

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

### Container query for the deck ✅
I made a container query for my dj controller to make it responsive. I used an inline size container type and gave it a simple name: deck. With this. I could style the container based on how big the container is, and not the viewport. So I made it so that if I resized it smaller, the grid columns would change.

I ran into some issues where my container query wasn't even triggering at all. Apparently, this is because I had to make an additional wrapper for my dj controller itself, so that that could be considered the parent query, and the items being my controller itself that I could style. It works now, by resizing the container horizontally!


### Restyling some parts
I've decided to restyle the cd wheel to make it more real. I've used the same conic gradient in the colors grey and white for a more lighter look, and added a label circle inside with a repeating linear gradient to make it look like it's a vinyl record being played.

<img src="/readme-images/updatedversion.png" alt="Label circle in jog wheel" width="80%" height="auto">

### Perfecting the stage light buttons ✅
I used the hsl example by Sanne to make the rainbow effect for my buttons, and I'm figuring out how to grey them in my off state. I added a white box shadow as :checked to simulate the midi buttons when pressed in real life to give it a glowy effect.

<img src="/readme-images/glowy.png" alt="Glowy midi button effect" width="50%" height="auto">

### Add mini equalizer animation on top of deck along with music playing ✅
I added a mini equalizer with animation in the top of the deck to make it seem like there's music playing, also while visualized! I got fed up with div's so I used unordered list items to make plain bars in a row:

<img src="/readme-images/list.png" alt="HTML view of a bunch of list items in an unordered list" width="50%" height="auto">

### On/off switch for deck + states
I've connected the rainbow lighting and the equalizer to the general off and on button. If the user selects the button in the middle, the deck "switches" on and a bunch of main features will start to work as an animation. I used the :has() selector in different ways to make this work, but had an issue with the equalizer color not turning on. I fixed this by rewriting the selector a bit more specific and now it triggers correctly.

### Light show background ✅
I changed the party blur background into a 3 color linear gradient show, and added flickering lights to it to make it less boring. For the gradient, I made a simple animation where it loops between the 3 gradients, and for the flickering lights I made 8 or 9 lights that I all positioned and delayed uniquely, and gave it an lower opacity between the loops.


## Extra's
Here are some extra's that I could do if I had enough time (and if I didn't get sick):

- Adding sound to the jog wheel player
- Make the slider work with maybe my flickering lights or background
- Overall tweaks and rewriting code.


### Friday progress - March 1st
This week, showed my sketches, and made a start in HTML and CSS. I went with the dj controller instead, because you could do more functionality with it in CSS than the Switch that's a bit static (and that's good because I didn't have a lot of inspiration and I experimented instead). I took concerts and stages as inspiration for the decoration of my background. I  got feedback from fellow students that I could add maybe music. One already made a jog wheel design that he showed, and that could be a nice inspiration for the design of the wheel itself.

### Friday progress - March 8
- Started with stage lights and got help from Sanne. I got an issue where the entire stage light was moving but I wanted it to move from one fixed point, and I could do that with transform-origin: top;
- Added more mini modules to the deck such as checkbox buttons, slider and on/off deck, and a equalizer at the top
- Early version
- Updated version:

<img src="/readme-images/updatedversion.png" alt="Updated version of my deck" width="50%" height="auto">


- First version of my grid: 
<img src="/readme-images/grid.png" alt="First version of grid" width="50%" height="auto">



### Friday progress - March 15
I was sick so I didn't attend class on that day.


### Friday progress - March 19 (extra)
I did a extra progress conversation to make up for week 3. I had some issues while using the container query and my centering using position absolute, such as the left value not working. Apparently CSS skipped that because my container query styling was above the normal styling, and I had to place it below. But it wasn't necessary anyways because I could center my grid items using justify and align-items/self or using just one rule: place-items/self.

+ What did I do next?
- Rewriting my code into nesting
- Finishing touches


## Sources
- [Responsive container query house to experiment as example and inspiration for background](https://codepen.io/gayane-gasparyan/pen/yLqjVWb)
- [Sanne's custom properties with hsl for rainbow inspiration](https://codepen.io/shooft/pen/OJoMVOK)
- [Sanne's stage lights help](https://codepen.io/shooft/pen/LYvNPoo?editors=1100)
- ChatGPT for minor issues and troubleshooting prompts
- [Container queries - MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_containment/Container_queries) 
- [Nesting css - MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/Nesting_selector)
- [CSS Tricks - How to create neon text with CSS](https://css-tricks.com/how-to-create-neon-text-with-css/)
- [Pure CSS DJ Controller as one of the design inspirations](https://codepen.io/Antzee/pen/jzrJvx)
- [Clippy - CSS clip path maker](https://bennettfeely.com/clippy/)
- [LogRocket - How to use container queries](https://blog.logrocket.com/css-container-queries-guide/)
- [web.dev - Container queries land in stable browsers](https://web.dev/blog/cq-stable)
- [@property CSS - MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/@property)