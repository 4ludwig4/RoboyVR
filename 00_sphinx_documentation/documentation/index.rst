.. Software Documentation template master file, created by
   sphinx-quickstart on Fri Jul 29 19:44:29 2016.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to the RoboyVR documentation!
=====================================

**What is it?**

RoboyVR is a virtual reality experience in which the user can watch, 
but also interact with Roboy (a humanoid robot) while he performs specific tasks, e.g. walking, waving, etc.
A virtual environment opens up a whole new set of perspectives for the user to enjoy and spectate Roboy from all kinds of POVs.
In addition to the rendering of the virtual Roboy a mobile Head-Up-Display(HUD) shows detailed information about various Roboy components,
for example displaying the powerconsuption of particular motors. As the user chooses to take a more active part, Roboy's pose 
can be influenced and altered by physical contact, e.g. shooting a projectile at the virtual model.

**How does it work?**

Roboy and its behavior is simulated on a virtual machine via Gazebo/ROS. Important information
regarding Roboy's movement are then sent through a ROSBridge(e.g. messages) towards Unity.
In Unity Roboy is rendered and constantly updated concerning positions, rotations, etc.
On top of that detailed data (time lapsed) about components is displayed via graph rendering on different UI panels.
With the help of a VR-Headset you can watch Roboy move around in a virtual space.

**Current status of the project and goals**

Currently the project can render Roboy with his pose and generate random data about his motors to visualize them.
Our next tasks are as follow:

- Use real motor data and visualize that.
- Implement an interface to track the newest models and automate the process of creating the model in Unity.
- Implement an interface to record a simulation with all the data and save/ load it on runtime.
- Enable the project to be completely Plug&Play meaning that you can send all kinds of data with a given format.


.. _background_prerequisits:

Relevant Background Information and Pre-Requisits
--------------------------------------------------

**For the user:**

One of RoboyVR design goals is to be as user friendly and intuitively as possible. 
Therefore the explorer in the virtual reality does not need to be familiar with explicit requirements.
Yet it does no harm to have a basic understanding of how the HTC Vive and its tracking mechanism work.

Putting on the head mounted display in a way that fits the user is important for a frust-free experience,
you can adjust the distance from the lenses to your eyes as well as the distance between the lenses itself. These tweaks
help immensely when it comes to maintaining a sharp field of view. 

Apart from that the tracking system needs
to be setup correctly, too. The two base station should be able to see each other clearly with no viewing obstructions
in their sights. They should be put up diagonal spanning a virtual room of two by five meters.
For additional information take a look at this guide `HTC Vive setup <https://www.vive.com/uk/setup/>`_.

**For the developer:**

RoboyVR uses Unity3D to create an immersive and exciting virtual environment. Extensive expierence with Unity is recommended. 
Unity natively relies on C#, so advanced knowledge in this field is highly advised. Otherwise see `Unity3D <https://unity3d.com/>`_.

The Roboy simulation which runs on Gazebo/ROS is written in C++, for this section 
a basic overview is sufficient to be able to understand/construct messages which are then
sent via a ROSbridge. For starting the simulation you should be familiar with Linux/Ubuntu.
Further it is useful to have some understanding of python in order to transform the Roboy
models via the Blender-api(an early python script already exists for this purpose).
  
The following links can be seen as a guideline, of course you can do
the research by yourself.

- Unity provides a lot of tutorials for the editor and the API with code samples and videos: https://unity3d.com/de/learn/tutorials
- The UnityWiki has a lot of example scripts for all kind of extensions: http://wiki.unity3d.com/index.php/Main_Page
- StackOverflow is a forum where you can search for answers regarding your coding problems: http://stackoverflow.com/
- UnityAnswers, similar to StackOverflow but only for Unity specific questions. The community is not as active and most questions
  are really basic, so bear that in mind: http://answers.unity3d.com/
- As we use ROS and our own custom messages, it is important to understand how ROS works and how ROS messages are built: http://wiki.ros.org/

If you have any further questions about the project, feel free to contact us via email: Roboyvr@gmail.com

.. _requirements_overview:

Contents:
---------

.. _Usage:
.. toctree::
  :maxdepth: 1
  :glob:
  :caption: Usage and Installation

  Usage/*
  
.. _CoreFeatures:
.. toctree::
  :maxdepth: 1
  :glob:
  :caption: Core Features
  
  CoreFeatures/*  
  
.. _ModelWorldLoader:
.. toctree::
  :maxdepth: 1
  :glob:
  :caption: Automatic Update Pipeline
  
  ModelWorldLoader/*
    
.. _Pabi:
.. toctree::
  :maxdepth: 1
  :glob:
  :caption: PaBi VR
  
  Pabi/*
  
.. _StateVisualization:
.. toctree::
  :maxdepth: 1
  :glob:
  :caption: State Visualization
  
  StateVisualization/*
  
.. _Rosbridge
.. toctree::
  :maxdepth: 1
  :glob:
  :caption: ROSBridge
  
  Rosbridge/*
  
.. _ZEDWrapper
.. toctree::
  :maxdepth: 1
  :glob:
  :caption: ZEDWrapper
  
  ZEDWrapper/*

.. _ScopeContext:
.. toctree::
  :maxdepth: 1
  :glob:
  :caption: Interfaces and Scope

  ScopeContext/*

.. _DevelopmentGraphs:
.. toctree::
  :maxdepth: 1
  :glob:
  :caption: Development Graphs

  DevelopmentGraphs/*

.. toctree::
	:maxdepth: 1
	
	presentations
  
.. toctree::
   :maxdepth: 1

   about-arc42

   
   
