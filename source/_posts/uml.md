---
title: "UML"
date: 2015-04-14 00:58:12
categories:
- comp.lang
tags:
- uml
toc: true
---

[Unified Modeling Language (UML)](http://en.wikipedia.org/wiki/Unified_Modeling_Language)
[Business Process Model and Notation (BPMN)](http://en.wikipedia.org/wiki/Business_Process_Model_and_Notation) is very similar to activity diagram.
[YANG Central](http://www.yang-central.org/twiki/bin/view/Main/WebHome)

[Allen Holub's UML Quick Reference](http://www.holub.com/goodies/uml/)
[UML Diagram Types With Examples for Each Type of UML Diagrams](http://creately.com/blog/diagrams/uml-diagram-types-examples/)

[UML and Software Modeling Tools](http://www.slideshare.net/Zed4rReal/uml-and-software-modeling-toolspptx)

<!-- more -->

## Text based tools

I used to use the GUI tool [Dia](https://wiki.gnome.org/Apps/Dia/). But it was very buggy and no longer updated. I then went on to look for alternatives.

I am frustrated with the UI diagram apps:
- layout of components takes time
- it is difficult to modify the diagrams in UI (especially for batch operations, e.g. rename, grouping)
- application lock-in because of the binary file format
- binary file is not trackable by VCS
- hard to integrate to other system

So I focused on tools that provides a DSL for drawing UML from plain text.
Candidates are (ranked according to the criteria below):

Tool           | Language   | Diagrams           | Remark
--------       | -------    | -------            | -------
[PlantUML][]   | Java       | Activity, State, Sequence, Component, Class, Object, Use Case, etc | [live](http://www.plantuml.com/plantuml/), [Language Reference](http://plantuml.sourceforge.net/PlantUML_Language_Reference_Guide.pdf)http://www.patrick-wied.at/static/heatmapjs/
[blockdiag][]  | Python     | Block, Activity, Sequence, Network, Rack, Packet | [live](http://blockdiag.appspot.com/)
[mermaid][]    | JavaScript | Flowchart (Activity), Sequence, Gantt | [live](http://knsv.github.io/mermaid/live_editor/)
[JUMLY][]      | JavaScript | Sequence, Activity | [live](http://jumly.tmtk.net/try.html)
[js-sequence-diagrams][] | JavaScript | Sequence | live
[flowchart.js][]         | JavaScript | Flowchart | live
[UMLGraph][]   | Java       | Sequence, Class    |
[ckwnc][]      | ?          | Sequence           | live **only**, C-like syntax
[Graphviz][]   | C          | Digraph            | layout/rendering layer for PlantUML and UMLGraph, with browser port [viz.js](https://github.com/mdaines/viz.js), [dagre](https://github.com/cpettitt/dagre), [dagre-d3](https://github.com/cpettitt/dagre-d3)

[PlantUML]: http://plantuml.sourceforge.net/
[blockdiag]: http://blockdiag.com/en/
[mermaid]: https://github.com/knsv/mermaid
[JUMLY]: http://jumly.tmtk.net/
[js-sequence-diagrams]: http://bramp.github.io/js-sequence-diagrams/
[flowchart.js]: http://flowchart.js.org/
[UMLGraph]: http://www.umlgraph.org/index.html
[ckwnc]: http://www.ckwnc.com
[Graphviz]: http://www.graphviz.org/

I ended up choosing PlantUML because:
- the syntax is more familiar and flexible
- active development
- generates beautiful diagrams
- styleable
- supports more diagram types
- easy to setup
- bindings to more projects indicates widespread usage

BTW, blockdiag would be the first runner up. It also features several unique diagram types.

[Draw More, Work Less](http://www.slideshare.net/MichaelBarSinai/generated-siagramspublic)

### PlantUML

The automatic layout of PlantUML is a curse *and* a blessing.
On one hand you are free of the hassle of arranging the elements, on the other hand you have little control over the position of how your elements.
Hackery like `horizontalLineBetweenDifferentPackageAllowed` and hidden edges are needed to tame the layout engine.

PlantUML also embed other tools besides UML:
DITAA, Salt, JCCKit, Sudoku, XEarth

[Drawing UML with plantuml](http://kimi.im/2014-05-17-drawing-uml-with-plantuml/)

[PlantText](http://www.planttext.com/planttext)

[PlantUML Viewer - Chrome Web Store](https://chrome.google.com/webstore/detail/plantuml-viewer/legbfeljfbjgfifnkmpoajgpgejojooj)
[UML Diagram Editor - Chrome Web Store](https://chrome.google.com/webstore/detail/uml-diagram-editor/hoepdgfgogmeofkgkpapbdpdjkplcode)
[PlantUML QEditor | SourceForge.net](http://sourceforge.net/projects/plantumlqeditor/)

[Learn more - PlantUML Gizmo (add-on for Google Docs)](https://sites.google.com/site/plantumlgizmo/learn)

[Graphviz | UX Design and Development course](http://www.anotheruiguy.com/ux-design-dev/_book/ux/graphviz.html)
[dot - man page](https://www.mankier.com/1/dot)
[Drawing graphs with dot](http://www.graphviz.org/pdf/dotguide.pdf) PDF

### GaaS (graph as a service)

With an HTTP client and scraping code, any DSL with web editor could be made as a service. This is especially easy if the DSL is provided as a library of course.

[Your Graphviz, UMLGraph or PlantUML for your README](http://www.gravizo.com/)

PlantUML's [service](http://plantuml.sourceforge.net/server.html) mode, see[jQuery](http://plantuml.sourceforge.net/jquery.html) and JavaScript [async](http://plantuml.sourceforge.net/demojavascript.html) and [sync](http://plantuml.sourceforge.net/demojavascript2.html) integration.

## GUI Tools

PlantUML's weakness (and strength, sort of) is the user cannot (and need not) specify location of the nodes. This became an issue for component diagrams where we need more control of the position of the nodes and edges for a better look and feel of the diagram.

[UML Diagramming Tools | Diagramming.org](http://www.diagramming.org/)
[Our list of online modeling tools](http://modeling-languages.com/web-based-modeling-tools/)

[yEd - Graph Editor](http://www.yworks.com/products/yed)
[Gaphor UML Modelling](http://gaphor.sourceforge.net/download.php)  (Python)
[Modelio Open Source Community](https://www.modelio.org/index.php)
[ArgoUML](http://argouml.tigris.org/)  the UI is bad
[UMLet - Free UML Tool for Fast UML Diagrams](http://www.umlet.com/)
[Violet UML Editor : easy to use, completely free](http://alexdp.free.fr/violetumleditor/page.php)

### Chrome Apps

[Draw.io Desktop - Chrome Web Store](https://chrome.google.com/webstore/detail/drawio-desktop/pebppomjfocnoigkeepgbmcifnnlndla): the diagram is saved as XML with unknown encoding
[Gliffy Diagrams - Chrome Web Store](https://chrome.google.com/webstore/detail/gliffy-diagrams/bhmicilclplefnflapjmnngmkkkkpfad): the diagram is saved as JSON
[Lucidchart Diagrams - Desktop - Chrome Web Store](https://chrome.google.com/webstore/detail/lucidchart-diagrams-deskt/djejicklhojeokkfmdelnempiecmdomj)
[Sketchboard.io - Chrome Web Store](https://chrome.google.com/webstore/detail/sketchboardio/bgafhjpdkfjfmmjbebbdckolonomaoil)

