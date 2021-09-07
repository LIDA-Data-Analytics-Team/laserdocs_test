---
layout: default
title: Mermaid Test
parent: Mermaid
nav_order: 1
---

<head>
  <script src="https://cdn.jsdelivr.net/npm/mermaid/dist/mermaid.min.js">
  <script>mermaid.initialize({startOnLoad:true});</script>
</head>

# Flowcharts - Basic Syntax

<div class="mermaid">
graph TD;
A-->B;
A-->C;
B-->D;
C-->D;
</div>
