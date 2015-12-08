title: "Khronos Group"
date: 2015-01-05 15:58:27
categories:
- comp.lang
tags:
- opengl
- webgl
toc: true
---

[Khronos Group 3D Graphics Specs](http://www.wikiwand.com/en/Khronos_Group)
- [OpenGL](http://www.wikiwand.com/en/OpenGL)
- [OpenGL ES](http://www.wikiwand.com/en/OpenGL_ES)
- [WebGL](http://www.wikiwand.com/en/WebGL)

EGL is an interface between Khronos rendering APIs (such as OpenGL ES or OpenVG) and the underlying native platform windowing system. EGL handles graphics context management, surface/bufferbinding, rendering synchronization, and enables "high-performance, accelerated, mixed-mode 2D and 3Drendering using other Khronos APIs."

## Shading Languages

[Shader - Wikiwand](http://www.wikiwand.com/en/Shader)
[High-Level Shading Language (HLSL) - Wikiwand](http://www.wikiwand.com/en/High-Level_Shading_Language) by Microsoft
[OpenGL Shading Language (GLSL/GLslang) - Wikiwand](http://www.wikiwand.com/en/OpenGL_Shading_Language) by Khronos Group
[Cg (programming language) - Wikiwand](http://www.wikiwand.com/en/Cg_%28programming_language%29) by Nvidia, enables programmer to use C-like syntax to create shaders, generate HLSL or GLSL code.
The shader programs are loaded to a OpenGL application (context/shell) for execution.
http://www0.cs.ucl.ac.uk/staff/ucacbbl/cigpu2008/slides/shader-vs-cuda.pdf

[Primer : Shaders](http://notes.underscorediscovery.com/shaders-a-primer/)
[Shaders : second stage](http://notes.underscorediscovery.com/shaders-second-stage/)

## [GPGPU](http://en.wikipedia.org/wiki/GPGPU)

[CUDA](http://en.wikipedia.org/wiki/CUDA) provides an architecture for general-purpose computation in GPU, and is more flexible then shading languages in terms of memory access but lacks some of the graphic specific features. The program is loaded as "kernel" to the GPU without a need for graphic "shell". The host and kenels can communicate and synchronize with each other.
CUDA sits on top of specific language such as  OpenCL, DirectX, CUDA C. 

[OpenCL](http://en.wikipedia.org/wiki/OpenCL) is a framework for writing programs that execute across heterogeneous platforms consisting of central processing units (CPUs), graphics processing units (GPUs), digital signal processors (DSPs) and other processors.
HLSL 5.0 for DirectX 11 is going to add new GPGPU functions like CUDA that also works for AMD's and Intel's GPU.
These GPGPU framework can access the GPU without needing a graphics context.
Programmers that need to be platform agnostic will have to stick to GLSL before OpenCL is widely supported.
http://stackoverflow.com/questions/982911/cuda-opencl-pgi-etc-but-what-happened-to-glsl-and-cg

## OpenCV

> TODO: add link to [opencv]

All OpenXXX are frameworks and API that require driver implementation by chip vendor.

## OpenCL

[OpenCL 1.2: High-Level Overview by AJ.Gullon | MooCow develop notes](http://kywk.github.io/moco/dev/graphic/opencl_opencl-12-high-level-overview.html)

## WebGL

http://get.webgl.org/
chrome://gpu/
chrome://flags/

[WebGL Essentials - Tuts+ Code Tutorials](http://code.tutsplus.com/series/webgl-essentials--net-35335)
[Introduction To Polygonal Modeling And Three.js – Smashing Magazine](http://www.smashingmagazine.com/2013/09/introduction-to-polygonal-modeling-and-three-js/)

## Resources

[AdrienHerubel-imgui](https://github.com/AdrienHerubel/imgui)
[GLEW- The OpenGL Extension Wrangler Library](http://glew.sourceforge.net/)
[GLFW - An OpenGL library](http://www.glfw.org/)
[News - pygame - python game development](http://www.pygame.org/news.html)
[Simple DirectMedia Layer - Homepage](http://www.libsdl.org/)
