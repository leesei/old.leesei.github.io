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

## ImageMagick

Tool        | Description
---         | ---
`animate`   | animate an image sequence on any X server.
`compare`   | mathematically and visually annotate the difference between an image and its reconstruction.
`composite` | overlap one image over another.
`conjure`   | interpret and execute scripts written in the Magick Scripting Language (MSL).
`convert`   | convert between image formats as well as resize an image, blur, crop, despeckle, dither, draw on, flip, join, re-sample, and much more.
`display`   | display an image or image sequence on any X server.
`identify`  | describe the format and characteristics of one or more image files.
`import`    | save any visible window on an X server and outputs it as an image file. You can capture a single window, the entire screen, or any rectangular portion of the screen.
`mogrify`   | resize an image, blur, crop, despeckle, dither, draw on, flip, join, re-sample, and much more. `mogrify` *overwrites* the original image file, whereas, `convert` writes to a different image file.
`montage`   | create a composite image by combining several separate images. The images are tiled on the composite image optionally adorned with a border, frame, image name, and more.
`stream`    | a lightweight tool to stream one or more pixel components of the image or portion of the image to your choice of storage formats. It writes the pixel components as they are read from the input image a row at a time making stream desirable when working with large images or when you require raw pixel components.

[ImageMagick v6 Examples](http://www.imagemagick.org/Usage/)
[Command-line Tools @ ImageMagick](http://www.imagemagick.org/script/command-line-tools.php)
[ImageMagick: Convert, Edit, Or Compose Bitmap Images](http://www.imagemagick.org/script/index.php)

[ImageMagick使用心得](http://www.charry.org/docs/linux/ImageMagick/ImageMagick.html)
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

### Favicon

```sh
# create a 36*36 favicon
convert -resize 72x72 -extent 72x72 -gravity center -background white input.svg -resize 36x36 favicon.ico

# IE is still braindead so still use favicon.ico

convert -resize x16 -gravity center -crop 16x16+0+0 -flatten -colors 256 input.png output-16x16.ico
convert -resize x32 -gravity center -crop 32x32+0+0 -flatten -colors 256 input.png output-32x32.ico
convert output-16x16.ico output-32x32.ico favicon.ico

# Then, HTML needs to specify size="XxY" as largest size due to browser bugs

<link rel="shortcut icon" href="/favicon.ico" sizes="32x32">

# Create apple ones

convert -resize x152 input.png apple-touch-icon-152x152.png
convert -resize x120 input.png apple-touch-icon-120x120.png
convert -resize x76  input.png apple-touch-icon-76x76.png
convert -resize x60  input.png apple-touch-icon-60x60.png

# HTML for apple

<link rel="apple-touch-icon" sizes="152x152" href="<%= image_path 'apple-touch-icon-152x152.png' %>">
<link rel="apple-touch-icon" sizes="120x120" href="<%= image_path 'apple-touch-icon-120x120.png' %>">
<link rel="apple-touch-icon" sizes="76x76" href="<%= image_path 'apple-touch-icon-76x76png' %>">
<link rel="apple-touch-icon" href="<%= image_path 'apple-touch-icon-60x60.png' %>">
```

### Colorspace

[Color Management @ ImageMagick](https://imagemagick.org/script/color-management.php)
[Converting anything to RGB correctly - ImageMagick](https://www.imagemagick.org/discourse-server/viewtopic.php?t=16464)

```sh
convert CMYK.jpg -profile /usr/share/color/icc/colord/sRGB.icc RGB.jpg
```
