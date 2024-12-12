---
layout: default
title: Inicio
---
Bienvenido a nuestra Guía de Restaurantes
Últimos Restaurantes

{% for restaurante in site.data.restaurantes limit:3 %}
<div class="restaurante-teaser">
    <h2>{{ restaurante.nombre }}</h2>
    <img src="{{ restaurante.imagen }}" alt="{{ restaurante.nombre }}">
    <p>{{ restaurante.descripcion }}</p>
    <a href="/restaurantes/{{ restaurante.url }}">Ver más</a>
</div>
{% endfor %}