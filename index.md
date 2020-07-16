---

layout: default
title: tet
author: Hector Vasquez
lang: es
pagination:
  enabled: true
  locale: es

---

***
# Artículos
***
<br>

<table class="table table-hover">
 <tbody>
{% for post in site.posts %}
 <tr>
   <td>

<image class="img-fluid"  src="{{ site.baseurl }}{{post.images}}">
   <td> 
    <a class="text-dark" href="{{ site.baseurl }}{{ post.url }}"> <div><h5> {{ post.title }}</h5> <h6>{{post.fecha}}</h6><br>{{ post.description}}</div></a> 

{% endfor %}
  

