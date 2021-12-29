---
title: Image Tools
categories:
  - app
tags:
  - shell-tool
  - ImageMagick
  - primitive
toc: true
date: 2016-08-04 16:12:51
---

[fogleman/primitive: Reproducing images with geometric primitives.](https://github.com/fogleman/primitive)
[Bigjpg - AI 人工智能图片无损放大 - 使用人工智能深度卷积神经网络(CNN)无损放大图片](https://bigjpg.com/)
[分享 3 款图片处理神器，渣图还原大法好，老厉害了！ - 知乎](https://zhuanlan.zhihu.com/p/61399728)

## ImageMagick

| Tool        | Description                                                                                                                                                                                                                                                                                                             |
| ----------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `animate`   | animate an image sequence on any X server.                                                                                                                                                                                                                                                                              |
| `compare`   | mathematically and visually annotate the difference between an image and its reconstruction.                                                                                                                                                                                                                            |
| `composite` | overlap one image over another.                                                                                                                                                                                                                                                                                         |
| `conjure`   | interpret and execute scripts written in the Magick Scripting Language (MSL).                                                                                                                                                                                                                                           |
| `convert`   | convert between image formats as well as resize an image, blur, crop, despeckle, dither, draw on, flip, join, re-sample, and much more.                                                                                                                                                                                 |
| `display`   | display an image or image sequence on any X server.                                                                                                                                                                                                                                                                     |
| `identify`  | describe the format and characteristics of one or more image files.                                                                                                                                                                                                                                                     |
| `import`    | save any visible window on an X server and outputs it as an image file. You can capture a single window, the entire screen, or any rectangular portion of the screen.                                                                                                                                                   |
| `mogrify`   | resize an image, blur, crop, despeckle, dither, draw on, flip, join, re-sample, and much more. `mogrify` _overwrites_ the original image file, whereas, `convert` writes to a different image file.                                                                                                                     |
| `montage`   | create a composite image by combining several separate images. The images are tiled on the composite image optionally adorned with a border, frame, image name, and more.                                                                                                                                               |
| `stream`    | a lightweight tool to stream one or more pixel components of the image or portion of the image to your choice of storage formats. It writes the pixel components as they are read from the input image a row at a time making stream desirable when working with large images or when you require raw pixel components. |

[ImageMagick v6 Examples](http://www.imagemagick.org/Usage/)
[Command-line Tools @ ImageMagick](http://www.imagemagick.org/script/command-line-tools.php)
[ImageMagick: Convert, Edit, Or Compose Bitmap Images](http://www.imagemagick.org/script/index.php)

[ImageMagick 使用心得](http://www.charry.org/docs/linux/ImageMagick/ImageMagick.html)
[Turn many pictures into a movie | daniel.haxx.se](https://daniel.haxx.se/blog/2016/03/11/turn-many-pictures-into-a-movie/)

[The Definitive Guide to ImageMagick | Michael Still | Apress](http://www.apress.com/us/book/9781590595909) [author's site](http://www.stillhq.com/imagemagick/book/)

```sh
# crop lower part of image
convert input.jpg -crop 300x150+0+150 +repage image-cropped.jpg

# add shadow
convert screenshot.jpg \( +clone -background black -shadow 60×5+0+5 \) +swap -background white -layers merge +repage shadow.jpg

# add timestamp, http://www.imagemagick.org/script/escape.php
convert *.jpg -font Arial -pointsize 72 -gravity SouthEast -fill yellow -annotate +100+100 %[exif:datetime] output-%d.jpg

# convert to pdf
convert a.png b.png -compress jpeg -resize 1240x1753 \
                      -extent 1240x1753 -gravity center \
                      -units PixelsPerInch -density 150x150 multipage.pdf

# convert sequence of images to GIF
convert -delay '1x20' *.png output.gif # 20FPS
convert -delay '2x1' *.png output.gif  # 2 sec each frame
```

### Resizing Image

```sh
# resizing image
convert -resize 300x300 image.jpg image-small.jpg
convert -resize 1080 {from_path} {to_path}  # fix weight only
convert -resize x1080 {from_path} {to_path}  # fix height only

# very low quality
convert -thumbnail {width} *.jpg
```

[How can I scale all images in a folder to the same width? - Ask Ubuntu](https://askubuntu.com/questions/135477/how-can-i-scale-all-images-in-a-folder-to-the-same-width)

[Command-line Processing Geometry @ ImageMagick](http://www.imagemagick.org/script/command-line-processing.php#geometry)

[My favorite Linux commands for optimizing web images | Opensource.com](https://opensource.com/article/21/12/optimize-web-images-linux) with `mogrify`

### Image stitching

```sh
# horizontal
convert image.jpg ...  +append output.jpg
# vertical
convert image.jpg ...  -append output.jpg
```

`mogrify -adjoin`

### creating image

http://www.imagemagick.org/Usage/canvas/#random
http://www.imagemagick.org/Usage/canvas/#tile

```sh
# solid color image
convert -size 100x100 canvas:khaki  canvas_khaki.gif
convert -size 100x100 xc:wheat  canvas_wheat.gif

# patterned image
# use "tile" to take source from pipe and repeat
convert -size 30x54 pattern:hexagons \
          -fill tomato     -opaque white \
          -fill dodgerblue -draw 'color 10,10 floodfill' \
          -fill limegreen  -draw 'color 10,25 floodfill' \
          -roll +15+27 \
          -fill dodgerblue -draw 'color 10,10 floodfill' \
          -fill limegreen  -draw 'color 10,25 floodfill'   miff:- |\
convert -size 200x200 tile:- image.jpg

convert -size 500x500 pattern:checkerboard  miff:- |\
convert -size 5000x5000 tile:- image.jpg
```

```sh
# get quality of JPEG file
identify -verbose file.jpg | grep Quality
```

#### with text

```sh
convert -size 1280x720 xc:grey \
          -font roboto -pointsize 300 -draw "text 100,600 'userName' text 100,300 'userTitle'"  \
          image.jpg

convert -size 1280x720 xc:grey \
          \( -background none label:"A very much longer label" -trim -gravity center \) \
          -composite image.jpg

convert 0001.png \
          \( -size 560x230 -background white -font roboto-mono label:"0001" -trim -gravity center -extent 560x230 \) \
          -gravity northwest -geometry +1100+15 -composite 0001.png
```

[dynamic - ImageMagick best fit text within rectangle? - Stack Overflow](https://stackoverflow.com/questions/39764846/imagemagick-best-fit-text-within-rectangle)

### Colorspace

[Color Management @ ImageMagick](https://imagemagick.org/script/color-management.php)
[Converting anything to RGB correctly - ImageMagick](https://www.imagemagick.org/discourse-server/viewtopic.php?t=16464)

```sh
convert CMYK.jpg -profile /usr/share/color/icc/colord/sRGB.icc RGB.jpg
```
