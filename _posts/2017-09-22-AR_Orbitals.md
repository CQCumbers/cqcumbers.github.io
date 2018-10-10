---
title: AR Orbitals
video: ar_orbitals.mp4
links: 
- title: App Store
  url: https://itunes.apple.com/us/app/ar-orbitals/id1299537037
---

AR Orbitals is an iOS app that visualizes the shapes of electron clouds by solving Schrodinger's equations, volume tracing the result, and displaying the volume traced field visualization within the real world. It was written over a weekend with C#, Unity, and Vuforia. To create AR Orbitals, I had to implement the Legendre and Laguerre polynomials, write volume tracing code for mobile GPUs, and integrate Vuforia's augmented reality toolkit with my custom shaders. This taught me a lot about not only wavefunctions, but also C#, Unity, and GPU programming.

AR Orbitals was entirely designed as a learning experience, to help me better understand the shapes of molecular orbitals by actually calculating and visualizing them. I find that the app really helps with getting a sense of the three dimensional shapes of wavefunctions as entire density distributions (most visualizations only show isosurfaces) and for getting a sense of the scales of the wavefunctions, as one must manually change the spatial size of the volume rendered, and the scale of the gradient to get good looking results. You can really see how much larger a 3d orbital is than a 1s orbital, and also how much lower the electron probabilities are over the entire distribution. The entire project was done over one weekend (leaving little room for sleep!), and in addition to calculating wavefunctions for the first time it was also my first time using Unity, C#, and HLSL shader language, not to mention Vuforia's augmented reality tracking API, so I think I learned a great deal in trying to build this app. Now I am much more comfortable with these tools and look forward to using them in other projects. The idea of augmented reality data visualizations is also an exciting one and I'm sure I'll come up with related ideas in the future.
