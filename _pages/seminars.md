---
layout: page
title: Seminars
permalink: /seminars/
description: This page is about seminars I have organized or attended.
nav: true
years: [2018,2019,2020,2021]
horizontal: false
---
<div class="publications">
{% for y in page.years %}
    <h2 class="year">{{y}}</h2>
    {% assign year_seminars = site.seminars | where: "year", y %}
    {% assign sorted_seminars = year_seminars | sort: "time" %}
	<div class="container">
	{% for seminar in sorted_seminars %}
	    <div class="row row-cols-2">
    	         {% include seminars.html %}
	    </div>
    	{% endfor %}
	</div>
{% endfor %}

</div>
