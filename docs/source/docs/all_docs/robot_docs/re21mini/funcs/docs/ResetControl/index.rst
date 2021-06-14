Reset Control
================================

Use reset control variables to reset to motors' encoders.

.. tabs::

    .. tab:: Python

        **Location and name:** 
        
        - RobocadSim.RE21mini.reset_right_motor_enc
        - RobocadSim.RE21mini.reset_left_motor_enc
        - RobocadSim.RE21mini.reset_back_motor_enc
        - RobocadSim.RE21mini.reset_lift_motor_enc
        - RobocadSim.RE21mini.reset_gyro

        **Set:**  
        
        - *bool* reset right motor encoder
        - *bool* reset left motor encoder
        - *bool* reset back motor encoder
        - *bool* reset lift motor encoder
        - *bool* reset gyroscope

        **Get:**

        \-\-\-

        **Example:**

        .. code-block:: python
            :linenos:

            from robocadSimPy import RobocadSim


            robot = RobocadSim.RE21mini()
            robot.connect()
            robot.reset_right_motor_enc = True
            robot.reset_left_motor_enc = True
            robot.reset_back_motor_enc = True
            robot.reset_lift_motor_enc = True
            robot.reset_gyro = False
            robot.disconnect()
        
        **Additional info:**
        
        - You should write Your own gyro reset (cause my doesn't work well :) )

    .. tab:: C#

        **Location and name:** 

        - RobocadSim.RE21mini.resetRightMotorEnc
        - RobocadSim.RE21mini.resetLeftMotorEnc
        - RobocadSim.RE21mini.resetBackMotorEnc
        - RobocadSim.RE21mini.resetLiftMotorEnc
        - RobocadSim.RE21mini.resetGyro

        **Set:**  

        - *bool* reset right motor encoder
        - *bool* reset left motor encoder
        - *bool* reset back motor encoder
        - *bool* reset lift motor encoder
        - *bool* reset gyroscope

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
                        robot.resetRightMotorEnc = true;
                        robot.resetLeftMotorEnc = true;
                        robot.resetBackMotorEnc = true;
                        robot.resetLiftMotorEnc = true;
                        robot.resetGyro = false;
                        robot.Disconnect();
                    }
                }
            }
        
        **Additional info:**
        
        - You should write Your own gyro reset (cause my doesn't work well :) )