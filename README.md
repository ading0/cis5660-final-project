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


#### Timeline:
There is only one group member, me (Andrew Ding).

- Week 1: Have a generator supporting approximate parts. We should be able to generate a robot with space or all the parts mapped out, although they do not have to be very detailed.
- Week 2: Support a few different types of each part (mobility parts, sensors, functional parts) and allow switching between them.
- Week 3: Add support for multiple methods of constructing the main body.
- Week 4: Use PBR features in Houdini for a more realistic look.
- Any extra time: Try to add animations.

## Milestone 1: Implementation part 1 (due 11/13)
Begin implementing your engine! Don't worry too much about polish or parameter tuning -- this week is about getting together the bulk of your generator implemented. By the end of the week, even if your visuals are crude, the majority of your generator's functionality should be done.

Put all your code in your forked repository.

Submission: Add a new section to your README titled: Milestone #1, which should include
- written description of progress on your project goals. If you haven't hit all your goals, what's giving you trouble?
- Examples of your generators output so far
We'll check your repository for updates. No need to create a new pull request.
## Milestone 2: Implementation part 2 (due 11/25)
We're over halfway there! This week should be about fixing bugs and extending the core of your generator. Make sure by the end of this week _your generator works and is feature complete._ Any core engine features that don't make it in this week should be cut! Don't worry if you haven't managed to exactly hit your goals. We're more interested in seeing proof of your development effort than knowing your planned everything perfectly. 

Put all your code in your forked repository.

Submission: Add a new section to your README titled: Milestone #3, which should include
- written description of progress on your project goals. If you haven't hit all your goals, what did you have to cut and why? 
- Detailed output from your generator, images, video, etc.
We'll check your repository for updates. No need to create a new pull request.

Come to class on the due date with a WORKING COPY of your project. We'll be spending time in class critiquing and reviewing your work so far.

## Final submission (due 12/2)
Time to polish! Spen this last week of your project using your generator to produce beautiful output. Add textures, tune parameters, play with colors, play with camera animation. Take the feedback from class critques and use it to take your project to the next level.

Submission:
- Push all your code / files to your repository
- Come to class ready to present your finished project
- Update your README with two sections 
  - final results with images and a live demo if possible
  - post mortem: how did your project go overall? Did you accomplish your goals? Did you have to pivot?

## Topic Suggestions

### Create a generator in Houdini

### A CLASSIC 4K DEMO
- In the spirit of the demo scene, create an animation that fits into a 4k executable that runs in real-time. Feel free to take inspiration from the many existing demos. Focus on efficiency and elegance in your implementation.
- Example: 
  - [cdak by Quite & orange](https://www.youtube.com/watch?v=RCh3Q08HMfs&list=PLA5E2FF8E143DA58C)

### A RE-IMPLEMENTATION
- Take an academic paper or other pre-existing project and implement it, or a portion of it.
- Examples:
  - [2D Wavefunction Collapse Pokémon Town](https://gurtd.github.io/566-final-project/)
  - [3D Wavefunction Collapse Dungeon Generator](https://github.com/whaoran0718/3dDungeonGeneration)
  - [Reaction Diffusion](https://github.com/charlesliwang/Reaction-Diffusion)
  - [WebGL Erosion](https://github.com/LanLou123/Webgl-Erosion)
  - [Particle Waterfall](https://github.com/chloele33/particle-waterfall)
  - [Voxelized Bread](https://github.com/ChiantiYZY/566-final)

### A FORGERY
Taking inspiration from a particular natural phenomenon or distinctive set of visuals, implement a detailed, procedural recreation of that aesthetic. This includes modeling, texturing and object placement within your scene. Does not need to be real-time. Focus on detail and visual accuracy in your implementation.
- Examples:
  - [The Shrines](https://github.com/byumjin/The-Shrines)
  - [Watercolor Shader](https://github.com/gracelgilbert/watercolor-stylization)
  - [Sunset Beach](https://github.com/HanmingZhang/homework-final)
  - [Sky Whales](https://github.com/WanruZhao/CIS566FinalProject)
  - [Snail](https://www.shadertoy.com/view/ld3Gz2)
  - [Journey](https://www.shadertoy.com/view/ldlcRf)
  - [Big Hero 6 Wormhole](https://2.bp.blogspot.com/-R-6AN2cWjwg/VTyIzIQSQfI/AAAAAAAABLA/GC0yzzz4wHw/s1600/big-hero-6-disneyscreencaps.com-10092.jpg)

### A GAME LEVEL
- Like generations of game makers before us, create a game which generates an navigable environment (eg. a roguelike dungeon, platforms) and some sort of goal or conflict (eg. enemy agents to avoid or items to collect). Aim to create an experience that will challenge players and vary noticeably in different playthroughs, whether that means procedural dungeon generation, careful resource management or an interesting AI model. Focus on designing a system that is capable of generating complex challenges and goals.
- Examples:
  - [Rhythm-based Mario Platformer](https://github.com/sgalban/platformer-gen-2D)
  - [Pokémon Ice Puzzle Generator](https://github.com/jwang5675/Ice-Puzzle-Generator)
  - [Abstract Exploratory Game](https://github.com/MauKMu/procedural-final-project)
  - [Tiny Wings](https://github.com/irovira/TinyWings)
  - Spore
  - Dwarf Fortress
  - Minecraft
  - Rogue

### AN ANIMATED ENVIRONMENT / MUSIC VISUALIZER
- Create an environment full of interactive procedural animation. The goal of this project is to create an environment that feels responsive and alive. Whether or not animations are musically-driven, sound should be an important component. Focus on user interactions, motion design and experimental interfaces.
- Examples:
  - [The Darkside](https://github.com/morganherrmann/thedarkside)
  - [Music Visualizer](https://yuruwang.github.io/MusicVisualizer/)
  - [Abstract Mesh Animation](https://github.com/mgriley/cis566_finalproj)
  - [Panoramical](https://www.youtube.com/watch?v=gBTTMNFXHTk)
  - [Bound](https://www.youtube.com/watch?v=aE37l6RvF-c)

### YOUR OWN PROPOSAL
- You are of course welcome to propose your own topic . Regardless of what you choose, you and your team must research your topic and relevant techniques and come up with a detailed plan of execution. You will meet with some subset of the procedural staff before starting implementation for approval.
