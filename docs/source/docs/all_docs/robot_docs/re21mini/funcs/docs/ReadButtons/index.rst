ReadButtons
================================

ReadButtons function is used to get buttons values from a robot.

.. tabs::

    .. tab:: Python

        **Location and name:** RobocadSim.RE21mini.read_buttons()

        **Inputs:**  

        \-\-\-

        **Output:**

        *bool map* that includes:

        - EMS button value
        - Start button value
        - Limit button value

        **Example:**

        .. code-block:: python
            :linenos:

            from robocadSimPy import RobocadSim


            robot = RobocadSim.RE21mini()
            ems_button, start_button, limit_button = robot.read_buttons()
        
        **Additional info:**
        
        \-\-\-

    .. tab:: C++

        **Location and name:** "RE21mini.h".RE21mini.ReadButtons()

        **Inputs:**  

        \-\-\-

        **Output:**

        *bool\** that includes:

        - EMS button value
        - Start button value
        - Limit button value

        **Example:**

        .. code-block:: c++
            :linenos:

            #include "RE21mini.h"
            #include <iostream>

            int main()
            {
                RE21mini robot;
                bool* all_buttons = robot.ReadButtons();
                bool ems_button = all_buttons[0];
                bool start_button = all_buttons[1];
                bool limit_button = all_buttons[2];
            }

        **Additional info:**
        
        \-\-\-

    .. tab:: C#

        **Location and name:** RobocadSim.RE21mini.ReadButtons()

        **Inputs:**  

        \-\-\-

        **Output:**

        *bool[]* that includes:

        - EMS button value
        - Start button value
        - Limit button value

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
                        bool[] allButtons = robot.ReadButtons();
                        bool emsButton = allButtons[0];
                        bool startButton = allButtons[1];
                        bool limitButton = allButtons[2];
                    }
                }
            }
        
        **Additional info:**
        
        \-\-\-