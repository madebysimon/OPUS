<html lang="en" >
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <style>
    .container {
      padding-right: 0px;
      padding-left: 0px;
      margin-right: auto;
      margin-left: auto;
      padding-top: 1rem;
      max-width: 735px;
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
      border-top: 1px solid #DADADA;
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
      padding-top: 0px;
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
		<svg class="svg-icon" viewBox="0 0 20 20">
			<path d="M10,10.9c2.373,0,4.303-1.932,4.303-4.306c0-2.372-1.93-4.302-4.303-4.302S5.696,4.223,5.696,6.594C5.696,8.969,7.627,10.9,10,10.9z M10,3.331c1.801,0,3.266,1.463,3.266,3.263c0,1.802-1.465,3.267-3.266,3.267c-1.8,0-3.265-1.465-3.265-3.267C6.735,4.794,8.2,3.331,10,3.331z"></path>
			<path d="M10,12.503c-4.418,0-7.878,2.058-7.878,4.685c0,0.288,0.231,0.52,0.52,0.52c0.287,0,0.519-0.231,0.519-0.52c0-1.976,3.132-3.646,6.84-3.646c3.707,0,6.838,1.671,6.838,3.646c0,0.288,0.234,0.52,0.521,0.52s0.52-0.231,0.52-0.52C17.879,14.561,14.418,12.503,10,12.503z"></path>
		</svg>
            </div>
            <div class="aks-accordion-item-title">
              <h3 itemprop="name">by @{{ page.author }}</h3>
            </div>
          </div>
          <div class="aks-accordion-item-content" itemscope itemprop="acceptedAnswer" itemtype="https://schema.org/Answer" data-accordion-content="">
            <p itemprop="text"><h4>published on {{ page.published }} | last edit: {{ page.last_edit }}</h4><br>this article was written by @{{ page.author }}<br><br>Thanks to all further contributors to this page:<br>{{ page.contributors }}</p>
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