# Workshop 1: Introducing JavaScript with P5.js

Collaborators: [your github username] & [your partners github username]

Make sure you’re working in pairs - on a single laptop. You’ll be **pair
programming**. In pair programming, there are two roles - **driver** and
**navigator**.

The **driver** is at the keyboard. They’re responsible for typing and figuring
out syntax. They shouldn’t make decisions though! That’s the responsibility of
the **navigator**. They make decisions, and ask the driver to implement them.

Start by forking this repo:
![fork button](https://readme-pics.s3.amazonaws.com/fork_button.jpg)

Forking creates a copy of this repo in your own GitHub account. Add your partner
as a collaborator by going to 'Settings' > 'Collaborators & teams' and entering
their GitHub username in the 'Collaborators' box. That means you'll both have
access to the repo.

You should now have a copy of this git repository in your own github account.
Now, we need to get a copy on our own laptop for us to work with. Start by
opening a terminal and creating a projects/ada folder if you don't already have
one:

```sh
cd Desktop
mkdir Projects
cd Projects
```

Next, we need to clone the repo. This copies all the files and history from
github to our own computer:

```sh
git clone https://github.com/<your github username>/di-workshop-01-intro-to-p5.git
cd di-workshop-01-intro-to-p5
```

You can see that it's a git repository and some of the history by running these
commands:

```sh
git status
git log
```

> **Note:** If you get stuck in `git log`, it's because you're in something
> called a pager. This is a really old bit of software from before computers
> could scroll in the way we're used to. You can move up and down in the pager
> with your arrow keys, and exit it by pressing `q`

Finally, we need to install some bits and pieces that in our new repo to finish
setting it up:

```sh
npm install
```

---

We’ll be working with some software called P5. P5 is a **JavaScript library**
for drawing shapes - it’s used for making simple games and cool generative art.

For each of the **bold** questions below:

<h3 align="center">
  🗣 Discuss &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  👩‍💻 Change &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  👀 Observe &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  🔄 Repeat
</h3>

1. **🗣 Discuss** the question with your partner
1. **👩‍💻 Change the code** - what do you expect your changes to do?
1. **👀 Observe the results** - what happened when you ran your code? How did it
   differ from your expectations
1. **🔄 Repeat** - keep discussing, changing, and running the code until you
   feel you understand it

**The aim of this workshop is _exploration_, hopefully leading to
_understanding_. It’s really important that you _take your time_. The questions
below are _guidelines_, meant to prompt your _curiosity_. If you can’t answer a
question, use a search engine or ask someone nearby. Don’t move on until you
_fully understand_ what’s happening.**

**Explore and have fun! Be curious!**

# Setup

Now you've got the repo cloned and installed, we need to start it up:

```sh
npm start
```

This runs a web server - a little program that your browser can connect to so
that the files you write in this project can run in there. Now, when you visit
http://localhost:5000/, you'll see all your files right there.

Open the workshop folder in your editor. In VSCode, choose File > Open and
select the folder - _not any of the files inside it_. You should see all the
workshop files in the left-hand file pane.

Open this file - README.md - in your editor. Make notes in here about everything
you do. If you don't know the answer to a question, it's your job to experiment
with the code to see what you can find out.

# Sketch A

Open the `part-a` sketch in your browser, and open `part-a/sketch.js` in your
editor. The code in `sketch.js` is what's running on the page. Every time you
make a change in `sketch.js`, you need to save the file (ctrl-S or cmd-S) and
refresh your web browser (ctrl-r or cmd-r) to see the change.

---

Look at these lines:

```js
var r = 255
var g = 80
var b = 0
```

**What might these lines do?**

These are the colors.

**What happens if you change the numbers?**

The color changed.

**What numbers are allowed / What numbers have an effect?**

Look at this line:

```js
createCanvas(400, 400)
```

**What does createCanvas do?**

It creates a square or rectangle.

**What happens if you change the numbers?**

The size of the canvas will change.

**What numbers are allowed/what numbers have an effect?**

Numbers without decimals are allowed

**What happens if you add/remove a number?**

When i add a number nothing happens, when i remove a number th canvas disappears.

**Can you guess what the `function setup() {` part does? What happens if you
change the name of setup?**

It literally sets up the canvas. when you change the name the canvas doesnt get created and there is a blank page.

Look at this line:

```js
background(r, g, b)
```

**What does background do?**

It select the background to take on a new color.

**What happens if you change the order of the letters in background? What does
this tell you about how the computer uses them?**

The background color will change, the computer is set to read them in the order R, G, B.

**What happens if you change the number of letters?**

The code does not work.

**What happens if you change the letters for different ones?**

The code does not work.

# Sketch B

Open the `part-b` sketch in your browser, and open `part-b/sketch.js` in your
editor.

Read the code and play with the sketch in your browser.

> **Note**: There's two main sections in the code - the bit called `setup` and
> the bit called `draw`. The code in the `setup` section runs **once**, when
> your program first starts up. The code in the `draw` section runs again and
> again and again - 60 times every second.

Look at these lines:

```js
function setup() {
  createCanvas(400, 400)
  background(0, 0, 0)
}
```

**What does setup do?**

It sets up the box that you can draw in.

**What do `{` `}` mean? What happens if you remove one?**

These contain the code, if we remove one the whole code stops working.

**What do the numbers in `background(0, 0, 0)` do? What happens when you change
them? How is this different from Sketch A?**

They change the colors of the bakcground, they are RGB values. Here we change the color hues in the brackets instead of setting the hue values as variables.

Now look at these lines:

```js
function draw() {
  fill(255, 0, 0)
  ellipse(mouseX, mouseY, 30, 30)
}
```

**What does draw do?**

Draw allows us to draw into the canvas with our cursor.

Now look at:

```js
fill(255, 0, 0)
```

**What do these numbers do? What happens when you change them?**

They are the RBG values of Draw. it changes the color that we draw in.

**What does fill mean? What happens if you change it to stroke?**

fill makes the color fill the dots that we are drawing. stroke makes the color the outer diameter ring color of the dots that we draw with.

**What happens if you remove (or comment out) this line? What about if you
include both fill and stroke on seperate lines?**

If we comment out the "fill" line, we just get white dots with no color at all. If we add both fill and stroke on separate lines, the dots have one uniform color. both the outer diameter ring as the inside of the dots are the same color, or both colors can be changed.

Now look at this line:

```js
ellipse(mouseX, mouseY, 30, 30)
```

**What does `ellipse` do?**

ellipse determines the shape that we are drawing.

**What happens if you change the numbers?**

The shape of the dots changes.

**What do `mouseX` and `mouseY` mean?**

It means that we can draw on both the X and Y axis. for instance if we delete Y, we can only draw horizontally (along the X axis).

**What happens if you change the order of the items between the `(` `)`?**

It messes with our ability to draw. I changed to this (mouseX, 30, mouseY, 30) and i can only draw along the X axis.

---

**What happens if you add `background(0)` after `draw() {`? Why?**

It adds a background to the draw layer, we can't see what we are drawing as the canvas is covered by this new background.

Replace the ellipse with a triangle. Use https://p5js.org/reference/ (the 2D
primitives section) to help.

Play around with the sketch - how else can you change it?

# Sketch C

Open the `part-c` sketch in your browser, and open `part-c/sketch.js` in your
editor.

Read the code, then play with the sketch and observe what happens - try clicking
the mouse on the sketch.

Look at:

```js
if (mouseIsPressed) {
  fill(255, 0, 0)
} else {
  fill(0, 255, 0)
}
```

**What does `mouseIsPressed` mean?**

When you keep your mouse pressed the color that you draw with will change.

**What happens if you change `mouseIsPressed` to `keyIsPressed`?** You’ll need
to click on the sketch so it registers keyboard events – use the ctrl key if you
have issues with the keyboard.

It does the same as keyIsPressed, but instead of pressing your mouse you can press any key on your keyboard.

**What does if / else do?**

If/else is the part of the code that has the color set for each situation (mouse hover or mouse/key pressed).

**What happens if you remove the { } or ( )? Why?**

The code doesn't work properly, the {} and () are used to contain the code.

**What happens if you change 255 to mouseX ? Why?**

It puts a dark fade over the canvas from left to right.

**Remove the outline of the circle. Use Google and the P5.js reference to help
you.**

# Challenge

In your pairs, take the code in sketch c and adapt it into a simple paint
program. The user should be able

- click and drag to paint on the screen
- press keys on the keyboard to choose a colour
  - e.g. pressing ‘r’ changes the paint colour to red, pressing ‘g’ changes the
    paint colour to green.

Use this code as a starting point:

```js
if (keyIsPressed) {
  if (key == 'r') {
    // set paint colour to red
  }
  if (key == 'g') {
    // set paint colour to green
  }
  // add more keys/colours
}
```

**Document your process in this file.**

## Extension

- Change the shape of the brush (explore other shapes like squares or triangles)
  based on a key pressed
- Change the size of the brush based on a key pressed.
