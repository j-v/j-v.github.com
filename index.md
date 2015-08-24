---
layout: main
permalink: /
title: 
image:
  feature: me_bike_helmet.jpg
---

<div id="social" class="socialbox">
    <!-- social network icons from http://www.flaticon.com/packs/simpleicon-social-media -->
    <a href="https://github.com/j-v/">
        <img src="/images/icons/github13.png" class="socialbadge"/>
    </a>
    <a href="https://twitter.com/jonotron">
        <img src="/images/icons/twitter21.png" class="socialbadge"/>
    </a>
    <a href="https://www.linkedin.com/pub/jonathon-volkmar/28/a5b/522">
        <img src="/images/icons/linkedin12.png" class="socialbadge"/>
    </a>
</div>

<a id="about"></a>

# Hi there

Software Engineer at Microsoft, working on Text Input and Pen UX for Windows.

I have a penchant for C++ programming and big data processing. 

Interests in computer vision, graphics, music...

<a name="portfolio"></a>

# Portfolio

<div class="tiles">
{% for post in site.categories.portfolio %}
	{% include portfolio-post-grid.html %}
{% endfor %}
</div><!-- /.tiles -->