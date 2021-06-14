Button Indicator
================================

Use button indicator variables to get buttons states.

.. tabs::

    .. tab:: Python

        **Location and name:** 
        
        - RobocadSim.RE21mini.button_ems  
        - RobocadSim.RE21mini.button_start  
        - RobocadSim.RE21mini.button_limit  

        **Set:**  
        
        \-\-\-

        **Get:**

        - *bool* EMS button state
        - *bool* Start button state
        - *bool* Limit button state

        **Example:**

        .. code-block:: python
            :linenos:

            from robocadSimPy import RobocadSim


            robot = RobocadSim.RE21mini()
            robot.connect()
            buttons = [0] * 3
            buttons[0] = robot.button_ems
            buttons[1] = robot.button_start
            buttons[2] = robot.button_limit
            robot.disconnect()
        
        **Additional info:**
        
        \-\-\-

    .. tab:: C#

        **Location and name:** 

        - RobocadSim.RE21mini.buttonEMS
        - RobocadSim.RE21mini.buttonStart
        - RobocadSim.RE21mini.buttonLimit

        **Set:**  

        \-\-\-

        **Get:**

        - *bool* EMS button state
        - *bool* Start button state
        - *bool* Limit button state

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
                        robot.Connect();
                        bool[] buttons = new bool[3];
                        buttons[0] = robot.buttonEMS;
                        buttons[1] = robot.buttonStart;
                        buttons[2] = robot.buttonLimit;
                        robot.Disconnect();
                    }
                }
            }
        
        **Additional info:**
        
        \-\-\-