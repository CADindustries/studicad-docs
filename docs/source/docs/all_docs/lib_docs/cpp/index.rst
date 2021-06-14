C++ library
======================================

Here is some info about how to use robocadSim C++ library in your project. I am going to use Visual Studio 2019.

1. You need open-cv installed in your project. `(How to install example). <https://www.youtube.com/watch?v=M-VHaLHC4XI>`__  
2. Right click on Your project name in **Solution explorer** -> **Properties**

.. image:: cpp_lib/first_step_cpp.png
   :align: center
   :width: 600
  
  
3. Click on **Configuration Properties** -> **C/C++** -> **General** -> **Additional Include Directories** -> **Edit**

.. image:: cpp_lib/second_step_cpp.png
   :align: center
   :width: 700

4. Create a new line and paste here path to C++ header files (./robocadSim/Lib/cpp/robocadSimLibCpp) -> click **OK**  

.. image:: cpp_lib/third_step_cpp.png
   :align: center
   :width: 600

5. Go to **Linker** -> **General** -> **Additional Library Directories** -> **Edit**

.. image:: cpp_lib/fourth_step_cpp.png
   :align: center
   :width: 700

6. Create new line and paste here path to **.lib** file (./robocadSim/Lib/cpp/x64/Release) -> click **OK**

.. image:: cpp_lib/fifth_step_cpp.png
   :align: center
   :width: 600

7. Go to **Linker** -> **Input** -> **Additional dependencies** -> **Edit**

.. image:: cpp_lib/sixth_step_cpp.png
   :align: center
   :width: 700

8. Paste here robocadSimLibCpp.lib line -> click **OK**

.. image:: cpp_lib/seventh_step_cpp.png
   :align: center
   :width: 600

9. Now You can use robocadSim C++ library in Your project!


If You can't use some header files:
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1. Copy **.dll** file in robocadSim release folder (./robocadSim/Lib/cpp/x64/Release)
2. Paste it to the path: **path_to_your_project/your_project_name/your_project_name/**