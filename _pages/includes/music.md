# 🎧 Beloved Music

{% if site.data.albums.size > 0 %}
<div class="album-grid">
  {% for album in site.data.albums %}
  <a class="album-card" href="{{ album.url | escape }}" target="_blank" rel="noopener noreferrer" aria-label="{{ album.title | escape }} by {{ album.artist | escape }} (opens in a new tab)">
    <img class="album-card__cover" src="{{ album.cover | relative_url }}" alt="{{ album.title | escape }} album cover" loading="lazy" width="400" height="400">
    <span class="album-card__title">{{ album.title | escape }}</span>
    <span class="album-card__artist">{{ album.artist | escape }}</span>
  </a>
  {% endfor %}
</div>
{% endif %}
