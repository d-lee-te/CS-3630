# CS 3630 - Introduction to Robotics and Perception (Fall 2022)
I took CS 3630 in the Fall of 2022.

Lectured by Frank Dellaert.

## About
[Official course listing page](https://oscar.gatech.edu/bprod/bwckctlg.p_disp_course_detail?cat_term_in=201308&subj_code_in=CS&crse_numb_in=3630).

The class used Python for all projects. 

Different projects in this class also included different libraries:
- NumPy
- Plotly
- GTSAM (A sensor fusion library based on factor graphs from GT)
- Pandas
- PyTorch (and TorchVision)

### Course Curriculum
- Describe and explain what robots are and what they can do
- Describe mathematically the position and orientation of objects and how they move
- Develop a control architecture for a mobile robotic system
- Implement navigation and localization algorithms based on sensor fusion and environment representation
- Write moderately involved programs in Python and Java to control a robotic system
- Construct, program, and test the operation of a robotic system to perform a specified task

### Projects
Originally, each of these projects were given to us (the students) with wrapper files. 

These wrapper files included .ipynb files (interative python notebooks) that I would have loved to throw into this repo, but I don't believe I'm allowed to. 

As the next best description, I'll provide the steps to building the robots and pathing algorithms and a brief description the notebooks provide.

1. Trash sorting robot
    1. Model the world state by trash category and prior probabilities
    2. Create actions for sorting trash and their corresponding costs
    3. Represent the conditional probabilities of sensors
    4. Calculate likelihood of trash w/ and w/o sensors
    5. Incorporate the cost table with the perception data to reach a sorting decision

2. Vacuum cleaning robot
    1. Model the state space
    2. Create a motion model to model the uncertainty of transition probabilities for the robot moving between rooms
    3. Use this motion model to create a discrete/dynamic Bayes Net based on different sensor data
    4. Use ancestral sampling on the DBN based on an action sequence for a state sequence
    5. Use MPE to for any unknown variable values
    6. Use Markov Decision Processes to determine the robot's future state based on the current state based on reward values
    7. Test and output optimal policy using reward values, transitions, prior probabilities, and number of iterations

3. Pathing - Markov localization, particle filtering aka Monte Carlo localization, and pathing
    1. Using Markov localization to determine the probabilistic location of a warehouse robot
    2. Particle filtering as opposed to Markov localization to represent state as samples instead of continuous space
    3. Pathing based on particle filtering

4. Complex Pathing - Object detection w/ deep learning, path planning for a differential drive robot
    1. Build a simple CNN (convolutional neural net)
       - Define layers
       - Define hyper-parameters
       - Setup training
       - Test for accuracy
    2. Build an LeNet
    3. Tune hyperparameters and optimize performance of LeNet
    4. Classify characters on the image below
    5. Implement RRT (rapidly exploring random tree)
    6. Implement differential drive
    7. Implement object detection for RRT

  ![Hiragana Sheet](https://github.com/d-lee-te/CS-3630/blob/4cd5b622da4223d58d006a0816ceac23f81d81c2/hiraganasheet.png)
  
    

5. Localization and Mapping - Simultaneous localization using ICP (iterative closest point) and GTSAM, mapping (SLAM - simultaenous localization and mapping) on LIDAR (light detection and ranging) scans
    1. Mapping based on LIDAR point cloud visualizations (i.e. poses)
    2. Use ICP to align consecutive point clouds

6. Aerial Drone Pathing - Rapidly explore 3D RRT(random trees) for trajectory optimization and path planning for aerial drones
   1. Generate a random point function
   2. Find the parent node to the newly sampled node in the RRT function
   3. Grow the tree/implement RRT loop
      - Start RRT w/ start node
      - Sample a random node in configuration space
      - Find the nearest node to the newly sampled node
      - Find the node in the direction of the sampled node and add it to the tree
      - Repeat sampling and finding parent nodes until the distance of the latest node in the tree and the target node are less than a predetermined threshold
      - Return RRT and parent node list

### Debrief

This class was incredibly cool. 

There was so much information to absorb, I'm still not sure exactly how much I understand and don't, but having the opportunity to build these algorithms and these different NNs was exciting. 

And as if it wasn't enough that we had built neural net algorithms that would work with actual robots, we got to simulate a drone race for our last project. 

# Disclaimer
As most of the course content belongs to either the College or the Professors, I am transcribing my work and assignments to record the course.

As such, many assignments and files **may not include detailed descriptions or solutions**. This is done to avoid violations, avoid doxing myself and others, and any number of other reasons. If, for any reason, the full repo must be accessed, all assignments, descriptions, solutions, and class files are stored in a private version of the repo (so contact me. If you're a current student, don't bother since I won't give you access and it wouldn't help you anyway xp).

If possible, portions of the class will be linked to a separate readme explaining more about the linked assignment/solution/description/other.

If there exist any honorcode violations or any problems/solutions are *too* in-depth, please contact me. The intention of each public class repo is to record my experience and assignments of each class taken.

