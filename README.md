# Node-Red Button+ flow #

TLDR explaination:
In the global context store of my node-red (persistent storage) are my menu configs stored, there are 2 main stores:
- Menus (the actual menus)
- Entities (the individual entities i can use in my menus)
Reason for the entities is to use them in multiple places without the need to duplicate nodes.
As you can see I don't like to use function nodes unless it can not be done without them.
The main flows purpose is to create the menus and entities and keep everything updated.

![alt text](https://github.com/[username]/[reponame]/blob/[branch]/screenshot/example.jpg?raw=true)

## main_flow.json ##
Main flow containts 2 main flows:
- ButtonPlus - Get Button Events, this listens to the command topics for all buttonplus in my home, the + items are wildcards to ignore the topic and listen to the subtopics.
- ButtonPlus - Update ButtonPlus, this updates the buttons for each defined buttonplus devices defined in the step after Update.

## EXAMPLE - global_context.json ##
Contains my exported global context used by my button+ devices. Active running state of my devices.

## EXAMPLE - example_sonos.json ##
Contains an example how I update my sonos active playing state.

## EXAMPLE - example_light.json ##
Contains an example how I control a light and update its status to the device entities for buttonplus.

## Buttonplus config ##

![alt text](https://github.com/[username]/[reponame]/blob/[branch]/screenshots/display_menu.jpg?raw=true)
![alt text](https://github.com/[username]/[reponame]/blob/[branch]/screenshots/buttonplus_button_config.jpg?raw=true)
![alt text](https://github.com/[username]/[reponame]/blob/[branch]/screenshots/example_mqtt.jpg?raw=true)
