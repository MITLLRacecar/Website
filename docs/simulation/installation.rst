.. _simulation_installation:

Setup Instructions
==================

=====================
Installing RacecarSim
=====================

1. If you have not done so already, complete all of the steps in :ref:`computer_setup`.
2. Download the most recent version of RacecarSim compatible with your operating system using the links below:

  * `Windows <https://drive.google.com/file/d/11mGov-zlDJYqW4jPHuZM9ysExtHa--DR/view?usp=sharing>`_
  * `Mac <https://drive.google.com/file/d/1pGTtzdQCE_-Mcpd0LV_qIzo_Ocp3WKyH/view?usp=sharing>`_
  * `Linux <https://drive.google.com/file/d/1QDYordP_OYeaveXo4kDyip1u7WfI2-zf/view?usp=sharing>`_

3. RacecarSim will be downloaded as a zipped file.  Unzip or untar the directory.
4. Open the extracted directory to find the executable program. Launch the RacecarSim executable.
5. Once RacecarSim finishes loading, you should see a screen titled "RACECAR-MN Simulation". Click the "Begin Simulation" button.

.. image:: /assets/img/simulation/MainMenu.*
  :width: 100%
  :align: center

6. A level will load with the racecar. The car begins in default drive mode, allowing you to drive around with the standard default drive controls (triggers to accelerate, left joystick to steer).

.. image:: /assets/img/simulation/FirstLevel.*
  :width: 100%
  :align: center


Troubleshooting
"""""""""""""""

**1. When driving in default drive mode, the simulation has a very low frame rate and/or is lagged, making it appear choppy or delayed.**

The depth camera is one of the most computationally intensive parts of the simulation. From the main menu, select "Settings" and reduce the "Depth Resolution". This decreases the number of samples collected by the depth camera, which should decrease lag but may make programs using the depth camera less accurate.

If RacecarSim only lags when connected to a Python program but not in default drive mode, see the troubleshooting in :ref:`simulation_python`.

===========================
Mac Only: Controller Driver
===========================

If you are using a Mac and wish to use an Xbox 360 controller with RacecarSim, you will first need to install the corresponding driver.

Installation
""""""""""""

1. Go to the `release page <https://github.com/360Controller/360Controller/releases>`_ on GitHub.
2. Under the "Assets" dropdown, double click the ``.dmg`` file. It should have a name similar to ``360ControllerInstall_1.0.0-alpha.6.dmg``. This will create a new window titled "Install Install360Controller".
3. Complete all of the steps in the installation window. The final step will cause your computer to restart.

Testing
"""""""

1. Plug your Xbox 360 controller into a USB port on your computer.
2. Under "System Preferences", you should see an option titled "Xbox 360 Controllers". Click this option to create a new window titled "Xbox 360 Controllers".
3. On the "Controller Test" page, you will see a model of the controller which indicates when each button is pressed. Test that each button on your controller causes the corresponding button on the controller test to register. If so, you are now ready to use your Xbox 360 controller with RacecarSim.

.. note::
  These instructions were adopted from `this article <https://macpaw.com/how-to/use-xbox-controller-on-mac>`_. **Beware that this article will also instruct you to install unnecessary programs such as CleanMyMac X and Joystick Mapper. We do not recommend that you install this software.**
