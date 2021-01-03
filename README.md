# OpenAIStreetFighter
Custom implementation of Open AI Gym Retro for training a Street Fighter 2 AI via reinforcement learning.

The first commit uses largely unchanged model examples from https://github.com/openai/retro as a POC to train the AI using the 'Brute' method.

This repo contains example .bk2 files for those interested to play back and observe the AI in action.

## (Planned) additions & changes 
* [ ] Track learning in game with interactive parser
* [ ] Implement and test other algorithms (e.g. PPO)
* [ ] Code in character special moves as inputs
* [ ] Apply pre-trained models to new situations (experiment with different states and characters)
* [ ] Add ability to train from human input parameters or play against human opponent

## Instructions:
* Install the 'retro' and 'gym' packages to Python.
* Add the custom scenario json file included in this repo to your retro/data/stable folder which has the roms in. 
* Update any parameters in the 'brute.py' example.
* Run (note you will need a valid copy of the rom (Street Fighter 2 Champion Edition (USA) for this to work) - the training will output a .bk2 with the button inputs used each time there is a significant innovation. The algorithm will stop once the timestep limit is reached.

### To render the outputs in mp4 format
In CMD cd into your directory which has the .bk2 files
run ```py -m retro.scripts.playback_movie NAMEOFYOURFILE.bk2```


