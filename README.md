# Ecosystem Simulation, Foxes and Rabbits
Contributers: Vani Banerjee and Alex Yang
## Overview
This is a simple ecosystem simulation, involving predator (Foxes) and prey (Rabbits).
The demo is live at https://banerv.github.io/ecosystem.
- click on a rabbit/fox to view its datafields.
- click the rabbit/fox icon at the bottom right corner to spawn a new rabbit/fox
- each simulation is saved locally, so progress is never lost
## Recent Updates
- added nametags above all animals
- added an average speed stat for bunnies and for foxes
- added progress saving
## Environment
* Javascript ES13
* CSS3
* HTML5
## Process
The simulation starts off with 80 bunnies, 4 foxes, 200 carrots, and 2 (permanent) pools of water. Each bunny and fox has 3 desires, each of which is represented by an integer:
- Hunger: Hunger increases direcly proportionally with the speed gene value. (Higher speed -> Get hungry faster)
- Thirst: Thrist increases constantly for all animals.
- Reprodudctive urge: Reproductive urge increases constantly for all animals.
At any given moment, the animal will follow their greatest urge. If they're hungry, they'll hunt for carrots/bunnies. If they're thirsty, they'll head to the nearest pool of water. If they have reproductive urge, they'll search for a mate.

Other important datafields:
- Maturity: The animals can only reproduce if they're old enough.
- Speed: This is an inheritable trait, randomly initialied at .7 - 1.3 for bunnies, and 1.2 - 1.8 for foxes. When animals reproduce, the offspring has speed between .7 - 1.3 * avg(speed of parents).
## Observations
Interestingly enough, if you let the simulation play for 5 minutes or so, there's two possible outcomes.
1. You're left with a ton of really fast bunnies. Foxes eat slow bunnies -> Only fast bunnies left -> Foxes can't catch the fast bunnies -> Foxes die of starvation -> Bunnies compete with each other for food -> Faster bunnies get more food.
![Diagram 1](/images/Ecosystem1.jpg?raw=true)
2. The foxes prevail, and the bunnies go extinct. Then, the foxes go extinct since they have no food source.
![Diagram 2](/images/Ecosystem2.jpg?raw=true)
