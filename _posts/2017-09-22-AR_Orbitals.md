---
title: AR Orbitals
image: ar_orbitals.gif
links: 
- title: App Store
  url: 
---

AR Orbitals is an app that visualize the shapes of electron orbitals in augmented reality. It does this by solving Schrodinger's equations for electron probability in a hydrogen-like atom at runtime, for any valid set of quantumn numbers. I implemented all of the necessary mathematical functions for this, such as Legendre and Laguerre polynonomials, in Unity C#, so that I could integrate the Vuforia AR toolkit and some existing volume-tracing code (which I customized heavily to render transparency and color gradients as well as preform better on mobile GPUs) to actually render the wavefuntions as an augmented reality, translucent object that one can look around and handle, using a printed tracking target.

AR Orbitals was entirely designed as a learning experience, to help me better understand the shapes of molecular orbitals by actually calculating and visualizing them. I find that the app really helps with getting a sense of the three dimensional shapes of wavefunctions as entire density distributions (most visualizations only show isosurfaces) and for getting a sense of the scales of the wavefunctions, as one must manually change the spatial size of the volume rendered, and the scale of the gradient to get good looking results. You can really see how much larger a 3d orbital is than a 1s orbital, and also how much lower the electron probabilities are over the entire distribution. The entire project was done over one weekend (leaving little room for sleep!), and in addition to calculating wavefunctions for the first time it was also my first time using Unity, C#, and HLSL shader language, not to mention Vuforia's augmented reality tracking API, so I think I learned a great deal in trying to build this app. Now I am much more comfortable with these tools and look forward to using them in other projects. The idea of augmented reality data visualizations is also an exciting one and I'm sure I'll come up with related ideas in the future.

I'm still working on polishing the app and getting it distributed on the app store. In the meantime you can see some examples of ARbitron's functionality below.
