---
title: KBRenders
image: kbrenders.jpg
links:
- title: Website
  url: https://kbrenders.com/
- title: Github Repo
  url: https://github.com/CQCumbers/kbrenders
---

kbrenders creates automated, professional quality 3D renders of keycap set designs. By programmatically converting keyboard layout files into 3D scenes, it cuts the time required for photorealistic set visualizations from weeks to hours. Built using a microservice architecture, kbrenders uses Flask for taking orders and charging customers, Redis for queuing, and Blender-based worker nodes for scene generation and ray tracing. Building it was a fantastic way to put my experience in 3D modelling and cloud computing to use, while setting up a real business for the first time.

I've wanted to set up a way to automate 3D renders of keycaps ever since designing Classic Space, my own attempt at a custom keycap set. I made most of the models used in kbrenders after becoming rather disenchanted with the process of getting slow and expensive custom renders done by others. I initially wanted to do it in Keyshot, due to its ease of use and integration with Solidworks, but while the renders were good, scripting automated material changes proved impossible. After maybe a year of working on it, I found success with blender scripting. Although the process of updating the blender models is tedious, scripting blender is both much more pleasant and powerful than scripting Keyshot. It also supports being run headless on linux, meaning not only could I more easily setup my own scenes, but I could handle others' layouts in the cloud as well. While the actual blender scripting took only a few days, I've been working on the project in some form - making 3D models, setting up Keyshot scenes, etc. - since probably 2015, making it probably my longest running project.
