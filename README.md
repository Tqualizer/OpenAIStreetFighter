# OpenAIStreetFighter
Custom implementation of Open AI Gym Retro for training a Street Fighter 2 AI via reinforcement learning.

The first commit uses largely unchanged model examples from https://github.com/openai/retro as a POC to train the AI using the 'Brute' method.

*UPDATE 21/02/21 -'Brute' example includes live tracking graph of learning rate. ppo2 implementation is work in progress.
*UPDATE 28/02/21 - 'PPO2' model has been integrated and testing. Mlp is much faster to train than Cnn and has similar results. Additional tracking tools for training added. So far I cannot get PPO2 to comfortably outperform brute. Task added to experiment further with hyperparameters.

This repo includes some example .bk2 files in the folder for those interested to play back and observe the AI in action. I have uploaded the 'SFII610543' output from the training outputs folder from the Brute method as an example. 

<div align="center">
      <a href="https://youtu.be/ei-xojQE_hQ?t=42">
            <img src="https://youtu.be/ei-xojQE_hQ?t=42" width ="700" />
      </a>
</div>



## (Planned) additions & changes 
* [x] Implement and test other algorithms
* [x] Implement discretization so that special moves are part of the moveset
* [x] Track learning in game
* [ ] NEW: Experiment with different Hyperparameters
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


