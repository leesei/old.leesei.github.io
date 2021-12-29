---
title: Image Optimization
categories:
  - app
tags:
  - shell-tools
toc: true
date: 2016-08-04 16:12:51
---

[18 image file compression tools tested | Creative Bloq](http://www.creativebloq.com/design/image-compression-tools-1132865)
[Comparison of all optimisation tools | ImageOptim-CLI](https://jamiemason.github.io/ImageOptim-CLI/)

[ImageOptim — better Save for Web](https://imageoptim.com/mac)
[ImageOptim alternatives for Windows and Linux](https://imageoptim.com/versions.html)

[Caesium - Image Compressor](https://saerasoft.com/caesium)
[Antelope 5.2.0.0 for Windows - Download](https://antelope.en.uptodown.com/windows)

[BPG Image format](http://bellard.org/bpg/) H.265
[A new image format for the Web | WebP | Google Developers](https://developers.google.com/speed/webp/)

[squoosh/cli at dev · GoogleChromeLabs/squoosh](https://github.com/GoogleChromeLabs/squoosh/tree/dev/cli)

[imagemin](https://github.com/imagemin?type=source) provides prebuild binaries
[imagemin/imagemin-cli: Minify images seamlessly](https://github.com/imagemin/imagemin-cli)
[imagemin/imagemin: Minify images seamlessly](https://github.com/imagemin/imagemin)

```
npm i -g imagemin-cli imagemin-mozjpeg imagemin-pngcrush imagemin-pngquant
imagemin --plugin=pngcrush --plugin=pngquant --plugin=mozjpeg --plugin=gifsicle --plugin=svgo "images/**" "outdir"
```

[imgmini - npm](https://www.npmjs.com/package/imgmini) `gulp-image` contains all the binaries
[Asikur22/npm-imgmini: Image Minify with Gulp Image.](https://github.com/Asikur22/npm-imgmini) CLI wrapper for `gulp-image`
[1000ch/gulp-image: Optimize PNG, JPEG, GIF, SVG images with gulp task.](https://github.com/1000ch/gulp-image) uses `imagemin` binaries

```sh
npm i -g @leesei/imgmini
find <folder> -type f | xargs -P$(nproc) -- imgmini -s
```

[wuwu8ku/imgminify: imgminify](https://github.com/wuwu8ku/imgminify) bundled binaries, custom wrapper

[toy/image_optim: Optimize images using multiple utilities](https://github.com/toy/image_optim) Ruby
[spatie/image-optimizer: Easily optimize images using PHP](https://github.com/spatie/image-optimizer) PHP, saving not prominent

[unjs/ipx: High performance, secure and easy to use image proxy based on Sharp and libvips.](https://github.com/unjs/ipx/)

[JPNG.svg (Transparent PNG with JPEG Compression)](https://codepen.io/shshaw/full/LVKEdv?__cf_chl_jschl_tk__=15fe89eba4cfcd91483b5f446e2bd7e5ab144a98-1576653921-0-ARmYaylhbR0Nwzr7Mb1AyZfGpO-GnPHy5k34lS3n7FiDgdgDmphs82JUSbBitFdYosbBbcLbt3SMeNGDXfAg7qcL8aCfPc3aVx-H1FO8IE8lPAt4HL7pB9SqkIHxhSzdVtLbzZvZM_1aCFCBQYIBt4qhNpL3qNW-BW9BW7ywQXFm1hO9iZHbvT3KfbYlS7yH63F4Eh2K7encgLe89AfCvVEkoQckqI-16qekSdQt4PUznsma9fmmpgazM1G3xqO-lmc0gVczow9ykDT2FRLV3m4iCEtJgsKJN0hXf80xaSRyoz0ag-6mn7iimQf2zzl6NTU4Thbs8hz-L11V7PlL1zkjanQpR6aEoGEKHanbXEiM)

# JPEG

[The Problem with JPEG - Computerphile - YouTube](https://www.youtube.com/watch?v=yBX8GFqt6GA)

[Comparison of JPEG Lossless Compression Tools - blarg.co.uk](https://blarg.co.uk/blog/comparison-of-jpeg-lossless-compression-tools)

[mozilla/mozjpeg: Improved JPEG encoder.](https://github.com/mozilla/mozjpeg)

[Lepton image compression: saving 22% losslessly from images at 15MB/s | Dropbox Tech Blog](https://blogs.dropbox.com/tech/2016/07/lepton-image-compression-saving-22-losslessly-from-images-at-15mbs/)

[The home of PackJPG](http://www.elektronik.htw-aalen.de/packjpg/)

jpegoptim -P -p --all-progressive -s -m 90 --no-action <file>

# PNG

[A guide to PNG optimization](http://optipng.sourceforge.net/pngtech/optipng.html)
[This Lossless PNG Optimization You're Probably Not Using Shrunk One File an Extra 39% - Zoompf Web Performance](https://zoompf.com/blog/2014/11/png-optimization)

[PNGGauntlet](https://pnggauntlet.com/) Combines PNGOUT, OptiPNG, and DeflOpt to create the smallest PNGs
[PNGOUT Tutorial](http://advsys.net/ken/util/pngout.htm)
`pngout pngout.png -k0 out.png`

[OptiPNG Home Page](http://optipng.sourceforge.net/)
`optipng -preserve -strip all -simulate <file>` default compression is fair enough
[DeflOpt Program: Optimize Compressed Files](http://www.dotnetperls.com/deflopt)
[pngquant — lossy PNG compressor](https://pngquant.org/)
[TinyPNG – Compress PNG images while preserving transparency](https://tinypng.com/) use color palette instead
[PNGCRUSH](https://pmt.sourceforge.io/pngcrush/) very slow, creates larget file ><
pingo
[Advance Projects](http://www.advancemame.it/doc-advpng.html) `advpng`, uses zopflipng, creates larget file ><

zopflipng

# SVG

[High Performance SVGs | CSS-Tricks](https://css-tricks.com/high-performance-svgs/)
[svg/svgo: Node.js tool for optimizing SVG files](https://github.com/svg/svgo)
[svg/svgo-gui: Node-WebKit based GUI for SVGO](https://github.com/svg/svgo-gui)

# QOI

[PhobosLab](https://phoboslab.org/log/2021/11/qoi-fast-lossless-image-compression)
[A Super Speedy Lightweight Lossless Compression Algorithm | Hackaday](https://hackaday.com/2021/11/30/a-super-speedy-lightweight-lossless-compression-algorithm/)
[phoboslab/qoi: The “Quite OK Image” format for fast, lossless image compression](https://github.com/phoboslab/qoi)

---

# Cloudinary

[Image Optimization for Websites: Beautiful Pages That Load Quickly](https://cloudinary.com/blog/image_optimization_for_websites_beautiful_pages_that_load_quickly)
[CDN for Images: Optimize and Deliver Images Faster](https://cloudinary.com/blog/delivering_all_your_websites_images_through_a_cdn)
[Get started with Cloudinary Media Optimizer | Cloudinary](https://cloudinary.com/documentation/media_optimizer_get_started)

[Compress an Image Automatically Without Losing Quality](https://cloudinary.com/blog/the_holy_grail_of_image_optimization_or_balancing_visual_quality_and_file_size) compression ratio
[Automatically Reduce Image Size Without Losing Quality](https://cloudinary.com/blog/adaptive_browser_based_image_format_delivery) format
[Match Device Pixel Ratio by Automatically Adapting Images](https://cloudinary.com/blog/how_to_automatically_adapt_website_images_to_retina_and_hidpi_devices) resolution

[Cloudinary for WordPress Plugin for Images and Video](https://cloudinary.com/blog/introducing_cloudinary_s_wordpress_plugin_for_dynamic_images_and_video)

# Web Service

[Compressor.io - optimize and compress JPEG photos and PNG images](https://compressor.io/) 10MB limit
[Free Online Image Optimizer · Kraken.io](https://kraken.io/web-interface) 1MB limit
[Online Image Сompressor](https://imagecompressor.com/) ? limit
[TinyPNG – Compress PNG images while preserving transparency](https://tinypng.com/) 5MB limit, create indexed PNG, PNG only
