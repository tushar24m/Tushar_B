# productivity_analysis
Problem Statement
The purpose of this program is to analyze the productivity of a truck and shovel system used in mining, excavation or construction operations. The analysis involves calculating various aspects of the truck cycle, including loading, hauling, dumping, and returning times, in order to optimize the operation's productivity and cost efficiency.


Description
The truck cycle consists of several elements:
  •	Loading Time: The time taken for the shovel to load material into the truck.
  •	Hauling Time: The time taken for the truck to travel from the loading site to the dump site.
  •	Dumping Time: The time taken for the truck to unload its content at the dump site.
  •	Returning Time: The time taken for the truck to return from the dump site to the loading site.

The main goal is to balance the capacities of the hauling units (trucks) with the shovel's bucket size and production capability. This balance ensures maximum loading efficiency and cost reduction.

The program performs the following steps to analyze the productivity: 
1. Calculate the cost of the operation based on the shovel and truck costs, as well as the calculated production rate.
  Case 1: Balanced Number of Bucket Loads
  When the number of bucket loads is rounded down to an integer lower than the balanced number of loads:
    •	Truck Load = Number of bucket loads × Bucket volume
  Case 2: Imbalanced Number of Bucket Loads
  When the number of bucket loads is rounded up to an integer higher than the balanced number of loads:
    •	Truck Load = Truck capacity
  Hauling Time
    •	Calculate hauling time = Haul distance / Haul speed
  Returning Time
    •	Calculate returning time = Return distance / Return travel speed
  Number of Trucks Required
2.Calculate the number of trucks required based on truck cycle time and loading time:
  Balanced Number of Trucks = Truck cycle time / Truck loading time (rounded down)

  If loading time is less than cycle time, then:
    •	Number of trucks = Balanced Number of Trucks
    •Production rate in loose cubic yards per hour = Truck load (in loading time) × Number of trucks × 60 / Truck cycle time (in minutes) × Efficiency
  If loading time is greater than cycle time, then:
    •	Number of trucks = Balanced Number of Trucks + 1
    •	Production rate in loose cubic yards per hour = Truck load (in loading time) × Number of trucks × 60 / Truck cycle time (in minutes) × Efficiency

    
GUI Interface Comments:
The GUI is implemented using the tkinter library, providing an interactive user interface. Input fields (Label and Entry widgets) are provided for users to input various parameters. A "Calculate" button is included to trigger the calculation process and display results. When the "Calculate" button is clicked, the display_results function is called. The calculation results are displayed in a separate frame (results_frame) below the input fields.





