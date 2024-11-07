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
    <a href="https://www.linkedin.com/pub/jonathon-volkmar/28/a5b/522">
        <img src="/images/icons/linkedin12.png" class="socialbadge"/>
    </a>
</div>

<a id="about"></a>

# Hi there

I am Software Engineer living in Seattle, formerly at Microsoft. Interests include front-end web development, C++ systems and graphics programming, and data visualization.

Email: jon (at) jonvolkmar (dot) com

<a name="portfolio"></a>

# Portfolio

Here are a few personal and academic projects I have worked on over the past few years.

<div class="tiles">
{% for post in site.categories.portfolio reversed %}
	{% include portfolio-post-grid.html %}
{% endfor %}
</div><!-- /.tiles -->