ReadButtonsVoid
================================

ReadButtonsVoid function is used to write buttons values from a robot into variables.

.. tabs::

    .. tab:: Python

        **Location and name:** RobocadSim.RE21mini.read_buttons_void()

        **Inputs:**  

        \-\-\-

        **Output:**

        \-\-\-

        **Example:**

        .. code-block:: python
            :linenos:

            from robocadSimPy import RobocadSim


            robot = RobocadSim.RE21mini()
            robot.read_buttons_void()
            ems_button = robot.button_ems
            start_button = robot.button_start
            limit_button = robot.button_limit
        
        **Additional info:**
        
        \-\-\-

    .. tab:: C++

        **Location and name:** "RE21mini.h".RE21mini.ReadButtonsVoid()

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
                robot.ReadButtonsVoid();
                bool ems_button = robot.buttonEMS;
                bool start_button = robot.buttonStart;
                bool limit_button = robot.buttonLimit;
            }

        **Additional info:**
        
        \-\-\-

    .. tab:: C#

        **Location and name:** RobocadSim.RE21mini.ReadButtonsVoid()

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
                        robot.ReadButtonsVoid();
                        bool emsButton = robot.buttonEMS;
                        bool startButton = robot.buttonStart;
                        bool limitButton = robot.buttonLimit;
                    }
                }
            }
        
        **Additional info:**
        
        \-\-\-