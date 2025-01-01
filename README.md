# Final Project!

This is it! The culmination of your procedural graphics experience this semester. For your final project, we'd like to give you the time and space to explore a topic of your choosing. You may choose any topic you please, so long as you vet the topic and scope with an instructor or TA. We've provided some suggestions below. The scope of your project should be roughly 1.5 homework assignments). To help structure your time, we're breaking down the project into 4 milestones:

## Members

Just me (Andrew Ding).


## Project planning: Design Doc (due 11/6)
Before submitting your first milestone, _you must get your project idea and scope approved by Rachel, Adam or a TA._

#### Introduction
My project will be to create a robotic character generator, inspired by the specialized robots as featured in science fiction media (e.g. *Horizon Zero Dawn*, *Titanfall*). These robots are diverse in appearance and functionality, but typically follow some natural rules which might enable procedural generation. I will make a tool to generate such robotic generators more easily.

#### Goal
To produce a robotic character generator as a Houdini program. Given a main body pattern, it should be able to generate random robots or allow the user to easily customize individual parts. 

#### Inspiration/reference:
As reference for the typical kind robots that this tool should generate, here are some fanarts of the robots from *Rimworld*:
![ref - rimworld diabolus fanart](https://github.com/user-attachments/assets/ea872896-253c-4619-8ab2-4c2bf0024d52)
![ref - rimworld light mechanoids fanart](https://github.com/user-attachments/assets/75334196-6583-4412-9ff3-11a05acbe1d1)

Another major reference is the machines from *Horizon Zero Dawn*.
![ref - HZD scrapper](https://github.com/user-attachments/assets/dc56410b-4235-4b15-ba0d-b8476d50892c)
![ref - HZD Machines](https://github.com/user-attachments/assets/90479cf6-a6a2-4f3b-ba7b-e99c831cb65b)

However, HZD's robots are very detailed and mostly imitate animals; thus, they are an auxiliary reference.

#### Specification:
The program will be a geometry graph in Houdini. As input, this graph will require a piece of geometry to use as the "main body" as the robot. The program will then construct the main body in that approximate shape and continuously add legs/wheels, sensors, tools, and weapons until it deems the robot "complete." All of the additional parts should have their scale and type controllable by other parameters that are inputs to the graph. The final output will be a geometry in Houdini as well; it should be a robot that is both aesthetic and physically plausible.

#### Techniques:
This project should take a semi-teleological approach to generating robots. The goal is to construct a robot that looks like it could perform a particular function well. For example, legs must be an appropriate length and shape to support the main body, and weapons must be located in an area where they would be effective. 

Key techniques to use:
- Scaling limbs by body size in a manner analogous to animals' legs; ref. *Scale effects between body size and limb design in quadrupedal mammals* by Kilbourne, Hoffman
- Approximate collision detection via approximate convex hulls (ref. *Fast Approximation of Convex Hull* by Kavan, Kolingerova, Zara); it will be necessary to generate some parts that don't collide with another
- rejection sampling; for the most part it will not be possible to generate robots that are always satisfactory
- limb-based inverse kinematics for making reasonable limbs

#### Design:
- ![diagram](https://github.com/user-attachments/assets/ca5f96b7-2d49-4b8b-9163-3d396588a8a6)

## Final submission (due 12/2)
Time to polish! Spen this last week of your project using your generator to produce beautiful output. Add textures, tune parameters, play with colors, play with camera animation. Take the feedback from class critques and use it to take your project to the next level.

Submission:
- Push all your code / files to your repository
- Come to class ready to present your finished project
- Update your README with two sections 
  - final results with images and a live demo if possible
  - post mortem: how did your project go overall? Did you accomplish your goals? Did you have to pivot?

## Final Results

Demo:
https://github.com/user-attachments/assets/2f848260-a4c8-4e12-aafb-9d66f3a5a505

Images:
![](render.png)
![](torus.png)
![](complex.png)



