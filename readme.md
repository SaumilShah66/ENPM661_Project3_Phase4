This project is the simulation of the turtlebot on gazebo for the verification of the A* pathnplanning algorithm. This is a ROS workspace which will simulate the results.

## Dependencies

-- ROS kinetic
-- python 2.7
-- Gazebo
-- turtlebot package
-- numpy
-- matplotlib

## Run the planner

You can run the Planner with following commands.

```
cd project3_ws/src/planner/src/scripts
python Phase3.py --ShowExploration=1 --Start="[-4.5,-4.5,0]" --End
="[4.5,4.5,0]" --Weight=1.3
```
You can change the start and end positions. Add weight values to implement weighted A* algorithm.

## Run the Simulation

Once you are in workspace, build the package and add this package to the source with the following commands.

```
cd project3_ws
catkin_make
source devel/setup.bash
```

With the following command you can run the planner, find the path and move the turtlebot along that specified path to reach the final goal position.

```
roslaunch planner planner.launch start:="[-4,-3,120]" end:="[0,-3,0]" RPM:="[10,10] clearance:="0.05" 
```

This will take the turtlebot from initial position of (x,y,theta) = (-4,-3,120) to the final position of (x,y) = (0,-3). Video was recorded for this inputs and is recorded under the file name "turtlebot_1.mp4"

```
roslaunch planner planner.launch start:="[-4,-4,120]" end:="[4,2,0]" RPM:="[10,5]" clearance:="0.05"
```

This will take the turtlebot from initial position of (x,y,theta) = (-4,-4,120) to the final position of (x,y) = (4,2). Video was recorded for this inputs and is recorded under the file name "turtlebot_2.mp4"

```
roslaunch planner planner.launch start:="[4,3,0]" end:="[-2,-1,0]" RPM:="[5,10]" clearance:="0.05"
```

This will take the turtlebot from initial position of (x,y,theta) = (4,3,0) to the final position of (x,y) = (-2,-1). Video was recorded for this inputs and is recorded under the file name "turtlebot_3.mp4"
