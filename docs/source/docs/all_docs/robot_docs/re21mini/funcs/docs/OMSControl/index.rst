OMS Control
================================

Use OMS control variables to set speeds, angles and directions to motors and servo motors.

.. tabs::

    .. tab:: Python

        **Location and name:** 
        
        - RobocadSim.RE21mini.lift_motor_speed
        - RobocadSim.RE21mini.angle_to_big
        - RobocadSim.RE21mini.dir_to_plates

        **Set:**  
        
        - *float* speed to lift motor
        - *float* angle to big servo 
        - *float* direction to small servo

        **Get:**

        \-\-\-

        **Example:**

        .. code-block:: python
            :linenos:

            from robocadSimPy import RobocadSim


            robot = RobocadSim.RE21mini()
            robot.connect()
            robot.lift_motor_speed = 10
            robot.angle_to_big = 1600
            robot.dir_to_plates = 1400
            robot.disconnect()
        
        **Additional info:**
        
        - Range of speed is from -50 to 50
        - Range of angles for big servo motor is from 1490 to 1750
        - Range of values for small servo motor is from 1400 to 1600

    .. tab:: C#

        **Location and name:** 

        - RobocadSim.RE21mini.liftMotorSpeed
        - RobocadSim.RE21mini.angleToBig
        - RobocadSim.RE21mini.dirToPlates

        **Set:**  

        - *float* speed to lift motor
        - *float* angle to big servo 
        - *float* direction to small servo

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
                        robot.liftMotorSpeed = 10;
                        robot.angleToBig = 1600;
                        robot.dirToPlates = 1400;
                        robot.Disconnect();
                    }
                }
            }
        
        **Additional info:**
        
        - Range of speed is from -50 to 50
        - Range of angles for big servo motor is from 1490 to 1750
        - Range of values for small servo motor is from 1400 to 1600