TransfunctionCoda
================================

TransfunctionCoda function is used to rearrange input value. Created by subsystems developer Coda.

.. tabs::

    .. tab:: Python

        **Location and name:** Funcad.Funcad.transfunc_coda()

        **Inputs:**  

        - *float* value to remake
        - *list* input array
        - *list* output array

        **Output:**

        *float* remaded input

        **Example:**

        .. code-block:: python
            :linenos:

            from robocadSimPy import Funcad


            funcad = Funcad.Funcad()
            out = funcad.transfunc_coda(5, [2, 10], [20, 100])  # out will be 50
        
        **Additional info:**
        
        \-\-\-

    .. tab:: C++

        **Location and name:** "Funcad.h".Funcad.transfunc_coda()

        **Inputs:**  

        - *float* value to remake
        - *float\** input array
        - *float\** output array
        - *int* size of input or output array

        **Output:**

        *float* remaded input

        **Example:**

        .. code-block:: c++
            :linenos:

            #include "Funcad.h"
            #include <iostream>

            int main()
            {
                Funcad funcad;
                float in_arr[] = { 2, 10 };
                float out_arr[] = { 20, 100 };
                float out = funcad.transfunc_coda(5, in_arr, out_arr, 2); // out will be 50
            }

        **Additional info:**
        
        \-\-\-

    .. tab:: C#

        **Location and name:** RobocadSim.Funcad.TransfunctionCoda()

        **Inputs:**  

        - *float* value to remake
        - *List<float>* input array
        - *List<float>* output array

        **Output:**

        *float* remaded input

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
                        float[] inArr = { 2, 10 };
                        List<float> inList = new List<float>(inArr);
                        float[] outArr = { 20, 100 };
                        List<float> outList = new List<float>(outArr);
                        float outVal = funcad.TransfunctionCoda(5, inList, outList); // out will be 50
                    }
                }
            }
        
        **Additional info:**
        
        \-\-\-