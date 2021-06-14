Encoder Indicator
================================

Use encoder indicator variables to get motors' encoders' values.

.. tabs::

    .. tab:: Python

        **Location and name:** 
        
        - RobocadSim.RE21mini.right_motor_enc 
        - RobocadSim.RE21mini.left_motor_enc 
        - RobocadSim.RE21mini.back_motor_enc 
        - RobocadSim.RE21mini.lift_motor_enc 

        **Set:**  
        
        \-\-\-

        **Get:**

        - *float* right motor' encoder' value
        - *float* right motor' encoder' value
        - *float* right motor' encoder' value
        - *float* right motor' encoder' value

        **Example:**

        .. code-block:: python
            :linenos:

            from robocadSimPy import RobocadSim


            robot = RobocadSim.RE21mini()
            robot.connect()
            encoders = [0] * 4
            encoders[0] = robot.right_motor_enc
            encoders[1] = robot.left_motor_enc
            encoders[2] = robot.back_motor_enc
            encoders[3] = robot.lift_motor_enc
            robot.disconnect()
        
        **Additional info:**
        
        - You should use Transfunction with encoders for a more convenient representation of values

    .. tab:: C#

        **Location and name:** 

        - RobocadSim.RE21mini.rightMotorEnc
        - RobocadSim.RE21mini.leftMotorEnc
        - RobocadSim.RE21mini.backMotorEnc
        - RobocadSim.RE21mini.liftMotorEnc

        **Set:**  

        \-\-\-

        **Get:**

        - *float* right motor' encoder' value
        - *float* right motor' encoder' value
        - *float* right motor' encoder' value
        - *float* right motor' encoder' value

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
                        float[] encoders = new float[4];
                        encoders[0] = robot.rightMotorEnc;
                        encoders[1] = robot.leftMotorEnc;
                        encoders[2] = robot.backMotorEnc;
                        encoders[3] = robot.liftMotorEnc;
                        robot.Disconnect();
                    }
                }
            }
        
        **Additional info:**
        
        - You should use Transfunction with encoders for a more convenient representation of values