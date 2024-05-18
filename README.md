## Infrastructure Engineering 

Open tofu migration for UCLA Health cloud infrastructure

## OpenTofu Dir:

Open Tofu configuration examples with yaml and eng:

https://github.com/HenrikMoe/UCLAhealth-DevOps-AppEngineering/blob/master/OpenTofu.txt

### example dir



## ~Dep~ Terraform: 


Dep OpenTofu file within terraform package global var context: https://github.com/HenrikMoe/UCLAhealth-DevOps-AppEngineering/blob/master/globalVars.yaml

Needs docker-compose files for img and container cleaning

Needs iam privaleges/graph query privaleges + variable port routing

### example dir

```python

terraform/
|-- main.tf
|-- modules/
|   |-- web_server/
|   |   |-- main.tf
|   |   |-- variables.tf
|   |   |-- outputs.tf
|   |-- database/
|   |   |-- main.tf
|   |   |-- variables.tf
|   |   |-- outputs.tf
|-- scripts/
|   |-- deploy.sh
|-- .gitignore
|-- README.md
|-- variables.tf
|-- outputs.tf
|-- terraform.tfvars
|-- provider.tf

```

## ~Dep~ [PyMaze Critiques](./pymazeNotes.py)

This script contains notes and changes that get the PyMaze working from the gist: https://gist.github.com/super-phreak/e6a700d4807e6a7c83348cb469b3280a.

## Developer notes - Henrik Moe 2/8/24 - 

1) After successfully reaching the exit of the maze the maze does not acknowledge success and does not reset.

2) After consuming item noting happens

## Diganosis:  

1) if maze[player_pos[0]][player_pos[1]] == EXIT:# the first item returns the players icon, the second will always be exit.

2) no ideas for the item note

## Solutions: 

1) Hardcode the exit coordinates into the if comparison.

2) Write additional logic to store the exits' location. 
