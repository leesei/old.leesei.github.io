---
title: Tiled Image
categories:
  - web
tags:
  - null
toc: true
date: 2016-04-08 10:40:45
---

[Mipmap - Wikiwand](https://www.wikiwand.com/en/Mipmap)

When viewing extremely large image (maps, medical and astrological images), it's more efficient to:

- build a pyramid of images of different zoom level
- cut the image at a particular zoom level as tiles

There are many formats that specify the file structure and file name convention to archive these two goals.
There are also many viewer to render these images on browser that provide different features.

[Viewing Large Images - OpenLayers, GSIV, ModestMaps, DeepZoom, and Python « Itinerant Source](https://web.archive.org/web/20090127042842/http://blog.kapilt.com/2008/11/30/sharing-large-images-openlayers-gsiv-modestmaps-deepzoom-and-python) (from WaybackMachine)
[Deep Zoom and others for displaying large images on the web](https://moreati.github.io/2008/11/26/deep-zoom-and-others-for-displaying-large-images-on-the-web.html)

> see `web-map.md`

[iangilman/zooming: Resources for people interested in zooming technology.](https://github.com/iangilman/zooming) with dead links

<!-- more -->

# Formats

## OpenSlide

[OpenSlide](http://openslide.org/) vendor neutral library for reading WSI
[List of Known Properties](http://openslide.org/docs/properties/)
[Virtual slide formats understood by OpenSlide](http://openslide.org/formats/)

[Adding a New Slide Format to OpenSlide](http://openslide.org/docs/newformat/)

## Deep Zoom Image

Deep Zoom is a standard by Microsoft. It allows users to pan around and zoom in a large, high resolution image . It reduces the time required for initial load by downloading only the region being viewed or only at the resolution it is displayed at.

[Deep Zoom - Wikiwand](http://www.wikiwand.com/en/Deep_Zoom)  
[A deepzoom primer ( explained and coded).. – Jaime Rodriguez](https://blogs.msdn.microsoft.com/jaimer/2008/04/01/a-deepzoom-primer-explained-and-coded/)  
[Deep Zoom](https://msdn.microsoft.com/en-us/library/cc645050)  
[Deep Zoom File Format Overview](https://msdn.microsoft.com/en-us/library/cc645077) !important
[Deep Zoom Schema Reference](https://msdn.microsoft.com/en-us/library/cc645022)
[About Deep Zoom Composer](https://msdn.microsoft.com/en-us/library/dd409068)  
[Creating Zooming Images | OpenSeadragon](http://openseadragon.github.io/examples/creating-zooming-images/)

[Inside Deep Zoom – Part I: Multiscale Imaging – RTFM / Daniel Gasienica](http://web.archive.org/web/20150429205932/http://www.gasi.ch/blog/inside-deep-zoom-1/)
[Inside Deep Zoom – Part II: Mathematical Analysis – RTFM / Daniel Gasienica](http://web.archive.org/web/20150429205956/http://www.gasi.ch/blog/inside-deep-zoom-2)
[Inside Deep Zoom – Part III: Deep Zoom in Flash – RTFM / Daniel Gasienica](http://web.archive.org/web/20150404123937/http://www.gasi.ch/blog/inside-deep-zoom-3/)

[OpenSlide Python](http://openslide.org/api/python/) have built-in deep zoom support. See [RunningDeepZoomServerOnApache · openslide/openslide Wiki](https://github.com/openslide/openslide/wiki/RunningDeepZoomServerOnApache) for setting up an sample server.

`TileSize` is the effective content, each tile has a padding of `Overlap` pixels. So a non edge tile is has side length of `TileSize + 2*Overlap`.
[Use 254 pixels as default tile size by gasi · Pull Request #359 · jcupitt/libvips](https://github.com/jcupitt/libvips/pull/359) (recommend tile size)
[vips dzsave saves tiles with incorrect size because it ignores the overlap parameter · Issue #357 · jcupitt/libvips](https://github.com/jcupitt/libvips/issues/357) (fix overlap)

## IIIF

[Home — IIIF | International Image Interoperability Framework](http://iiif.io/)
[Apps & Demos — IIIF | International Image Interoperability Framework](http://iiif.io/apps-demos/)
[Technical Details — IIIF | International Image Interoperability Framework](http://iiif.io/technical-details/)
[Image API 2.0 — IIIF | International Image Interoperability Framework](http://iiif.io/api/image/2.0/)
[Presentation API 2.0 — IIIF | International Image Interoperability Framework](http://iiif.io/api/presentation/2.0/)

[IIPImage](http://iipimage.sourceforge.net/)

[[1403.6025] Web-Based Visualization of Very Large Scientific Astronomy Imagery](https://arxiv.org/abs/1403.6025)

## Zoomify

[thematic mapping blog: Creating a custom map tiling scheme for New Zealand’s seafloor](http://blog.thematicmapping.org/2012/09/creating-custom-map-tiling-scheme-for.html)
[Zoomify PFF file format documentation · lovasoa/pff-extract Wiki](https://github.com/lovasoa/pff-extract/wiki/Zoomify-PFF-file-format-documentation)

[Does Zoomify work with Akamai and other edge servers?](http://www.zoomify.com/support.htm#a20081222_1838)

## WMS/TMS/EPSG:4326

The [OSGeo](http://www.osgeo.org/) group published Web Map Server and Tile Map Service specs for map viewing.

WMS also have API for [FeatureInfo ](http://openlayers.org/en/master/examples/getfeatureinfo-tile.html)
[epsg > EPSG home](http://www.epsg.org/)

[Tile Map Service Specification - OSGeo Wiki](http://wiki.osgeo.org/wiki/Tile_Map_Service_Specification)
[TilingStandard - OSGeo Wiki](http://wiki.osgeo.org/wiki/TilingStandard)

[Welcome to MapServer](http://www.mapserver.org/)
[TileCache, from MetaCarta Labs](http://tilecache.org/)
[FeatureServer](http://featureserver.org/)

---

# Tools

[Help:Zoomable images - Wikimedia Commons](https://commons.wikimedia.org/wiki/Help:Zoomable_images)

[Dezoomify](http://ophir.alwaysdata.net/dezoomify/dezoomify.html)
[lovasoa/dezoomify: Download images from websites using Zoomify, Deep Zoom (seadragon), and other zoomable image formats](https://github.com/lovasoa/dezoomify)

## Deep Zoom

[Download Deep Zoom Composer from Official Microsoft Download Center](https://www.microsoft.com/en-us/download/details.aspx?displaylang=en&id=24819)
[zoomhub/node-deepzoomtools: Node.js Deep Zoom Tools](https://github.com/zoomhub/node-deepzoomtools)

Generators in Python usually requires [Python Imaging Library (PIL)](http://www.pythonware.com/products/pil/).  
[openzoom/deepzoom.py](https://github.com/openzoom/deepzoom.py)  
[openslide-python/deepzoom_tile.py at master](https://github.com/openslide/openslide-python/blob/master/examples/deepzoom/deepzoom_tile.py)

Each folder is a layer, which contains tiles of side length (max of width, height) <= 2^N

| Layer | Tile Resolution (Max)    |
| ----- | ------------------------ |
| 1     | 2\*2                     |
| 2     | 4\*4                     |
| 8     | 256\*256                 |
| 10    | 1024\*1024 (1M pixels)   |
| 14    | 16384\*16384             |
| 15    | 32768\*32768 (1G pixels) |
| 16    | 65536\*65536             |

Within a layer, files are named in `{col}_{row}.{format}` fashion:

```
  -----> x (cols)
| 0_0  1_0
| 0_1  1_1
| 0_2  1_2
v
y (rows)
```

## Zoomify

[Zoomify HTML5 Express](http://www.zoomify.com/express.htm)
[asfez/CsZoomify: A c# library to create Zoomify compatible tiles from big images.](https://github.com/asfez/CsZoomify)
http://tools.wmflabs.org/zoomable-images/zoomify.php
http://tools.wmflabs.org/zoomable-images/zoomify-form-source.php
http://tools.wmflabs.org/zoomable-images/zoomify-source.php
[moravianlibrary/opentiler: OpenTiler is a desktop application which generates Zoomify tiles](https://github.com/moravianlibrary/opentiler)
[sebastianhohns/JImagePyramide: Convert images to a image pyramide file format (usable by Zoomify and Openzoom)](https://github.com/sebastianhohns/JImagePyramide)

[lovasoa/pff-extract: pff (zoomify single-file image format) to jpeg converter](https://github.com/lovasoa/pff-extract)

[zoomify_dl](http://xuth.net/programming/zoomify_dl.html)
[Xuth/zoomify_dl: script to download and stitch resolution zoomify'd images (perl / perlmagick)](https://github.com/Xuth/zoomify_dl)

[valgur/dezoomify: Download and losslessly untile Zoomify images](https://github.com/valgur/dezoomify) python
[fun-dac/daconv: Daemon script for converting Zoomify format](https://github.com/fun-dac/daconv) python
[dbalcomb/dezoomify: Reverse Zoomify](https://github.com/dbalcomb/dezoomify) livescript

## VIPS

[VIPS](https://github.com/openslide/openslide/wiki/OpenSlideAndVIPS) is recommended for convertion to avoid loading the entire image to RAM.
`vips` memory use scales with image width, not number of pixels, so it can process very large images without using much memory.  
It supports various input format, including OpenSlide (requires `libopenslide` at build). It can perform many operation on the image. The `dzsave` operation supports deep zoom ([requires `libgsf`](https://github.com/jcupitt/libvips/issues/141) at build),zoomify and google layout.  
[pyvips – Image processing with libvips — pyvips documentation](https://jcupitt.github.io/pyvips/) official Python binging  
[sharp](http://sharp.dimens.io/en/stable/) is VIPS's Node binding.

[VipsWiki](http://www.vips.ecs.soton.ac.uk/index.php?title=VIPS)  
[VIPS from the command-line: VIPS Reference Manual](http://www.vips.ecs.soton.ac.uk/supported/current/doc/html/libvips/using-cli.html)

[libvips and nip2](http://libvips.blogspot.hk/)
[Tips and tricks for vipsthumbnail](http://libvips.blogspot.hk/2013/11/tips-and-tricks-for-vipsthumbnail.html)
[Profiling libvips](http://libvips.blogspot.hk/2013/11/profiling-libvips.html)
[Making DeepZoom, Zoomify and Google Maps image pyramids with vips](http://libvips.blogspot.co.uk/2013/03/making-deepzoom-zoomify-and-google-maps.html)

VIPS can infer pipeline with extension, you can also pass options to the transform with:

```sh
# using dzsave as action
vips huge.svs mydz --layout google
# specifying jpeg saving option
vips huge.svs mydz --suffix .jpg[Q=90]
# using dzsave in pipeline (with .dz suffix)
vips extract_area huge.svs mypy.dz[layout=google] 100 100 10000 10000
```

## MapTiler

Commercial with feature limited free version.

[MapTiler - map overlay, cut map tiles for Google Maps, GIS layers and mobile apps – MapTiler](https://www.maptiler.com/)
[Features of MapTiler](https://www.maptiler.com/features/)

[Tiling schemes](https://www.maptiler.com/how-to/advanced-image-settings/):
Open GIS WMTS / Open Street Maps / Google XYZ (top-left-origin)
OSGEO TMS (bottom-left-origin)

[Coordinate systems – MapTiler](https://www.maptiler.com/how-to/coordinate-systems/)

## GeGL

[GEGL](http://gegl.org/) a graph based image processing framework
[babl](http://gegl.org/babl/) babl is a dynamic, any to any, pixel format translation library.

Another image processing library.

## Custom

[Creating zoomable images using Graphics Mill and Leaflet](http://www.graphicsmill.com/blog/2014/08/05/Creating-zoomable-images-using-Graphics-Mill-and-Leaflet)

---

# Viewers

[Apps & Demos — IIIF | International Image Interoperability Framework](http://iiif.io/apps-demos/)

## OpenSeadragon

> see `openseadragon.md`

## OpenLayers

[OpenLayers 3 - Welcome](http://openlayers.org/)
[OpenLayers 3 Examples](http://openlayers.org/en/v3.15.1/examples/) features

[OpenLayers 3 - OpenLayers Custom Build](http://openlayers.org/en/master/builder/)
[Introduction | OpenLayers Workshop](http://openlayers.org/workshop/)
[OpenLayers 3 - Tutorials](http://openlayers.org/en/master/doc/tutorials/)
[OpenLayers 3 - Frequently Asked Questions (FAQ)](http://openlayers.org/en/master/doc/faq.html)
[OpenLayers 3 API Reference - Index](http://openlayers.org/en/master/apidoc/)

## Leaflet.js

[Leaflet JS Bin](http://playground-leaflet.rhcloud.com/?html,output)

[Using Leaflet.js with non-geographic imagery - Oliver Marriott](http://omarriott.com/aux/leaflet-js-non-geographical-imagery/)
[Deep Zoom Image with multiple views – Leaflet.js](https://gist.github.com/egardner/755fe6ab7ae7459fece6)

[React-Leaflet · ⚛️ React components for 🍃 Leaflet maps](https://react-leaflet.js.org/)
[How to use React-Leaflet - LogRocket Blog](https://blog.logrocket.com/how-to-use-react-leaflet/)

[thematic mapping blog: Creating a synchronized view of two maps or images with Leaflet](http://blog.thematicmapping.org/2013/06/creating-synchronized-view-of-two-maps.html) [source](https://github.com/turban/Leaflet.Sync)

[thematic mapping blog: Showing Zoomify images with Leaflet](http://blog.thematicmapping.org/2013/06/showing-zoomify-images-with-leaflet.html) [source](https://github.com/turban/Leaflet.Zoomify)

### Overlap handling

[Custom Tile Rendering in Leaflet - Google Groups](https://groups.google.com/forum/#!topic/leaflet-js/e-2BIf2bB3g)

`leaflet-src.js` (of 2012-10)

```diff
--- a/leaflet-src.js
+++ b/leaflet-src.js
@@ -2270,7 +2270,7 @@
 _getTilePos: function (tilePoint) {
   var origin = this._map.getPixelOrigin(),
-  tileSize = this.options.tileSize;
+  tileSize = this.options.tileSize - 2;

   return tilePoint.multiplyBy(tileSize).subtract(origin);
 },
```

> This does not handle the edge tiles!!

## IIPMooViewer

[IIPImage » IIPMooViewer](http://iipimage.sourceforge.net/documentation/iipmooviewer/)
[ruven/iipmooviewer: IIPMooViewer is an advanced javascript HTML5 image viewer for streaming high resolution scientific images](https://github.com/ruven/iipmooviewer) supports rectangular annotation, synced view, image blending

[jcupitt/iipmooviewer](https://github.com/jcupitt/iipmooviewer) fork that support experimental WebGL rendering (from author of VIPS)

## Zoomify

The official viewer of Zoomify is a commercial product and less interesting.
Use the above OSS.

[Zoomify HTML5 Enterprise](http://www.zoomify.com/enterprise.htm)

[Zoomify Product Comparison](http://www.zoomify.com/compare.htm)
[Zoomify Updates & Version History](http://www.zoomify.com/updates.htm)

## Honorable Mentions

[Universal Viewer](http://universalviewer.io/examples/#?c=0&m=0&s=0&cv=0&z=-0.5358%2C-0.0766%2C2.0716%2C1.5324) [source](https://github.com/universalviewer) It uses OpenSeadragon and [virtex3d](https://github.com/edsilv/virtex) over three.js

[Free whole slide image viewer - PMA.start | Universal digital microscopy software](http://free.pathomation.com/)
