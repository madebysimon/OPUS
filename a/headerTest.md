---
title: HeaderTest
nav_exclude: true
---
<!DOCTYPE html>
<html lang="en" >
<head>
  <meta charset="UTF-8">
  <title>CodePen - Scale hero section on scroll</title>
  <link rel="stylesheet" href="./style.css">
<style>
  body {
  letter-spacing: -1px;
  text-align: center;
  font-size: 20px;
  min-height: 100vh;
  color: #fff;
  margin: 0;
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
  width: 100%;
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
</div>
<div class="content">

# This is markdown stuff 

</div>
  <script src='https://cdnjs.cloudflare.com/ajax/libs/jquery/3.4.1/jquery.min.js'></script><script  src="./script.js"></script>

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
