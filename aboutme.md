---
layout: page

title: ABOUT ME

chart: true
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

I'm **Shivam Dixit**, pre-final year undergraduate student and web developer. During the daytime you would find me glued to my laptop, at night I fight ninjas. I love to explore new technologies and always looking forward for challenging problems.

I'm pursuing **B.Tech** in Computer Science and Engineering from LNM-IIT, India. I've been working with a software company as a __student employee__ since 2013. I was selected in Google Summer Of Code 2014 in my sophomore year. I've been actively contributing to open source softwares since then. I love to break things, especially web applications and have reported security vulnerabilities in various web applications.

###Resume
Download the latest version. Personal information has been removed from the online version of the resume.

###Blog Stats

