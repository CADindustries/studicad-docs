WriteReset
================================

WriteReset function is used to set reset values to a robot.

.. tabs::

    .. tab:: Python

        **Location and name:** RobocadSim.RE21mini.write_reset()

        **Inputs:**  
        
        - *bool* reset right motor encoder
        - *bool* reset left motor encoder
        - *bool* reset back motor encoder
        - *bool* reset lift motor encoder
        - *bool* reset gyroscope

        **Output:**

        \-\-\-

        **Example:**

        .. code-block:: python
            :linenos:

            from robocadSimPy import RobocadSim


            robot = RobocadSim.RE21mini()
            robot.write_reset(True, True, True, False, False)
        
        **Additional info:**
        
        - You should write Your own gyro reset (cause my doesn't work well :) )

    .. tab:: C++

        **Location and name:** "RE21mini.h".RE21mini.WriteReset()

        **Inputs:**  

        - *bool* reset right motor encoder
        - *bool* reset left motor encoder
        - *bool* reset back motor encoder
        - *bool* reset lift motor encoder
        - *bool* reset gyroscope

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
                robot.WriteReset(true, true, true, false, false);
            }

        **Additional info:**
        
        - You should write Your own gyro reset (cause my doesn't work well :) )

    .. tab:: C#

        **Location and name:** RobocadSim.RE21mini.WriteReset()

        **Inputs:**  

        - *bool* reset right motor encoder
        - *bool* reset left motor encoder
        - *bool* reset back motor encoder
        - *bool* reset lift motor encoder
        - *bool* reset gyroscope

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
                        robot.WriteReset(true, true, true, false, false);
                    }
                }
            }
        
        **Additional info:**
        
        - You should write Your own gyro reset (cause my doesn't work well :) )