---
layout: page
permalink: /dailydoodletest/
title: "Daily Doodle Test"
description: "Testing new format"
redirect: false
---


Testing new format

{% for i in data.dailydoodle.doodle %}
  
  <div class="col-md-4 col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path=i.path
            title={{ i.date | date: "%b %d, %Y" }} + " " + {{i.title}}
            class="gallery img-fluid rounded z-depth-1" 
            zoomable=true 
        %}
        <div class="caption">
        {{ i.date | date: "%D" }}
        </div>
  </div>

{% endfor %}