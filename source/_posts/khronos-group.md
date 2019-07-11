---
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
- [OpenGL ES](http://www.wikiwand.com/en/OpenGL_ES) (subset of OpenGL for embedded systems)
- [WebGL](http://www.wikiwand.com/en/WebGL) (share spec with OpenGL ES)

EGL is an interface between Khronos rendering APIs (such as OpenGL ES or OpenVG) and the underlying native platform windowing system. EGL handles graphics context management, surface/bufferbinding, rendering synchronization, and enables "high-performance, accelerated, mixed-mode 2D and 3Drendering using other Khronos APIs."

[OpenGL – Then and Now | Cognitive Waves](https://cognitivewaves.wordpress.com/2015/04/24/opengl-then-and-now/)

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

However, OpenGL ES3 have compute shader and async read the provides most of the feature of OpenCL.

## OpenCV

> see `opencv.md`

All OpenXXX are frameworks and API that require driver implementation by chip vendor.

## OpenCL

> see `android-notes#renderscript`

[Khronos OpenCL Registry](https://www.khronos.org/registry/OpenCL/)
[OpenCL 1.2: High-Level Overview by AJ.Gullon | MooCow develop notes](http://kywk.github.io/moco/dev/graphic/opencl_opencl-12-high-level-overview.html)

x86 的 OpenCL 要注意的是 memory bus 的速度，因為 GPU 的記憶體和 RAM 的溝通很花時間，所以 x86 版本除了 AMD 的 APU 之外都要特別小心這件事

[OpenCL on Mobile Devices | ArrayFire](http://arrayfire.com/opencl-on-mobile-devices/)
[Getting Started with OpenCL on Android | ArrayFire](https://arrayfire.com/getting-started-with-opencl-on-android/)
[TzuTaLin's blog: OpenCL on Android](http://tzutalin.blogspot.hk/2016/06/opencl-on-android.html)

**ARM**
http://malideveloper.arm.com/develop-for-mali/sdks/mali-opencl-sdk/
Mali T604 | Samsung Exynos 5250 | Nexus 10

```sh
<toolchain>/bin/arm-linux-androideabi-gcc main.cpp -lm -lstdc++ \
-l<android_src>/out/target/product/arndale/system/vendor/lib/egl/libGLES_mali.so -o test_opencl
```

**Imageon** (formerly ATI Imageon, now Qualcomm's subsidary)
https://developer.qualcomm.com/discover/chipsets-and-modems/adreno-gpu

Adreno 305 | Qualcomm MSM8x2x, MSM8x3x, APQ8030 | 
Adreno 320 | Qualcomm S4 Pro (APQ8064, MSM8960T), S4 Prime | Nexus 4, XiaoMi2, Sony Xperia Z

**Imagination PowerVR**
http://forum.imgtec.com/discussion/2532/opencl-sdk-or-driver
Although our Series5 and Series6 GPUs are capable of supporting the API, there are currently no public devices with our GPUs that expose OpenCL.

SGX 540 | Intel Atom | Motorola RAZR !
SGX 543MP2 | Apple A5 | iPhone4S, iPad2
SGX 543MP3 | Apple A6 | iPhone5
SGX 543MP4 | Apple A5X | iPad3

**Nvidia**
Tegra 3 T30L | Tegra 3 T30L | Nexus 7

## WebGL

> see `web-3d.md`

## Vulkan 

[Vulkan - Industry Forged](https://www.khronos.org/vulkan/)
[Vulkan (API) - Wikiwand](https://www.wikiwand.com/en/Vulkan_%28API%29)
Vulkan is the successor to OpenGL. It aims to offer lower-level access to the graphics hardware to improve rendering performance.

[Vulkan in 30 minutes](https://renderdoc.org/vulkan-in-30-minutes.html)
[Introduction To Vulkan API | Toptal](https://www.toptal.com/api-developers/a-brief-overview-of-vulkan-api/)
[Transitioning from OpenGL to Vulkan](https://developer.nvidia.com/transitioning-opengl-vulkan)
[What is Vulkan and how does it differ from OpenGL? - Game Development Stack Exchange](http://gamedev.stackexchange.com/questions/96014/what-is-vulkan-and-how-does-it-differ-from-opengl)
[Vulkan 1.0 Graphics API Brings Cross-Platform Performance Boost; Intel, AMD, Nvidia Contribute](http://www.tomshardware.com/news/khronos-group-vulkan-1-api,31207.html)
[Khronos unveils Vulkan: OpenGL built for modern systems | Ars Technica UK](http://arstechnica.co.uk/gadgets/2015/03/khronos-unveils-vulkan-opengl-built-for-modern-systems/)
[Vulkan now official, with 1.0 API release and AMD driver [Updated] | Ars Technica](http://arstechnica.com/gaming/2016/02/vulkan-gets-official-with-1-0-release-and-amd-driver/)

[googlesamples/android-vulkan-tutorials: A set of samples to illustrate Vulkan API on Android](https://github.com/googlesamples/android-vulkan-tutorials)
[googlesamples/vulkan-basic-samples](https://github.com/googlesamples/vulkan-basic-samples)

[Make shinier, faster mobile games with Vulkan - Google I/O 2016 - YouTube](https://www.youtube.com/watch?v=zV_H3QzRhuI)

### Shaders

Compile GLSL to SPIR-V with `shaderc` or `glslang`

## Cinder

[Cinder](https://libcinder.org/) is C++ creating coding framework built upon OpenGL on desktop and OpenES on mobile. Vulkan support is added.

## Resources

[AdrienHerubel-imgui](https://github.com/AdrienHerubel/imgui)
[GLEW- The OpenGL Extension Wrangler Library](http://glew.sourceforge.net/)
[GLFW - An OpenGL library](http://www.glfw.org/)
[News - pygame - python game development](http://www.pygame.org/news.html)
[Simple DirectMedia Layer - Homepage](http://www.libsdl.org/)

[baldurk/renderdoc: RenderDoc is a stand-alone graphics debugging tool.](https://github.com/baldurk/renderdoc)
