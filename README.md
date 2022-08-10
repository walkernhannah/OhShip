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
1. When a ship is hit, its health (displayed by the stars under each ship) will decrease until hitting zero and turning the ship icon into an 'X' 

***

### Code
