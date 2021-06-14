ReadEncs
================================

ReadEncs function is used to get encoder values from a robot.

.. tabs::

    .. tab:: Python

        **Location and name:** RobocadSim.RE21mini.read_encs()

        **Inputs:**  

        \-\-\-

        **Output:**

        *float map* that includes:

        - Right motor' encoder value
        - Left motor' encoder value
        - Back motor' encoder value
        - Lift motor' encoder value

        **Example:**

        .. code-block:: python
            :linenos:

            from robocadSimPy import RobocadSim


            robot = RobocadSim.RE21mini()
            right_enc, left_enc, back_enc, lift_enc = robot.read_encs()
        
        **Additional info:**
        
        - You should use Transfunction with encoders for a more convenient representation of values

    .. tab:: C++

        **Location and name:** "RE21mini.h".RE21mini.ReadEncs()

        **Inputs:**  

        \-\-\-

        **Output:**

        *float\** that includes:

        - Right motor' encoder value
        - Left motor' encoder value
        - Back motor' encoder value
        - Lift motor' encoder value

        **Example:**

        .. code-block:: c++
            :linenos:

            #include "RE21mini.h"
            #include <iostream>

            int main()
            {
                RE21mini robot;
                float* all_encs = robot.ReadEncs();
                float right_enc = all_encs[0];
                float left_enc = all_encs[1];
                float back_enc = all_encs[2];
                float lift_enc = all_encs[3];
            }

        **Additional info:**
        
        - You should use Transfunction with encoders for a more convenient representation of values

    .. tab:: C#

        **Location and name:** RobocadSim.RE21mini.ReadEncs()

        **Inputs:**  

        \-\-\-

        **Output:**

        *float[]* that includes:

        - Right motor' encoder value
        - Left motor' encoder value
        - Back motor' encoder value
        - Lift motor' encoder value

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
                        float[] allEncs = robot.ReadEncs();
                        float rightEnc = allEncs[0];
                        float leftEnc = allEncs[1];
                        float backEnc = allEncs[2];
                        float liftEnc = allEncs[3];
                    }
                }
            }
        
        **Additional info:**
        
        - You should use Transfunction with encoders for a more convenient representation of values