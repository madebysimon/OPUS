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
    flex: 0 1 200px;
    flex: 1 1 200px;
    border: 1px solid;
    border-radius: 5px;
    border-color: #f8f8f8;
    text-align: center;
    margin: .25em;
    }
    
  .content {
    text-align: left;
    margin: 3em;
  } 
  body {
    font-family: system-ui, serif;
  }
  </style>
  </head>
  <body>
  <div class="parent">
    <div class="child" style="">
      <h2>Planned</h2>
      <div class="content">
	{% include_relative future.md %}
      </div>
    </div>
        <div class="child" style="">
      <h2>Current</h2>
      <div class="content">
	{% include_relative present.md %}
      <br>
      </div>
    </div>
    <div class="child" style="">
      <h2>Backlog</h2>
      <div class="content">
 	{% include_relative future.md %}
      <br>
      </div>
    </div>
  </div>
  </body>
</html>

