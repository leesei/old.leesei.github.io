---
title: "OpenCV"
date: 2014-12-31 20:00:33
categories:
  - comp.lang
tags:
  - opencv
toc: true
---

[OpenCV](http://opencv.org/) (Open Source Computer Vision Library) is an open source computer vision and machine learning software library.

freeCodeCamp:
[OpenCV Course - Full Tutorial with Python - YouTube](https://www.youtube.com/watch?v=oXlwWbU8l2o)
[Advanced Computer Vision with Python - Full Course - YouTube](https://www.youtube.com/watch?v=01sAkU_NvOY)

This note will focus on the Python binding. Though popular, the Python binding lacks in documentation. Prepare to study its source code and be familiar with OpenCV's C API.
[opencv-python · PyPI](https://pypi.org/project/opencv-python/) is recommended over the one provided by package manager
[opencv-python-headless · PyPI](https://pypi.org/project/opencv-python-headless/) have less dependencies for headless use, but see [#208 opencv-python-headless requires x11](https://github.com/skvark/opencv-python/issues/208)
[piwheels blog - New opencv builds](https://blog.piwheels.org/new-opencv-builds/) dependencies of OpenCV (and headless)
[jrosebr1/imutils: A series of convenience functions to make basic image processing operations such as translation, rotation, resizing, skeletonization, and displaying Matplotlib images easier with OpenCV and Python.](https://github.com/jrosebr1/imutils)

Murtaza's Workshop  
[LEARN OPENCV in 3 HOURS with Python | Including 3xProjects | Computer Vision - YouTube](https://www.youtube.com/watch?v=WQeoO7MI0Bs)  
[LEARN OPENCV C++ in 4 HOURS | Including 3x Example Projects Win/Mac (2021) - YouTube](https://www.youtube.com/watch?v=2FYm3GOonhk)  
[OpenCV Python Projects - YouTube](https://www.youtube.com/playlist?list=PLMoSUbG1Q_r8jFS04rot-3NzidnV54Z2q)

[Install OpenCV 4 on Raspberry Pi 4 and Raspbian Buster - PyImageSearch](https://www.pyimagesearch.com/2019/09/16/install-opencv-4-on-raspberry-pi-4-and-raspbian-buster/) compile from source

[Image Processing 101](https://codewords.recurse.com/issues/six/image-processing-101)
[Welcome to OpenCV-Python Tutorials’s documentation! — OpenCV-Python Tutorials 1 documentation](https://opencv-python-tutroals.readthedocs.io/en/latest/)

<!-- more -->

[How The Camera is Becoming the World's Most Important Sensor - Greg Borenstein - YouTube](https://www.youtube.com/watch?v=QLvoCiO5DqU)
[A fun, hands-on deep learning project for beginners, students, and hobbyists - PyImageSearch](https://www.pyimagesearch.com/2018/04/30/a-fun-hands-on-deep-learning-project-for-beginners-students-and-hobbyists/)

[So I Suck At 24: Automating Card Games Using OpenCV and Python | Arnab Nandi](http://arnab.org/blog/so-i-suck-24-automating-card-games-using-opencv-and-python)
[Dominating an Online Game with Object Detection Using OpenCV - Template Matching. - YouTube](https://www.youtube.com/watch?v=vXqKniVe6P8)

[Finger Detection and Tracking using OpenCV and Python - DEV Community 👩‍💻👨‍💻](https://dev.to/amarlearning/finger-detection-and-tracking-using-opencv-and-python-586m)

[How to track football players using Yolo, SORT and Opencv. | by C Kuan | Aug, 2020 | Towards Data Science](https://towardsdatascience.com/how-to-track-football-players-using-yolo-sort-and-opencv-6c58f71120b8)

[Image Segmentation Using Color Spaces in OpenCV + Python – Real Python](https://realpython.com/python-opencv-color-spaces/)
[Python Face Detection & OpenCV Examples Mini-Guide](https://static.realpython.com/guides/python-opencv-examples.pdf) (PDF)

[Page dewarping](https://mzucker.github.io/2016/08/15/page-dewarping.html)

[Introduction to programming with OpenCV](http://www.cs.iit.edu/~agam/cs512/lect-notes/opencv-intro/) old, 2006
[Computer Vision: Algorithms and Applications](http://szeliski.org/Book/)

[Build a Face Detection Model on a Video using Python](https://www.analyticsvidhya.com/blog/2018/12/introduction-face-detection-video-deep-learning-python/)

## Video

[OpenCV: Getting Started with Videos](https://docs.opencv.org/master/dd/d43/tutorial_py_video_display.html)
[Read, Write and Display a video using OpenCV ( C++/ Python ) | Learn OpenCV](https://www.learnopencv.com/read-write-and-display-a-video-using-opencv-cpp-python/)
[Create a video in Python from images](http://www.xavierdupre.fr/blog/2016-03-30_nojs.html)
[opencv - Python - Extracting and Saving Video Frames - Stack Overflow](https://stackoverflow.com/questions/33311153/python-extracting-and-saving-video-frames?utm_medium=organic&utm_source=google_rich_qa&utm_campaign=google_rich_qa)

Open video with [`cv::VideoCapture`](https://docs.opencv.org/master/d8/dfe/classcv_1_1VideoCapture.html)
Output images with [`cv.imwrite()`](https://docs.opencv.org/master/d4/da8/group__imgcodecs.html#gabbc7ef1aa2edfaa87772f1202d67e0ce), [supported image formats](https://docs.opencv.org/master/d4/da8/group__imgcodecs.html#ga288b8b3da0892bd651fce07b3bbd3a56)

## Text/OCR

[Read Text from Image with One Line of Python Code | by Dario Radečić | Towards Data Science](https://towardsdatascience.com/read-text-from-image-with-one-line-of-python-code-c22ede074cac)

## Tips and Tricks

[Unicode Path/Filename for imread and imwrite · Issue #4292 · opencv/opencv](https://github.com/opencv/opencv/issues/4292#issuecomment-601686965) read from buffer instead

## Blogs

[opencv | More Than Technical](http://www.morethantechnical.com/category/opencv/)
[OpenCV 3 Tutorials, Resources, and Guides | PyImageSearch](https://www.pyimagesearch.com/opencv-tutorials-resources-guides/)
[Computer Vision – Real Python](https://realpython.com/tutorials/computer-vision/)

## PyImageSearch

[PyImageSearch - Be awesome at OpenCV, Python, deep learning, and computer vision](https://www.pyimagesearch.com/)
[The 7 best deep learning books you should be reading right now - PyImageSearch](https://www.pyimagesearch.com/2018/03/05/7-best-deep-learning-books-reading-right-now/)
[ImageSearchEngineResourceGuide.pdf](./opencv/ImageSearchEngineResourceGuide.pdf)

[Neural Style Transfer with OpenCV - PyImageSearch](https://www.pyimagesearch.com/2018/08/27/neural-style-transfer-with-opencv/)

[Face recognition with OpenCV, Python, and deep learning - PyImageSearch](https://www.pyimagesearch.com/2018/06/18/face-recognition-with-opencv-python-and-deep-learning/)
[How to build a custom face recognition dataset - PyImageSearch](https://www.pyimagesearch.com/2018/06/11/how-to-build-a-custom-face-recognition-dataset/)
[Face recognition with OpenCV, Python, and deep learning - PyImageSearch](https://www.pyimagesearch.com/2018/06/18/face-recognition-with-opencv-python-and-deep-learning/)
[How to build a custom face recognition dataset - PyImageSearch](https://www.pyimagesearch.com/2018/06/11/how-to-build-a-custom-face-recognition-dataset/)
[Black and white image colorization with OpenCV and Deep Learning - PyImageSearch](https://www.pyimagesearch.com/2019/02/25/black-and-white-image-colorization-with-opencv-and-deep-learning/)

[How to Build a Kick-Ass Mobile Document Scanner in Just 5 Minutes - PyImageSearch](https://www.pyimagesearch.com/2014/09/01/build-kick-ass-mobile-document-scanner-just-5-minutes/)

[Simple Scene Boundary/Shot Transition Detection with OpenCV - PyImageSearch](https://www.pyimagesearch.com/2019/08/19/simple-scene-boundary-shot-transition-detection-with-opencv/)

[A gentle guide to deep learning object detection - PyImageSearch](https://www.pyimagesearch.com/2018/05/14/a-gentle-guide-to-deep-learning-object-detection/)
[Object detection with deep learning and OpenCV - PyImageSearch](https://www.pyimagesearch.com/2017/09/11/object-detection-with-deep-learning-and-opencv/)
[Real-time object detection with deep learning and OpenCV - PyImageSearch](https://www.pyimagesearch.com/2017/09/18/real-time-object-detection-with-deep-learning-and-opencv/)

[A fun, hands-on deep learning project for beginners, students, and hobbyists - PyImageSearch](https://www.pyimagesearch.com/2018/04/30/a-fun-hands-on-deep-learning-project-for-beginners-students-and-hobbyists/)
[Keras and Convolutional Neural Networks (CNNs) - PyImageSearch](https://www.pyimagesearch.com/2018/04/16/keras-and-convolutional-neural-networks-cnns/)
[Multi-label classification with Keras - PyImageSearch](https://www.pyimagesearch.com/2018/05/07/multi-label-classification-with-keras/)
[Running Keras models on iOS with CoreML - PyImageSearch](https://www.pyimagesearch.com/2018/04/23/running-keras-models-on-ios-with-coreml/)

## JavaScript

[Image Processing - Making Custom Filters - React.js - Part 2](https://overflowjs.com/posts/Image-Processing-Making-Custom-Filters-Reactjs-Part-2.html)
[Image Processing - OpenCV and Node.js (Part 3)](https://overflowjs.com/posts/Image-Processing-OpenCV-and-Nodejs-Part-3.html)

## C Sharp

[shimat/opencvsharp: .NET Framework wrapper for OpenCV](https://github.com/shimat/opencvsharp)
[OpenCvSharp Example](https://www.csharpcodi.com/csharp-examples/?api=OpenCvSharp)

## References

[OpenCV: OpenCV modules](https://docs.opencv.org/master/)

[atduskgreg-opencv-processing-book · GitHub](https://github.com/atduskgreg/opencv-processing-book) book based on the Java binding

```python
(height, width, bytes_per_pixel) = image.shape
```
