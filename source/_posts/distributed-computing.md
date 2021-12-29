---
title: Distributed Computing
categories:
  - web
tags:
  - null
toc: true
date: 2016-09-21 23:05:16
---

> FIXME: some info are for distributed computing, some are for hardware (GPU) acceleration
> see `data-analytics.md`
> see `data-analytics-python.md`

[9 crushing performance problems in scalable systems | InfoWorld](http://www.infoworld.com/article/3211526/database/9-crushing-performance-problems-in-scalable-systems.html)
[Get more done at the Linux command line with GNU Parallel | Opensource.com](https://opensource.com/article/18/5/gnu-parallel)

[The Cluster Documentation Project » ADMIN Magazine](http://www.admin-magazine.com/HPC/Articles/Cluster-Documentation-Project)
[Cluster Documentation Project](https://cdp.clustermonkey.net/index.php/Main_Page)

[Multigrid method - Wikiwand](https://www.wikiwand.com/en/Multigrid_method)
[Fallacies of distributed computing - Wikiwand](https://www.wikiwand.com/en/Fallacies_of_distributed_computing)
[Understanding the 8 Fallacies of Distributed Systems - DZone Microservices](https://dzone.com/articles/understanding-the-8-fallacies-of-distributed-syste)

[Four Distributed Systems Architectural Patterns by Tim Berglund - YouTube](https://www.youtube.com/watch?v=tpspO9K28PM)

[HPC » ADMIN Magazine](http://www.admin-magazine.com/HPC)
[Parallelizing Code – Loops » ADMIN Magazine](http://www.admin-magazine.com/HPC/Articles/OpenACC-Parallelizing-Loops)

[Jepsen: On the perils of network partitions](https://aphyr.com/posts/281-call-me-maybe-carly-rae-jepsen-and-the-perils-of-network-partitions)
[Strong consistency models](https://aphyr.com/posts/313-strong-consistency-models)
[The network is reliable](https://aphyr.com/posts/288-the-network-is-reliable)
[Burn the Library](https://aphyr.com/posts/254-burn-the-library)

[Tick or Tock? Keeping Time and Order in Distributed Databases| PingCAP](https://pingcap.com/blog/Time-in-Distributed-Systems/)

A split brain is what happens when you have multiple autonomous sub-clusters forming, and more than one believe they're the "master". This can cause irreconcilable changes and data loss.

[分布式系统的事务处理 | | 酷 壳 - CoolShell](https://coolshell.cn/articles/10910.html)
[Paxos (computer science) - Wikiwand](<https://www.wikiwand.com/en/Paxos_(computer_science)>)

[Raft Consensus Algorithm](https://raft.github.io/)
[Raft (computer science) - Wikiwand](<http://www.wikiwand.com/en/Raft_(computer_science)>)

[Google I/O 2009 - Transactions Across Datacenters.. - YouTube](https://www.youtube.com/watch?v=srOgpXECblk)
[Debugging Incidents in Google’s Distributed Systems - ACM Queue](https://queue.acm.org/detail.cfm?id=3404974)

[How to do distributed locking — Martin Kleppmann’s blog](https://martin.kleppmann.com/2016/02/08/how-to-do-distributed-locking.html)
[Distributed Locks Are Dead, Long Live Distributed Locks - DZone Java](https://dzone.com/articles/distributed-locks-are-dead-long-live-distributed-l)

## Byzantine Fault Tolerance

[Byzantine fault - Wikiwand](https://www.wikiwand.com/en/Byzantine_fault)
[Byzantine Fault Tolerance Explained | Binance Academy](https://academy.binance.com/blockchain/byzantine-fault-tolerance-explained)

## Concurrency and Parallelism

[Concurrency is not parallelism - The Go Blog](http://blog.golang.org/concurrency-is-not-parallelism)
[The Way of the Gopher. Making the Switch from Node.js to… | by Alexandra Bueno | Digg Data | Medium](https://medium.com/digg-data/the-way-of-the-gopher-6693db15ae1f#.h4j5b62nh)

[Asynchronous vs Multithreading and Multiprocessing Programming (The Main Difference) - YouTube](https://www.youtube.com/watch?v=0vFgKr5bjWI&t=10s)

[Seven Concurrency Models in Seven Weeks: When Threads Unravel by Paul Butcher | The Pragmatic Bookshelf](https://pragprog.com/book/pb7con/seven-concurrency-models-in-seven-weeks)
[Thinking Concurrently: How Modern Network Applications Handle Multiple Connections | Linux Journal](https://www.linuxjournal.com/content/thinking-concurrently)
[还在疑惑并发和并行？ - laike9m's blog](https://laike9m.com/blog/huan-zai-yi-huo-bing-fa-he-bing-xing,61/)

[Parallel vs Concurrent in Node.js](http://bytearcher.com/articles/parallel-vs-concurrent/)
[Concurrent JavaScript: It can work! | WebKit](https://webkit.org/blog/7846/concurrent-javascript-it-can-work/)
[Concurrency model and Event Loop - JavaScript | MDN](https://developer.mozilla.org/en/docs/Web/JavaScript/EventLoop)

[The Little Book of Semaphores – Green Tea Press](https://greenteapress.com/wp/semaphores/)

## Node.js

[Mostafa-Samir/klyng: A message-passing distributed computing framework for node.js](https://github.com/Mostafa-Samir/klyng)

[bithound/farm.bithound.io: “All animals are equal, but some animals are more equal than others.”](https://github.com/bithound/farm.bithound.io) a simple "framework" that bitHound used for working in a distributed environment; uses ZeroMQ

[substack/dnode: turtles all the way down rpc](https://github.com/substack/dnode)
[substack/dnode-protocol: Implements the dnode protocol abstractly in node.js](https://github.com/substack/dnode-protocol)

[substack/fleet: multi-server continuous git-based deployment and process management](https://github.com/substack/fleet)
[substack/seaport: semver service registry for clusters](https://github.com/substack/seaport)
[substack/airport: role-based port management for upnode](https://github.com/substack/airport)

## Python

[pyamgx – Accelerated Python Library » ADMIN Magazine](http://www.admin-magazine.com/HPC/Articles/pyamgx-Accelerated-Python-[[Library]]) algebraic multigrid

[Scale your pandas workflow by changing a single line of code. — Modin documentation](https://modin.readthedocs.io/en/latest/) Pandas API on Ray/Dask
[Ray documentation](https://ray.readthedocs.io/en/latest/)
[Dask: Scalable analytics in Python](https://dask.org/)

[High-Performance Python – Distributed Python » ADMIN Magazine](https://www.admin-magazine.com/HPC/Articles/High-Performance-Python-4/)

## ArrayFire

[ArrayFire | Faster Code](https://arrayfire.com/)
[Blog | ArrayFire](https://arrayfire.com/blog/)
[ArrayFire Users - Google Groups](https://groups.google.com/forum/#!forum/arrayfire-users)

[Configuring ArrayFire Environment](http://arrayfire.org/docs/configuring_environment.htm)

The API docs seems outdated, source code may provide some functions not in the doc
[Docs Overview](http://arrayfire.org/docs/index.htm)
[Docs Tutorials](http://arrayfire.org/docs/usergroup0.htm)
[Docs Functions](http://arrayfire.org/docs/modules.htm)
[Docs Complete List of ArrayFire Functions](http://arrayfire.org/docs/group__arrayfire__func.htm)

[arrayfire/arrayfire: ArrayFire: a general purpose GPU library.](https://github.com/arrayfire/arrayfire)
[arrayfire/arrayfire-python: Python bindings for ArrayFire: A general purpose GPU library.](https://github.com/arrayfire/arrayfire-python)
[arrayfire/arrayfire-rust: Rust wrapper for ArrayFire](https://github.com/arrayfire/arrayfire-rust)

### Build

[Home · arrayfire/arrayfire Wiki](https://github.com/arrayfire/arrayfire/wiki)
[Jetson/Installing ArrayFire - eLinux.org](https://elinux.org/Jetson/Installing_ArrayFire)

ArrayFire master branch (3.7) as of 20190801 reports "Unsupported compiler Intel" upon build. Use official 3.6 release.

ArrayFire 3.6

- reports "Unsupported platform" on Ubuntu 16.04, requires CMake 3.8+
- requires `glibc` 2.27 at runtime (included in Ubuntu 18.04)

CUDA 10 requires CMake 3.12.3 (need to build from source on Ubuntu 18.04)

For PC it's easiest to install the [prebuilt binary](https://arrayfire.com/download/).

## GPU

[How GPUs are Beginning to Displace Clusters for Big Data & Data Science - By Dan Voyce](https://hackernoon.com/how-gpus-are-beginning-to-displace-clusters-for-data-science-opbn36pv)

[AmgX | NVIDIA Developer](https://developer.nvidia.com/amgx) algebraic, physics
[AmgX: Multi-Grid Accelerated Linear Solvers for Industrial Applications](https://devblogs.nvidia.com/amgx-multi-grid-accelerated-linear-solvers-industrial-applications/)

[PyOpenCL](https://mathema.tician.de/software/pyopencl/)

[NVIDIA GPUDirect | NVIDIA Developer](https://developer.nvidia.com/gpudirect)
[GPU 通信技术初探（一）](https://www.infoq.cn/article/3D4MsRVS8ZOtGCj7*krT)
[How to Overlap Data Transfers in CUDA C/C++ | NVIDIA Developer Blog](https://devblogs.nvidia.com/how-overlap-data-transfers-cuda-cc/)

[What differences and relations between SVM, HSA, HMM and Unified Memory](https://lists.linuxfoundation.org/pipermail/iommu/2017-June/022391.html)
[7 Years Late is Better than Never. - YouTube](https://www.youtube.com/watch?v=JGvrXXonoqM)
IOMMU: passthrough PCIe devices to VM (AMI-Vi/VT-d)

### CUDA

> see `docker-nvidia.md`

[CUDA - Wikiwand](https://www.wikiwand.com/en/CUDA)
[Programming Guide :: CUDA Toolkit Documentation](https://docs.nvidia.com/cuda/cuda-c-programming-guide/index.html)
[An Even Easier Introduction to CUDA | NVIDIA Developer Blog](https://developer.nvidia.com/blog/even-easier-introduction-cuda/)

[PyCUDA](https://mathema.tician.de/software/pycuda/)

[Intro to Parallel Programming CUDA - Udacity 458 - YouTube](https://www.youtube.com/playlist?list=PLGvfHSgImk4aweyWlhBXNF6XISY3um82_)

[Home - CUDA Tutorial](https://cuda-tutorial.readthedocs.io/en/latest/)
[Imaging and Computer Vision |NVIDIA](https://www.nvidia.com/object/imaging_comp_vision.html)

[NVIDIA Collective Communications Library (NCCL) | NVIDIA Developer](https://developer.nvidia.com/nccl) multi-GPU and multi-node collective communication primitives

### Triton

[Welcome to Triton’s documentation! — Triton documentation](https://triton-lang.org/)
[openai/triton: Development repository for the Triton language and compiler](https://github.com/openai/triton)

[Introducing Triton: Open-Source GPU Programming for Neural Networks](https://openai.com/blog/triton/)
[Wanna use your Nvidia GPU for acceleration but put off by CUDA? OpenAI has a Python-based alternative • The Register](https://www.theregister.com/2021/08/02/nvidia_cuda_openai/?td=keepreading-btm)

## MPI

[Message Passing Interface - Wikiwand](https://www.wikiwand.com/en/Message_Passing_Interface)
[Open MPI: Open Source High Performance Computing](https://www.open-mpi.org/)

[A Comprehensive MPI Tutorial Resource · MPI Tutorial](http://mpitutorial.com/)
[Performance Comparison of OpenMP, MPI, and MapReduce in Practical Problems](https://www.hindawi.com/journals/am/2015/575687/)

[MPI for Python — MPI for Python documentation](https://mpi4py.readthedocs.io/en/stable/index.html)
[mpi4py – High-Performance Distributed Python » ADMIN Magazine](https://www.admin-magazine.com/HPC/Articles/mpi4py-High-Performance-Distributed-Python)

[mpidotnet/MPI.NET: MPI.NET updated for .NET 4.0 and Linux](https://github.com/mpidotnet/MPI.NET)

## OpenMP

[OpenMP - Wikiwand](http://www.wikiwand.com/en/OpenMP)
[Home - OpenMP](https://www.openmp.org/)
[openmp - GCC Wiki](https://gcc.gnu.org/wiki/openmp)

[OpenMP Task Parallelism for Faster Genomic Data Processing](https://www.openmp.org/wp-content/uploads/OpenMP-Task-Parallelism-for-Faster-Genomic-Data-Processing.pdf)
[OpenMP Parallelization and Optimization of Graph-Based Machine Learning Algorithms](file:///home/kylee/Downloads/9783319455495-c2.pdf)
[Advancement of Computing on Large Datasets via Parallel Computing and Cyberinfrastructure](https://digitalcommons.usu.edu/cgi/viewcontent.cgi?article=5350&context=etd)

[OpenMP » ADMIN Magazine](http://www.admin-magazine.com/HPC/Articles/Parallelizing-Loops-with-OpenMP)
[In the Loop » ADMIN Magazine](http://www.admin-magazine.com/HPC/Articles/OpenMP-Loops-and-Data-Control)

## OpenACC

OpenMP like library for NVIDIA GPU
enables hybrid CPU + GPU programming
easier to use than CUDA

[OpenACC - Wikiwand](https://www.wikiwand.com/en/OpenACC)
[Homepage | OpenACC](https://www.openacc.org/)
[OpenACC - GCC Wiki](https://gcc.gnu.org/wiki/OpenACC)

[OpenACC: More Science Less Programming | NVIDIA Developer](https://developer.nvidia.com/openacc)

[Parallel Computing: What is better and why: OpenACC or OpenMP?](quora.com/Parallel-Computing-What-is-better-and-why-OpenACC-or-OpenMP)
[OpenMP + OpenACC](https://www.pgroup.com/userforum/viewtopic.php?t=6216)

## SIMD

[xtensor-stack/xsimd: C++ wrappers for SIMD intrinsics and parallelized, optimized mathematical functions (SSE, AVX, NEON, AVX512)](https://github.com/xtensor-stack/xsimd)

[An Introduction to GCC Compiler Intrinsics in Vector Processing | Linux Journal](https://www.linuxjournal.com/content/introduction-gcc-compiler-intrinsics-vector-processing)

## Linear Algebra

[xtensor-stack/xtensor-benchmark: Easy to use benchmarks for linear algebra frameworks](https://github.com/xtensor-stack/xtensor-benchmark)

[Intel® Math Kernel Library (Intel® MKL) | Intel® Software](https://software.intel.com/en-us/mkl)
[Math Kernel Library - Wikiwand](https://www.wikiwand.com/en/Math_Kernel_Library)

[LAPACK — Linear Algebra PACKage](http://www.netlib.org/lapack/)

[OpenBLAS : An optimized BLAS library](https://www.openblas.net/)

[Armadillo: C++ library for linear algebra & scientific computing](http://arma.sourceforge.net/)

[Boosting numpy: Why BLAS Matters - Weblog](https://markus-beuckelmann.de/blog/boosting-numpy-blas.html)
[Is your Numpy optimized for speed? - Towards Data Science](https://towardsdatascience.com/is-your-numpy-optimized-for-speed-c1d2b2ba515) different backends

[clifford: Geometric Algebra for Python — Clifford 1.4.0dev0 documentation](https://clifford.readthedocs.io/en/latest/)
