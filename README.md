# Handimations

Handimations is a drawing software that utilizes the LeapMotion hand sensor to allow users to draw their own flipbook gifs. No sticky-notes or art supplies needed! This project was developed in Fall 2018 as a final project for CSC 355: Human Computer Interaction.

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

The exportGif() function in index.html creates a GIF object and uses the following functions from the gif.js library
     * gif.addFrame(canvasElement, delay) - adds a new frame with a given delay
     * gif.render() - creates the finished gif

## Acknowledgments

* Hat tip to anyone whose code was used
* Inspiration
* etc
