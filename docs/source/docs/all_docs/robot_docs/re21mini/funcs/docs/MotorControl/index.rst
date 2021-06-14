Motor Control
================================

Use motor control variables to set speeds to motors.

.. tabs::

    .. tab:: Python

        **Location and name:** 
        
        - RobocadSim.RE21mini.right_motor_speed
        - RobocadSim.RE21mini.left_motor_speed
        - RobocadSim.RE21mini.back_motor_speed

        **Set:**  
        
        - *float* speed to right motor
        - *float* speed to left motor
        - *float* speed to back motor

        **Get:**

        \-\-\-

        **Example:**

        .. code-block:: python
            :linenos:

            from robocadSimPy import RobocadSim


            robot = RobocadSim.RE21mini()
            robot.connect()
            robot.right_motor_speed = 10
            robot.left_motor_speed = -10
            robot.back_motor_speed = 0
            robot.disconnect()
        
        **Additional info:**
        
        - Range of speed is from -50 to 50

    .. tab:: C#

        **Location and name:** 

        - RobocadSim.RE21mini.rightMotorSpeed
        - RobocadSim.RE21mini.leftMotorSpeed
        - RobocadSim.RE21mini.backMotorSpeed

        **Set:**  

        - *float* speed to right motor
        - *float* speed to left motor
        - *float* speed to back motor

        **Get:**

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
                        robot.Connect();
                        robot.rightMotorSpeed = 10;
                        robot.leftMotorSpeed = -10;
                        robot.backMotorSpeed = 0;
                        robot.Disconnect();
                    }
                }
            }
        
        **Additional info:**
        
        - Range of speed is from -50 to 50