WriteOMS
================================

WriteOMS function is used to set speed and angle values to a robot.

.. tabs::

    .. tab:: Python

        **Location and name:** RobocadSim.RE21mini.write_oms()

        **Inputs:**  
        
        - *float* speed to lift motor
        - *float* angle to big servo motor
        - *float* direction of small servo motor

        **Output:**

        \-\-\-

        **Example:**

        .. code-block:: python
            :linenos:

            from robocadSimPy import RobocadSim


            robot = RobocadSim.RE21mini()
            robot.write_oms(10, 1600, 1400)
        
        **Additional info:**
        
        - Range of speed is from -50 to 50
        - Range of angles for big servo motor is from 1490 to 1750
        - Range of values for small servo motor is from 1400 to 1600

    .. tab:: C++

        **Location and name:** "RE21mini.h".RE21mini.WriteOMS()

        **Inputs:**  

        - *float* speed to lift motor
        - *float* angle to big servo motor
        - *float* direction of small servo motor

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
                robot.WriteOMS(10, 1600, 1400);
            }

        **Additional info:**
        
        - Range of speed is from -50 to 50
        - Range of angles for big servo motor is from 1490 to 1750
        - Range of values for small servo motor is from 1400 to 1600

    .. tab:: C#

        **Location and name:** RobocadSim.RE21mini.WriteOMS()

        **Inputs:**  

        - *float* speed to lift motor
        - *float* angle to big servo motor
        - *float* direction of small servo motor

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
                        robot.WriteOMS(10, 1600, 1400);
                    }
                }
            }
        
        **Additional info:**
        
        - Range of speed is from -50 to 50
        - Range of angles for big servo motor is from 1490 to 1750
        - Range of values for small servo motor is from 1400 to 1600