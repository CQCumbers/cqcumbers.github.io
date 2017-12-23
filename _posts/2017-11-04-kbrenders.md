---
title: kbrenders
image: kbrenders.png
links:
- title: Website
  url: http://www.kbrenders.com/
- title: Github Repo
  url: https://github.com/CQCumbers/kbrenders
---

kbrenders is a paid cloud service that provides professional quality 3D renders of custom keycap designs. The app uses a flask web server to manage orders and charge customers using stripe. Then, every day, an auto-scaling backend of cloud servers renders each queued job using a custom blender scene and 3D models, and emails the final image to the customer. kbrenders can provide accurate visualizations to more people, more quickly and cheaply than the visualization services of individual artists. Unlike KLE-Render, kbrenders only supports a limited number of keyboard layouts, but its renders are individually ray-traced and thus much more realistic. Building it was a fantastic way to leverage my skills in 3D modelling and cloud computing while learning about setting up a real business.

I've wanted to set up a way to automate 3D renders of keycaps ever since designing Classic Space, my own attempt at a custom keycap set. I made most of the models used in kbrenders after becoming rather disenchanted with the process of getting slow and expensive custom renders done by others. I initially wanted to do it in Keyshot, due to its ease of use and integration with Solidworks, but while the renders were good, scripting automated material changes proved impossible. After maybe a year of working on it, I found success with blender scripting. Although the process of updating the blender models is tedious, scripting blender is both much more pleasant and powerful than scripting Keyshot. It also supports being run headless on linux, meaning not only could I more easily setup my own scenes, but I could handle others' layouts in the cloud as well. While the actual blender scripting took only a few days, I've been working on the project in some form - making 3D models, setting up Keyshot scenes, etc. - since probably 2015, making it probably my longest running project.
