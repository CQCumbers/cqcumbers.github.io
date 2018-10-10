---
title: Astronote
image: astronote.png
links:
- title: Latest Release
  url: https://github.com/CQCumbers/astronote/releases 
- title: Github Repo
  url: https://github.com/CQCumbers/astronote
---

Astronote is a markdown-based note taking app that can automatically save image and webpage links, work with LaTeX equations, and sync with your local file system. It helps you take more useful notes with links and diagrams, while ensuring you'll be able to read them later. My first major Javascript app, Astronote uses Electron for cross-platform desktop support, React for the user interface, and Travis/Appveyor for continuous integration. This tech stack helped me create the entire app within 2 weeks and learn a great deal about front-end programming in the process. 

I built this app as a solution to my problems managing large onenote notebooks for Science Olympiad astronomy competitions. These competitions allow participants to use a computer without an internet connection on the test, so comprehensive offline knowledge bases are very important. I initially did this by clipping pertinent pages to onenote, but we encountered problems with certain pages that could only be clipped as images, making them difficult to search, interactive pages that were no longer usable as clippings, and the desire to clip groups of linked pages all at once. I was also frustrated with onenote's equation editor and inconsistent formatting and feature set between windows and mac. I tried to address these by creating a markdown note taking app in electron (a cross platform desktop app framework) that would automatically download fully functional webpages, including all images and javascript code, linked to in notes, in addition to the webpages that those pages linked to. I also added LaTeX support, fuzzy search, autocorrect, and other features. Electron allows astronote to run the same way on windows, mac, and linux, and notes are stored as plain text files in standard folders, allowing notebooks to be easily exchanged with others and edited with other tools.
