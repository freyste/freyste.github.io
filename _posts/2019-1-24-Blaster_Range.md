---
layout: post
title: The Droid Blaster Range Toy
summary: A relatively safe shooting range toy for my nephews  
---

![_config.yml]({{ site.baseurl }}/images/IMG_2477.jpeg)

Lately my nephews have been obsessed with Star Wars and I wanted to make them a toy that no other kids on the block would have. Given that the Disney Star Wars franchise has probably made every toy they could, I had to come up with something just dangerous enough that they couldn’t.

![_config.yml]({{ site.baseurl }}/images/nephews.jpeg)

The concept was a storm trooper laser blaster and a series of targets that would tip and fall when struck by the laser. I thought this could be pulled off pretty simply with a laser module for the blaster and a photoresistor sensor plus servo for the targets. 

![_config.yml]({{ site.baseurl }}/images/starwars_concept.png)

At some point I realized that in order for the laser to hit the target but wirelessly trigger the servo to knock over that target, the laser light would need to be redirected. The solution I came up with was to have the target be a hole that the laser light would enter with a 45 degree angled mirror at the back of it which would redirect the light to a light sensor below.

*sketch of the mirror concept*

For the targets I had initially planned to put some living characters like Jar Jar Binks since this was a storm trooper blaster after all but opted instead for droids. Seemed less violent and also the way the targets would fall seemed pretty realistic to how a droid my respond to a blaster. 

![_config.yml]({{ site.baseurl }}/images/droid_fall.gif)
![_config.yml]({{ site.baseurl }}/images/gronk_fall.gif)

The target range uses 3 servo motors to raise and lower pins that destabilize and topple the target. These servos are triggered to actuate when the photoresistors tell an Arduino that they are seeing light from the laser. To create this signal the photoresistors are wired in parallel with 10K resistors and set up as a voltage divider for the Arduino to read as high/low light once a threshold is set.


![_config.yml]({{ site.baseurl }}/images/top_view.png)

![_config.yml]({{ site.baseurl }}/images/range_switch.gif)

The design of the blaster is simple and entirely 3D printed down the the springs, with the exception of the laser module, the tactile switch, and the battery.

![_config.yml]({{ site.baseurl }}/images/Blaster_Cross_Section.png)

Put it all together and it makes for a pretty fun little game

![_config.yml]({{ site.baseurl }}/images/range_trio.gif)

<!-- Import the component -->
<script type="module" src="https://unpkg.com/@google/model-viewer/dist/model-viewer.js"></script>
<script nomodule src="https://unpkg.com/@google/model-viewer/dist/model-viewer-legacy.js"></script>

<!-- Use it like any other HTML element -->
<model-viewer src="/images/Blaster2.glb" style="width:500px; height:500px;" auto-rotate camera-controls camera-orbit="180deg 30deg 105%"></model-viewer>

<model-viewer src="/images/range.glb" style="width:500px; height:500px;" auto-rotate camera-controls camera-orbit="180deg 30deg 105%"></model-viewer>

If I were to make improvements to this I might try to coat the internal holes of the targets with some kind of reflective paint or tape to prevent some of the light from being absorbed into the plastic and lost. Additionally I would opt not to use a single flat angled 45 degree mirror but instead use a curved light focusing mirror system that would be more tolerant to off angle lasers. In the current design one needs to be pretty close to perpendicular with the target hole axis. 

*sketch of the improved mirror concept*
