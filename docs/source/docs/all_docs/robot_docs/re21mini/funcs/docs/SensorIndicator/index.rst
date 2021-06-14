Sensor Indicator
================================

Use sensor indicator variables to get sensors values.

.. tabs::

    .. tab:: Python

        **Location and name:** 
        
        - RobocadSim.RE21mini.right_us  
        - RobocadSim.RE21mini.left_us  
        - RobocadSim.RE21mini.right_ir  
        - RobocadSim.RE21mini.left_ir  
        - RobocadSim.RE21mini.gyro   

        **Set:**  
        
        \-\-\-

        **Get:**

        - *float* right ultrasonic sensor value
        - *float* left ultrasonic sensor value
        - *float* right infrared sensor value
        - *float* left infrared sensor value
        - *float* gyro value

        **Example:**

        .. code-block:: python
            :linenos:

            from robocadSimPy import RobocadSim


            robot = RobocadSim.RE21mini()
            robot.connect()
            sensors = [0] * 5
            sensors[0] = robot.right_us
            sensors[1] = robot.left_us
            sensors[2] = robot.right_ir
            sensors[3] = robot.left_ir
            sensors[4] = robot.gyro
            robot.disconnect()
        
        **Additional info:**
        
        \-\-\-

    .. tab:: C#

        **Location and name:** 

        - RobocadSim.RE21mini.rightUS
        - RobocadSim.RE21mini.leftUS
        - RobocadSim.RE21mini.rightIR
        - RobocadSim.RE21mini.leftIR
        - RobocadSim.RE21mini.gyro

        **Set:**  

        \-\-\-

        **Get:**

        - *float* right ultrasonic sensor value
        - *float* left ultrasonic sensor value
        - *float* right infrared sensor value
        - *float* left infrared sensor value
        - *float* gyro value

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
                        float[] sensors = new float[5];
                        sensors[0] = robot.rightUS;
                        sensors[1] = robot.leftUS;
                        sensors[2] = robot.rightIR;
                        sensors[3] = robot.leftIR;
                        sensors[4] = robot.gyro;
                        robot.Disconnect();
                    }
                }
            }
        
        **Additional info:**
        
        \-\-\-