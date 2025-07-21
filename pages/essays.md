---
title: Essays
layout: page
permalink: /essays.html
---

<div class="row">
    {% for essay in site.essays %}
    {% assign item = site.data[site.metadata] | where: "objectid", essay.featured_image | first %}
    {% capture imageSrc %}{{ item.image_small | relative_url }}{% endcapture %}
        <div class="col-6 col-lg-4 mb-4 ">
            <div class="btn text-wrap w-100 image-btn" style="background-image: url({{ imageSrc }});">
                <div class="darkened-overlay"></div>
                <a href="{{ essay.url | relative_url }}"><h2 class="w-100 fs-2 p-1">{{ essay.title }}</h2></a>
            </div>
        </div>
    {% endfor %}
</div>