---
title: Essays
layout: page
permalink: /essays.html
tags:
published: false
---

<h2 id="page-title">{{ page.title }}</h2>
<div class="alert alert-primary text-center" role="alert">
  Progress Note: The sample essays currently available here are placeholders designed to showcase the features
  that future essays might have.
</div>
<a id="return-to-all" class="d-none" aria-hidden="true" href="#"><svg class="bi icon-sprite" aria-hidden="true"><use xlink:href="{{ '/assets/lib/icons/arrow-left.svg' | relative_url }}"/></svg> Return to all essays</a>

<!--<p>
<a class="btn btn-small btn-outline-light rounded-pill mb-1 tag-btn" href="#">all</a>
{% for film in site.films %}
    <a class="btn btn-small btn-outline-light rounded-pill mb-1 tag-btn" href="#{{ film.title | slugify }}">{{ film.title | slugify }}</a>
{% endfor %}
{% assign themes = site.data.config-facets | where: "name", "themes" | first %}
{% assign theme-tags = themes.values | split: "|" %}
{% for tag in theme-tags %}
    <a class="btn btn-small btn-outline-light rounded-pill mb-1 tag-btn" href="#{{ tag | slugify }}">{{ tag | slugify }}</a>
{% endfor %}
</p>-->

<!--
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
-->
{% for essay in site.essays %}
{% assign item = site.data[site.metadata] | where: "objectid", essay.featured_image | first %}
{% capture imageSrc %}{{ item.image_small | relative_url }}{% endcapture %}
<div class="essay row mb-4{% for tag in essay.tags %} {{ tag | slugify }}{% endfor %}">
    <div class="col-md-6 col-lg-3 mb-2">
        <a href="{{ essay.url | relative_url }}"><img class="rounded me-2 w-100" src="{{ imageSrc }}" alt=""><span class="visually-hidden">{{ essay.title }}</span></a>
    </div>
    <div class="col-md-6 col-lg-9 mb-2">
        <h3><a href="{{ essay.url | relative_url }}">{{ essay.title }}</a></h3>
        {% if essay.author %}<p class="by-line">By {{ essay.author }}</p>{% endif %}
        {% if essay.tags %}<p class="essay-tags">
        {% for tag in essay.tags %}
            <a class="btn btn-small btn-outline-light rounded-pill mb-1 tag-btn" href="#{{ tag | slugify }}">{{ tag | slugify }}</a>
        {% endfor %}
        </p>{% endif %}
    </div>
</div>
{% endfor %}

<script>
    function filterEssays(){
        var pageTitle = document.getElementById("page-title");
        var returnToAll = document.getElementById("return-to-all");
        // iterate through essays
        var essays = document.getElementsByClassName("essay");
        for (let i = 0; i < essays.length; i++) {
            if (location.hash == "") {
                // show all essays
                essays[i].classList.remove("d-none");
                essays[i].setAttribute("aria-hidden", "false");
                // hide link to return to all essays and remove focus
                returnToAll.classList.add("d-none");
                returnToAll.setAttribute("aria-hidden", "true");
                returnToAll.blur();
                // update page title
                pageTitle.innerHTML = "Essays";
            } else {
                // hide every essay to start
                essays[i].classList.add("d-none");
                essays[i].setAttribute("aria-hidden", "true");
                // unhide essays with the tag that matches the hash
                if (essays[i].classList.contains(location.hash.slice(1))) {
                    essays[i].classList.remove("d-none");
                    essays[i].setAttribute("aria-hidden", "false");
                }
                // reveal and focus link to return to all essays
                returnToAll.classList.remove("d-none");
                returnToAll.setAttribute("aria-hidden", "false");
                returnToAll.focus();
                // update page title
                pageTitle.innerHTML = "Essays: " + location.hash.slice(1);
            }
        }
        console.log("Filter applied")
    }
    // add event listener to filter essays on hash change
    window.addEventListener("hashchange", filterEssays);
</script>