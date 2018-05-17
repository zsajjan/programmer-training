#Veteran Robot Programmer Training

In the summer and offseason of 2018-2019, we will be taking steps to ensure that our second-year programmers (congrats! You made it through build season!) will be able to effectively manage the entire codebase by themselves - essentially, the sum of this second-year training should be enough to bring the programmers up to the level needed to fully contribute to the robot programming codebase. This training will involve several areas, including greater depth of understanding in C++ and Python programming as well as specific knowledge of the Linux operating system, the Bazel build system, and WPILib and the FRC control system.

Every programmer is not expected to understand all of the below topics in complete detail. Everyone should still have some basic familiarity with each of the topics: bolded entries below indicate topics that all veteran programmers should understand. Each programmer should also study in depth two or three other topics with the expectation that they will become one of the team’s "experts” on that topic.

This training will mostly involve the self-paced use of resources linked below. There may also be some formal lectures or exercises depending on what the programmers are having trouble with.

##Git and Github

###Goals

Understand...

* **The underlying commit model of git**
* **Pushing and pulling**
* **Branches**
* **Forks**
* Stashes
* **Remotes**
* Merge vs. **Squash** vs. Rebase
* **Pull Requests**
* **Code Review**

###Resouces

There are a lot of developers who post information on how to do specific git things.

* [Working with Remotes (and doing stuff with them)] (http://dont-be-afraid-to-commit.readthedocs.io/en/latest/git/remotes.html)

* [Using the Fork-and-Branch Git Workflow] (https://blog.scottlowe.org/2015/01/27/using-fork-branch-git-workflow/)

* [Pull Requests and Code Review Guidlines (Code Inspection Checklist)] (http://www.literateprogramming.com/Baldwin-inspect.pdf)

* [Test your basic knowledge of git] (http://gitreal.codeschool.com/levels/1/challenges/1)

##C++

###Goals

Understand...

* **All common syntax used in C++**
* The C++ compilation/linking process
* How templates work in C++ and how classes can be templated over both types and values
* **Stack vs. heap memory**
* Ownership semantics
* Different types of variables, including owned stack variables, references, pointers, and smart pointers
* Common pitfalls of C++
>Initialization
>Use-after-free or resource leaks
* The debugging process, and how to use a debugger to find issues in code 

###Resouces

Most C++ topics are covered by [Learn CPP] (http://www.learncpp.com/)

* [Stack and Heap Memory] (http://www.learncpp.com/cpp-tutorial/79-the-stack-and-the-heap/)

* [C++ Ownership Semantics] (http://ericlavesson.blogspot.com/2013/03/c-ownership-semantics.html)

* Multithreading
* Real-time Behavior
* Compiler stages
* Templates

##Linux/Unix

###Goals

Understand...

* **Navigation using terminal**
* Linux filessystem
>/
>/home/
>/etc/
>/usr/
Mount Points
* **SSH**, rsync, and SCP
* Networking
>Static IP vs. DHCP
>mDNS
>Ports

###Resources

* [Over the Wire (games)] (http://overthewire.org/wargames/bandit)
* [Linux Journey] (https://linuxjourney.com/)

##Bazel

###Goals

Be able to...

* **Use cc_library, cc_binary, and cc_test in real code**

>**Know when and how to properly declare dependencies in code**

* Create and use macros for code generation
* Configure the CROSSTOOL to fix the build system for different setups

###Resources

* [Bazel Documentation] (https://bazel.build/versions/master/docs/bazel-overview.html)
* [Bazel Wiki Home] (https://github.com/bazelbuild/bazel/wiki)

##WPILib and FRC Components

###Goals

Understand...

* **Each component in the control system and its purpose**

> **Encoder**

> **Potentiometer**

> **PCM**

> **PDP**

> **VRM**

> **Motor**

> **Battery**

> **RoboRIO**

> **Radio**

> **Spartan board**

* The protocols used in communication between the above components and the potential failure modes of each

>CAN

>SPI

>PWM

* **How to use the Driver Station to run a robot**

> **Enabling**

> **Disabling**

> **Joystick configuration**

* **Use of the RoboRIO configuration tool**
* **Use of the radio configuration tool**
* Basic electrical knowledge, including some understanding of how to diagnose issues with the above components
* How the radio’s configuration changes between the shop and competition

Be able to...

* Troubleshoot and help diagnose issues in the robot's control system
* Troubleshoot networking issues at competition

###Resources
[ScreenSteps Live (Official FRC Documentation)] (https://wpilib.screenstepslive.com/s/4485/m/13503)


##Python

###Goals

Understand...

* **Common syntax used in python**
* Numpy, especially with matrices and linear algebra
* Generation of C++ code from python

###Resources

* [Learn Python] (https://www.learnpython.org)
* [Numpy] (https://docs.scipy.org/doc/numpy-1.12.0/index.html)

##Math and Physics

###Goals

Understand...

* **What an integral is, what a derivative is, and the relationship between the two**
* **The concepts of velocity and acceleration and the difference between the two**
* Simple electrical and mechanical relationships and how they apply to robots

>P=IV

>V=IR

> **τ=Fx (torque)**

> **F=ma**

> **τ=Jα**

> **τ1ω1 = τ2ω2 (in a gearbox)**

>ΔE = W = Fd (work/energy)

>P = Fv (power)

* The motor (differential) equation
* Kirchoff's laws
* **The concept of differential equations and how it can apply to physics**
* Basic linear algebra

>Matrices as systems of equations

>Matrix multiplication as substitution

>Vectors and matrix-vector multiplication

>The concept of a matrix inverse

###Resources

* [Linear Algebra (Matrices and Vectors)] (https://www.cs.cornell.edu/courses/cs485/2006sp/LinAlg_Complete.pdf)
>**Important sections:** 
Matrices and Matrix Arithmetic & Operations

* [Differential Equations] (http://tutorial.math.lamar.edu/Classes/DE/DE.aspx)

>**Important sections:**

>Basic Concepts

>First Order

>Second Order

>Systems of Equations

>Higher Order

* [General Physics] (https://www.khanacademy.org/science/physics)

>**Important Sections**

>One-Dimensional Motion

>Forces and Newton's Laws of Motion

>Work and Energy

>Torque and Angular Momentum

>Circuits

##Control System Design and Modeling

###Goals

Understand...

* **What a PID controller is and how it works**
* **The concept of a system**

> **State, input, output**

* **Concept of a Controller**
* Ideas Behind motor profiling
* How differential equations can describe a system
* The state-space form of linear systems
* The concept of an observer and what one can do to help a controller

Be able to...

* **Tune a PID controller for a given system**
* Tune the state-space model of a system to match the physical response
* How to derive a state-space model from the physical parameters of a system
* Design a state-space controller through simulation using both LQR and pole placement
* Design an observer using both Kalman gains and pole placement

###Resources

* [Wesley's Blog: Control Theory Part 0] (http://blog.wesleyac.com/posts/intro-to-control-part-zero-whats-this)

* [254-Taking Control of your Robot] (https://www.team254.com/documents/control/)

* [254+971-Motion Planning and Control (youtube)] (https://www.youtube.com/watch?v=8319J1BEHwM)

##Vision

###Goals

Understand...

* Colorspaces and how colors are stored in the computer's memory

>RGB

>HSV

>YUV

>HSL

* How pose estimation can be applied to find the robot's position relative to a target

>Pitch

>Yaw

>Disance form target

>Horizontal displacement from a target

* The latency involved in image capture, and how to compensate for this in vision code

Be able to...

* Use OpenCV to capture, filter, and detect targets in images
* Tune thresholds to properly detect retroreflective targets on the field

###Resources

* [OpenCV turorials] (http://docs.opencv.org/master/d9/df8/tutorial_root.html)

* [254 "integrating Computer Vision and Motion Control"] (https://www.team254.com/documents/vision-control)
