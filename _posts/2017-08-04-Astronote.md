---
title: Astronote
image: astronote.png
links:
- title: Latest Release
  url: https://github.com/CQCumbers/astronote/releases 
- title: Github Repo
  url: https://github.com/CQCumbers/astronote
---

Astronote is a markdown-based note taking app that stores your notes locally as plain text files. It can automatically cache images and webpages linked to from your notes as well as display and edit LaTeX equations. The app was built in Javascript using Electron for cross-platform desktop support and React for the UI. This was my first foray into react and electron, as well as my first project to use continuous integration. The entire app built over the course of 2 weeks in order to address my frustrations with using OneNote for my Science Olympiad astronomy notes. Astronote has been effective in improving my astronomy notes, and building it myself was both educational and allows for even more future customization.

I built this app as a solution to my problems managing large onenote notebooks for Science Olympiad astronomy competitions. These competitions allow participants to use a computer without an internet connection on the test, so comprehensive offline knowledge bases are very important. I initially did this by clipping pertinent pages to onenote, but we encountered problems with certain pages that could only be clipped as images, making them difficult to search, interactive pages that were no longer usable as clippings, and the desire to clip groups of linked pages all at once. I was also frustrated with onenote's equation editor and inconsistent formatting and feature set between windows and mac. I tried to address these by creating a markdown note taking app in electron (a cross platform desktop app framework) that would automatically download fully functional webpages, including all images and javascript code, linked to in notes, in addition to the webpages that those pages linked to. I also added LaTeX support, fuzzy search, autocorrect, and other features. Electron allows astronote to run the same way on windows, mac, and linux, and notes are stored as plain text files in standard folders, allowing notebooks to be easily exchanged with others and edited with other tools.
