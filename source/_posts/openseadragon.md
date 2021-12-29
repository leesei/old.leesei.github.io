---
title: OpenSeadragon
categories:
  - web
tags:
  - null
toc: true
date: 2016-04-08 10:40:45
---

# OpenSeadragon

[OpenSeadragon](http://openseadragon.github.io/) [source](https://github.com/openseadragon/openseadragon)
[OpenSeadragon Features](http://openseadragon.github.io/#examples-and-features)

[NIST-ISG/WebDeepZoomToolkit](https://github.com/NIST-ISG/WebDeepZoomToolkit)
[NIST Computational Science in Metrology](https://isg.nist.gov/deepzoomweb/help)

## API

[OpenSeadragon API](http://openseadragon.github.io/docs/)  
[OpenSeadragon Options](http://openseadragon.github.io/docs/OpenSeadragon.html#Options)  
[OpenSeadragon Class: Viewer](http://openseadragon.github.io/docs/OpenSeadragon.Viewer.html)  
[OpenSeadragon Class: Viewport](http://openseadragon.github.io/docs/OpenSeadragon.Viewport.html)  
[OpenSeadragon Class: Navigator](http://openseadragon.github.io/docs/OpenSeadragon.Navigator.html)  
[OpenSeadragon Class: Overlay](http://openseadragon.github.io/docs/OpenSeadragon.Overlay.html)

`Open()` returns `Viewer`
`Viewer` contains `Viewport`, `Navigator`, `ControlDock`

## OpenSeadragon Plugins

[OpenSeadragon Plugins](http://openseadragon.github.io/#plugins)
[Making OpenSeadragon Plugins · openseadragon/openseadragon Wiki](https://github.com/openseadragon/openseadragon/wiki/Making-OpenSeadragon-Plugins)

Navigator (minimap) support is built-in

Sequence (previous/next) support is built-in  
[MartinPluta/OpenSeadragonMultiRow](https://github.com/MartinPluta/OpenSeadragonMultiRow) for multiple view angle  
[NIST-ISG/OpenSeadragonScalebar](https://github.com/NIST-ISG/OpenSeadragonScalebar)  
[NIST-ISG/OpenSeadragonFiltering](https://github.com/NIST-ISG/OpenSeadragonFiltering)

### Coordinate System

[Viewport Coordinates | OpenSeadragon](https://openseadragon.github.io/examples/viewport-coordinates/) !important
[OpenSeadragon Class: Viewport](https://openseadragon.github.io/docs/OpenSeadragon.Viewport.html)

When you get a click, it'll be in window pixel coordinates. You can then translate it into viewport coordinates (logical point, which goes from 0.0 on the left to 1.0 on the right). You can then translate those into pixel coordinates of the image. Here's how it would look all together:

```js
// Assuming we have an OpenSeadragon Viewer called "viewer", we can catch the clicks
// with addHandler like so:
viewer.addHandler("canvas-click", function (event) {
  // The canvas-click event gives us a position in web coordinates.
  var webPoint = event.position;

  // Convert that to viewport coordinates, the lingua franca of OpenSeadragon coordinates.
  var viewportPoint = viewer.viewport.pointFromPixel(webPoint);

  // Convert from viewport coordinates to image coordinates.
  var imagePoint = viewer.viewport.viewportToImageCoordinates(viewportPoint);

  // Show the results.
  console.log(
    webPoint.toString(),
    viewportPoint.toString(),
    imagePoint.toString()
  );
});
```

[Openseadragon image cordinates - Developer Blogger (Improve Your Develop Skill)](http://www.developerblogger.com/168_18434175/)

[msalsbery/OpenSeadragonViewerInputHook](https://github.com/msalsbery/OpenSeadragonViewerInputHook) overrides mouse tracking, see also [OpenSeadragon Class: MouseTracker](https://openseadragon.github.io/docs/OpenSeadragon.MouseTracker.html)

### Zoom

[OpenSeadragon Class: Viewport](http://openseadragon.github.io/docs/OpenSeadragon.Viewport.html)

[msalsbery/OpenSeadragonImagingHelper](https://github.com/msalsbery/OpenSeadragonImagingHelper) map client (browser) coordinates to data coordinates [docs](http://msalsbery.github.io/openseadragonimaginghelper/docs/) [demo](http://msalsbery.github.io/openseadragonimaginghelper/)  
The demo also shows how to anchor an SVG annotation to the image

[OpenSeadragonZoomLevels](http://picturae.github.io/openseadragonselection/#tabs-zoom-levels) [source](https://github.com/picturae/openseadragonzoomlevels) limit zoom level

[Medical image viewer · Issue #34 · openseadragon/openseadragon](https://github.com/openseadragon/openseadragon/issues/34)
[ZOOM Mismatch in overlay · Issue #542 · openseadragon/openseadragon](https://github.com/openseadragon/openseadragon/issues/542)
[Add the option for a zoom handler callback by lukemurray · Pull Request #160 · openseadragon/openseadragon](https://github.com/openseadragon/openseadragon/pull/160)

Zoom level: the ratio of the image's native size to the displayed size
Zoom factor / Pixel Zoom: the ratio of the displayed size to the image's native size

Image zoom: ratio of the original image size to displayed image size. 1 means original image size, 0.5 half size...
Viewport zoom: ratio of the displayed image's width to viewport's width. 1 means identical width, 2 means image's width is twice the viewport's width... Note: not accurate with multi-image.

```js
var viewportZoom = viewer.viewport.getZoom(true);
var imageZoom = viewer.viewport.viewportToImageZoom(viewportZoom);
```

### Overlay

[OpenSeadragon SVG Overlays](http://chrishewett.com/blog/openseadragon-svg-overlays/)
Disable overlay interaction with `$('.openseadragon-canvas').find('svg').css('pointer-events', 'none');`

[altert/OpenseadragonFabricjsOverlay: fabricjs canvas overlay for openseadragon](https://github.com/altert/OpenseadragonFabricjsOverlay)

[Overlays improvements by avandecreme · Pull Request #896 · openseadragon/openseadragon](https://github.com/openseadragon/openseadragon/pull/896)
[Add Line and Polygon Overlay · Issue #3 · thatcher/openseadragon](https://github.com/thatcher/openseadragon/issues/3)
[Add Line and Polygon Overlay · Issue #14 · openseadragon/openseadragon](https://github.com/openseadragon/openseadragon/issues/14)
[How to get overlay's child to scale with overlay · Issue #906 · openseadragon/openseadragon](https://github.com/openseadragon/openseadragon/issues/906)

[openseadragon/svg-overlay](https://github.com/openseadragon/svg-overlay)  
[Emigre/openseadragon-annotations](https://github.com/Emigre/openseadragon-annotations)
[msalsbery/OpenSeadragonAnnoHost](https://github.com/msalsbery/OpenSeadragonAnnoHost) annotation, WIP  
[picturae/openseadragonselection](https://github.com/picturae/openseadragonselection) make rectangular selection

[dgutman/OpenSeadragon-Plugins](https://github.com/dgutman/OpenSeadragon-Plugins) (WIP, evolved to svg-overlay)  
[demo](http://dgutman.github.io/OpenSeadragon-Plugins/) [gh-pages](https://github.com/dgutman/OpenSeadragon-Plugins/tree/master/examples)
Port of [Raphael Vector Overlays for Seadragon AJAX | no.5 geekvault](http://no5-geekvault.blogspot.hk/2011/04/raphael-vector-overlays-for-seadragon.html)

### Saving and Restoring FOV

You should also be able to

- `var box = viewer.viewport.getBounds()` to get the current location
- `viewer.viewport.fitBounds(box)` to return to that location.

[Get and restore zoom level and image position · Issue #418 · openseadragon/openseadragon](https://github.com/openseadragon/openseadragon/issues/418)

### Icons

[peterthomet/openseadragon-flat-toolbar-icons](https://github.com/peterthomet/openseadragon-flat-toolbar-icons)  
[MartinPluta/OpenSeadragonCustomIcons](https://github.com/MartinPluta/OpenSeadragonCustomIcons)

Of cause you can use custom toolbar and interact with OpenSeadragon via API.

### Issues

[OSD in an iframe fails to end drag · Issue #579 · openseadragon/openseadragon](https://github.com/openseadragon/openseadragon/issues/579)

[Dynamically toggle navigator? · Issue #907 · openseadragon/openseadragon](https://github.com/openseadragon/openseadragon/issues/907)

```js
var navigatorShown = true;
function toggleNavigator() {
  navigatorShown = !navigatorShown;
  viewer.navigator.element.style.display = navigatorShown ? "block" : "none";
}
```

http://openseadragon.github.io/docs/OpenSeadragon.Viewer.html#_showMessage
