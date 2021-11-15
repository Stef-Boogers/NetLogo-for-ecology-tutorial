# Agent-Based Modeling for Ecology in NetLogo

## 0. Preparation <br>

1. Install the latest version of NetLogo from the dedicated [website](https://ccl.northwestern.edu/netlogo/6.2.1/).
2. Make sure the installation is successful and open NetLogo.
3. Grab the presentation [here](https://github.com/Stef-Boogers/NetLogo-for-ecology-tutorial/blob/7ecc3bbc0941d7db4e13f4862a671f0e17ab5287/assets/Agent-Based%20Modelling%20for%20Ecologists.pptx), if needed. There's a **Download** button on the right.
4. Open the well-documented [NetLogo dictionary](https://ccl.northwestern.edu/netlogo/docs/dictionary.html), which will answer most questions you have about specific algorithms.
5. Also open the [Interactive Dictionary](https://ccl.northwestern.edu/netlogo/bind/primitive/patches.html), which will answer all remaining questions with great examples.
6. Follow the presentation at 12.30, either in room 01.252 or through Teams. After the presentation, you're ready to get started on the next section! <br>
--- <br>

## 1. Fireflies: playing with your first model <br>

In NetLogo, go to *File > Models Library* or type `Ctrl+M`. There, use the search bar at the bottom of the screen and type "Fireflies". The folder tree structure will show one option, under the folder "Biology". Doubleclick "Fireflies" and the model will load. If this fails, you can run the model online [here](http://www.netlogoweb.org/launch#http://ccl.northwestern.edu/netlogo/models/models/Sample%20Models/Biology/Fireflies.nlogo).
<br><br>
- Click the "Info" tab up top to get your bearings. What is being modelled? What are the different options? What do the authors recommend that you try?
- Get back to the "Interface" tab. On the left, you will find some typical input boxes (green). You can fidget around with them if you like. Nothing will happen yet. I advise you to set ![darkswitch](assets/DarkSwitch.JPG) to "On".
- When you have found some settings that suit you, press ![setup](assets/Setup.JPG). Afterwards, press ![go](assets/Go.JPG). The "go" button has a roundabout sign, which means that this procedure keeps repeating until you press the button again or until a predetermined number of 'ticks' or timesteps has passed.
- Does the output of the model match your expectations? Play around with settings. You can often do this while the model is running. Some inputs are however only passed into the model during the "setup" procedure, meaning that changing them during the "go" procedure, won't have an influence.

**To remember:**

> NetLogo is fun. Especially if someone else built the model. <br>
> Procedures, euhm, exist. So do ticks.<br>
> Please tell me more. Especially code, I love code.

---

## 2. Typical NetLogo code structure <br>

Onwards to coding! All NetLogo models follow the same general structure. Within that framework however, the user has a lot of freedom. <br>
NetLogo follows a class-based object-oriented paradigm, in which the user has to define classes (the types of turtles and patches), the attributes of these classes and the methods that can be applied to them. A fake example using pseudocodefor a basic version of a sheep-wolves predation model should make the rudimentaries clear. <br><br>

### A. Globals

At the top of our code, we name the global parameters. These are parameters that have the same value for all agents, across all procedures.
All values set through the user inputs on the interface page are considered globals. You only name the parameter here and will set its value later.

```
; Semicolons comment out lines. 

; Imagine that you want the model to stop when the screen becomes crowded with sheep. 

globals [
  max-sheep
]

```
<br>

### B. Turtle-own

After the globals, we name our classes of (non-patch) agents: the turtles. In our case, there are two separate classes: wolves and sheep. In our model, they both only have one 
attribute: their energy level.

## Fun other models to play with 
- [Camas-Douglas fir fire model](http://modelingcommons.org/browse/one_model/6020#model_tabs_browse_nlw): progression of a wildfire across a plairie filled with camas, becoming invaded with Douglas fir when a steady fire regime is abandoned. Similar to the burning of heath fields in our own region. 
- Autumn: you can find this one in NetLogo's modelling library (`Ctrl+M`). Model of a single tree losing its leaves due to the interactions of wind, rain, sun regime and branch architecture. A good example of how the modeling output window doesn't have to be a bird's eye view.
- Pac-Man: again from the modelling library. Yes, you can build simple games in NetLogo. But it's a little underwhelming.
- [Game of Thrones](https://www.comses.net/codebases/08e45650-f6a9-4c26-a99f-2938e7d8cbdc/releases/1.7.0/): a didactic exercise in Logo, NetLogo's spiritual predecessor. Layer by layer, the island of Westeros and its warring Houses are built from the ground up, only to let the White Walkers and the occasional dragon burn everything to the ground. Great timewaster and actually pretty informative, too.<br>


