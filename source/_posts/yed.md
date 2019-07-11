---
title: "UML"
date: 2015-04-14 01:00:12
categories:
- app
tags:
- uml
- yed
toc: true
---

[yEd Graph Editor Manual | yEd](http://yed.yworks.com/support/manual/index.html)
[yEd Q&A](http://yed.yworks.com/support/qa/) is a StackOverflow like Q&A site. yEd's staff will happily answer our questions.

<!-- more -->

## GraphML

[GraphML - Wikiwand](https://www.wikiwand.com/en/GraphML)
[The GraphML File Format](http://graphml.graphdrawing.org/)

GraphML is yFile's choice of interchange format. See Chapter 9 of [yFiles for Java Developer's Guide](http://docs.yworks.com/yfiles/doc/developers-guide/).

[GraphML Primer](http://graphml.graphdrawing.org/primer/graphml-primer.html)

Flash-based [GraphMLViewer](https://www.yworks.com/products/graphmlviewer)
[GraphML Viewer for the Web - DZone Database](https://dzone.com/articles/graphml-viewer-web)
[c99pjn/GraphMLViewer: Simple javascript which renders graphml files in the browser](https://github.com/c99pjn/GraphMLViewer)

[Gephi - The Open Graph Viz Platform](https://gephi.org/)

## Custom Palette

[Palette Manager | yEd](http://yed.yworks.com/support/manual/palette_manager.html)

[Network Diagrams with Open Security Architecture SVG Icon Set, freeDesktop tango! Icon Library Theme and yWorks yEd Graph Editor on any OS (Linux/Java) (Stefan Thieme Blog)](https://blogs.oracle.com/sthieme/entry/yworks_yed_graph_editor_with)

## Custom Properties

[Properties of Graph Elements | yEd](http://yed.yworks.com/support/manual/properties.html#custom_properties)

They are saved in the file and *local* to the file.
Use `template.graphml` to inherit these. You can also copy and paste the nodes.

## Properties Mapper

[Mapping Custom Properties to Visual Properties | yEd](http://yed.yworks.com/support/manual/properties_mapper.html)

*Properties Mapper* is a tool to change visual properties according to a given attribute. It allowed flexibility and consistency to style the content of the graph. This is a yEd app feature that can be applied to all graphs. The map can be exported.

"Tooltip" in property mapper is actually "Description" of the node.

*Properties Mapper* can change most of the properties: fill color, label text and styles, position, border.

The node type is mapped by (multiple) template mapping. However the label is reset upon applying such change. This is [by design](http://yed.yworks.com/support/qa/8462/label-cleared-after-applying-template-property).
We can use another custom property and apply as label in property mapper but:
- we don't get the immediate feedback of the label
- makes the editing process more troublesome (label should be read-only)

## Tips

- edge (which may not be visible) can be selected in the *Neighborhood Window* of a node
- use *Orthogonal Edges* by default; move/delete the turning points to control how it routes (disable *Orthogonal Edges* temporarily if it creates over complicated results)
- edge by default originates from and targets to center of node, it can be moved after selecting the edge (needed when a node has multiple edges)
- distribute group of nodes vertically (`Ctrl+Shift+v`)/horizontally (`Ctrl+Shift+h`)
