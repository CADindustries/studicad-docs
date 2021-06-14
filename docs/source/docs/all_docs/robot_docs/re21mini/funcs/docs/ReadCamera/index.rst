ReadCamera
================================

ReadCamera function is used to get camera image from a robot.

.. tabs::

    .. tab:: Python

        **Location and name:** RobocadSim.RE21mini.read_camera()

        **Inputs:**  

        \-\-\-

        **Output:**

        *numpy.ndarray* of image from robot

        **Example:**

        .. code-block:: python
            :linenos:

            from robocadSimPy import RobocadSim
            import cv2


            robot = RobocadSim.RE21mini()
            image = robot.read_camera()
        
        **Additional info:**
        
        \-\-\-

    .. tab:: C++

        **Location and name:** "RE21mini.h".RE21mini.ReadCamera()

        **Inputs:**  

        \-\-\-

        **Output:**

        *Mat* of image from robot

        **Example:**

        .. code-block:: c++
            :linenos:

            #include "RE21mini.h"
            #include <iostream>

            int main()
            {
                RE21mini robot;
                Mat image = robot.ReadCamera();
            }

        **Additional info:**
        
        \-\-\-

    .. tab:: C#

        **Location and name:** RobocadSim.RE21mini.ReadCamera()

        **Inputs:**  

        \-\-\-

        **Output:**

        *Mat* of image from robot

        **Example:**

        .. code-block:: csharp
            :linenos:

            using System;
            using RobocadSim;
            using Emgu.CV;

            namespace TestLib
            {
                class Program
                {
                    static void Main(string[] args)
                    {
                        RE21mini robot = new RE21mini();
                        Mat image = robot.ReadCamera();
                    }
                }
            }
        
        **Additional info:**
        
        \-\-\-