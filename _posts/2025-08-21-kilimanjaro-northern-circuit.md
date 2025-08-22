---
layout: post
title: Mt. Kilimanjaro - The Northern Circuit
date: 2025-08-22
description: The roof of Africa, this shows photos taken on the Northern Circuit route.
tags: kilimanjaro mountain
categories: mountaineering
thumbnail: assets/img/kilimanjaro/northern_circuit/8/0.jpeg
toc:
    sidebar: left
img_prefix: assets/img/kilimanjaro/northern_circuit
giscus_comments: true
map: true
---


 {% leaflet_map { "center" : [-3.0782300575536112,
            37.3326401936738
          ], "zoom" : 11,
                 "providerBasemap": "OpenTopoMap" } %}
    {% for day in (1..8) %}
    {% capture img_path %}{{"assets/img/kilimanjaro/northern_circuit/" | append: day | append: "/01.jpeg" }}{% endcapture %}
    {% capture has_gps %}{{ img_path | exif: "gps?" }}{% endcapture %}
    {% if has_gps=="true" %}
    {% capture lat %}{{ img_path | exif: 'gps.latitude' }}{% endcapture %}
    {% capture lon %}{{ img_path | exif: 'gps.longitude' }}{% endcapture %}
    
    {% leaflet_marker { "latitude" : {{lat}},
                       "longitude" : {{lon}},
                       "popupContent" : "Day {{day}}"} %}
                       
    {% endif %}
    {% endfor  %}

    {% leaflet_marker { "latitude" : -3.156363833668223,
                       "longitude" : 37.367156881772814,
                       "popupContent" : "Day 9"} %}
    {% leaflet_geojson "/assets/json/kilimanjaro.geojson" %}
{% endleaflet_map %} 

## Day 1 - Lemosho Gate to Mti Mkubwa
{% for image in site.static_files %}
    {% if image.path contains 'img/kilimanjaro/northern_circuit/1' and image.path contains '.jpeg' %}
        {% include figure.liquid loading="eager" path=image.path class="img-fluid rounded z-depth-1" zoomable=true %}
    {% endif %}
{% endfor %}

## Day 2 - Mti Mkubwa to Shira I Camp
{% for image in site.static_files %}
    {% if image.path contains 'img/kilimanjaro/northern_circuit/2' and image.path contains '.jpeg' %}
        {% include figure.liquid loading="eager" path=image.path class="img-fluid rounded z-depth-1" zoomable=true %}
    {% endif %}
{% endfor %}

## Day 3 - Shira I Camp to Moir Hut
{% for image in site.static_files %}
    {% if image.path contains 'img/kilimanjaro/northern_circuit/3' and image.path contains '.jpeg' %}
        {% include figure.liquid loading="eager" path=image.path class="img-fluid rounded z-depth-1" zoomable=true %}
    {% endif %}
{% endfor %}

## Day 4 - Moir Hut to Buffalo Camp
{% for image in site.static_files %}
    {% if image.path contains 'img/kilimanjaro/northern_circuit/4' and image.path contains '.jpeg' %}
        {% include figure.liquid loading="eager" path=image.path class="img-fluid rounded z-depth-1" zoomable=true %}
    {% endif %}
{% endfor %}

## Day 5 - Buffalo Camp to Third Cave
{% for image in site.static_files %}
    {% if image.path contains 'img/kilimanjaro/northern_circuit/5' and image.path contains '.jpeg' %}
        {% include figure.liquid loading="eager" path=image.path class="img-fluid rounded z-depth-1" zoomable=true %}
    {% endif %}
{% endfor %}

## Day 6 - Third Cave to Kibo Hut
{% for image in site.static_files %}
    {% if image.path contains 'img/kilimanjaro/northern_circuit/6' and image.path contains '.jpeg' %}
        {% include figure.liquid loading="eager" path=image.path class="img-fluid rounded z-depth-1" zoomable=true %}
    {% endif %}
{% endfor %}

## Day 7 - Kibo Hut to Uhuru Peak to Barafu Camp
{% for image in site.static_files %}
    {% if image.path contains 'img/kilimanjaro/northern_circuit/7' and image.path contains '.jpeg' %}
        {% include figure.liquid loading="eager" path=image.path class="img-fluid rounded z-depth-1" zoomable=true %}
    {% endif %}
{% endfor %}

## Day 8 - Barafu Camp to Mweka Camp
{% for image in site.static_files %}
    {% if image.path contains 'img/kilimanjaro/northern_circuit/8' and image.path contains '.jpeg' %}
        {% include figure.liquid loading="eager" path=image.path class="img-fluid rounded z-depth-1" zoomable=true %}
    {% endif %}
{% endfor %}

## Day 9 - Mweka Camp to Mweka Gate

Phone died, so unfortunately no photos! 
