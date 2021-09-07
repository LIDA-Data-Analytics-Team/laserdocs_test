---
layout: default
title: Mermaid Test
parent: Mermaid
nav_order: 1
mermaid: true
---

<html lang="en">

<head>
  <script src="https://cdn.jsdelivr.net/npm/mermaid/dist/mermaid.min.js">
  <script>mermaid.initialize({startOnLoad:true});</script>
</head>

<body>
  <div class="mermaid">
    graph 
      TB;A-->B;
  </div>
</body>

</html>

# Flowcharts - Basic Syntax

```html
<div class="mermaid">
graph TD;
A-->B;
A-->C;
B-->D;
C-->D;
</div>
```