# OhShip

Eclipse IDE for Java Developers 2021-06, JDK 16.0.2_7


## Desc: 
Battleship game that fires cannons to random coordinates in hopes of sinking a ship. Measures, such as remaining ships or individual health, are calculated and displayed to both the game panel and a separate 'Fleet Report' window. Required applying knowledge of loops, action listeners, packages, encapsulation, variable passing, random number generation, inheritance, scope, methods, and GUI design learned over the course of the semester.
(This was the final assignment, or Lab Three in MIS 4320 at Baylor, F2021)


## Application:

Upon running the program, you should see a blue window of 3 top-aligned buttons, 10 randomly scattered ships, and 2 aggregated descriptors - set to '0' and '10' respectively.


### Buttons
1. Fleet Report - Generates a list of each ship's name, location, hits, and health into a separate, smaller window. Additionally, the bottom banner of the report includes health stats on the fleet as a whole - here, you will see the minimum, maximum, and average health of all 10. 
2. Reset Game - Clears any running totals, wipes the board/report, restores default values, and re-randomizes ship locations. 
3. Fire Cannons - Fires volleys that result in either a hit to a ship or a miss into the water. 

### Fields
1. Total Volleys = # of times the 'Fire Cannons' button has been clicked 
2. Ships Left = # of ships remaining on the board (where individual health has not hit 0)
3. Location (x, y) = coordinates of each ship's location 
4. Hits = # of hits each ship has taken 
5. Health = total remaining health for each ship, where 'SUNK' is 0
6. Min = minimum health of fleet
7. Max = maximum health of fleet
8. Avg = average health of fleet

### Other
1. When a ship is hit, its health (displayed by the stars under each ship) will decrease until hitting zero and turning the ship icon from the ship .png into an 'X' 

***

## Code
Before running, make sure: 
1. That all packages are imported (lines 1-28)
2. That the following FOUR files are downloaded and accessible: cannon.wav, sinking.wav, softclick.wav, shippy.png
3. That the display font, 'Caribbean', is downloaded


### Overview
There are four general methods that comprise the main application function, LabThree(). 
1. load() = generates the fleet report, game panel, and button panel + randomizes individual locations of each ship + reads and stores sound files so they can be played
2. resetVariables() = clears the game panel & fleet report, resets all numbers, and generates a new array of ships to be placed 
3. populateReport() = makes the secondary 'Fleet Report' window visible, as well as reruns to display up-to-date stats of each ship 
4. end() = similar to resetVariables, it resets the game panel & fleet report, but occurs either once the game has ended or upon pressing the 'Reset' button 


## Variables 

### Java Containers 
_JPanels/JFrames_
- gamePanel = window that holds the game, ships, and buttons
- jp = area attached to the top of the game panel that holds the three buttons 
- jf = window that holds the fleetsummary 

_JTextAreas/JLabels_
- fleetsummary 
- l = banner attached to the bottom of the game panel that displays 'totalvolleys' and 'shipsleft' in the game 
- top(toplabel) = label that holds String 'toplabel' which displays the top header of the Fleet Report 
- bottom(bottomlabel) = label that holds String 'bottomlabel' which displays aggregations such as 'fleetmin', 'fleetmax', 'fleetavg' on the bottom of the Fleet Report

_JButtons & Their ActionListeners_
- _fire_ = sends a volley of cannons to random positions 
- _reset_ = clears the game
- _fleetreport_ = generates a fleet report 
- _replay_ = resets the game 

### Objects 
- _Ship (class)_ = creates a ship object, assigns and displays variables for each ship like health, name, location, and hits
- _PirateShip (class)_ = extends Ship to display the ship icon, lives/health, and name 
- _ship_ = instantiation of each PirateShip (like an object placeholder for the 10 generated) 
- _ships (array)_ = holds all 10 ships of fleet + allows for fleet to have numeric limit + instatiates each ship object and allows for reference/aggregation of indiividual variables assigned 

### Integers
- _totalvolleys_ = _refer to Fields section above_ 
- _volleys_ = number of (clicks) per 'fire' 
- _shipsleft_ = _refer to Fields section above_ 
- _shipsdown_ = _refer to Fields section above_ 
- _fleetmax_ = _refer to Fields section above_ 
- _fleetmin_ = _refer to Fields section above_ 

- _health_ = individual ship health
- _hitstaken_ = hits taken per 'fire' by an individual ship 
- _totalhitstaken_ = total hits taken by an individual ship in a game 

### Doubles
- _totalhealth_ = _refer to Fields section above_ 
- _fleetavg_ = _refer to Fields section above_ 

### Other
- _floating_ = boolean variable that 
- _clip, clap, clop_ = sound variables holding the sound clips that are played in different ActionListeners

***

## Logic and Loops





