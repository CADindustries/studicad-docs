WriteMotors
================================

WriteMotors function is used to set speed values to a robot.

.. tabs::

    .. tab:: Python

        **Location and name:** RobocadSim.RE21mini.write_motors()

        **Inputs:**  
        
        - *float* speed to right motor
        - *float* speed to left motor
        - *float* speed to back motor

        **Output:**

        \-\-\-

        **Example:**

        .. code-block:: python
            :linenos:

            from robocadSimPy import RobocadSim


            robot = RobocadSim.RE21mini()
            robot.write_motors(10, -10, 0)
        
        **Additional info:**
        
        - Range of speed is from -50 to 50

    .. tab:: C++

        **Location and name:** "RE21mini.h".RE21mini.WriteMotors()

        **Inputs:**  

        - *float* speed to right motor
        - *float* speed to left motor
        - *float* speed to back motor

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
                robot.WriteMotors(10, -10, 0);
            }

        **Additional info:**
        
        - Range of speed is from -50 to 50

    .. tab:: C#

        **Location and name:** RobocadSim.RE21mini.WriteMotors()

        **Inputs:**  

        - *float* speed to right motor
        - *float* speed to left motor
        - *float* speed to back motor

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
                        robot.WriteMotors(10, -10, 0);
                    }
                }
            }
        
        **Additional info:**
        
        - Range of speed is from -50 to 50