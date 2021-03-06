---
title: "Off Canvas (Вне экрана)"
description: "Приемы отзывчивого веб-дизайна быстро эволюционируют, но есть много проверенных вариантов, которые хорошо работают при использовании как настольных компьютеров, так и мобильных устройств"
updated_on: 2014-10-21
---

<p class="intro">
  Вместо того чтобы размещать элементы контента вертикально друг под другом, шаблон размещает контент, который используется редко, скажем, элементы навигации или меню приложения за пределами экрана, показывая его только тогда, когда это позволяет сделать размер экрана. На небольших же экранах контент можно открыть одним щелчком
</p>

{% link_sample _code/off-canvas.html %}
  <img src="imgs/off-canvas.svg">
  Попробовать
{% endlink_sample %}

В этом образце элементы контента не размещены вертикально друг под другом, а два контейнера 
`div` контента вынесены за пределы экрана с помощью `transform: translate(-250px, 0)`.  Для отображения
этих div используется JavaScript: к элементу, который необходимо показать на экране, добавляется класс open.  По мере
увеличения ширины экрана размещение элементов за пределами экрана убирается,и
они отображаются в пределах видимости.

По поводу этого образца следует отметить, что Safari для iOS 6 и Android Browser не поддерживают функцию 
`flex-flow: row nowrap` элемента`flexbox`, поэтому пришлось вернуться к
абсолютному позиционированию.

Сайты, созданные с использованием этого шаблона:

 * [HTML5Rocks
  Articles](http://www.html5rocks.com/en/tutorials/developertools/async-call-stack/)
 * [Google Nexus](http://www.google.com/nexus/)
 * [Сайт Facebook для мобильных устройств](https://m.facebook.com/)

{% include_code src=_code/off-canvas.html snippet=ocanvas lang=css %}


