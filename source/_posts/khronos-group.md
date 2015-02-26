title: Khronos Group
toc: true
date: 2015-01-05 15:58:27
tags:
- open-gl
---

[Khronos Group 3D Graphics Specs](http://en.wikipedia.org/wiki/Khronos_Group)
- [OpenGL](http://en.wikipedia.org/wiki/OpenGL)
- [OpenGL ES](http://en.wikipedia.org/wiki/OpenGL_ES)
- [WebGL](http://en.wikipedia.org/wiki/WebGL)

EGL is an interface between Khronos rendering APIs (such as OpenGL ES or OpenVG) and the underlying native platform windowing system. EGL handles graphics context management, surface/bufferbinding, rendering synchronization, and enables "high-performance, accelerated, mixed-mode 2D and 3Drendering using other Khronos APIs."

## Shading Languages

http://en.wikipedia.org/wiki/Shader
[High-level shading language (HLSL)](http://en.wikipedia.org/wiki/High-level_shader_language) by Microsoft
[OpenGL Shading Language (GLSL/GLslang)](http://en.wikipedia.org/wiki/GLSL) by Khronos Group
[Cg (C for Graphics)](http://en.wikipedia.org/wiki/Cg_(programming_language)) by Nvidia, enables programmer to use C-like syntax to create shaders, generate HLSL or GLSL code.
The shader programs are loaded to a OpenGL application (context/shell) for execution.
http://www0.cs.ucl.ac.uk/staff/ucacbbl/cigpu2008/slides/shader-vs-cuda.pdf

## [GPGPU](http://en.wikipedia.org/wiki/GPGPU)

[CUDA](http://en.wikipedia.org/wiki/CUDA) provides an architecture for general-purpose computation in GPU, and is more flexible then shading languages in terms of memory access but lacks some of the graphic specific features. The program is loaded as "kernel" to the GPU without a need for graphic "shell". The host and kenels can communicate and synchronize with each other.
CUDA sits on top of specific language such as  OpenCL, DirectX, CUDA C. 

[OpenCL](http://en.wikipedia.org/wiki/OpenCL) is a framework for writing programs that execute across heterogeneous platforms consisting of central processing units (CPUs), graphics processing units (GPUs), digital signal processors (DSPs) and other processors.
HLSL 5.0 for DirectX 11 is going to add new GPGPU functions like CUDA that also works for AMD's and Intel's GPU.
These GPGPU framework can access the GPU without needing a graphics context.
Programmers that need to be platform agnostic will have to stick to GLSL before OpenCL is widely supported.
http://stackoverflow.com/questions/982911/cuda-opencl-pgi-etc-but-what-happened-to-glsl-and-cg

OpenCV

All OpenXXX are frameworks and API that require driver implementation by chip vendor.
