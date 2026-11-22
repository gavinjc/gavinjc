## Gavin Charlesworth

Software engineer in Melbourne, Australia. Twenty-five years of it, mostly C++ on long-lived
enterprise systems.

What's here is the other half: Windows applications, local-first AI, and developer tooling,
built over the past year largely with AI-assisted development.

### Published on the Microsoft Store

Four Windows apps under [The Bureau of Stuff](https://apps.microsoft.com/search/publisher?name=The+Bureau+of+Stuff).
Each adds a File Explorer right-click action — WinUI 3, a native shell extension, packaged as MSIX.

| App | What it does | Repo |
| --- | --- | --- |
| [ClickTo: PDF](https://apps.microsoft.com/detail/9nf364x93v6l) | Combine images into one ordered PDF | [ClickToPdf](https://github.com/gavinjc/ClickToPdf) |
| [ClickTo: Images](https://apps.microsoft.com/detail/9nw19cxqrll7) | Save PDF pages as PNG, JPEG or TIFF | [ClickToImages](https://github.com/gavinjc/ClickToImages) |
| [ClickTo: Speech](https://apps.microsoft.com/detail/9n37b96cs0p5) | Turn documents into audio with Windows voices | [ClickToSpeech](https://github.com/gavinjc/ClickToSpeech) |
| [ClickTo: Slideshow](https://apps.microsoft.com/detail/9plkc14mgc3n) | Photos and music into an MP4 or editable PowerPoint | [ClickToSlideshow](https://github.com/gavinjc/ClickToSlideshow) |

All four sit on [Bureau.Common](https://github.com/gavinjc/Bureau.Common) — shared WinUI chrome,
so the About dialog, Help, theming and message bar are written once.

### Other projects

**[Atlas](https://github.com/gavinjc/Atlas)** — local-first photo and document search for Windows.
CLIP embeddings run on-device through ONNX Runtime with an NPU path; nothing leaves the machine.
Flutter front end, Python and FastAPI behind it. *Dart, Python*

**[LogViewer](https://github.com/gavinjc/LogViewer)** — config-driven multi-source log viewer.
Live tail, filtering, archive mode. *Python, PySide6*

### How this gets built

I use AI tooling daily and have written a coordinator for it: headless coding agents dispatched
across a group of related projects, with the concurrency control needed to keep several of them
from interfering with each other — a shared lock for anything driving the desktop, one agent per
project, and a hook that blocks an agent going around it. The apps above are built and maintained
through it.

The view I formed building that: agents are productive and are not trustworthy by default. Most of
the engineering is deciding what they may do unsupervised and what has to come back for review.

---

Melbourne, Victoria · [gavin.charlesworth@outlook.com](mailto:gavin.charlesworth@outlook.com)
