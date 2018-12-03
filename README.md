# Handimations

Handimations is a drawing software that utilizes the LeapMotion hand sensor to allow users to draw their own flipbook gifs. No sticky-notes or art supplies needed! This project was developed in Fall 2018 as a final project for CSC 355: Human Computer Interaction.

![screen](https://github.com/madelinefebinger/handimations/blob/master/Handimations/src/img/Screen%20Shot%202018-12-02%20at%209.14.25%20PM.png)

## Team Hunnie Badgers

* **Maddie Febinger** - *febingm1@tcnj.edu*

* **Victoria Green** - *greenv2@tcnj.edu*

* **Emily Kazenmayer** - *kazenme1@tcnj.edu*

* **Ananya Srinivasan** - *sriniva5@tcnj.edu*

## Getting Started

To get started, clone or fork our repository on GitHub. The main file we are working from is *Handimations/src/index.html*. Styling is handled by *Handimations/css/main.css*. See deployment for notes on how to deploy the project.

### Prerequisites

Ensure that JavaScript is enabled in a Firefox, Internet Explorer, Opera, or Safari browser. Note that the gif making library used in this application is not compatible with Google Chrome, as we were unable to find a GIF exporting library that is compatible. Clone or download this GitHub repository to access the files.

## Deployment

To run the application, navigate to *Handimations/src/index.html* and open the file in your browser. Ensure that JavaScript is enabled in your browser.

## Functions

Explaining the functions


## Built With

* [LeapJS](https://developer-archive.leapmotion.com/documentation/javascript/index.html) - LeapMotion Javascript SDK - The official library that supports LeapMotion development in JavaScript. This library represents hands/fingers, along with their movements as objects. Some of this objects and attributes we used in our project include:

    * Hand: This object represents the hand(s) held over the LeapMotion sensor. The Hand object consists of an array of Finger attributes. In fact, the LeapMotion has labeled attributes for all of the hands, such as hand.indexFinger and hand.pinky for the respective fingers.
    * Finger: The Finger objects represent the fingers of a hand. We particularly used the extended attribute for the fingers to determine whether the index finger, pinky, or all fingers were extended. 
    * InteractionBox: The InteractionBox object was used to plot the hand movements on to the canvas element on screen. Using the InteractionBox, we received the normalizedPositions of the fingers, and then plotted the lines between the points using lineTo() and stroke().
    * Frame: Frames were used to detect hand gestures and movements at a particular instance. We iterate through Frames using Leap.loop() to look for particular gestures or movements. In a particular frame, we can get the fingers and hands 

* [Atom](https://atom.io/) - IDE for teletyping
* [gif.js](https://github.com/jnordberg/gif.js) - JavaScript GIF Encoder that runs in your browser - We used the gif.js library to export the animation as a GIF. The following files are from the gif.js library and we did not implement them:
     * gif.js
     * gif.js.map
     * gif.worker.js
     * gif.worker.js.map

   Functions:
   
     * exportGif() function in index.html creates a GIF object and uses the following functions from the gif.js library
     * gif.addFrame(canvasElement, delay) - adds a new frame with a given delay
     * gif.render() - creates the finished gif

## Controls

### LeapMotion

Hold one hand over the LeapMotion, with your palm facing down. 
   * Change color: Use the color palette button on the toolbar with your mouse and select a color using the color picker
   * Draw: Point with your index finger and move your finger over the LeapMotion area
   * Erase: Point with your pinky and move your finger over the LeapMotion area
   * Switch to mouse mode: Click the Cursor button on the toolbar
   * Create a new layer: Make a swiping motion from left to right
   * Undo last line: Click the Undo button on the toolbar with your mouse
   * Clear current layer: Click the Trash button on the toolbar

### Mouse

Use the mouse of the computer you are using the application with.
   * Change color: Use the color palette button on the toolbar with your mouse and select a color using the color picker
   * Draw: Toggle the Draw button (“Pencil” icon). To start drawing, use your mouse to click on the area of the drawing canvas you want to start at. Drag your mouse across the canvas to draw a line. To stop, click the area you want to stop and release your mouse.
   * Erase: Toggle the Erase button (“Eraser” icon). Follow the same instructions as Draw to erase lines. 
   * Switch to LeapMotion mode: Click the LeapMotion button on the toolbar
   * Undo last line: Click the Undo button on the toolbar with your mouse
   * Clear current layer: Click the Trash button on the toolbar
   
### Exporting Animations

* Export GIF: Click the Export button on the toolbar. The GIF will open in a new window. Right-click the GIF and select “Save Image As” to download the GIF to your computer. 
* Preview GIF: Click the Play button on the toolbar


## Acknowledgments

* Hat tip to anyone whose code was used
* Inspiration
* etc
