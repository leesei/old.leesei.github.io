---
title: Computer Graphics
categories:
  - comp
tags:
  - null
toc: true
date: 2016-10-18 14:30:58
---

[GPU Hierarchy - Comparison of Graphics Cards for Gaming](http://www.tomshardware.com/reviews/gpu-hierarchy,4388.html)
[How Rendering Graphics Works in Games! - YouTube](https://www.youtube.com/watch?v=cvcAjgMUPUA)

[How Do Graphics Cards Work? - ExtremeTech](https://www.extremetech.com/gaming/269335-how-graphics-cards-work)

RAM of GPU matters the most on high texture and output resolution.

[A REVOLUTION in graphics is coming - YouTube](https://www.youtube.com/watch?v=i537qwchiAw)
[A REVOLUTION in graphics #2 - YouTube](https://www.youtube.com/watch?v=h8H_7VguCzg)
[The History of the Modern Graphics Processor](https://www.techspot.com/article/650-history-of-the-gpu/)

[Scratchapixel](https://www.scratchapixel.com/index.php) Learn Computer Graphics From Scratch!

[ICTGraphicsLab - YouTube](https://www.youtube.com/channel/UCOgm-72B_tibAM2I5j-mBiQ)

## History

[A Brief History of Graphics - YouTube](https://www.youtube.com/watch?v=QyjyWUrHsFc)
[A Brief History of Graphics - YouTube](https://www.youtube.com/playlist?list=PLOQZmjD6P2HlOoEVKOPaCFvLnjP865X1f) series
[The 30 Year History of AMD Graphics, In Pictures](http://www.tomshardware.com/picturestory/735-history-of-amd-graphics.html)
[The History Of Nvidia GPUs](http://www.tomshardware.com/picturestory/715-history-of-nvidia-gpus.html)

[【科技杂谈 79】从 GTX 到 RTX，NVIDIA GEFORCE 显卡家族的历史（1999-2019） - YouTube](https://www.youtube.com/watch?v=UUxUCVlXV0A)

极客湾 Geekerwan
[20 年前的游戏与 PC：探秘 3D 游戏史上最辉煌的岁月（上） - YouTube](https://www.youtube.com/watch?v=TeJ2IFae2-0)
[N 卡是如何崛起的？20 年前的 PC 和游戏（下） - YouTube](https://www.youtube.com/watch?v=JsVfKeJKJu0)
[A 卡崛起之路：重现当年 AN 显卡巅峰对决！ - YouTube](https://www.youtube.com/watch?v=BlI9PVQA8ZA)

## Antialiasing

[Anti-aliasing - Wikiwand](http://www.wikiwand.com/en/Anti-aliasing)
[Spatial anti-aliasing - Wikiwand](http://www.wikiwand.com/en/Spatial_anti-aliasing)
[TweakGuides.com - Crysis 3 Tweak Guide](http://www.tweakguides.com/Crysis3_6.html)

[Tech Focus: Anti-Aliasing - What Is It And Why Do We Need It? - YouTube](https://www.youtube.com/watch?v=NbrA4Nxd8Vo)
[【硬件科普】免费提升画质和帧数？详解 DLSS2.0 的工作原理与作用 - YouTube](https://www.youtube.com/watch?v=Hi5vbf7sdVQ)

FXAA does AA on full screen post-processing and may introduce blurriness
SMAA based on MLAA post-processing and may add temporal AA to the mix (which causes shadows for slow moving objects) \*
TSSAA/TXAA uses temporal information (previous frames) to do AA, but the averaging may cause blurring/ghosting
MSAA is the traditional approach but takes more resources, only super sample on polygon edges
SSAA super sample AA, super sample on all pixels
DLAA Deep learning Super Sampling (nVidia) AA

## Ray Tracing

[Ray Tracing Resources Page](http://www.realtimerendering.com/raytracing.html)
[Ray Tracing Gems](https://www.realtimerendering.com/raytracinggems/)
[Call for Participation: Ray Tracing Gems II](https://www.realtimerendering.com/raytracinggems/rtg2/index.html)

[Ray Tracing in Games: How Today's Big Tech Gamble Became Tomorrow's Sure Thing [Sponsored] - YouTube](https://www.youtube.com/watch?v=SJ0NzZAkPlo)
[Ray Tracing Essentials Part 1: Basics of Ray Tracing – NVIDIA Developer News Center](https://news.developer.nvidia.com/ray-tracing-essentials-part-1-basics-of-ray-tracing/)
[Ray Tracing Essentials Part 2: Rasterization versus Ray Tracing – NVIDIA Developer News Center](https://news.developer.nvidia.com/ray-tracing-essentials-part-2-rasterization-versus-ray-tracing/)
[Ray Tracing Essentials Part 3: Ray Tracing Hardware – NVIDIA Developer News Center](https://news.developer.nvidia.com/ray-tracing-essentials-part-3-ray-tracing-hardware/)
[Ray Tracing Essentials Part 4: The Ray Tracing Pipeline – NVIDIA Developer News Center](https://news.developer.nvidia.com/ray-tracing-essentials-part-4-the-ray-tracing-pipeline/)

[What's the Deal With Raytracing? - YouTube](https://www.youtube.com/watch?v=lyfTPG-dwOE)
[NVIDIA RTX In 2020 - STILL Not Worth It? - YouTube](https://www.youtube.com/watch?v=QETexVf8Gz8)

[Intel® Embree](https://www.embree.org/)

## Hardware Scheduling

[Faster Gaming for FREE - Hardware GPU Scheduling Explained - YouTube](https://www.youtube.com/watch?v=47VDnHyCUig)

## API

> see `khronos-group.md`
> see `khronos-group.md#vulkan`

The next gen API all focus on exposing the low level GPU hardware to software developer.

[Reaching Console Performance: Shader Intrinsic Functions | techPowerUp](https://www.techpowerup.com/226960/closer-to-the-metal-shader-intrinsic-functions)
[WTF is going on with DX12 and Vulkan? - YouTube](https://www.youtube.com/watch?v=r0fgEVEgK_k)
[Does DirectX 12 Suck? - YouTube](https://www.youtube.com/watch?v=ApvTaSAG--4)

[WTF is going on with SLI? - YouTube](https://www.youtube.com/watch?v=A91BPapLK38)
Adapters are linked if they are close to the same hardware, unlinked otherwise.
Implicit Mode (linked implicitly) (IMA, Implicit Multiadaptor) is SLI/Crossfire.
Explicit Modes (EMA, Explicit Multiadaptor) can work on linked and unlinked hardware.

### DX12

[Exclusive: The Nvidia and AMD DirectX 12 Editorial - Complete DX12 Graphic Card List with Specifications, Asynchronous Shaders and Hardware Features Explained](http://wccftech.com/nvidia-amd-directx-12-graphic-card-list-features-explained/) !important
[DirectX 12 tested: An early win for AMD and disappointment for Nvidia | Ars Technica](http://arstechnica.com/gaming/2015/08/directx-12-tested-an-early-win-for-amd-and-disappointment-for-nvidia/)
[Multi-GPU DirectX 12 shootouts show AMD with performance lead over Nvidia | Ars Technica](http://arstechnica.com/gaming/2016/02/directx-12-amd-and-nvidia-gpus-finally-work-together-but-amd-still-has-the-lead/)
[Direct3D 12 Glossary (Windows)](https://msdn.microsoft.com/en-us/library/windows/desktop/dn899119(v=vs.85%29.aspx)

Asynchronous compute shaders in DX12 benefits the most when CPU is the bottleneck

### Mental

[Mantle Graphics API | AMD](http://www.amd.com/mantleen-us/innovations/software-technologies/technologies-gaming/mantle)

[Gaming: One of Mantle's Futures: Vulkan | Community](https://community.amd.com/community/gaming/blog/2015/05/12/one-of-mantles-futures-vulkan) Chronos Group has chosen the best and brightest parts of Mantle to serve as the foundation for "Vulkan"
[Gaming: On APIs and the future of Mantle | Community](https://community.amd.com/community/gaming/blog/2015/05/12/on-apis-and-the-future-of-mantle) AMD recommends DX12 or Vulcan
[Mantle is a Vulkan: AMD's dead graphics API rises from the ashes in OpenGL's successor | PCWorld](http://www.pcworld.com/article/2894036/mantle-is-a-vulkan-amds-dead-graphics-api-rises-from-the-ashes-as-opengls-successor.html)
[AMD's Mantle 1.0 is dead; long live DirectX | PCWorld](http://www.pcworld.com/article/2891672/amds-mantle-10-is-dead-long-live-directx.html)

---

# Hardware

## NVIDIA

[NVIDIA's next-gen Ampere GPUs will arrive in 2020 on 7nm](https://www.tweaktown.com/news/64340/nvidias-next-gen-ampere-gpus-arrive-2020-7nm/index.html)
[NVIDIA GeForce RTX 3080/3080 Ti: more VRAM, way faster and CHEAPER?!](https://www.tweaktown.com/news/68455/nvidia-geforce-rtx-3080-ti-more-vram-way-faster-cheaper/amp.html)

## AMD

[AMD's next-gen Navi GPU confirmed to support ray tracing](https://www.tweaktown.com/news/65582/amds-next-gen-navi-gpu-confirmed-support-ray-tracing/index.html)
