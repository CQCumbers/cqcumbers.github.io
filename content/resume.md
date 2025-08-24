+++
title = "Resume"
template = "resume.html"

[extra]
name = "Alexander Zhang"

[[extra.contact]]
name = "Email"
link = "mailto:alexbrianzhang@gmail.com"
print = "alexbrianzhang@gmail.com"
public = false

[[extra.contact]]
name = "Portfolio"
link = "https://cqcumbers.com"
print = "cqcumbers.com"
public = true

[[extra.contact]]
name = "Github"
link = "https://github.com/cqcumbers"
print = "github.com/cqcumbers"
public = false
+++

## Work Experience

{{ heading(name="Software Engineer, Topaz Labs", date="2021-") }}
- Released Gigapixel v5.7-6.3 as solo dev, adding face recovery, ARM support, etc.
- Designed and maintained image processing pipeline for all image processing apps
- Wrote cross-platform inference code for Nvidia/AMD/Apple/Intel GPUs & NPUs
- Worked with vendors to optimize GAN & diffusion models for edge deployment

{{ heading(name="Intern, UM Real Time Water Systems Lab", date="2019-20") }}
- Designed and wrote cooperative multitasking OS for Cortex-M3 based systems
- Developed LTE modem driver, OTA update decompressor, and HTTP request parser

{{ heading(name="Intern, UConn Hydroclimatology Lab", date="2017") }}
- Processed and analyzed regional climate model data from NCAR supercomputers

## Education

{{ heading(name="University of Michigan College of Engineering", date="2018-21") }}
- B.S.E. in Computer Science from College of Engineering

## Selected Projects

{{ heading(name="Minaret") }}
- Wrote LLVM backend and toolchain ports for RISC instruction set
- Implemented multicycle CPU, DDR3 controller, display, etc. on FPGA
- Ported Doom, Coremark, and other software to custom SoC design

{{ heading(name="Navi Search") }}
- Search engine for over 400 million pages written from scratch in C++
- Worked with team of 6 over 4 months to develop crawler, index, etc.

{{ heading(name="Nmulator") }}
- Experimental Nintendo 64 emulator that boots many commercial games
- Wrote MIPS to x64 JIT compiler, including SIMD instruction handling
- Emulated RDP using software rasterization in a Vulkan compute shader

{{ heading(name="KLE-Render") }}
- Webapp for making mockups of custom keyboard layouts and keycap set designs
- Widely used by keycap set designers, >200 mockups generated daily in 2019

## Technical Skills

- C, C++, Python, Javascript, Java, Swift, OCaml, SQL, HTML/CSS, x86/ARM/MIPS, HLSL
- CUDA, ONNX, Pytorch, TensorRT, CoreML, OpenVINO, Vulkan, Qt, Ghidra, Git
