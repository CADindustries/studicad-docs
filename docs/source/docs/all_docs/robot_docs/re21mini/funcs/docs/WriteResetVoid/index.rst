WriteResetVoid
================================

WriteResetVoid function is used to set reset values to a robot from variables.

.. tabs::

    .. tab:: Python

        **Location and name:** RobocadSim.RE21mini.write_reset_void()

        **Inputs:**  
        
        \-\-\-

        **Output:**

        \-\-\-

        **Example:**

        .. code-block:: python
            :linenos:

            from robocadSimPy import RobocadSim


            robot = RobocadSim.RE21mini()
            robot.reset_right_enc = True
            robot.reset_left_enc = True
            robot.reset_back_enc = True
            robot.reset_lift_enc = False
            robot.reset_gyro = False
            robot.write_reset_void()
        
        **Additional info:**
        
        - You should write Your own gyro reset (cause my doesn't work well :) )

    .. tab:: C++

        **Location and name:** "RE21mini.h".RE21mini.WriteResetVoid()

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
                robot.resetRightEnc = true;
                robot.resetLeftEnc = true;
                robot.resetBackEnc = true;
                robot.resetLiftEnc = false;
                robot.resetGyro = false;
                robot.WriteResetVoid();
            }

        **Additional info:**
        
        - You should write Your own gyro reset (cause my doesn't work well :) )

    .. tab:: C#

        **Location and name:** RobocadSim.RE21mini.WriteResetVoid()

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
                        robot.resetEncRight = true;
                        robot.resetEncLeft = true;
                        robot.resetEncBack = true;
                        robot.resetEncLift = false;
                        robot.resetGyro = false;
                        robot.WriteResetVoid();
                    }
                }
            }
        
        **Additional info:**
        
        - You should write Your own gyro reset (cause my doesn't work well :) )