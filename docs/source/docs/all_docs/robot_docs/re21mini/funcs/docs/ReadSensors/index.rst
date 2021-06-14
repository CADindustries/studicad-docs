ReadSensors
================================

ReadSensors function is used to get sensors values from a robot.

.. tabs::

    .. tab:: Python

        **Location and name:** RobocadSim.RE21mini.read_sensors()

        **Inputs:**  

        \-\-\-

        **Output:**

        *float map* that includes:

        - Right US value
        - Left US value
        - Right IR value
        - Left IR value
        - Gyroscope value

        **Example:**

        .. code-block:: python
            :linenos:

            from robocadSimPy import RobocadSim


            robot = RobocadSim.RE21mini()
            right_us, left_us, right_ir, left_ir, gyro = robot.read_sensors()
        
        **Additional info:**
        
        \-\-\-

    .. tab:: C++

        **Location and name:** "RE21mini.h".RE21mini.ReadSensors()

        **Inputs:**  

        \-\-\-

        **Output:**

        *float\** that includes:

        - Right US value
        - Left US value
        - Right IR value
        - Left IR value
        - Gyroscope value

        **Example:**

        .. code-block:: c++
            :linenos:

            #include "RE21mini.h"
            #include <iostream>

            int main()
            {
                RE21mini robot;
                float* all_sens = robot.ReadSensors();
                float right_us = all_sens[0];
                float left_us = all_sens[1];
                float right_ir = all_sens[2];
                float left_ir = all_sens[3];
                float gyro = all_sens[4];
            }

        **Additional info:**
        
        \-\-\-

    .. tab:: C#

        **Location and name:** RobocadSim.RE21mini.ReadSensors()

        **Inputs:**  

        \-\-\-

        **Output:**

        *float[]* that includes:

        - Right US value
        - Left US value
        - Right IR value
        - Left IR value
        - Gyroscope value

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
                        float[] allSens = robot.ReadSensors();
                        float rightUS = allSens[0];
                        float leftUS = allSens[1];
                        float rightIR = allSens[2];
                        float leftIR = allSens[3];
                        float gyro = allSens[4];
                    }
                }
            }
        
        **Additional info:**
        
        \-\-\- 