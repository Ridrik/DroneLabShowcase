---
title: "Building a 3D simulator and visualizer for drones in C++: Dynamics, GUI, replay features, and project roadmap"
seoTitle: "DroneLab: a 3D simulator, visualizer and replayer for Drones"
datePublished: Thu Nov 13 2025 18:35:37 GMT+0000 (Coordinated Universal Time)
cuid: cmhxrrqyn000102l5gfqsfhjb
slug: building-a-3d-simulator-and-visualizer-for-drones-in-c-dynamics-gui-replay-features-and-project-roadmap
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1763053013532/0683d883-4845-4998-a016-2a1b794d5cda.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1763058859552/bd7d03c5-147e-47b0-8083-13ac8824d18c.jpeg
tags: cpp, simulation, drone

---

Hi! In the past few months, I’ve been developing DroneLab: a 3D simulator, visualizer, and replayer for drones, built in C++. It integrates rigid-body dynamics, GNC (Guidance, navigation, control) modules, visualization tools, and a user-friendly GUI that allows easy configuration editing. Above all, it features a replayer that lets the user load and visualize past sessions on demand.

The main purpose of this simulator is to provide a lightweight and smooth procedure to explore entry-level drone dynamics and drone experimentation. The planned introduction of external interfaces like MAVLink will also enable testing and experimentation with external flight controllers in both SITL and HITL modes.

Context: My interest in aerospace vehicle dynamics and software systems led me to create DroneLab. During my latest work experience, I helped implement a GPS/GNSS receiver prototype, which deepened my curiosity about drone dynamics. I wanted to explore further by building a tool that combines modular design, a node-based actor system, and custom graphics — all while maintaining control over the architecture and avoiding unnecessary bloat*.* This project features graphics using OpenGL and a UI based on the popular Dear ImGUI library.

Some of the key features in DroneLab, at this early version, include:

**Simulation and Control:**

* Configurable Editor: Load, save, and tweak flight parameters, environment settings, sensors, and estimators.
    
* Flight Modes: Waypoint following, return-to-launch (RTL), with additional modes planned.
    
* Simulation Control: Pause, slow, and speed up simulation; switch between drone orbit mode or free mode.
    

**Visualization and Interaction:**

* Live Interaction: Add waypoints on screen, disable/enable sensors (e.g., GPS or Magnetometer).
    
* Visual Outputs: Real-time and replayable telemetry, plots, minimap, 3D trajectory trails, ghost drone estimates, and more.
    

**Core Functionality:**

* Quadcopter GNC & Flight Controller Core: Rigid-body dynamics integration, discrete Extended Kalman filter for state estimation, and cascade PID controllers.
    
* Replay & Storage: Load any previous run and replay at the given moment of the flight as if it were live.
    

A live showcase is displayed here: [DroneLab Showcase](https://ridrik.github.io/DroneLabShowcase/)

This software is currently in development. The roadmap, as of now, includes:

**Immediate Work**

* Backend simulation mode
    
* UDP communication with MAVLink for SITL and HITL usage
    
* Actuator ESC modes (open-loop and closed-loop)
    
* Sensor adjustments
    

**Future Plans**

* Add vehicle modes (currently features quadcopter in X configuration)
    
* Multi-vehicle support
    
* Batch simulations
    
* Enhanced 3D visualization tools
    

I’ll share updates on new features that get introduced and make their way into preview/demo releases.

Let me know what you think of this, and what features you typically miss from a simulator that could help your own applications. If you are interested in trying out a demo version, I’ll be happy to send an invitation to a release demo preview version over GitHub! You may also contact me on [LinkedIn](https://www.linkedin.com/in/rodrigo-rosa-4547b115b/).