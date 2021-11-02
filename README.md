# Dragon_Aide
## Goal
The goal here is to create a Python will assist in writing campaigns/one-shots for Dungeons & Dragons. 
Creating homebrew campaigns (a storyline or mission that is entirely made up, as opposed to being from one of the many D&D books) is pretty challenging- you as the Dungeon Master (DM) are responsible for entertaining a group of players, making them care about what happens to their characters, creating an interesting plothook, and making sure the conflict and resolution are satisfying. Building a story whilst implementing encounters, characters and quests with a consistent level of emersion is very tricky- which is why this software will be built to complement the world-building aspect of running and D&D campaign to make it easier for the DM. 

## Premise 
Say you're writing up a new set of encounters for a location that your players will enter. You're getting writer's block, and none of your ideas seem good enough to proceed with. You're sure you want an encounter with an NPC, but aren't sure what the NPC will want (because you just came up with all this for a group of NPC's in the last town your players encountered and this process took the rest of your creative energy). So you turn on the software and type "players arrive in **[location]**... and the sofware will auto-insert a random name from a repository full of location names. If you want location names that sound particularly Dwarven, Elven or Infernal, just type **[location Dwarven]** and the software will insert a random name from a list of Dwarven themed location names. Similar inserts will exist for **[name]**, **[name male]**, **[name elven female]** and so on. 

## How
I'll create a bunch of repositories, or dictionaries in Python. Each will be titled something like "name dwarven", and it'll have ideally hundreds of named associated with that class or style. Once it gets bigger, I can make names more specific to a region in the given world, or DMs can plug in names of their own. Similar dictionaries will exist for "encounter" and "hook" or "monster". 

The code for a single dictionary ("Human", for instance) will be like so: Human = {Arran, Allan, Aldridge, Alaster}. 

# Dictionaries
## NPCs
Below is a list of Dictionaries that I will develop for DMs to use as they introduce new characters to their players. 

1. Human 
2. Human Female
3. Human Male
4. Dwarf
5. Dwarf Female
6. Dwarf Male
7. Elf 
8. Elf Female
9. Elf Male
10. Orc
11. Orc Female
12. Orc Male
13. Halfling
14. Halfling Female
15. Halfling Male
16. Halfling Male
17. Gnome
18. Gnome Female
19. Gnome Male
20. Dragonborn
21. Dragonborn Female
22. Dragonborn Male
