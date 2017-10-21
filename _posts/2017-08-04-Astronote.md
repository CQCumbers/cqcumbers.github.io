---
title: Astronote
image: astronote.png
links:
- title: Latest Release
  url: https://github.com/CQCumbers/astronote/releases 
- title: Github Repo
  url: https://github.com/CQCumbers/astronote
---

Astronote is a markdown-based note taking app that stores notes as plain text files in your computer's file system. It can also locally cache images and webpages linked to from your notes, and supports LaTeX equations and fuzzy search. The app is built using electron for cross-platform desktop app support, react for UI, javascript for code, and simplemde for markdown editing and previewing. This was my first foray into javascript, react, and electron, as well as my first project to use continuous integration, and was mostly built over the course of 2 weeks. Astronote addresses my frustrations with using OneNote's equation editor for extensive math notes as well as my problems with its web clipper, which often did not clip functional web pages, and did not locally cache hyperlinks in those pages.

I built this app as a solution to my problems managing large onenote notebooks for Science Olympiad astronomy competitions. These competitions allow participants to use a computer without an internet connection on the test, so comprehensive offline knowledge bases are very important. I initially did this by clipping pertinent pages to onenote, but we encountered problems with certain pages that could only be clipped as images, making them difficult to search, interactive pages that were no longer usable as clippings, and the desire to clip groups of linked pages all at once. I was also frustrated with onenote's equation editor and inconsistent formatting and feature set between windows and mac. I tried to address these by creating a markdown note taking app in electron (a cross platform desktop app framework) that would automatically download fully functional webpages, including all images and javscript code, linked to in notes, in addition to the webpages that those pages linked to. I also added LaTeX support, fuzzy search, autocorrect, and other features. Electron allows astronote to run the same way on windows, mac, and linux, and notes are stored as plain text files in standard folders, allowing notebooks to be easily exchanged with others and edited with other tools.
