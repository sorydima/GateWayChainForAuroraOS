# Architecture Overview

```
+-------------+     Matrix Homeserver
|  QML  UI    |  <--   REST / WebSockets
+-------------+          ^
       |                 |
       v                 |
+-------------+      +---+----+
|   Qt/C++    |----->| Matrix |
| Application |      | Client |
+-------------+      +--------+
       |
       v
 +------------+
 |  Storage   |   (SQLite)
 +------------+
```

* **QML UI** — Sailfish/Aurora‑native GUI components  
* **Qt/C++ Core** — business logic, node state, and plugin system  
* **Matrix Client** — lightweight wrapper around `libQuotient` providing encrypted messaging for REChain gossip  
* **Storage Layer** — single‑user SQLite DB holding keys & cached blocks

Modules live in `src/`, QML in `qml/`, translations in `translations/`, and RPM packaging scripts under `rpm/`.

_Last updated: 2025-07-06_
