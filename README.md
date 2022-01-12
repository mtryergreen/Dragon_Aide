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

