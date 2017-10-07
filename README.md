# VR-devices-lab
This is my first experiment with [A-Frame](https://aframe.io/), and it's great! :)

Jump to [the demo](https://leaf-trip.glitch.me). See [the code](https://glitch.com/edit/#!/leaf-trip) at Glitch, or in this repo.

## Background
I've created this demo as part of a hackathon at work. The "functional" aspect of it is managing a lab of mobile devices, but in a different kind of UI. I wanted to play with VR, especially WebVR, quickly set sights on A-Frame, and then just tried adding different bits.

I really like A-Frame's approach of using HTML for setting up a scene, and also the live ecosystem around it. If you're into VR and web, you should definitely try it.

Since this is *Web*VR, A-Frame is built for all kinds of devices -- but I found out that the trick is setting up convenient *controls* for all these devices. That took me most of the time and was the most challenging part. More on that below.

## Building blocks I've used
* Plain objects, like boxes with image textures for the phones and very low cylinders for the "stepping stones". Also text labels (2D and visible from only one side :thumbdown:) and a-sky, which is just a big sphere with an equirectangular image on its inside.

* Plugin for replacing the sky image nicely with fade to black.

* Various controls (see below)

* Tried all kinds of other stuff that I didn't have time to investigate why are they not working: displaying content of HTML from outside the scene; adding a physics engine; better lights; user interaction; dynamically add or remove elements from the scene; grouping to entities and moving/rotating the group.

* Background
* What I've used
* Controls
* A word about Glitch
