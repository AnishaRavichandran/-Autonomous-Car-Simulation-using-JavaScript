# -Autonomous-Car-Simulation-using-JavaScript
Developed a 2D traffic simulation using A* pathfinding for dynamic route optimization. Impact: Demonstrated efficient route planning and decision-making in autonomous systems under dynamic conditions.
**1.INTRODUCTION**

This project involves simulating a 2D traffic world with autonomous vehicles using the A* pathfinding algorithm. The goal is to model a set of vehicles moving on a grid-based street layout while avoiding obstacles (other cars). The vehicles calculate and adjust their paths dynamically in response to their environment. The project leverages the p5.js library for visualization and interaction.

•	Key Objectives:
           - Implement an A* pathfinding algorithm to navigate vehicles.
           - Simulate the dynamic interaction between vehicles and obstacles.
           - Create a visual representation of the vehicles' paths using p5.js.

**2.RESEARCH AND BACKGROUND**
Before starting the project, I researched several concepts that were crucial for its development:
- A* Pathfinding Algorithm: A popular and efficient algorithm used in navigation and pathfinding tasks. It uses a heuristic approach to find the shortest path between two points while considering obstacles.
 - Autonomous Vehicles and Traffic Simulation: Simulation of autonomous vehicles in traffic environments is crucial for testing various aspects like path optimization and collision avoidance.
- p5.js: A JavaScript library used for graphical rendering and animation. It allows the creation of interactive and visual applications like this one.
Problems Encountered:
•	Obstacle Management: 
Ensuring that vehicles recalculated their paths when encountering other cars in the grid was challenging. Initially, the cars would ignore the dynamic changes in their environment.
•	Pathfinding in a Dynamic Grid: 
As vehicles move, their presence in a grid cell changes the environment, so recalculating paths as cars moved was essential to avoid collisions.
•	Performance: 
The performance of the pathfinding algorithm needed to be optimized as more vehicles and grid cells were added.

**3.SPECIAL FEATURES OF THE ASSIGNMENT**
- Dynamic Path Calculation: The project dynamically recalculates paths in real-time as vehicles move, ensuring that the A* algorithm adapts to changes in the grid.
  - Visualization: The use of p5.js allows for real-time visual updates of the vehicle movements and paths. Vehicles are represented by emojis, and paths are drawn on the grid.
- Realistic Behavior: The vehicles do not simply jump to their destination; instead, they move one step at a time, making the simulation appear more realistic.
- Path Recalculation: If a vehicle encounters an obstacle (another vehicle), the algorithm recalculates its path, ensuring that the car avoids collisions.

**4.EXPERIMENTAL RESULTS**
To test the effectiveness of the simulation, several configurations of vehicles and grid sizes were tested. Results included:
- Grid Size and Vehicle Count: We observed how increasing the grid size and the number of vehicles affected performance. With more vehicles, the recalculation of paths became more computationally expensive and time consuming
- Pathfinding Accuracy: The A* algorithm consistently found the shortest path between start and end cells, even when vehicles encountered obstacles. However, performance dropped when vehicles were placed in highly congested grid areas.
- Collision Avoidance: The vehicles dynamically avoided each other by recalculating their paths when they encountered other cars, demonstrating the real-time adaptability of the simulation.

**5.FUNCTIONALITY NOT OBVIOUS**
Some features that might not be immediately apparent are:

-Sequential Vehicle Movement: The vehicles do not move simultaneously but sequentially, one at a time. This was implemented using a ‘moveCounter’ variable that increments with each frame to control the movement of each vehicle in turn.
  
- Dynamic Obstacle Handling: The grid includes random barriers (walls), and each vehicle dynamically recalculates its path when it encounters obstacles or other vehicles. The ‘resetScores()’ method ensures that each time a vehicle moves, the grid is recalibrated to account for new conditions.

**6.CONCLUSION**
This project successfully demonstrates the use of the A* algorithm in a dynamic traffic simulation, with vehicles that intelligently avoid obstacles and adjust their paths in real-time. The use of p5.js provides a clear and interactive way to visualize the simulation, making it an effective tool for understanding autonomous vehicle behavior in a controlled environment.



