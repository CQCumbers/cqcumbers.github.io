+++
title = "Projects"

[extra]
bio = "<b>Alexander Zhang</b> is a software engineer with extensive experience deploying deep learning models on user devices. He enjoys pushing the boundaries of performance by making full use of all aspects of the modern computing stack. Currently, he's most experienced in ML model deployment, GPU programming, low level performance optimization, and compiler development - but he's always itching to try new things. His (mostly) finished projects are cataloged below."

links = [
  { title = "Resume", url = "resume" },
  { title = "Github Profile", url = "https://github.com/CQCumbers" }
]
+++


{% card(image="flickpad.jpg") %}
# Flickpad

Flickpad is wireless keypad with 20 5-direction switches. Pushing each direction triggers a different key, so it can imitate the flick keyboard often used for typing Japanese on phones. It was inspired by Furikku, Google GBoard's April Fool's Day joke from 2016. I designed the PCB in KiCad, modeled the case and keycaps in Solidworks, and wrote the firmware using ZMK. This was my first from-scratch PCB design, and I learned a lot about laying out microcontroller circuits, positioning parts so that they can be assembled, and incorporating debugging features in advance. Integrating ZMK and adding Japanese typographic symbols also taught me a lot about Zephyr RTOS, and the interactions between keyboard firmware, the USB HID spec, Windows keyboard handling, and IMEs.

{{ button(title="Github Repo", url="https://github.com/CQCumbers/zmk-keyboard-flickpad") }}
{% end %}


{% card(image="github_achievements.png") %}
# Github Achievements

This one-weekend project was inspired by flet's list of imaginary github achievements, as well as Simon Willison's articles exploring Clickhouse's free Github activities dataset. After running a few queries for users that fulfilled flet's various achievement criteria, I found a surprising number of accounts with interesting and unusual usage, and decided to share the results in the form of an online leaderboard. Github's activities data is event-based and rather large, so getting user statistics was a satisfying puzzle in efficient SQL query construction. The leaderboard itself was also a good way to practice building a reasonably polished website with handwritten HTML and CSS.

{{ button(title="Website", url="https://cqcumbers.com/github_achievements") }}
{{ button(title="Github Repo", url="https://github.com/CQCumbers/github_achievements") }}
{% end %}


{% card(video="diffusionapp.mp4") %}
# Diffusion.app

Diffusion.app is a native mac implementation of Stable Diffusion 1.5, including a full text-to-image inference pipeline and minimal Cocoa UI. Soon after the release of Stable Diffusion, I realized there was a need for a simple interface for running the model locally, with better performance and fewer installation issues than the reference python implementation, or a webapp wrapper. My approach was to rewrite the pipeline, including tokenizer, scheduler, and noise generation, in Objective C, and export the network itself to CoreML. Efficient memory reuse and some python library patches allowed it to run even on Intel Macs. Though largely superseded by other implementations, it was useful for exploring models locally, and a helpful introduction to diffusion model inference.


{{ button(title="Downloads", url="https://nightly.link/CQCumbers/diffusionapp/workflows/build/master") }}
{{ button(title="Github Repo", url="https://github.com/CQCumbers/diffusionapp") }}
{% end %}


{% card(image="minaret.jpg") %}
# Minaret

Minaret is an experimental softcore CPU and lightweight system-on-chip based on the MINA instruction set architecture, designed for use on FPGAs. It includes a DDR3 controller and direct-mapped cache, as well as a display controller, keyboard controller, timer, and UART interface. A fully LLVM/newlib based toolchain and instruction-level simulator allow others to write and test their own software for the platform in C. Getting DOOM running on Minaret was a long process (about 3 months porting LLVM and 3 months implementing hardware) but through it I learned a lot about the low-level foundations of computing - including not only compiler internals and CPU architecture, but also often overlooked pieces like linker defaults, compiler runtimes, and DRAM standards. Overall, it was a fun and rewarding exercise in building a computing system from scratch, and gave me a stronger understanding of LLVM, newlib, Verilog, and FPGAs.

{{ button(title="Github Repo", url="https://github.com/CQCumbers/minaret") }}
{% end %}


{% card(image="navi_search.png") %}
# Navi Search

Built with 5 other students for a capstone class, Navi Search is a complete internet search engine written from scratch in C++. It includes a robust HTML parser and web crawler, capable of downloading over 300 pages per second per machine over HTTPS, while respecting robots.txt rules and server timeouts. An inverted index generator and constraint solver allow the over 400 million pages and 5TB of text crawled to be quickly queried over multiple machines, and a query compiler transforms English-like syntax into efficient query plans. All this is attached to a ranker that takes into account word frequency, relative positions, URL and body text, and other factors to deliver useful results. In creating it my team and I learned a great deal about debugging and profiling distributed systems, tuning low-level Linux features on AWS, interacting with web protocols at several layers of the stack, and working as a team to deliver a complete product on a tight schedule.
{% end %}


{% card(video="css_tetris.mp4") %}
# CSS Tetris

CSS Tetris uses the space-toggler hack, a way of expressing logical ANDs and ORs using certain properties of CSS3 variables, to implement a limited version of the Quest for Tetris processor, and thus provide an extremely impractical way for someone with a great deal of patience to (theoretically) play Tetris in the browser. It includes 142 bytes of RAM, 10 opcodes, and 3 addressing modes. It also showcases a fundamental limitation to the Turing completeness of CSS - there is no way to automatically feed the outputs back into the inputs, so all state between cycles must be stored in HTML through human input, in this via lots of checkboxes and labels. While impractical to run, it was a very interesting challenge in logic design, and helped me better understand both CSS variables and CPU design.

{{ button(title="Website", url="https://cqcumbers.com/css_tetris") }}
{{ button(title="Github Repo", url="https://github.com/CQCumbers/css_tetris") }}
{% end %}


{% card(image="dungeon_bot.png") %}
# Dungeon Bot

Dungeon Bot is a Discord bot interface for the popular game AI Dungeon 2, an open-ended text adventure based on OpenAI's GPT-2 language model. It is currently used by over 1000 servers, and provides a unique way to craft interesting narratives together with other users. An experiment in deploying large deep learning models on GPU servers, it relies on a central redis server to handle incoming requests, and spins up relatively inexpensive vast.ai GPU workers to generate interesting scenarios from free-form player inputs. While not as technically challenging as some of my other projects, through it I gained experience in deploying GPU-based deep learning models via Docker, as well as debugging distrubuted systems.

{{ button(title="Invite Link", url="https://discordapp.com/oauth2/authorize?client_id=664915224595398666&scope=bot") }}
{{ button(title="Github Repo", url="https://github.com/CQCumbers/dungeon_bot") }}
{% end %}


{% card(image="nmulator.png") %}
# Nmulator

nmulator is an experimental Nintendo 64 emulator for Windows and Mac, which currently boots a decent number of commercial games. Internally, it consists of a dynamic recompiler that translates N64 CPU and RSP instructions into x86 for the host CPU, and a vulkan compute shader that processes RDP commands on the host GPU. SSE4 is used to emulate the RSP's vector coprocessor instructions. Building nmulator was a valuable experience in reverse engineering real-world software, implementing and optimizing JITs, using SIMD instructions to improve performance, and understanding both older fixed-function rasterization pipelines and modern GPU compute. Along the way, I also learned the value of building debugging tools like gdb servers, and of writing readable documentation for yourself and others.

{{ button(title="Downloads", url="https://nightly.link/CQCumbers/nmulator/workflows/build/master") }}
{{ button(title="Github Repo", url="https://github.com/CQCumbers/nmulator") }}
{% end %}

{% card(image="ping.jpg") %}
# Ping

Inspired by the game Apex Legends, Ping is an iOS app that lets you notify your friends about specific real-world locations using context-sensitive messages. Tap a location on the map and Ping will give you a list of canned messages - like "Mexican Food here!" or "Mozambique here!" - using reverse geocoding and Mapbox's point of interest data.  You can then send a rich push notification to your squadmates including an address and map of the location. Ping includes Auth0-based signup and squad management functionality, and helped me learn more about authentication, push notifications, and geocoding.

{{ button(title="App Store", url="https://itunes.apple.com/us/app/get-ping/id1457503873") }}
{% end %}


{% card(image="body_smasher.png") %}
# Body Smasher

Built in 48 hours for the Ludum Dare 43 compo, Body Smasher is a puzzle platformer with the theme "Sacrifices must be made". This was my first time making a video game, and I had a lot of fun figuring out how to create pixel art tiles, compose background music, and design thoughtful levels under the strict time limit. Body Smasher was written in Wren for the TIC-80 fantasy console, a platform with high level scripting support but the color palette, file size, sound channel, and other technical limitations of 8-bit retro computers. It helped me learn to work within the constraints of less powerful hardware as well as balance programming with all the other tasks needed to make a game.

{{ button(title="Website", url="/body_smasher.html") }}
{{ button(title="Github Repo", url="https://github.com/CQCumbers/body_smasher") }}
{% end %}


{% card(image="bloom_boys.jpg") %}
# Bloom Boys

This project was built together with 4 other students for my first year college engineering class. It was designed to monitor dissolved oxygen at various depths, and detect algal blooms or lake turnover near a drinking water intake. Building it was a challenge in many ways, but especially in debugging the communications between the microcontroller and peripherals, as we found that problems could be anything from faulty hardware and incorrect wiring to typos in the code. Testing it in the field was also educational, as we struggled with broken wires, insufficient waterproofing, and incompatible power cables in the cold. We made a lot of mistakes, but in the process learned many valuable lessons about building field-ready embedded systems.

{{ button(title="Github Repo", url="https://github.com/CQCumbers/bloom_boys") }}
{% end %}


{% card(image="frame_boy.png") %}
# Frame Boy

Frame Boy emulates early model Game Boy (DMG) hardware in the browser using C++ and webassembly. Though I had created a Chip8 emulator before, the Game Boy's PPU, stereo audio, memory banking, and other features made for a significant jump in complexity, necessitating better code organization and performance. I had to learn about topics from static analysis and cache efficiency to signal decimation and the emscripten toolchain - not to mention the complexities of Game Boy hardware, which is often surprisingly poorly documented. Though there are many faster and more accurate game boy emulators out there, I can't imagine a more engaging way to learn the inner workings of computers than emulating one yourself.

{{ button(title="Website", url="https://cqcumbers.com/frame_boy") }}
{{ button(title="Github Repo", url="https://github.com/CQCumbers/frame_boy") }}
{% end %}


{% card(image="masa_dashboard.png") %}
# MASA Dashboard
  
Conceived as a way to allow more people to check on rocket engine hotfire tests, MASA Dashboard provides a flexible solution to real time data visualization, without all the complexity of a time series database and grafana plugins. It is well suited to projects where you need more than a serial monitor, but not a whole IoT system - just constantly update a CSV with your data and MASA Dashboard will create a web accessible interface with draggable panels and several configurable graph types. Building it was a good exercise in UI design, structuring React apps, and writing server side javascript.

{{ button(title="Github Repo", url="https://github.com/CQCumbers/masa_dashboard") }}
{% end %}


{% card(image="geodoodle.png") %}
# Geodoodle

Geodoodle is an augmented reality game inspired by reddit's r/place. Like in r/place, you can only place one pixel at a time on a large canvas, so players must work together to create pixel art images. In Geodoodle, however, the canvas covers the entire globe, and you have to be in a particular location to place a pixel there. This encourages players to explore their local area and collaborate with neighbors to create an ever-changing piece of digital art. Originally built for Pennapps Spring 2018, the current Geodoodle app is written in Swift using Mapbox and Auth0 (earlier versions used React Native or Cordova), while the backend uses aiohttp, Socket.io, and Postgres. Through Geodoodle, I learned how to build cross platform apps, work with mapping software and geohashes, and write asynchronous backend servers. 

{{ button(title="App Store", url="https://itunes.apple.com/us/app/geodoodle/id1354245869") }}
{% end %}


{% card(image="chip8-emu.png") %}
# Chip8 Emulator

This project replicates the functionality of the Chip8, a simple virtual computer. Like most emulators, it reads machine codes, 1s and 0s that encode simple tasks like adding 2 numbers, and replicates their effects using a higher level language - in this case, Swift. This emulator also uses mac APIs to replicate the Chip8's timers, keypad, and black-and-white display. While the Chip8 is simple, emulating it quickly enough is still difficult for Swift Playgrounds, which encouraged me to learn ways of improving efficiency. Overall, this project was a useful, hands-on way to understand CPUs and learn how to write higher performance code.

{{ button(title="Github Repo", url="https://github.com/CQCumbers/chip8-emu") }}
{% end %}

{% card(image="kbrenders.jpg") %}
# KBRenders

kbrenders creates automated, professional quality 3D renders of keycap set designs. By programmatically converting keyboard layout files into 3D scenes, it cuts the time required for photorealistic set visualizations from weeks to hours. Built using a microservice architecture, kbrenders uses Flask for taking orders and charging customers, Redis for queuing, and Blender-based worker nodes for scene generation and ray tracing. Building it was a fantastic way to put my experience in 3D modelling and cloud computing to use, while setting up a real business for the first time.

{{ button(title="Website", url="https://kbrenders.com") }}
{{ button(title="Github Repo", url="https://github.com/CQCumbers/kbrenders") }}
{% end %}


{% card(image="grifbot.png") %}
# Grifbot

Grifbot seeks to imitate Grif, a character from the show *Red vs. Blue*, with a deep learning language model - specifically, a character-level recurrent neural network trained on hundreds of scripts from the show. By running facebook messages through this model, Grifbot can generate in-character responses that, while usually incoherent, can be entertaining nevertheless. Grifbot was built with Python and Keras, and deployed on DigitalOcean. Building it was a fun way to apply deep learning to a real data set and learn about the challenges of deploying models in the cloud.


{{ button(title="Website", url="https://grifbot.cqcumbers.com") }}
{{ button(title="Github Repo", url="https://github.com/CQCumbers/grifbot") }}
{% end %}


{% card(video="ar_orbitals.mp4") %}
# AR Orbitals

AR Orbitals is a mobile app that visualizes the shapes of electron clouds by solving Schrodinger's equations, volume tracing the result, and displaying the volume traced field visualization within the real world. It was written over a weekend with C#, Unity, and Vuforia. To create AR Orbitals, I had to implement the Legendre and Laguerre polynomials, write volume tracing code for mobile GPUs, and integrate Vuforia's augmented reality toolkit with my custom shaders. This taught me a lot about not only wavefunctions, but also C#, Unity, and GPU programming.

{{ button(title="App Store", url="https://itunes.apple.com/us/app/ar-orbitals/id1299537037") }}
{{ button(title="Play Store", url="https://play.google.com/store/apps/details?id=com.CQCumbers.AROrbitals") }}
{% end %}


{% card(image="strobr.jpg") %}
# Strobr

Strobr is an iOS app that uses variable framerate imaging to measure the frequency of a cyclical process, for example the speed of a spinning car wheel. Traditionally, these frequencies are measured with stroboscopes, devices that combine persistence of vision with flashing lights. By changing the frequency of flashes until it looks like the car wheel stays still, you can measure the wheel's speed. Strobr works similarly, but you change the imaging framerate instead, allowing you to measure more diverse processes, more conveniently. Two friends and I built Strobr in 36 hours at Pennapps Fall 2017, where it won top 30. We had a lot of fun while learning about Swift programming, iOS APIs, and high framerate imaging.


{{ button(title="App Store", url="https://itunes.apple.com/us/app/strobr-scope/id1330331187") }}
{{ button(title="Github Repo", url="https://github.com/lachm/strobr") }}
{% end %}


{% card(image="astronote.png") %}
# Astronote

Astronote is a markdown-based note taking app that can automatically save image and webpage links, work with LaTeX equations, and sync with your local file system. It helps you take more useful notes with links and diagrams, while ensuring you'll be able to read them later. My first major Javascript app, Astronote uses Electron for cross-platform desktop support, React for the user interface, and Travis/Appveyor for continuous integration. This tech stack helped me create the entire app within 2 weeks and learn a great deal about front-end programming in the process. 

{{ button(title="Latest Release", url="https://github.com/CQCumbers/astronote/releases") }}
{{ button(title="Github Repo", url="https://github.com/CQCumbers/astronote") }}
{% end %}


{% card(image="kle-render.png") %}
# KLE-Render

A free online tool for visualizing custom keycap set designs, KLE-Render has been widely adopted by the mechanical keyboard community and is used in the majority of set designs posted on the internet today. To create its visualizations, it parses JSON layout files, generates individual key images, and composites them together, all in under a second. I wrote KLE-Render in Python using Flask, Pillow, Solidworks, and Blender. Building it was a great way for me to learn about maintaining open source projects while building useful tools for a larger community.

{{ button(title="Website", url="http://kle-render.herokuapp.com") }}
{{ button(title="Github Repo", url="https://github.com/CQCumbers/kle_render") }}
{% end %}


{% card(image="scibowldb.png") %}
# SciBowlDB

With over 16,000 categorized questions, ScibowlDB is the largest database of DOE Science Bowl questions available online, and an invaluable resource for high school science bowl teams across the US. Its web interface helps you search for specific questions to study, simulate infinite practice rounds, and create randomized questions sets for team meetings or scrimmages. SciBowlDB was built with Python, Flask, and SQL, and deployed on Heroku. As my first major web application, it taught me a great deal about full-stack web development and handling large, irregular data sets.

{{ button(title="Website", url="https://scibowldb.com") }}
{{ button(title="Github Repo", url="https://github.com/CQCumbers/scibowldb") }}
{% end %}
