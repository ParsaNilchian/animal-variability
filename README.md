1. DATA

The data for this study was provided to us by Alme et al., 2014 (PNAS) and permission was given to us to perform the analyses found in the code.
All data files can be found in the DATA folder. Each file contains the behavioral and electrophysiological data of a single animal in a single session. 
For example, the file 17769_novel6begin2.h5 contains the data collected for animal 17769 in room 6 in the second session (see methods for details on experimental design).
The data of animals 17724 and and 17490 was not used because these animals were not run in the repetitions of novel room N1 and N6 at the ends of the days. 


2. Implementation instructions

The folder contains 3 files:  
- a main file which processes the data and runs the majority of the analyses.
- a revision file which performs most of the analyses requested in the review process.
- a functions file which contains the functions used in the main and revision files.

The first file that should be run is main code. The main code preprocesses the data, computes rate maps, extracts the behavioral data, and creates some of the 
figures shown in the paper. 

IMPORTANT note 1: The code creates and saves files in the same directory as itself. The first 4 cells (including PART 2: organizing the data)
must be run for each animal individually first - this saves the rate maps, behavioral data, and thresholds for each animal. 
To do this the animal-flag in the second cell (executing the data analysis) must be changed to the correct animal ID (17769, 17894, 18023, 18237, 19251). 
All the following cells must be implemented afterwards and implement the actual analyses/statistics/figures.

IMPORTANT note 2: The code creates and saves other files throughout the data. These files are then reimported to run the anlyses. For example, in Part 4: plotting 
the data the most important file that is created is rate_map_allsession_final_animalID for each animal. This file is then reimported to create the figures for 
each animal individually. Here again, the code is implemented consecutively for each animal and the person running the code must manually enter the animal ID and cell number for each animal. 
