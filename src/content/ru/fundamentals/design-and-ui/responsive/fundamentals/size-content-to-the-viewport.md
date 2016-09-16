project_path: /web/_project.yaml
book_path: /web/fundamentals/_book.yaml
description: Большинство интернет-ресурсов не оптимизировано для просмотра на разных типах устройств. Изучив основы, вы узнаете, как обеспечить одинаково хорошую работу сайта на телефонах, планшетах, домашних компьютерах... в общем, на любых устройствах, у которых есть экран.

{# wf_review_required #}
{# wf_updated_on: 2014-04-29 #}
{# wf_published_on: 2000-01-01 #}

# Масштабирование контента для области просмотра {: .page-title }

{% include "web/_shared/contributors/TODO.html" %}


Для просмотра сайтов на обычных компьютерах и мобильных устройствах используется вертикальная прокрутка. Если пользователю приходится прокручивать сайт по горизонтали или уменьшать масштаб, чтобы увидеть страницу полностью, он испытывает большие неудобства.


### TL;DR {: .hide-from-toc }
- Не используйте крупные элементы с фиксированной шириной.
- Для корректного отображения контента не ограничивайте его определенной шириной области просмотра.
- 'Используйте медиазапросы CSS, чтобы указать разные стили для больших и маленьких экранов.'


Используя метатег viewport при разработке сайта для мобильных устройств, можно по ошибке создать контент страницы, которые не полностью соответствует определенной области просмотра. Например, если ширина показываемого изображения больше области просмотра, придется использовать горизонтальную прокрутку. Чтобы избавить пользователей от этой необходимости, потребуется подогнать контент под шир ну области просмотра.

Диапазон размеров экрана и ширины в пикселях CSS очень велик (например, телефоны могут значительно отличаться от планшетов или даже от других телефонов), поэтому отображение контента не должно зависеть от конкретной ширины области просмотра.

Установка больших абсолютных значений ширины CSS для компонентов страницы сделает div слишком большим для более узкой области просмотра (например, на устройствах шириной 320 пикселей CSS, таких как iPhone). Вместо этого можно использовать значения в относительных единицах, например width: 100%.  Также старайтесь избегать больших абсолютных значений позиционирования. Из-за них на маленьком экране элемент может оказаться эа пределами области просмотра.

<div class="mdl-grid">
  <div class="mdl-cell mdl-cell--6--col">
    
      <img src="imgs/vp-fixed-iph.png" class="attempt-left" srcset="imgs/vp-fixed-iph.png 1x, imgs/vp-fixed-iph-2x.png 2x"  alt="Страница с элементом фиксированной ширины (344 пикс.) на iPhone.">
      См. пример
    
  </div>

  <div class="mdl-cell mdl-cell--6--col">
    
      <img src="imgs/vp-fixed-n5.png" class="attempt-right" srcset="imgs/vp-fixed-n5.png 1x, imgs/vp-fixed-n5-2x.png 2x"  alt="Страница с элементом фиксированной ширины (344 пикс.) на Nexus 5.">
      См. пример
    
  </div>
</div>


