ReadCameraBytesVoid
================================

ReadCameraBytesVoid function is used to write camera bytes from a robot into variables.

.. tabs::

    .. tab:: Python

        **Location and name:** RobocadSim.RE21mini.read_camera_bytes_void()

        **Inputs:**  

        \-\-\-

        **Output:**

        \-\-\-

        **Example:**

        .. code-block:: python
            :linenos:

            from robocadSimPy import RobocadSim


            robot = RobocadSim.RE21mini()
            robot.read_camera_bytes_void()
            image_bytes = robot.bytes_from_camera
        
        **Additional info:**
        
        \-\-\-

    .. tab:: C++

        **Location and name:** "RE21mini.h".RE21mini.ReadCameraBytesVoid()

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
                robot.ReadCameraBytesVoid();
                char* imageBytes = robot.bytesFromCamera;
            }

        **Additional info:**
        
        \-\-\-

    .. tab:: C#

        **Location and name:** RobocadSim.RE21mini.ReadCameraBytesVoid()

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
                        robot.ReadCameraBytesVoid();
                        byte[] imageBytes = robot.bytesFromCamera;
                    }
                }
            }
        
        **Additional info:**
        
        \-\-\-