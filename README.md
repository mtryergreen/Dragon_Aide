# Dragon_Aide
## Goal
The goal here is to create a Python program that will assist in writing campaigns/one-shots for Dungeons & Dragons. 
Creating homebrew campaigns (a storyline or mission that is entirely made up, as opposed to being from one of the many D&D books) is pretty challenging- you as the Dungeon Master (DM) are responsible for entertaining a group of players, making them care about what happens to their characters, creating an interesting plothook, and making sure the conflict and resolution are satisfying. Building a story whilst implementing encounters, characters and quests with a consistent level of emersion is very tricky- which is why this software will be built to complement the world-building aspect of running and D&D campaign to make it easier for the DM. 

## Premise 
Say you're writing up a new set of encounters for a location that your players will enter. You're getting writer's block, and none of your ideas seem good enough to proceed with. You're sure you want an encounter with an NPC, but aren't sure what the NPC will want (because you just came up with all this for a group of NPC's in the last town your players encountered and this process took the rest of your creative energy). So you turn on the software and type "players arrive in **[location]**... and the sofware will auto-insert a random name from a repository full of location names. If you want location names that sound particularly Dwarven, Elven or Infernal, just type **[location Dwarven]** and the software will insert a random name from a list of Dwarven themed location names. Similar inserts will exist for **[name]**, **[name male]**, **[name elven female]** and so on. 

## How
I'll create a bunch of lists in Python. A list is just an array that contains data items (a list of counties could look like **counties = ["Arapahoe" "Denver", "Jefferson"]**. Each list will be titled something like "Dwarf", and it'll have hundreds of names that could be associated with Dwarven characters. Once it gets bigger, I can make names more specific to a region in the given world, or DMs can plug in names of their own. Similar dictionaries will exist for "encounter" and "hook" or "monster". 

The code for a single list ("Human", for instance) will be like so: Human = {Arran, Allan, Aldridge, Alaster}. An individual dictionary exists inside the brackets {}. 

# Dictionaries
## NPCs
First, there would need to be a list for when the DM can't decide what race the new NPC should be. Here's a snapshot of this list could look like: 

<img width="596" alt="Screen Shot 2021-11-02 at 7 36 47 PM" src="https://user-images.githubusercontent.com/89936913/139966299-a5af7918-298c-4fd8-96c0-4fdad656f472.png">

The next step would be to retrieve one of the items in the list at random. This is new ground for me, but it looks like the code (retrieved from https://www.geeksforgeeks.org/python-random-sample-function/) for this would be **from random import sample** to setup the random selection, then printing it with **print(sample(list1,3))**. This example makes the list name "list1", which I'll change to "race". Translate this for my use and what I get is: 

<img width="218" alt="Screen Shot 2021-11-02 at 7 48 27 PM" src="https://user-images.githubusercontent.com/89936913/139967290-ead33819-40be-4118-a1f4-11e962409d48.png">

The code worked, and it retrieved "halfling" and "dragonborn female" as the items. Very cool- if a DM wanted to put two more NPCs into a tavern, there could be an interesting mix of a dragon-esque adventurer conversing with a three-foot tall humanoid. 
