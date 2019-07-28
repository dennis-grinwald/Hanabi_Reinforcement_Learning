# NIP_Hanabi_2019
## Installation
In order to get everything up and running please first run the follwing commands:
```
sudo apt-get install g++       
sudo apt-get install cmake       
sudo apt-get install python-pip
pip -r install requirements.txt
```

Next compile the environemnt by entering the hanabi_learning_enviroment directory
```
cd hanabi_learning_environment
```

and run:
```
cmake .
make
```
## Training
Training the different algorithms is straight forward. Before running training though, make sure to set the PYTHONPATH environment variable to the root directory of this project. In order to do so, run:
```
export PYTHONPATH="Enter-root-directory-of-this-project-here"
```
### Training DQN Agent variations:
Enter the ```training/``` directory and run:
```
python -um train_rainbow_variants.py --base_dir="ENTER_PREFERRED_BASE_DIR" --gin_files="ENTER_PATH_TO_GIN_FILE_HERE"
```
The ```base_dir path``` specifies the directory where training checkpoints(neural network weights, logs etc.) are saved during training. In general we recommend placing it inside ```agents/trained_models/```.
The ```--gin_files``` flag specifies, which agent you want to train. Each DQN agent has it's own gin file. Find these in ```configs/```. For the specific explanations of the different DQN-agents, please refer to the paper.

### TODO: PPO, RULE-BASED, REINFORCE agent training explanation
## Evaluate Performances
In order to evaluate how the agents perform in self and adhoc play, run the jupyter-notebook:
```
cd evaluation
jupyter-notebook AdHocViz.ipynb
```
There you see how to run evaluation games with the trained agents and plot their performances.
## Interact with trained agents via Graphical User Interface
### TODO
## Further resources
Please find detailed explanations about the learning environment, encoding of objects, Framework specifics in the wiki of this REPO and theoretical background about this project in the paper.
