FromMotorsToAxis
================================

FromMotorsToAxis function is used to remake input motors values into axis values for **tricycle** robot.

.. tabs::

    .. tab:: Python

        **Location and name:** Funcad.Funcad.from_motors_to_axis()

        **Inputs:**  

        - *float* speed to right motor
        - *float* speed to left motor
        - *float* speed to back motor

        **Output:**

        *numpy.ndarray* that includes:

        - Speed to X axis
        - Speed to Y axis
        - Speed to Z axis

        **Example:**

        .. code-block:: python
            :linenos:

            from robocadSimPy import Funcad


            funcad = Funcad.Funcad()
            out = funcad.from_motors_to_axis(5, -5, 0)  # [8.66 0.   0.  ]
        
        **Additional info:**
        
        \-\-\-

    .. tab:: C++

        **Location and name:** "Funcad.h".Funcad.from_motors_to_axis()

        **Inputs:**  

        - *float* speed to right motor
        - *float* speed to left motor
        - *float* speed to back motor

        **Output:**

        *float\** that includes:

        - Speed to X axis
        - Speed to Y axis
        - Speed to Z axis

        **Example:**

        .. code-block:: c++
            :linenos:

            #include "Funcad.h"
            #include <iostream>

            int main()
            {
                Funcad funcad;
                float* out = funcad.from_motors_to_axis(5, -5, 0); // 8.66 0 0
            }

        **Additional info:**
        
        \-\-\-

    .. tab:: C#

        **Location and name:** RobocadSim.Funcad.FromMotorsToAxis()

        **Inputs:**  

        - *float* speed to right motor
        - *float* speed to left motor
        - *float* speed to back motor

        **Output:**

        *System.Numerics.Vector3* that includes:

        - Speed to X axis
        - Speed to Y axis
        - Speed to Z axis

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
                        Vector3 vec = funcad.FromMotorsToAxis(5, -5, 0); // 8.66 0 0
                    }
                }
            }
        
        **Additional info:**
        
        \-\-\-