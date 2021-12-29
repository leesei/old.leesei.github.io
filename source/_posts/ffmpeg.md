---
title: "avconv/ffmpeg"
date: 2015-01-13 01:27:30
categories:
  - app
tags:
  - shell-tool
  - ffmpeg
  - avconv
toc: true
---

FFmpeg is a library and utility for AV format conversion.
Libav is a fork of FFmpeg with more transparent governance.
The parameters for `ffmepg` and `avconv` are _MOSTLY_ compatible.

[The FFmpeg/Libav situation](http://blog.pkh.me/p/13-the-ffmpeg-libav-situation.html)
[FFmpeg versus Libav · mpv-player/mpv Wiki](https://github.com/mpv-player/mpv/wiki/FFmpeg-versus-Libav)
[Debate/libav-provider/ffmpeg - Debian Wiki](https://wiki.debian.org/Debate/libav-provider/ffmpeg)
[libavcodec - What is ffmpeg, avcodec, x264? - Stack Overflow](https://stackoverflow.com/questions/16772558/what-is-ffmpeg-avcodec-x264)

```sh
ffmpeg [global options] [[infile options][-i infile]]... {[outfile options] outfile}...
```

<!-- more -->

| Parameter              | Description                         |
| ---------------------- | ----------------------------------- |
| `-c:v`, `-c:a`         | Set video/audio codec               |
| `-b:v`, `-b:a`         | Set video/audio bitrates            |
| `-c codec`             | e.g. `-c copy`                      |
| `-vn`, `-an`           | Skip video/audio                    |
| `-t duration`          | Specify duration, preempts `-to`    |
| `-to position`         | Specify stop position               |
| `-ss positio`n         | Specify stop position (before `-i`) |
| `-frames:v framecount` | Specify frame count limit           |
| `-filter:v`, `-vf`     | Video filters                       |
| `-filter:a`, `-af`     | Audio filters                       |

## FFMpeg on Debian

> http://stackoverflow.com/a/9477756/665507

If you wanted real FFMpeg on Ubuntu/Debian:

```sh
sudo add-apt-repository ppa:jon-severinsson/ffmpeg
sudo apt-get update
sudo apt-get install ffmpeg
```

```sh
# list codecs
ffmpeg -formats -E
```

## screenshot

```sh
# capture 10s of frames starting from 5 minute mark
ffmpeg -ss 05:00 -to 05:10 -i <input> screenshot%05d.png
```

## trim clip

```sh
# frame accurate, may not be keyframe
avconv -i <infile> -ss <second/hh:mm:ss[.xxx]> -t <second/hh:mm:ss[.xxx]> -c copy <outfile>
# search by keyframe, faster
avconv -ss <second/hh:mm:ss[.xxx]> -i <infile> -t <second/hh:mm:ss[.xxx]> -c copy <outfile>
```

> TODO: add tool to do diff of `hh:mm:ss[.xxx]` format time

```sh
# keyframe seek, time is reset
ffmpeg -ss <second/hh:mm:ss[.xxx]> -i <infile> -to <second/hh:mm:ss[.xxx]> -c copy <outfile>
```

## merge clips

```sh
ffmpeg -i VTS_01_2.VOB -ss 463 -c copy -vframes 325 2-manuchoisit.vob
ffmpeg -i VTS_01_2.VOB -ss 353 -t 16 -c copy 3-manutombe.vob

# use `-vn`/`-an` to skip encoding
# `-b:a 192k` may be smaller than `aq`
# `crf` controls the video quality. 18-28 is acceptable range, default is 23.
ffmpeg -analyzeduration 200M -probesize 150M \
  -i concat:"2-manuchoisit.vob|3-manutombe.vob" \
  -vcodec libx264 -vf yadif -preset veryslow -crf 23 \
  -acodec aac -aq 100 -ac 2 -vol 2048 1990-Manu_Redpants.mp4
```

## color format conversion

```sh
ffmpeg -pix_fmt yuv420p -s 352x288 -i in.yuv -pix_fmt nv12 out.yuv
```

## Overlay text

```
.\ffmpeg  -i test2.wmv \
  -vf "drawtext=fontfile=C\\:/Windows/fonts/consola.ttf:text=%{n}:fontsize=72:r=60:x=(w-tw)/2: y=h-(2*lh):fontcolor=white:box=1:boxcolor=0x00000099" \
  test2.mp4
```

## GIF generation

```sh
# generate 1 FPS for the first minute
ffmpeg -i input.mp4 -vf "scale=320:-1,fps=1" -to 60 output.gif

# using per frame palettes
ffmpeg -i input.mp4 -vf "scale=320:-1:flags=lanczos,fps=1,palettegen" -to 60  -y /tmp/palette.png
ffmpeg -i input.mp4 -i /tmp/palette.png -to 60 -lavfi "scale=320:-1:flags=lanczos,fps=1[x];[x][1:v]paletteuse=dither=sierra2_4a" output.gif

# same with Imagemagic
ffmpeg -i input.mp4 -vf scale=320:-1,fps=1 -to 60 -f image2pipe -vcodec ppm - | convert -delay 100 -loop 0 - output.gif
# with optimize (~15% reduction)
ffmpeg -i input.mp4 -vf scale=320:-1,fps=1 -to 60 -f image2pipe -vcodec ppm - | convert - gif:- | convert -layers Optimize  -delay 100 -loop 0 - output.gif
```

Using per frame palettes:
[High quality GIF with FFmpeg](http://blog.pkh.me/p/21-high-quality-gif-with-ffmpeg.html)
[lukechilds/gifgen: Simple high quality GIF encoding](https://github.com/lukechilds/gifgen)
[How do I convert a video to GIF using ffmpeg, with reasonable quality? - Super User](https://superuser.com/questions/556029/how-do-i-convert-a-video-to-gif-using-ffmpeg-with-reasonable-quality)

## Reference

[Documentation](http://ffmpeg.org/documentation.html)
[`ffmpeg` Documentation](http://ffmpeg.org/ffmpeg.html)
[FFmpeg Filters Documentation](https://ffmpeg.org/ffmpeg-filters.html)

[FFmpeg - ArchWiki](https://wiki.archlinux.org/index.php/FFmpeg)
[FFmpeg wiki](http://trac.ffmpeg.org/wiki)
[Seeking – FFmpeg](https://trac.ffmpeg.org/wiki/Seeking)

[ffmpeg audio/video manipulation](http://howto-pages.org/ffmpeg/)
[19 ffmpeg commands for all needs | CatsWhoCode.com](http://www.catswhocode.com/blog/19-ffmpeg-commands-for-all-needs)
[ffmpeg | Video Encoding & Streaming Technologies](https://sonnati.wordpress.com/category/ffmpeg/)
[using ffmpeg to extract audio from video files](https://gist.github.com/protrolium/e0dbd4bb0f1a396fcb55)
[A quick guide to using FFmpeg to convert media files | Opensource.com](https://opensource.com/article/17/6/ffmpeg-convert-media-file-formats)

[Understanding FFmpeg - Part I: General usage | reneVolution](http://www.renevolution.com/understanding-thegeneral-usage-of-ffmpeg-part-one/)
[Understanding FFmpeg - Part II: Scaling video | reneVolution](http://www.renevolution.com/understanding-ffmpeg-part-ii-scaling-video/)
[Understanding FFmpeg - Part III: Cropping | reneVolution](http://www.renevolution.com/understanding-ffmpeg-part-iii-cropping/)

[Libav documentation : avconv](https://libav.org/avconv.html)
[Amit Mund: Media Coversion with avconv](http://amitmund.blogspot.hk/2013/05/media-coversion-with-avconv.html)
