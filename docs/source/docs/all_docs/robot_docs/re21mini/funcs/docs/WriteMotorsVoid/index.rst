WriteMotorsVoid
================================

WriteMotorsVoid function is used to set speed values to a robot from variables.

.. tabs::

    .. tab:: Python

        **Location and name:** RobocadSim.RE21mini.write_motors_void()

        **Inputs:**  
        
        \-\-\-

        **Output:**

        \-\-\-

        **Example:**

        .. code-block:: python
            :linenos:

            from robocadSimPy import RobocadSim


            robot = RobocadSim.RE21mini()
            robot.right_motor_speed = 10
            robot.left_motor_speed = -10
            robot.back_motor_speed = 0
            robot.write_motors_void()
        
        **Additional info:**
        
        - Range of speed is from -50 to 50

    .. tab:: C++

        **Location and name:** "RE21mini.h".RE21mini.WriteMotorsVoid()

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
                robot.rightMotorSpeed = 10;
                robot.leftMotorSpeed = -10;
                robot.backMotorSpeed = 0;
                robot.WriteMotorsVoid();
            }

        **Additional info:**
        
        - Range of speed is from -50 to 50

    .. tab:: C#

        **Location and name:** RobocadSim.RE21mini.WriteMotorsVoid()

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
                        robot.speedRight = 10;
                        robot.speedLeft = -10;
                        robot.speedBack = 0;
                        robot.WriteMotorsVoid();
                    }
                }
            }
        
        **Additional info:**
        
        - Range of speed is from -50 to 50