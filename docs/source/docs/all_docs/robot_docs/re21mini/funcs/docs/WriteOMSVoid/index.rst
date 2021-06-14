WriteOMSVoid
================================

WriteOMSVoid function is used to set speed and angle values to a robot from variables.

.. tabs::

    .. tab:: Python

        **Location and name:** RobocadSim.RE21mini.write_oms_void()

        **Inputs:**  
        
        \-\-\-

        **Output:**

        \-\-\-

        **Example:**

        .. code-block:: python
            :linenos:

            from robocadSimPy import RobocadSim


            robot = RobocadSim.RE21mini()
            robot.lift_motor_speed = 10
            robot.angle_for_big = 1600
            robot.dir_for_small = 1400
            robot.write_oms_void()
        
        **Additional info:**
        
        - Range of speed is from -50 to 50
        - Range of angles for big servo motor is from 1490 to 1750
        - Range of values for small servo motor is from 1400 to 1600

    .. tab:: C++

        **Location and name:** "RE21mini.h".RE21mini.WriteOMSVoid()

        **Inputs:**  

        \-\-\-

        **Output:**

        \-\-\-

        **Example:**

        .. code-block:: c++
            :linenos:

            #include "RE21mini.h"
            #include <iostream>

            int main()
            {
                RE21mini robot;
                robot.liftMotorSpeed = 10;
                robot.bigServoAngle = 1600;
                robot.smallServoDir = 1400;
                robot.WriteOMSVoid();
            }

        **Additional info:**
        
        - Range of speed is from -50 to 50
        - Range of angles for big servo motor is from 1490 to 1750
        - Range of values for small servo motor is from 1400 to 1600

    .. tab:: C#

        **Location and name:** RobocadSim.RE21mini.WriteOMSVoid()

        **Inputs:**  

        \-\-\-

        **Output:**

        \-\-\-

        **Example:**

        .. code-block:: csharp
            :linenos:

            using System;
            using RobocadSim;

            namespace TestLib
            {
                class Program
                {
                    static void Main(string[] args)
                    {
                        RE21mini robot = new RE21mini();
                        robot.speedLift = 10;
                        robot.angleBig = 1600;
                        robot.dirSmall = 1400;
                        robot.WriteOMSVoid();
                    }
                }
            }
        
        **Additional info:**
        
        - Range of speed is from -50 to 50
        - Range of angles for big servo motor is from 1490 to 1750
        - Range of values for small servo motor is from 1400 to 1600