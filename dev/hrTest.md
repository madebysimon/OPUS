---
title: <Hr>Test
nav_exclude: true
---
this article is written for mental health professionals

# HR Test
Pro
{: .label }

This is a paragraph.

<html>
<style>
hr {
  border: none;
  border-top: 1px solid rgba(255,255,255,.3);
  border-bottom: 1px solid rgba(0,0,0,.08);
  margin: 2.5em 0;
  position: relative;
}
hr:before,hr:after {
  content: '';
  position: absolute;
  bottom:0px;
  height: 5em;
  width: 100%;
  background: radial-gradient(ellipse at bottom, rgba(255,255,255,0.35) 0%,rgba(255,255,255,0) 70%);
  z-index:0;
}
hr:after {
  top:0px;
  bottom:auto;
  height: 1.5em;
  background: radial-gradient(ellipse at top, rgba(0,0,0,0.06) 0%,rgba(0,0,0,0) 70%);
}
</style>
<hr>
</html>

This is another.
