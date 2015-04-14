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

[Allen Holub's UML Quick Reference](http://www.holub.com/goodies/uml/)

<!-- more -->

## Text based

I used to use [Dia](https://wiki.gnome.org/Apps/Dia/). But it was very buggy and no longer updated. I then went on to look for alternatives.

I am frustrated with the UI diagram apps:
- layout of components takes time
- it is difficult to modify the diagrams in UI (especially for batch operations, e.g. rename, grouping)
- application lock-in becaused of the saved file format

So I focused on toolkits that provides a DSL for drawing UML from plain text.
Candidates are (ranked according to the criteria below):

Tool           | Language   | Diagrams           | Remark
--------       | -------    | -------            | -------
[PlantUML][]   | Java       | Activity, State, Sequence, Component, Class, Object, Use Case, DITAA, JCCKit, Sudoku, XEarth | [live](http://www.plantuml.com/plantuml/), [Language Reference](http://plantuml.sourceforge.net/PlantUML_Language_Reference_Guide.pdf)
[blockdiag][]  | Python     | Block, Activity, Sequence, Network, Rack, Packet | [live](http://blockdiag.appspot.com/)
[mermaid][]    | JavaScript | Flowchart (Activity), Sequence, Gantt | [live](http://knsv.github.io/mermaid/live_editor/)
[js-sequence-diagrams][] | JavaScript | Sequence | live
[UMLGraph][]   | Java       | Sequence, Class    |
[ckwnc][]      | ?          | Sequence           | live **only**, C-like syntax
[Graphviz][]   | C          | Digraph            | supports `dot`, layout/rendering layer for PlantUML and UMLGraph

[PlantUML]: http://plantuml.sourceforge.net/
[blockdiag]: http://blockdiag.com/en/
[mermaid]: https://github.com/knsv/mermaid
[js-sequence-diagrams]: http://bramp.github.io/js-sequence-diagrams/
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
- binings to more projects indicates widespread usage

BTW, blockdiag would be the first runner up. It also features several unique diagram types.

### GaaS (graph as a service)

[Your Graphviz, UMLGraph or PlantUML for your README](http://www.gravizo.com/)

## GUI

[Gaphor UML Modelling](http://gaphor.sourceforge.net/download.php)  (Python)

[UMLet - Free UML Tool for Fast UML Diagrams](http://www.umlet.com/)

[ArgoUML](http://argouml.tigris.org/)

[Violet UML Editor : easy to use, completely free](http://alexdp.free.fr/violetumleditor/page.php)

[Lucidchart Diagrams - Desktop - Chrome Web Store](https://chrome.google.com/webstore/detail/lucidchart-diagrams-deskt/djejicklhojeokkfmdelnempiecmdomj?hl=en)

[Gliffy Diagrams - Chrome Web Store](https://chrome.google.com/webstore/detail/gliffy-diagrams/bhmicilclplefnflapjmnngmkkkkpfad?hl=en)

[Sketchboard.io - Chrome Web Store](https://chrome.google.com/webstore/detail/sketchboardio/bgafhjpdkfjfmmjbebbdckolonomaoil?hl=en)
