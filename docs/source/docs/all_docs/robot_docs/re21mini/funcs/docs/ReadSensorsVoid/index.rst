ReadSensorsVoid
================================

ReadSensorsVoid function is used to write sensors values from a robot into variables.

.. tabs::

    .. tab:: Python

        **Location and name:** RobocadSim.RE21mini.read_sensors_void()

        **Inputs:**  

        \-\-\-

        **Output:**

        \-\-\-

        **Example:**

        .. code-block:: python
            :linenos:

            from robocadSimPy import RobocadSim


            robot = RobocadSim.RE21mini()
            robot.read_sensors_void()
            right_us = robot.right_us
            left_us = robot.left_us
            right_ir = robot.right_ir
            left_ir = robot.left_ir
            gyro = robot.navX
        
        **Additional info:**
        
        \-\-\-

    .. tab:: C++

        **Location and name:** "RE21mini.h".RE21mini.ReadSensorsVoid()

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
                robot.ReadSensorsVoid();
                float right_us = robot.rightUS;
                float left_us = robot.leftUS;
                float right_ir = robot.rightIR;
                float left_ir = robot.leftIR;
                float gyro = robot.navX;
            }

        **Additional info:**
        
        \-\-\-

    .. tab:: C#

        **Location and name:** RobocadSim.RE21mini.ReadSensorsVoid()

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
                        robot.ReadSensorsVoid();
                        float rightUS = robot.rightUS;
                        float leftUS = robot.leftUS;
                        float rightIR = robot.rightIR;
                        float leftIR = robot.leftIR;
                        float gyro = robot.navX;
                    }
                }
            }
        
        **Additional info:**
        
        \-\-\- 