ReadCameraVoid
================================

ReadCameraVoid function is used to write camera image from a robot into variables.

.. tabs::

    .. tab:: Python

        **Location and name:** RobocadSim.RE21mini.read_camera_void()

        **Inputs:**  

        \-\-\-

        **Output:**

        \-\-\-

        **Example:**

        .. code-block:: python
            :linenos:

            from robocadSimPy import RobocadSim
            import cv2


            robot = RobocadSim.RE21mini()
            robot.read_camera_void()
            image = robot.image_from_camera
        
        **Additional info:**
        
        \-\-\-

    .. tab:: C++

        **Location and name:** "RE21mini.h".RE21mini.ReadCameraVoid()

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
                robot.ReadCameraVoid();
                Mat image = robot.imageFromCamera;
            }

        **Additional info:**
        
        \-\-\-

    .. tab:: C#

        **Location and name:** RobocadSim.RE21mini.ReadCameraVoid()

        **Inputs:**  

        \-\-\-

        **Output:**

        \-\-\-

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
                        robot.ReadCameraVoid();
                        Mat image = robot.imageFromCamera;
                    }
                }
            }
        
        **Additional info:**
        
        \-\-\-