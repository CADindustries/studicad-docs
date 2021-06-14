InRangeBool
================================

InRangeBool function is used to check that input value is in range.

.. tabs::

    .. tab:: Python

        **Location and name:** Funcad.Funcad.in_range_bool()

        **Inputs:**  

        - *float* input value
        - *float* lower threshold
        - *float* upper threshold

        **Output:**

        *bool* is in range

        **Example:**

        .. code-block:: python
            :linenos:

            from robocadSimPy import Funcad


            funcad = Funcad.Funcad()
            out = funcad.in_range_bool(5, 0, 12)  # True
        
        **Additional info:**
        
        \-\-\-

    .. tab:: C++

        **Location and name:** "Funcad.h".Funcad.in_range_bool()

        **Inputs:**  

        - *float* input value
        - *float* lower threshold
        - *float* upper threshold

        **Output:**

        *bool* is in range

        **Example:**

        .. code-block:: c++
            :linenos:

            #include "Funcad.h"
            #include <iostream>

            int main()
            {
                Funcad funcad;
                bool out = funcad.in_range_bool(5, 0, 12); // true
            }

        **Additional info:**
        
        \-\-\-

    .. tab:: C#

        **Location and name:** RobocadSim.Funcad.InRangeBool()

        **Inputs:**  

        - *float* input value
        - *float* lower threshold
        - *float* upper threshold

        **Output:**

        *bool* is in range

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
                        bool output = funcad.InRangeBool(5, 0, 12); // true
                    }
                }
            }
        
        **Additional info:**
        
        \-\-\-