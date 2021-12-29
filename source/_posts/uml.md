---
title: "UML"
date: 2015-04-14 00:58:12
categories:
  - comp.lang
tags:
  - uml
toc: true
---

[Unified Modeling Language - Wikiwand](https://www.wikiwand.com/en/Unified_Modeling_Language)
[Business Process Model and Notation (BPMN)](http://en.wikipedia.org/wiki/Business_Process_Model_and_Notation) is very similar to activity diagram.
[YANG Central](http://www.yang-central.org/twiki/bin/view/Main/WebHome)

[Allen Holub's UML Quick Reference](http://www.holub.com/goodies/uml/)
[UML Diagram Types With Examples for Each Type of UML Diagrams](http://creately.com/blog/diagrams/uml-diagram-types-examples/)
[Practical UML: A Hands-On Introduction for Developers](http://edn.embarcadero.com/print/31863)

[UML and Software Modeling Tools](http://www.slideshare.net/Zed4rReal/uml-and-software-modeling-toolspptx)

[Unified Modeling Language (UML) | An Introduction - GeeksforGeeks](https://www.geeksforgeeks.org/unified-modeling-language-uml-introduction/)

[Voxxed Athens 2017 :: Opening Ceremony + Keynote Software Architecture Diagramming - YouTube](https://www.youtube.com/watch?v=aPtT2GNu8vM)
[The Art of Visualising Software Architecture - Coding the Architecture](http://www.codingthearchitecture.com/presentations/agilehongkong2016-the-art-of-visualising-software-architecture)

> see `learn-to-code.md#architecture-design`

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

| Tool                     | Language   | Diagrams                                                           | Remark                                                                                                                                                                                                        |
| ------------------------ | ---------- | ------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [PlantUML][]             | Java       | Activity, State, Sequence, Component, Class, Object, Use Case, etc | [live](http://www.plantuml.com/), [Language Reference](http://plantuml.com/guide)                                                                                                                             |
| [blockdiag][]            | Python     | Block, Activity, Sequence, Network, Rack, Packet                   | [live](http://interactive.blockdiag.com)                                                                                                                                                                      |
| [mermaid][]              | JavaScript | Flowchart (Activity), Sequence, Gantt                              | [live](http://knsv.github.io/mermaid/live_editor/), [Schachte/Mermrender](https://github.com/Schachte/Mermrender)                                                                                             |
| [JUMLY][]                | JavaScript | Sequence, Activity                                                 | [live](http://jumly.tmtk.net/try.html)                                                                                                                                                                        |
| [js-sequence-diagrams][] | JavaScript | Sequence                                                           | live                                                                                                                                                                                                          |
| [flowchart.js][]         | JavaScript | Flowchart                                                          | live                                                                                                                                                                                                          |
| [UMLGraph][]             | Java       | Sequence, Class                                                    |
| [ckwnc][]                | ?          | Sequence                                                           | live **only**, C-like syntax                                                                                                                                                                                  |
| [Graphviz][]             | C          | Digraph                                                            | layout/rendering layer for PlantUML and UMLGraph, with browser port [viz.js](https://github.com/mdaines/viz.js), [dagre](https://github.com/cpettitt/dagre), [dagre-d3](https://github.com/cpettitt/dagre-d3) |

[plantuml]: http://plantuml.com/
[blockdiag]: http://blockdiag.com/en/
[mermaid]: https://github.com/knsv/mermaid
[jumly]: http://jumly.tmtk.net/
[js-sequence-diagrams]: http://bramp.github.io/js-sequence-diagrams/
[flowchart.js]: http://flowchart.js.org/
[umlgraph]: http://www.umlgraph.org/index.html
[ckwnc]: http://www.ckwnc.com
[graphviz]: http://www.graphviz.org/

I ended up choosing PlantUML because:

- the syntax is more familiar and flexible
- active development
- generates beautiful diagrams
- style-able
- supports more diagram types
- easy to setup
- bindings to more projects indicates widespread usage

BTW, `blockdiag` would be the first runner up. It also features several unique diagram types.

[Draw More, Work Less](http://www.slideshare.net/MichaelBarSinai/generated-siagramspublic)

### PlantUML

[Welcome to The Hitchhiker’s Guide to PlantUML! — The Hitchhiker's Guide to PlantUML documentation](https://crashedmind.github.io/PlantUMLHitchhikersGuide/)
[General and common command to handle graphic layout in diagrams.](http://plantuml.com/commons)
[Language specification pages](http://plantuml.com/sitemap-language-specification)
[Use creole syntax to style your texts](http://plantuml.com/creole)
[Changing colors and fonts](http://plantuml.com/skinparam)

[PlantUML Standard Library](http://plantuml.com/stdlib) icons
[tupadr3/plantuml-icon-font-sprites: plantuml-font-icon-sprites](https://github.com/tupadr3/plantuml-icon-font-sprites)

The automatic layout of PlantUML (with GraphViz) is a curse _and_ a blessing.
On one hand you are free of the hassle of arranging the elements, on the other hand you have little control over the position of how your elements.
Hackery like `horizontalLineBetweenDifferentPackageAllowed` and hidden links (`-[hidden]-`) are needed to tame the layout engine.

PlantUML also embed other tools besides UML:
DITAA, Salt, JCCKit, Sudoku, XEarth

[Drawing UML with plantuml](http://kimi.im/2014-05-17-drawing-uml-with-plantuml)  
[PlantUML | DrawUML](http://ogom.github.io/draw_uml/plantuml/) cheat sheet  
[PlantUML Pleasantness -Messages from mrhaki](http://mrhaki.blogspot.hk/search/label/PlantUML%3APleasantness)
[PlantUML Diagrams | SAP Blogs](https://blogs.sap.com/2017/04/27/plantuml-diagrams/)

Live Editor:  
[PlantUML Web Server](http://www.plantuml.com/plantuml/uml/SyfFKj2rKt3CoKnELR1Io4ZDoSa70000)
[PlantUML Editor](https://plantuml-editor.kkeisuke.com/#)  
[PlantText](http://www.planttext.com/planttext)

[PlantUML Viewer - Chrome Web Store](https://chrome.google.com/webstore/detail/plantuml-viewer/legbfeljfbjgfifnkmpoajgpgejojooj)
[UML Diagram Editor - Chrome Web Store](https://chrome.google.com/webstore/detail/uml-diagram-editor/hoepdgfgogmeofkgkpapbdpdjkplcode)
[PlantUML QEditor | SourceForge.net](http://sourceforge.net/projects/plantumlqeditor/)
[nrekretep/pikturr: Simple tool to turn a swagger api spec into a uml class diagram.](https://github.com/nrekretep/pikturr)

[Learn more - PlantUML Gizmo (add-on for Google Docs)](https://sites.google.com/site/plantumlgizmo/learn)

[Graphviz | UX Design and Development course](http://www.anotheruiguy.com/ux-design-dev/_book/ux/graphviz.html)
[dot - man page](https://www.mankier.com/1/dot)
[Drawing graphs with dot](http://www.graphviz.org/pdf/dotguide.pdf) PDF

#### Samples

[Real World PlantUML](https://real-world-plantuml.com/) gallery  
[ui-cs383/Class-Diagrams](https://github.com/ui-cs383/Class-Diagrams)
[hnakamur/asciidoctor-ditaa-graphviz-plantuml-example](https://github.com/hnakamur/asciidoctor-ditaa-graphviz-plantuml-example)
[jmbruel/basics: Basic UML concepts and diagrams in plantUML for easy modification/translation](https://github.com/jmbruel/basics)
[BracketsUML/diagrams at master · KyleKorndoerfer/BracketsUML](https://github.com/KyleKorndoerfer/BracketsUML/tree/master/diagrams)
[Examples Gallery — PlantUML Client in Python 1.0.0 documentation](http://plantweb.readthedocs.io/examples.html)

styling:
[hackebrot/plantuml-snippets: Code snippets for drawing diagrams with PlantUML](https://github.com/hackebrot/plantuml-snippets)
[mmmpa/colors_for_plantUML](https://github.com/mmmpa/colors_for_plantUML)
[templates/plantuml at master - mark.george/templates](https://isgb.otago.ac.nz/infosci/mark.george/templates/tree/master/plantuml)

### GaaS (graph as a service)

With an HTTP client and scraping code, any DSL with web editor could be made as a service. This is especially easy if the DSL is provided as a library of course.

[Your Graphviz, UMLGraph or PlantUML for your README](http://www.gravizo.com/)

PlantUML's [service](http://plantuml.com/server) mode, see[jQuery](http://plantuml.com/jquery) and JavaScript [async](http://plantuml.com/demo-javascript-asynchronous) and [sync](http://plantuml.com/demo-javascript-synchronous) integration.

[Excalidraw | Hand-drawn look & feel • Collaborative • Secure](https://excalidraw.com/) virtual whiteboard
[Excalidraw: Cool JS Tricks Behind the Scenes - Christopher Chedeau aka @vjeux at @ReactEurope 2020 - YouTube](https://www.youtube.com/watch?v=fix2-SynPGE)
[Rough.js](https://roughjs.com/)

[Online Diagram Software & Visual Solution | Lucidchart](https://www.lucidchart.com/pages/)
[Online Collaborative Whiteboard | Sketchboard](https://sketchboard.io/)
[diagrams.net](https://app.diagrams.net/) Formerly draw.io

## Gaphor

[Modeling for Everyone | Gaphor](https://gaphor.org/)
[Gaphor: Open Source Graphical Modeling Tool - It's FOSS](https://itsfoss.com/gaphor-modeling-tool/)

## GUI Tools

PlantUML's weakness (and strength, sort of) is the user cannot (and need not) specify location of the nodes. This became an issue for component diagrams where we need more control on node position and edge routing, which are crucial for component diagram for a better look and feel of the diagram.

[UML Diagramming Tools | Diagramming.org](http://www.diagramming.org/)
[Our list of online modeling tools](http://modeling-languages.com/web-based-modeling-tools/)

[yEd - Graph Editor](http://www.yworks.com/products/yed)
[Astah Community - Free UML Modeling tool | Astah.net](http://astah.net/editions/community)
[Gaphor UML Modelling](http://gaphor.sourceforge.net/download.php) (Python)
[Modelio Open Source Community](https://www.modelio.org/index.php)
[ArgoUML](http://argouml.tigris.org/) the UI is bad
[UMLet - Free UML Tool for Fast UML Diagrams](http://www.umlet.com/)
[Violet UML Editor : easy to use, completely free](http://alexdp.free.fr/violetumleditor/page.php)

### yEd

After trying out several GUI tools, yEd comes to my liking.

- decent and non-buggy UI
- better community support
- can save as XML (`graphml`) format that can be edited manually or programmatically
- provides (limited) transform with _Properties Mapper_

> see `yed.md`

### Chrome Apps

[Gliffy Diagrams - Chrome Web Store](https://chrome.google.com/webstore/detail/gliffy-diagrams/bhmicilclplefnflapjmnngmkkkkpfad): the diagram is saved as JSON
[Sketchboard.io - Chrome Web Store](https://chrome.google.com/webstore/detail/sketchboardio/bgafhjpdkfjfmmjbebbdckolonomaoil)

## Code Generation

[lovasoa/dia2code: Dia2Code is a small utility used to generate code from a Dia diagram.](https://github.com/lovasoa/dia2code)
