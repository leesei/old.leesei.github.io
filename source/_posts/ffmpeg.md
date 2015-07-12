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

FFmpeg is a library and utility for AV format convertion.
Libav is a fork of FFmpeg with more transparent governance.
The paramters for `ffmepg` and `avconv` are *MOSTLY* compatible.

[The FFmpeg/Libav situation](http://blog.pkh.me/p/13-the-ffmpeg-libav-situation.html)
[FFmpeg versus Libav · mpv-player/mpv Wiki](https://github.com/mpv-player/mpv/wiki/FFmpeg-versus-Libav)

```
ffmpeg [global options] [[infile options][-i infile]]... {[outfile options] outfile}...
```

<!-- more -->

## FFMpeg on Debian

> http://stackoverflow.com/a/9477756/665507

If you wanted real FFMpeg on Ubuntu/Debian:

```sh
sudo add-apt-repository ppa:jon-severinsson/ffmpeg
sudo apt-get update
sudo apt-get install ffmpeg
```

## trim clip

```sh
# frame accurate, may not be keyframe
avconv -i <infile> -ss <second/hh:mm:ss[.xxx]> -t <second/hh:mm:ss[.xxx]> -c copy <outfile>
# search by keyframe, faster
avconv -ss <second/hh:mm:ss[.xxx]> -i <infile> -t <second/hh:mm:ss[.xxx]> -c copy <outfile>
```

`t` is duration counts from `ss`
> TODO: add tool to do diff of `hh:mm:ss[.xxx]` format time

```sh
# keyframe seek, time is reset, `-to` should be the duration
ffmpeg -ss <second/hh:mm:ss[.xxx]> -i <infile> -to <second/hh:mm:ss[.xxx]> -c copy <outfile>
```

use `-c:a` and `-c:v` to specify audio and video codecs

## color format conversion

```sh
ffmpeg -pix_fmt yuv420p -s 352x288 -i in.yuv -pix_fmt nv12 out.yuv
```


## Reference

[Documentation](http://ffmpeg.org/documentation.html)
[ffmpeg Documentation](http://ffmpeg.org/ffmpeg.html)

[FFmpeg](http://trac.ffmpeg.org/)
[FFmpeg - ArchWiki](https://wiki.archlinux.org/index.php/FFmpeg)
[Seeking – FFmpeg](https://trac.ffmpeg.org/wiki/Seeking)

[ffmpeg audio/video manipulation](http://howto-pages.org/ffmpeg/)
[19 ffmpeg commands for all needs | CatsWhoCode.com](http://www.catswhocode.com/blog/19-ffmpeg-commands-for-all-needs)

[Understanding FFmpeg - Part I: General usage | reneVolution](http://www.renevolution.com/understanding-thegeneral-usage-of-ffmpeg-part-one/)
[Understanding FFmpeg - Part II: Scaling video | reneVolution](http://www.renevolution.com/understanding-ffmpeg-part-ii-scaling-video/)
[Understanding FFmpeg - Part III: Cropping | reneVolution](http://www.renevolution.com/understanding-ffmpeg-part-iii-cropping/)

[Libav documentation : avconv](https://libav.org/avconv.html)
[Amit Mund: Media Coversion with avconv](http://amitmund.blogspot.hk/2013/05/media-coversion-with-avconv.html)



