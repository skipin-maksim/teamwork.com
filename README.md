**teamwork.com Second work in team**
===
Полезно
* Сделать клон данного репозитория
* Из папки проекта войти в ветку `dev`
* Из `dev` сделать свою рабочую ветку
* Работаем только в своей ветке, НЕ В `dev`
* Делаем merge `pull request` из СВОЕЙ ветки в `dev`


### Сделать свою ветку и перейти в нее
    git checkout -b [name branch]
### Чтоб сделать push своей ветки на GitHub
    git push -u origin [name branch]

---
---

Пожелания - не правила
---
* `блок__элемент--мод`       написание БЭМ
* `class="list"`             пишем ul
* `class="link"`             пишем для ссылок
* `class="visually-hidden"`  пишем скрытым заголовкам и тд

>`mixin.scss`   код пишем с помощью миксинов (перед версткой ознакомиться с ними, что не понятно, спрашивать в общий чат).
>* Хочешь добавить? Вперед! Только остальным скажи, может они тоже захотят его использовать?;

>`placeholders.scss`                код пишем с помощью плейсхолдеров (сделаем их когда увидим макет).
>* Хочешь добавить? Вперед! Только остальным скажи, может они тоже захотят его использовать?;

---
---

**Пример создания шестигранника** 
-----------------------------
### HTML code
```html
<div class="hexagon">
      <div class="hexagon__hexagon">
        <h3 class="hexagon__title">ПРИВЕТ</h3>
        <p class="hexagon__text">шестигранник</p>
      </div>
    </div>
```
### SCSS code
```scss
.hexagon {
  position: relative;
  margin: 50px;
  @include hexagon(
    $width: 100px,
    $height: 90px,
    $background: $color_accent-lite
  );
  color: $color_white;

  &__hexagon {
    @include сenter-xy($pos: relative);
    @include hexagon($width: 85px, $height: 75px, $background: $color_accent);
    padding: 50px;
    text-align: center;
    margin: 0;
    padding: 0;
  }

  &__title {
    padding-top: 15px;
  }

  &__text {
    font-size: 12px;
  }
}
```
---
---

Подключил Animate.css вот ссылки на [GitHub](https://github.com/daneden/animate.css) и [animate.css](https://daneden.github.io/animate.css/)
----------------------
Пишем не `animated`
```html
<div class="animated infinite pulse delay-2s">Привет</div>
```
а `wow`
```html
<div class="wow infinite pulse delay-2s">Привет</div>
```
и добавил свою длительность анимации
```css
.dur-0.5s       
.dur-1.5s
.dur-2.5s 
.dur-3.5s 
.dur-4s 
.dur-4.5s 
.dur-5s 
```
и задержку
```css
.delay-1.5s
.delay-2.5s
.delay-3.5s
.delay-4.5s
```