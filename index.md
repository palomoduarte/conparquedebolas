---
layout: default
title: Inicio
---
Bienvenido a nuestra Guía de Restaurantes
Últimos Restaurantes

<div class="restaurantes-grid">
{% for restaurante in site.data.restaurantes limit:3 %}
<div class="restaurante-teaser">
    <img src="{{ restaurante.imagen }}" alt="{{ restaurante.nombre }}">
    <div class="teaser-content">
        <h2>{{ restaurante.nombre }}</h2>
        <p class="ciudad">{{ restaurante.ciudad }}</p>
        <p class="descripcion">{{ restaurante.descripcion }}</p>
        <a href="/restaurantes/{{ restaurante.url }}" class="btn">Ver Restaurante</a>
    </div>
</div>
{% endfor %}
</div>
Todas las Ciudades
<div class="ciudades-list">
{% assign ciudades = site.data.restaurantes | map: 'ciudad' | uniq %}
{% for ciudad in ciudades %}
<a href="/categorias/{{ ciudad | slugify }}" class="ciudad-tag">{{ ciudad }}</a>
{% endfor %}
</div>