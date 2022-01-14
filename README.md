# Dragon_Aide

# Intro
## Context
Dungeons & Dragons is a tabletop role-playing game. There is a Dungeon Master who is in charge of telling and crafting a story, and there are players (1-6, ideally) who act as travellers/adventurers in this imaginary story world. The dynamics are math-based, with odds of success and skills largely depending on dice rolls. The basic principle of the game is shared storytelling in a sandbox format- anything can happen. Because anything can happen, it is the job of the Dungeon Master (DM) to be creative, offer their players unique and interesting challenges as they progress, and to make the world seem as real and livable (or hostile) as possible. One of the most difficult aspects of the DM's job is to constantly create new and intriguing non-player-characters, or NPCs. This program will aim to make this responsibility easier for the DM. 
## Goal
The goal here is to create a Python program that will assist in NPC and mission development for Dungeon Masters as they run games of Dungeons & Dragons. 
Creating homebrew campaigns (a storyline or mission that is entirely made up, as opposed to being from one of the many D&D books) is pretty challenging- you as the Dungeon Master (DM) are responsible for entertaining a group of players, making them care about what happens to their characters, creating an interesting plothook, and making sure the conflict and resolution are satisfying. Building a story whilst implementing encounters, characters and quests with a consistent level of emersion is very tricky- which is why this software will be built to complement the world-building aspect of running and D&D campaign to make it easier for the DM. 
## Application 
Say you're writing up a new set of encounters for a location that your players will enter. You're getting writer's block, and none of your ideas seem good enough to proceed with. You're sure you want an encounter with an NPC, but aren't sure what the NPC will want (because you just came up with all this for a group of NPC's in the last town your players encountered and this process took the rest of your creative energy). So you turn on the software and type "players arrive in **[location]**... and the sofware will auto-insert a random name from a repository full of location names. If you want location names that sound particularly Dwarven, Elven or Infernal, just type **[location Dwarven]** and the software will insert a random name from a list of Dwarven themed location names. Similar inserts will exist for **[name]**, **[name male]**, **[name elven female]** and so on. 

# Strategy
## How (JavaScript)
I think JavaScript would be the ideal language to create this. The finished product can be displayed on a HTML file that is stylized in CSS and programmed with JavaScript. I can also do all the work in VSCode. 
## Storyboard
I've created a storyboard for the layout of the HTML page. Seeing it displayed like this is actually really invigorating- the potential here is huge. 
<img width="1181" alt="Screen Shot 2022-01-11 at 4 59 29 PM" src="https://user-images.githubusercontent.com/89936913/149045157-f31efe25-04fa-4999-b95f-bdb3db7eaa8a.png">


## Arrays
I'll create dozens of arrays containing names, races, quests and locations. All of the arrays, when utilized together, will be able to quickly put together the name, race, goal, and origin point of an NPC.
Arrays in JavaScript are variables that can hold more than one value. 
One array may look like:
**const race = ["human", "elf", "dwarf", "dragonborn"];**. 
This is a race array, containing a few races that the DM can draw on should they need to quickly decide what race a new NPC will be. Cool. 

## Randomize
Next, I'll write code that can extract a random item from the target array. 
I've no idea how to generate something like this, so I'm looking up array randomizers on StackOverflow. It looks like one option is a line of code looking like:

**const random = Math.floor(Math.random() * race.length);
console.log(random,race[random]);**
This line is meant to retrieve a random item from the race list. 
I tried this in the console tab of Chrome, and it worked great:
![Screen Shot 2022-01-11 at 5 30 53 PM](https://user-images.githubusercontent.com/89936913/149048035-96a4cc01-b0a5-4ddd-bc4a-77d22e26d769.png)

We can see where the array was labeled as undefined, meaning that it worked. The randomizer indeed retrieves a random item from the list, the the console.log function prints the item. 

## Button
Then, I'll create a button that takes that random item and puts it in a text box. 
First, I need to learn how to create a button. These tutorials are scattered around the web, and some are easier to understand than others. This is the best one I found, it worked just by copying and pasting it into my own HTML file: https://www.w3schools.com/tags/tryit.asp?filename=tryhtml_button_css. 
![Screen Shot 2022-01-11 at 9 47 23 PM](https://user-images.githubusercontent.com/89936913/149071064-23151cc0-a2a1-44a6-bf1b-0310b9e9eb79.png)

So here I've created the button, now I need to attach it to a command and have the result appear in a text box next to it so that the "Race" button actually retrieves a random race. This'll be the hardest step, I think... the others just mirror this one. 

The more I peruse button functions on StackOverflow, the more "appendChild" shows up. A JavaScript blog says that appendChild can be used to append/add the button and its function to the HTML page. It also says that to execute some code when the button is pressed, I'll need to change the "onclick" property of the button. 

I found a way to use the Inspect page of the Drage Aid html doc using this code:
Here is the code itself from VSCode: 
<img width="449" alt="Screen Shot 2022-01-12 at 1 48 14 AM" src="https://user-images.githubusercontent.com/89936913/149116168-7e716bdf-a13a-4895-92c1-c351275b6076.png">

And here is the code inserted into the Chrome console: 
<img width="709" alt="Screen Shot 2022-01-11 at 10 27 29 PM" src="https://user-images.githubusercontent.com/89936913/149075537-095d7b81-47ca-4cf4-987a-77aebd457d2d.png">

It indeed creates a "Race" button that gives me a new, random race each time I press it. Awesome. 
The issue with typing this all into the console of Chrome is that it doesn't save... or I don't know how to yet. 
## Actual solution
It took more prodding, but I found a way to code HTML directly into VSCode, which should be standard stuff but again, its hard as a beginner to understand a lot of coding tutorials. 
Basically, I just go to my VSCode HTML file and type "!" and hit enter. This formats the bones of a body of text. I then insert <button> between the body items.
<img width="449" alt="Screen Shot 2022-01-12 at 1 48 14 AM" src="https://user-images.githubusercontent.com/89936913/149229498-f37ae8e2-4cac-4bed-be78-054d204b14a0.png">
All these tutorials point out that in HTML alone, buttons can't do much. I need another language, like JavaScript, to program the functionality and logistics of these HTML functions. 

## Button Output
Now I need a place on-screen for the output text to go. Pressing the "Race" button should have a text box next to the button fill with the result. 





