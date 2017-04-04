---
permalink: /
layout: index
title:
---


<div class="homepage-hero-module">
    <div class="video-container">
      <div class="filter text-center">
        <h2 class="wow slide-fade">
            Guard Your Oragnization's End Points And Products<br/>
            Using Against Any Known &amp; Unknowned Adversaries
          </h2>
          <button class="button large black">Learn More</button>&nbsp;&nbsp;&nbsp;&nbsp;
          <button class="button success large">Contact Us</button>
        </div>
        <video autoplay loop class="fillWidth hide-for-small-only" defaultPlayBackRate="0.1">
            <source src="assets/img/blue-digital-binary-data-on-computer-screen-loopable.mp4" type="video/webm" />Your browser does not support the video tag. I suggest you upgrade your browser.
        </video>
        <div class="poster hidden show-for-small-only">

        </div>
      </div>
</div>

<div class="row alternate fullWidth testMe" style="marging-bottom:5px;">
<div class="small-12 columns text-center" style="padding-top:50px;">
  <h1>Security Without Obscurity</h1>
</div>
{% for item in site.data.benefits %}
<div class="small-12 large-4 columns text-center  slide-up">
  <br/>
  <h3>{{item.Title}}</h3>
  <p><i class="{{item.fa}} fa-5x"></i></p>
  <p>{{item.Content}}</p>
  <br/>
</div>
{% endfor %}
<div class="small-12 text-center slide-fade" style="margin-top: 10px; padding-bottom:50px;">
  <a href="#" class="button large alert">Learn More About What Makes Us Better</a>
</div>
</div>


<div class="row" style="text-transform:capitalize;">
  <div class="small-12 columns text-center">
    <h2>Presenting TrulyProtect's Patented TPVisor Trusted Platform</h2>
  </div>
  <div class="small-12 large-6 columns text-center">
    <img src="http://placehold.it/600x400" class="wow slide-right" />
  </div>
  <div class="small-12 large-6 columns text-left">
    <br/>
    <ul class="fa-ul wow slide-left">
      {% for item in site.data.bullets %}
          <li class="visorItem">{{item.Content}}</li>
          <br/>
      {% endfor %}
  </ul>

  </div>

</div>

<div class="row fullWidth" style="margin-top:5px;">
  <div class="small-12 columns text-center fullWidth" style="position:relative;">
    <img src="http://placehold.it/2000x750">
    <div style="position:absolute; bottom:0; left:0; right:0; padding-left:5rem; padding-right:5rem; padding-bottom:2rem">
      <h3>Utilize TrulyProtect's Core Technology And Protect Your Business Assets</h3>
      <h3>By Employing Our Top Cyber Solutions</h3>
    </div>
  </div>
</div>

<div class="row fullWidth">
  {% for item in site.data.products %}
  <div class="small-12 large-4 columns text-center">
      <h3>{{item.Title}}</h3>
      <p>{{item.Content}}</p>
  </div>
  {% endfor %}
</div>

<div class="row alternate fullWidth text-center" style="padding-top:50px;">
  <div class="small-12 columns">
    <h3>Protect Your Organization Now</h3>
  </div>
  <div class="small-12 columns">
    <img src="assets/img/TP_Bear_logo_Vector.png" style="max-height:250px;" />
  </div>
  <div class="small-12 columns" style="padding-top:50px;">
    <a class="button alert large" href="/contact">Contact Us Now</a>
  </div>
</div>
