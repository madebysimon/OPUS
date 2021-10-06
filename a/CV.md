---
title: CV
nav_exclude: true
---

## Notable Experiences

<!DOCTYPE html>
  <html lang="en" >
  <head>
    <meta charset="UTF-8">
    <style>
      .container ul {
      margin: 0;
      margin-top: 10px;
      list-style: none;
      position: relative;
      padding: 0px 60px;
      color: #000;
    }
    .container ul:before {
      content: "";
      width: 0px;
      height: 100%;
      position: absolute;
      border-left: 2px dashed #ddd;
    }
    .container ul li {
      position: relative;
      margin-left: 30px;
      background-color: rgba(0, 0, 0, 0.05);
      padding: 20px;
      border-radius: 6px;
      width: auto;
      box-shadow: 0 0 4px rgba(0, 0, 0, 0.12), 0 2px 2px rgba(0, 0, 0, 0.08);
    }
    .container ul li:not(:first-child) {
      margin-top: 60px;
    }
    .container ul li > span {
      width: 2px;
      height: 100%;
      background: #ddd;
      left: -30px;
      top: 0;
      position: absolute;
    }
    .container ul li > span:before, .container ul li > span:after {
      content: "";
      width: 8px;
      height: 8px;
      border-radius: 50%;
      border: 2px solid #ddd;
      position: absolute;
      background: #fff;
      left: -5px;
      top: 0;
    }
    .container ul li span:after {
      top: 100%;
    }
    .container ul li > div {
      margin-left: 10px;
    }
    .container div .title {
      font-weight: 600;
      font-size: 20px;
      margin-bottom: 5px;
    }
    .container div .type {
      font-weight: 500;
      margin-top: 5px;
      margin-bottom: 10px;
    }
    .container div .info {
      font-weight: 300;
    }
    .container span.number {
      height: 100%;
    }
    .container span.number span {
      position: absolute;
      font-size: 12px;
      left: -50px;
      font-weight: bold;
    }
    .container span.number span:first-child {
      top: 0;
    }
    .container span.number span:last-child {
      top: 100%;
    }
    </style>
  </head>
  <body>
    <div class="container">
      <ul>
        <li><span></span>
          <div>
            <div class="title">Wissenschaftlicher Mitarbeiter</div>
            <div class="type">Universitätsklinikum Hamburg Eppendorf</div>
            <div class="info">Let&apos;s make coolest things in cssLet&apos;s make coolest things in cssLet&apos;s make coolest things in cssLet&apos;s make coolest things in css</div>
          </div> <span class="number"><span>today <br> 10/2021</span> <span>9/2021</span></span>
        </li>
        <li>
          <div><span></span>
            <div class="title">Codify</div>
            <div class="info">Let&apos;s make coolest things in javascript</div>
            <div class="type">Presentation</div>
          </div> <span class="number"><span>13:00</span> <span>14:00</span></span>
        </li>
        <li>
          <div><span></span>
            <div class="info">Let&apos;s make coolest things in css</div>
            <div class="title">Codify</div>
            <div class="type">Review</div>
          </div> <span class="number"><span>15:00</span> <span>17:45</span></span>
        </li>
      </ul>
    </div>
  </body>
</html>