ReadCameraBytes
================================

ReadCameraBytes function is used to get camera bytes from a robot.

.. tabs::

    .. tab:: Python

        **Location and name:** RobocadSim.RE21mini.read_camera_bytes()

        **Inputs:**  

        \-\-\-

        **Output:**

        *bytes* of image from robot

        **Example:**

        .. code-block:: python
            :linenos:

            from robocadSimPy import RobocadSim


            robot = RobocadSim.RE21mini()
            image_bytes = robot.read_camera_bytes()
        
        **Additional info:**
        
        \-\-\-

    .. tab:: C++

        **Location and name:** "RE21mini.h".RE21mini.ReadCameraBytes()

        **Inputs:**  

        \-\-\-

        **Output:**

        *char\** of image from robot

        **Example:**

        .. code-block:: c++
            :linenos:

            #include "RE21mini.h"
            #include <iostream>

            int main()
            {
                RE21mini robot;
                char* imageBytes = robot.ReadCameraBytes();
            }

        **Additional info:**
        
        \-\-\-

    .. tab:: C#

        **Location and name:** RobocadSim.RE21mini.ReadCameraBytes()

        **Inputs:**  

        \-\-\-

        **Output:**

        *byte[]* of image from robot

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
                        byte[] imageBytes = robot.ReadCameraBytes();
                    }
                }
            }
        
        **Additional info:**
        
        \-\-\-