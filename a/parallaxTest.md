---
title: HeaderTest
nav_exclude: true
---
<html>
<head>
  <meta charset="UTF-8">
<style>
  body {
  min-height: 100vh;
}
.hero {
  background: url('https://images.unsplash.com/photo-1550353127-b0da3aeaa0ca') no-repeat center center;
  justify-content: center;
  background-size: cover;
  flex-direction: column;
  align-items: center;
  position: fixed;
  display: flex;
  min-height: 25vh;
  max-width: 800px;
}
.content {
  box-shadow: 0 0 40px rgba(255,255,255,.2);
  border-radius: 10px;
  justify-content: center;
  align-items: flex-end;
  padding-bottom: 40px;
  position: relative;
  background: #fff;
  min-height: 100vh;
  height: auto;
  display: flex;
  top: 25vh;
}
</style>
</head>
<body>

<div class="hero">
  <h1>Get scrollin'</h1>
</div>
<div class="content">

# This is markdown stuff 

</div>
  <script src='/assets/page/jquery.min'></script>
  <script>
    $(window).scroll(function() {
  var scroll = $(window).scrollTop();
  $(".hero").css({
    transform: 'translate3d(0, -'+(scroll/10)+'%, 0)'
    });
  });
  </script>
</body>
</html>