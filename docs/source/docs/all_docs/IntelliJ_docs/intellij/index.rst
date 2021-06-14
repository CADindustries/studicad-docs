IntelliJ Project creation
======================================

Here is some info about how to create project on IntelliJ to use it via **shufflecad**.

Project creation:
^^^^^^^^^^^^^^^^^^^^^^^

1. Open Your IntelliJ -> click on **File** -> **New** -> **Project...**. Select **Maven** and SDK version - 11

.. image:: imgs/first_step.PNG
   :align: center
   :width: 700

2. Click **Next** -> Enter here your project name and its location -> **Finish**

.. image:: imgs/second_step.PNG
   :align: center
   :width: 800

3. Click **File** -> **Project Structure...** -> **Project Settings** -> **Modules** -> **Dependencies** -> click on plus button -> **1 JARs or directories**

.. image:: imgs/third_step_2.PNG
   :align: center
   :width: 800

4. Select **picad4j.jar** file -> **Apply** -> **OK**

.. image:: imgs/fourth_step.PNG
   :align: center
   :width: 800

5. Create a package inside java folder -> create main class inside it

.. image:: imgs/fifth_step.PNG
   :align: center
   :width: 800

6. Click **File** -> **Project Structure...** -> **Project Settings** -> **Artifacts** -> click on plus button -> **JAR** -> **From modules with dependencies...**

.. image:: imgs/sixth_step.PNG
   :align: center
   :width: 800

7. Select here your Main class and inside **Directory for META-INF...** at the end of the line instead of *java* writedown *resources* -> **OK** -> **Apply** -> **OK**

.. image:: imgs/seventh_step_2.PNG
   :align: center
   :width: 800

8. Now your project tree should look like this

.. image:: imgs/nineth_step.PNG
   :align: center
   :width: 800

8. Then click on **Build** -> **Build Artifacts...** -> Select your artifact -> **Build**
