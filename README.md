# ADDED FUNCTIONALITY FROM THIS REPO
With the update provided in this repo moveit is started with integration of the kinect sensor. This allows for collision avoidance of the arms (and every movement that is planned with moveit).


AMIGO MoveIt config
===================
This package keeps the AMIGO configuration files for the ROS MoveIt stack.

For a nice demonstration, do this:

    roscore
    
    astart
    
    rviz-amigo
    
    roslaunch amigo_moveit_config demo.launch

Then, click on the rviz that opened last on 'planning' then on 'update' then on 'Plan' then on 'Execute'. This last command will move amigo (see the other rviz for the fast_simulator effect).

To test stuff in practice:

    roscore

    astart

    amiddle (does not yet start the manipulation stuff)

    roslaunch amigo_bringup manipulation.launch

    amigo-console

    In the console: 
    amigo.leftArm.send_goal(0.5,0.2,0.8,0,0,0,pre_grasp=True)
