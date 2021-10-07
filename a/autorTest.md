---
title: Autor
nav_exclude: true
---

## Notable Experience

---

<html lang="en" >
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <style>
    .container {
      padding-right: 10px;
      padding-left: 0px;
      margin-right: auto;
      margin-left: auto;
      padding-top: 2rem;
      max-width: 800px;
    }
    @media (min-width: 768px) {
      .container {
        width: 750px;
      }
    }
    @media (min-width: 992px) {
      .container {
        width: 970px;
      }
    }
    @media (min-width: 1200px) {
      .container {
        width: 1170px;
      }
    }
    [data-ripple] {
      position: relative;
      overflow: hidden;
    }
    .ripple-effect {
      position: absolute;
      border-radius: 9999px;
      animation: ripple-animation 2s;
    }
    @keyframes ripple-animation {
      from {
        transform: scale(1);
        opacity: 0.4;
      }
      to {
        transform: scale(100);
        opacity: 0;
      }
    }
    .aks-accordion {
      width: 100%;
      margin: 0 auto;
    }
    .aks-accordion-row {
    }
    .aks-accordion-item {
      width: 100%;
      border-bottom: 1px solid #DADADA;
      padding-top: 20px;
      padding-right: 5px;
      padding-bottom: 12px;
      padding-left: 5px;
      cursor: pointer;
    }
    .aks-accordion-item-row {
      display: flex;
      align-items: center;
      justify-content: flex-start;
    }
    .aks-accordion-item-icon {
      width: 25px;
      height: 25px;
      background: rgb(218,218,218,0.5);
      border-radius: 9999px;
      cursor: pointer;
      user-select: none;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-right: 1rem;
      text-align: center;
    }
    .aks-accordion-item-icon svg {
      width: 15px;
      fill: black;
      margin: 0 auto;
    }
    .aks-accordion-item-title {
      width: 90%;
      text-align: left;
      line-height: 1.5;
      display: flex;
      align-items: center;
    }
    .aks-accordion-item-title h4 {
      margin: 0;
    }
    .aks-accordion-item-content {
      display: none;
      width: 100%;
      padding-top: 12px;
      padding-right: 8px;
      padding-bottom: 0;
      padding-left: 42px;
      overflow: hidden;
      word-break: break-word;
      width: 88%;
      text-align: left;
      line-height: 1.5;
    }
    .aks-accordion-item.opened .aks-accordion-item-icon-open {
      display: none;
    }
    .aks-accordion-item-icon-close {
      display: none;
    }
    .aks-accordion-item.opened .aks-accordion-item-icon-close {
      display: block;
    }
    @media screen and (max-width: 500px) {
      .aks-accordion {
        width: 100%;
      }
      .aks-accordion-item-content {
        padding-left: 11px;
        width: 92%;
      }
    }
    </style>
  </head>
  <body>
  <div class="container">
    <div class="aks-accordion" itemscope itemtype="https://schema.org/FAQPage" data-accordion="">
      <div class="aks-accordion-row">
        <div class="aks-accordion-item" itemscope itemprop="mainEntity" itemtype="https://schema.org/Question" data-accordion-item="" data-ripple="#00000026">
          <div class="aks-accordion-item-row">
            <div class="aks-accordion-item-icon">
            </div>
            <div class="aks-accordion-item-title">
              <h3 itemprop="name">written by @Simon</h3>
            </div>
          </div>
          <div class="aks-accordion-item-content" itemscope itemprop="acceptedAnswer" itemtype="https://schema.org/Answer" data-accordion-content="">
            <p itemprop="text">Simon Kelch is the author of this article.<a href="#">test</a></p>
          </div>
        </div>
      </div>
    </div>
  </div>
  <script src='/assets/page/jquery.min'></script>
  <script src="./script.js"></script>
  <script>
      (function () {
    "use strict";
    var jQueryPlugin = (window.jQueryPlugin = function (ident, func) {
      return function (arg) {
        if (this.length > 1) {
          this.each(function () {
            var $this = $(this);
            if (!$this.data(ident)) {
              $this.data(ident, func($this, arg));
            }
          });
          return this;
        } else if (this.length === 1) {
          if (!this.data(ident)) {
            this.data(ident, func(this, arg));
          }
          return this.data(ident);
        }
      };
    });
  })();
  (function () {
    "use strict";
    function Accordion($roots) {
      var element = $roots;
      var accordion = $roots.first("[data-accordion]");
      var accordion_target = $roots.find("[data-accordion-item]");
      var accordion_content = $roots.find("[data-accordion-content]");
      $(accordion_target).click(function () {
        $(this).toggleClass("opened");
        $(this).find(accordion_content).slideToggle("slow");
        $(this).siblings().find(accordion_content).slideUp("slow");
        $(this).siblings().removeClass("opened");
      });
    }
    $.fn.Accordion = jQueryPlugin("Accordion", Accordion);
    $("[data-accordion]").Accordion();
    function Ripple_Button($root) {
      var elements = $root;
      var ripple_btn = $root.first("[data-ripple]");
      $(ripple_btn).on("click", function (event) {
        event.preventDefault();
        var $div = $("<div/>"),
          btnOffset = ripple_btn.offset(),
          xPos = event.pageX - btnOffset.left,
          yPos = event.pageY - btnOffset.top;
        $div.addClass("ripple-effect");
        $div.css({
          height: ripple_btn.height(),
          width: ripple_btn.height(),
          top: yPos - $div.height() / 2,
          left: xPos - $div.width() / 2,
          background: ripple_btn.data("ripple") || "#ffffff26"
        });
        ripple_btn.append($div);
        window.setTimeout(function () {
          $div.remove();
        }, 2000);
      });
    }
    $.fn.Ripple_Button = jQueryPlugin("Ripple_Button", Ripple_Button);
    $("[data-ripple]").Ripple_Button();
  })();
    </script>
  </body>
</html>

