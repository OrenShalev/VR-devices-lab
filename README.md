# VR-devices-lab
This is my first experiment with [A-Frame](https://aframe.io/), and it's great! :)

Jump to [the demo](https://leaf-trip.glitch.me) using your laptop, phone, or any other device with a modern browser. See [the code](https://glitch.com/edit/#!/leaf-trip) at Glitch, or in this repo.

## Background
I've created this demo as part of a hackathon at work. The "functional" aspect of it is managing a lab of mobile devices, but in a different kind of UI. I wanted to play with VR, especially WebVR, quickly set sights on A-Frame, and then just tried adding different bits.

I really like A-Frame's approach of using HTML for setting up a scene, and also the live ecosystem around it. If you're into VR and web, you should definitely try it.

Since this is *Web*VR, A-Frame is built for all kinds of devices -- but I found out that the trick is setting up convenient **controls** for all these devices. That took me most of the time and was the most challenging part. More on that below.

## Building blocks I've used
* Plain objects, like boxes with image textures for the phones and very low cylinders for the "stepping stones". Also text labels (2D and visible from only one side :thumbsdown:) and a-sky, which is just a big sphere with an equirectangular image on its inside.

* Plugin for replacing the sky image nicely with fade to black.

* Various controls (see below)

* Tried all kinds of other stuff that I didn't have time to investigate why are they not working: displaying content of HTML from outside the scene; adding a physics engine; better lights; user interaction; dynamically add or remove elements from the scene; grouping to entities and moving/rotating the group.

## Controls
So if you build for the web, you want to accomodate as much as possible these input methods (and others): keyboard+mouse; gyro+touchscreen, gyro+touchscreen-but-in-HMD such as Google Cardboard, and maybe HMDs with controls -- but I don't have anything with controls, and wanted something for non-VR-oriented people.

So this is the simplest setup I came up with, and IMO it works wonderfully with any hardware I have:

* Look around with mouse and/or gyro. Unlike the default controls you get from A-Frame, the mouse is "locked" into the scene -- this is wonderful because dragging is a terrible interaction in itself, and in "world-sized" places like VR you keep hitting the edge of the window. The "lock" solves this, it's much much better.

* Walk around with WASD or arrow keys. Simple and works well. BTW, if you're not familiar with the WASD's "fly" mode, try it (look for a comment in my code).

**The trick was to find a convenient way to "walk" with devices that don't have keyboard, such as a smartphone.**

* I solved this with gaze-based interactions and checkpoint controls (the "stepping stones"). (TODO: add links)
Basically you have a little sight at the center, and if you look at something actionable it changes color to hint you. If you stay on it a little while, you trigger the action. The action for a stepping stone is "walk to here"; the action for a background thumbnail is "apply this image on the sky".

## Glitch
This is an amazing tool. Terrific feature set with a neat UI. 
