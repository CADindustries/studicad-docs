ReadEncsVoid
================================

ReadEncsVoid function is used to write encoder values from a robot into variables.

.. tabs::

    .. tab:: Python

        **Location and name:** RobocadSim.RE21mini.read_encs_void()

        **Inputs:**  

        \-\-\-

        **Output:**

        \-\-\-

        **Example:**

        .. code-block:: python
            :linenos:

            from robocadSimPy import RobocadSim


            robot = RobocadSim.RE21mini()
            robot.read_encs_void()
            right_enc = robot.right_motor_enc
            left_enc = robot.left_motor_enc
            back_enc = robot.back_motor_enc
            lift_enc = robot.lift_motor_enc
        
        **Additional info:**
        
        - You should use Transfunction with encoders for a more convenient representation of values

    .. tab:: C++

        **Location and name:** "RE21mini.h".RE21mini.ReadEncsVoid()

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
                robot.ReadEncsVoid();
                float right_enc = robot.rightMotorEnc;
                float left_enc = robot.leftMotorEnc;
                float back_enc = robot.backMotorEnc;
                float lift_enc = robot.liftMotorEnc;
            }

        **Additional info:**
        
        - You should use Transfunction with encoders for a more convenient representation of values

    .. tab:: C#

        **Location and name:** RobocadSim.RE21mini.ReadEncsVoid()

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
                        robot.ReadEncsVoid();
                        float rightEnc = robot.encRight;
                        float leftEnc = robot.encLeft;
                        float backEnc = robot.encBack;
                        float liftEnc = robot.encLift;
                    }
                }
            }
        
        **Additional info:**
        
        - You should use Transfunction with encoders for a more convenient representation of values