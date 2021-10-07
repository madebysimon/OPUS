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
    flex: 0 1 240px;
    flex: 1 1 240px;
    border: 1px solid;
    border-radius: 20px;
    border-color: #f8f8f8;
    text-align: center;
    background: rgba(44,71,112,.1);
    background: linear-gradient(0deg, rgba(44,71,112,.15) 0%, rgba(44,71,112,.1) 100%);
    backdrop-filter: blur(10px) saturate(100%) contrast(45%) brightness(130%);
    box-shadow: 0 0 .5rem 0 rgba(0, 0, 0, 0.1);
    margin: 1em;
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

