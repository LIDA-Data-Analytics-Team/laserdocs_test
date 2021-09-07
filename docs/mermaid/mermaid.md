---
layout: default
title: Mermaid Test
parent: Mermaid
nav_order: 1
mermaid: true
---

<div class="mermaid">graph TB;A-->B;</div>

```html
<header>
	<script src="https://cdn.jsdelivr.net/npm/mermaid/dist/mermaid.min.js">
</header>
```

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