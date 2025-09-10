# Фреймы и `<iframe>` в HTML

## Краткая информация
Фреймы позволяют **встраивать одно HTML-содержимое в другое**. В современном HTML чаще используется `<iframe>` вместо устаревших `<frame>` и `<frameset>`.  
- `<iframe>` — встраиваемое окно для загрузки другой страницы, видео, карт, интерактивного контента.  

---

## Пример использования `<iframe>`

```html
<iframe src="https://www.example.com" width="600" height="400" title="Пример сайта">
  Ваш браузер не поддерживает фреймы.
</iframe>
src — ссылка на внешний ресурс.

width и height — размеры фрейма.

title — описание для доступности.

Текст внутри <iframe> отображается только если браузер не поддерживает фреймы.

Подробная информация
Атрибуты <iframe>
src — URL встраиваемого ресурса.

width и height — размеры окна.

title — важен для доступности.

sandbox — ограничение действий внутри iframe (например, запрет скриптов).

allow — разрешения для видео, микрофона, камеры.

frameborder — рамка (устаревший, лучше CSS).

loading="lazy" — отложенная загрузка для ускорения страницы.

name — идентификатор для ссылок с target.

Использование <iframe> для интерактивного контента
Встраивание видео с YouTube:

html
Копировать код
<iframe width="560" height="315" src="https://www.youtube.com/embed/dQw4w9WgXcQ" 
title="Видео пример" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen>
</iframe>
Встраивание карт Google:

html
Копировать код
<iframe src="https://www.google.com/maps/embed?pb=..." width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
Объяснение
<iframe> позволяет встраивать внешний контент без необходимости редактирования основного HTML.

Использование sandbox и allow обеспечивает безопасность и контроль действий во фрейме.

Отложенная загрузка (loading="lazy") ускоряет работу страницы.

<iframe> часто применяется для видео, карт, виджетов социальных сетей и сторонних сервисов.

В современных проектах <iframe> заменяет старые <frameset> и <frame>, которые устарели и плохо поддерживаются.