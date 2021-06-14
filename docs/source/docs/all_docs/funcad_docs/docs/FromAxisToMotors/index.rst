FromAxisToMotors
================================

FromAxisToMotors function is used to remake input axis values into motors values for **tricycle** robot.

.. tabs::

    .. tab:: Python

        **Location and name:** Funcad.Funcad.from_axis_to_motors()

        **Inputs:**  

        - *float* speed to X axis
        - *float* speed to Y axis
        - *float* speed to Z axis

        **Output:**

        *numpy.ndarray* that includes:

        - Speed to right motor
        - Speed to left motor
        - Speed to back motor

        **Example:**

        .. code-block:: python
            :linenos:

            from robocadSimPy import Funcad


            funcad = Funcad.Funcad()
            out = funcad.from_axis_to_motors(5, -5, 3)  # [ 2.273672 -9.273672  4.      ]
        
        **Additional info:**
        
        \-\-\-

    .. tab:: C++

        **Location and name:** "Funcad.h".Funcad.from_axis_to_motors()

        **Inputs:**  

        - *float* speed to X axis
        - *float* speed to Y axis
        - *float* speed to Z axis

        **Output:**

        *float\** that includes:

        - Speed to right motor
        - Speed to left motor
        - Speed to back motor

        **Example:**

        .. code-block:: c++
            :linenos:

            #include "Funcad.h"
            #include <iostream>

            int main()
            {
                Funcad funcad;
                float* out = funcad.from_axis_to_motors(5, -5, 3); // 2.2735 -9.2735 4
            }

        **Additional info:**
        
        \-\-\-

    .. tab:: C#

        **Location and name:** RobocadSim.Funcad.FromAxisToMotors()

        **Inputs:**  

        - *float* speed to X axis
        - *float* speed to Y axis
        - *float* speed to Z axis

        **Output:**

        *System.Numerics.Vector3* that includes:

        - Speed to right motor
        - Speed to left motor
        - Speed to back motor

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
                        Funcad funcad = new Funcad();
                        Vector3 vec = funcad.FromAxisToMotors(5, -5, 3); // 2,273672  -9,273672  4
                    }
                }
            }
        
        **Additional info:**
        
        \-\-\-