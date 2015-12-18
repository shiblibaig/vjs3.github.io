---
layout: page

title: About Me


---


{% assign total_words = 0 %}
{% assign total_readtime = 0 %}
{% assign featuredcount = 0 %}

{% for post in site.posts %}
    {% assign post_words = post.content | strip_html | number_of_words %}
    {% assign ert = post_words | divided_by:180 %}
    {% assign ertremainder = post_words | modulo:180 %}
        {% if ertremainder >= 90 %}
            {% assign readtime = ert | plus:1 %}
        {% else %}
            {% assign readtime = ert %}
        {% endif %}
    {% assign total_words = total_words | plus: post_words %}
    {% assign total_readtime = total_readtime | plus: readtime %}
    {% if post.featured %}
    {% assign featuredcount = featuredcount | plus: 1 %}
    {% endif %}
{% endfor %}

I'm **Vishwajeet Srivastava**, pre-final year undergraduate student and Android Application Developer. I love to analyze various android applications and usually spend time to find out how they work.

I'm pursuing **B.Tech** in Computer Science and Engineering from LNMIIT, India.Currently  I've been working with an Indian Startup in the field of Digital Health named HealthGraph India.I am Entreprenuer by heart and an avid startup lover.I have experience working with several startups both techniocally and non-technically.

I am currently interested in the field of Open Source and actively contributing to some of the open source projects specially in the field of **Android**.Though I am new to the world of open source but with the helping nature and guidance of open source community, I am learning new stuff and actively contributing.

