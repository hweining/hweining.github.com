---
layout: page
title: No Zuo No Die
tagline: Supporting tagline
---
{% include JB/setup %}
<link type="text/css" rel="Stylesheet" href="/assets/home/home.css" />
<div id="banner-fade" title="这家伙很懒"><ul class="bjqs"></ul></div>

<script>
(function($){
    var imageList = [
        "/assets/home/Otter/4425238315_cf801e4e08_b.jpg:    10%",    //
        "/assets/home/HarpSeal/9197166267_9ca479c4bc_o.jpg: 80%",    //
        "/assets/home/Otter/cac1ce12e59a563bd052662f65fcd589.jpg",
        "/assets/home/HarpSeal/2839526_172840877177_2.jpg:  center",
        "/assets/home/Otter/5964623878_4c51e27aff_b.jpg  : 50%",
        "/assets/home/HarpSeal/Baby_Seal_2.jpg",
        "/assets/home/Otter/62973_small-cb1359744191.jpg : 50%",
        "/assets/home/HarpSeal/9199946140_693361cc26_o.jpg: 80%",
        "/assets/home/HarpSeal/9199948412_5e39d33949_o.jpg: 0%", //
        "/assets/home/HarpSeal/1337256000000.cached.jpg",
        "/assets/home/HarpSeal/a-harp-seal-pup-lies-on-its-side-norbert-rosing.jpg",
        "/assets/home/HarpSeal/9199947200_e711f09e55_o.jpg",
        "/assets/home/HarpSeal/r9c6552-2-800x533.jpg: 50%",      //
        "/assets/home/HarpSeal/harp-seal-pup.jpg",
        "/assets/home/Otter/enhanced-31254-1406586403-17.jpg",
        "/assets/home/Otter/Bath-Time-Sea-Otter-480x800.jpg"
    ];

    if ($(window).width() < 600) {
        imageList = imageList.slice(0, 10);
    }

    $('#banner-fade .bjqs').html($.map(imageList, function(def) {
        var arr = def.match(/^([^\s]+)\s*:\s*(.*)$/);
        var imageSrc = arr ? arr[1] : def;
        var cssStyle = arr ? "; background-position: 0 " + arr[2] : "";
        return '<li class="banner-img" style="background-image: url(' + imageSrc + ')' + cssStyle + '" >'
             + '<a href="http://github.com/lwr/lwr.github.io">&nbsp;</a></li>';
    }).join(""));

    $('#banner-fade').bjqs({
      width  : '640',
      height : '360',

      // animation values
      animtype : 'fade',  // accepts 'fade' or 'slide'
      animduration : 500,  // how fast the animation are
      animspeed : 10000,   // the delay between each slide

      prevtext : "<",
      nexttext : ">",
      centercontrols : false,

      responsive : true
    });
    $(".bjqs-markers li a").each(function(index, e) {
        e.innerHTML = (1 + index).toString(36).toUpperCase();
    });
})(jQuery);
</script>

Follow me on [Twitter →](https://twitter.com/SoloCompany) （（ 话痨指数 %10（（ 精神污染指数 80%

## Blog Posts

<ul class="posts">
  {% for post in site.posts limit:8 %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
    <li><a href="/archive.html">More &raquo;</a></li>
</ul>
    


<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

## To-Do

This theme is still unfinished. If you'd like to be added as a contributor, [please fork](http://github.com/plusjade/jekyll-bootstrap)!
We need to clean up the themes, make theme usage guides with theme-specific markup examples.


