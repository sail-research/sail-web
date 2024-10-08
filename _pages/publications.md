---
title: "Security and Artificial Intelligence Lab - Publications"
layout: gridlay
excerpt: "Security and Artificial Intelligence Lab -- Publications."
sitemap: false
permalink: /publications/
---


# Publications

## Group highlights

**At the end of this page, you can find the [full list of publications and patents](#full-list-of-publications). All papers are also available on [arXiv](https://arxiv.org/search/?query=Kok-Seng+Wong&searchtype=author&abstracts=show&order=-announced_date_first&size=50).**

{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <!-- <pubtit>{{ publi.title }}</pubtit> -->
  <!-- <a href="{{ publi.link.url }}"><pubtit>{{ publi.title }}</pubtit></a> -->
  <a href="{{ publi.link.url }}" target="_blank"><pubtit>{{ publi.title }}</pubtit></a>
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ publi.description }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <!-- <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p> -->
  <p><strong>{{ publi.link.display }}</strong></p>

  <p><em>
    {% if publi.link.url.size > 0 %}<a href="{{ publi.link.url }}" style="color: blue;" target="_blank">[Paper]</a> {% endif %}
    {% if publi.link.code.size > 0 %}<a href="{{ publi.link.code }}" style="color: green;" target="_blank">[Code]</a> {% endif %}
    {% if publi.link.talk.size > 0 %}<a href="{{ publi.link.talk }}" style="color: red;" target="_blank">[Video]</a> {% endif %}
  </em></p>



  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
  <p> {{ publi.news2 }}</p>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>


<!-- ## Patents
<em>Milan P Allan, S Gröblacher, RA Norte, M Leeuwenhoek</em><br />Novel atomic force microscopy probes with phononic crystals<br /> PCT/NL20-20/050797 (2020)

<em>Milan P Allan</em><br /> Methods of manufacturing superconductor and phononic elements <br /> <a href="https://patents.google.com/patent/US10439125B2/en?inventor=Milan+ALLAN&oq=inventor:(Milan+ALLAN)">US10439125B2 (2016)</a> -->

## Full List of publications

{% for publi in site.data.publist %}
  <a href="{{ publi.link.url }}" target="_blank">{{ publi.title }}</a><br />
  <strong>{{ publi.authors }} </strong><br /> <em>{{ publi.link.display }} </em>

{% endfor %}
