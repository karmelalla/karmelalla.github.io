---
layout: page
title: О сайте
permalink: /about/
---
<img src="/assets/images/avatar.jpg" class="about">
Всем привет! Меня зовут Алла. В январе 2017 года мы с мужем переехали из Санкт-Петербурга в Сан-Франциско. Раньше я никогда не планировала вести блог, но переезд изменил моё отношение.

Новый опыт, множество интересных путешествий и впечатлений. Очень захотелось всем этим поделиться с родными и друзьями. Чтобы вы могли лучше следить за происходящим. Хоть немного прочувствовать наши впечатления и переживания.
Да и самим очень хочется не забывать то, какими мы были, когда приехали. Как искали свою первую квартиру, как первый раз проехали пол-штата на машине, как первый раз поучаствовали в полумарафоне и ещё очень много таких "первых раз".

Буду очень рада всем, кому будет интересно следить за нашими сказочными приключениями. Оставляйте комментарии, делитесь идеями и советами.

Пожалуйста, подписывайтесь <a href="http://karmelalla.com/subscribe/" target="_blank"> по этой ссылке </a> и читайте с удовольствием!

{% assign cooking_counter = 0 %}
{% assign stories_counter = 0 %}
{% assign images_counter = 0 %}

{% for post in site.posts %}
  {% if post.categories contains "cooking" %}
    {% assign cooking_counter = cooking_counter | plus: 1 %}
  {% else %}
    {% assign stories_counter = stories_counter | plus: 1 %}
  {% endif %}

  {% for image in post.all_images %}
    {% assign images_counter = images_counter | plus: 1 %}
  {% endfor %}
{% endfor %}

<u>Статистика сайта:</u>
  * Количество [историй](/): {{stories_counter}}
  * Количество [рецептов](/cooking/): {{cooking_counter}}
  * Количество [фотографий](/gallery/): {{images_counter}}
