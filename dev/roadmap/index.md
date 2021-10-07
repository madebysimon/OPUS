---
title: Roadmap
---

# Roadmap

<html>
  <head>
  <style>
      .parent {
    display: flex;
    flex-wrap: wrap;
  }
  .child {
    flex: 0 1 300px;
    flex: 1 1 300px;
    background: white;
    border: 1px;
    border-radius: 15%;
    border-color: #f8f8f8;
    text-align: center;
  }
  body {
    font-family: system-ui, serif;
  }
  </style>
  </head>
  <body>
  <div class="parent">
    <div class="child">
	{% include_relative past.md %}
    </div>
    <div class="child">
	{% include_relative present.md %}
    </div>
    <div class="child">
	{% include_relative future.md %}
    </div>
  </div>
  </body>
</html>