---
layout: about
title: about
permalink: /
description: AI Enthusiast & Passionate Full Stack Developer 🚀

profile:
  align: right
  image: img_profile.jpg

news: false  # includes a list of news items
selected_papers: false # includes a list of papers marked as "selected={true}"
social: true  # includes social icons at the bottom of the page
---

I am a final year undergraduate student at Veermata Jijabai Technological Institute, majoring in Electronics Engineering. 

Currently I am working as a Software Developer Intern at GroundUp, India.

My Interests are:
* Machine Learning
* Deep Learning
* Software Development
* Cross-platform Application Development
* Open Source

If you are inquisitive about DL you can read my blogs at [hashnode.com/@sp-lit5](https://hashnode.com/@sp-lit5)

# Experience

{% for experience in site.data.experience %}
<div>
    {% if experience.title %}
    <h4 class="title font-weight-bold">{{experience.title}}</h4>
    {% endif %}
    {% if experience.role %}
    <h6 class="title font-weight-bold">{{experience.role}}</h6>
    {% endif %}
    {% if experience.year %}
    <span class="badge bg-dark font-weight-bold">
        {{ experience.year }}
    </span>
    {% endif %}
    {% if experience.description %}
        <ul class="items">
            {% for item in experience.description %}
                <li>
                    {% if item.contents %}
                        <span class="item-title">{{ item.title }}</span>
                        <ul class="subitems">
                        {% for subitem in item.contents %}
                            <li><span class="subitem">{{ subitem }}</span></li>
                        {% endfor %}
                        </ul>
                    {% else %}
                        <span class="item">{{ item }}</span>
                    {% endif %}
                </li>
            {% endfor %}
        </ul>
    {% endif %}
    {% if content.items %}
        <ul class="items">
            {% for item in content.items %}
                <li>
                    {% if item.contents %}
                        <span class="item-title">{{ item.title }}</span>
                        <ul class="subitems">
                        {% for subitem in item.contents %}
                            <li><span class="subitem">{{ subitem }}</span></li>
                        {% endfor %}
                        </ul>
                    {% else %}
                        <span class="item">{{ item }}</span>
                    {% endif %}
                </li>
            {% endfor %}
        </ul>
    {% endif %}
</div>
{% endfor %}
