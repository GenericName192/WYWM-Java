# WYWM-Java
A project to finish off the WYWM java course

Criteria

This assessment requires the student to create a project in Java that meets the
written requirements below. The project will be graded against its complexity, use
of OOP concepts and adherence to code conventions.
The student is required to develop the backend framework for a video game.
The project must have at least:
• Two types of territory that can house villagers (e.g., Kingdom,
Dynasty, etc.)
• Villager class that extends to three professions (e.g., Knight,
Blacksmith, Farmer).
• Three types of buildings that exist within each territory
The program must:
• Allow the user to create their Territory and then add buildings
and villagers.
• The user must be able to name their territory and villagers
• Allow the user to assign a villager to a building within the
territory
• Be able to print out the structure of the territory listing the name
of the territory, the buildings, and the villagers assigned to each
building.
Students are encouraged to explore the functionality and develop their own ideas
within the scope of the assessment. As an example, Resource management could
be implemented with buildings providing resources and the creation of units or
buildings costing more resources. The program could be turned into a turn-based
text game where each player can act for their territory.
The program can be as complex or as simple as you desire, provided it meets the
criteria listed within the Marking Criteria Matrix

Plan:

world:
function to generate a 2d list to server as a map
function to populate each title with 3 random resources
resources types - ore, forest, farmland, river, clay
each title must be able to contain a territory object so that the player can claim it and build on it

villager:
abstract class for villager: will have things like: name and age and 
classes for each type of job: Knight, farmer, miner, fisher, labourer, lumberjack, hunter
each class will have a generate resources function that will generate appropriate resources which can be used to claim territory and upgrade them:
farmer: food
lumberjack: wood
miner: ore
labourer: clay
hunter: food
fisher: food
knights: influence which will allow claiming of territory
each villager will belong to a building and a territory - territory type will change how many workers you can have and building will be what villager you can have
each turn you can hire up to 3 villagers

buildings:
building will only be buildable on an appropriate resource except barracks which can be built anywhere
each building can house 3 villagers
a fire function to get rid of villagers

territory:
3 types, captial - you start with can only have 1, city and village, captial can house 15 villagers, city - 10 villagers and village - 5, 
each territory will be on a world tile which contains 3 resources the territory can then house 4 buildings one for each of the resources and a barracks for knights
territory will cost influence to claim and once the tile has been claimed a free village will appear, each village will consume 1 food a turn with cities and the captial consuming 2
villages cost an assortment of materials to be upgraded into citys, 3 of wood, ore and clay.
demolish function to delete the buildings on a territory - need some logic to preverse villagers when you do this maybe unemployed list?

game logic:
split game into rounds, each action taking a round
round types: 
do nothing - when you need to gather more resources
survey land - tell you what resources are on a land, 
build building, 
interact with building - can hire, fire or change 3 villagers on a building, 
hold tournament - atleast 2 knights battle it out gives bonus influence, 
claim land - spend influence to claim a world tile