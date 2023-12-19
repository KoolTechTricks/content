# uBlock Origin
> browser_extensions, internet, privacy

[uBlock Origin](https://github.com/gorhill/uBlock) — расширение с открытым
исходным кодом, предназначенное для блокировки нежелательного контента на
сайтах: рекламы, трекеров, майнеров, всплывающих окон, анти-блокировщиков и
т.д. Не требователен к ресурсам компьютера. Имеется множество фильтров,
которые обновляются автоматически. Можно создавать свои фильтры для блокировки
любых элементов на сайтах.

![Скриншот меню uBlock Origin](/media/ublock_origin.jpg)

> [warn]
**uBlock Origin** никак не связан с сайтом `ublock.org` и расширением uBlock.

## Применение

Блокировщики контента предотвращают загрузку скриптов на веб-страницах, которые
собирают какие-либо данные о вас в целях создания персонализированной рекламы.
Лишние элементы также расходуют больше трафика и ресурсов компьютера, из-за чего
замедляется загрузка сайтов.

Блокировка рекламы включена в uBlock Origin по умолчанию, хотя в настройках
фильтров можно отключить. Блокировка рекламы может вредить администраторам
сайта, которые используют деньги с рекламы для оплаты хостинга и в качестве
заработка. Однако у вас должно быть право на конфиденциальность. Реклама может
собирать данные, быть вредоносной или мешать просмотру контента.

uBlock Origin также позволяет заблокировать любой элемент на странице через
контекстное меню элемента или меню расширения.

> [info] Согласно [Консорциуму Всемирной паутины](https://www.w3.org),
организации, разрабатывающей и внедряющей технологические стандарты для Всемирной паутины:
>
> [2.12 Люди должны иметь возможность отображать веб-контент по своему усмотрению](https://www.w3.org/TR/ethical-web-principles/#render)
>
> Люди должны иметь возможность изменять веб-страницы в соответствии со своими
потребностями. Например, люди должны иметь возможность устанавливать таблицы
стилей, вспомогательные расширения для браузера, блокировать нежелательный
контент, скрипты или автоматически воспроизводимое видео. <...>

## Установка

Установите расширение для:

- [Firefox](https://addons.mozilla.org/addon/ublock-origin) (ПК и Android)
- [Chromium](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm)
- [Edge](https://microsoftedge.microsoft.com/addons/detail/ublock-origin/odfafepnkmbhccpbejgmiehpchacaeak)
- [Opera](https://addons.opera.com/extensions/details/ublock)
- [Thunderbird](https://addons.thunderbird.net/thunderbird/addon/ublock-origin)

> [warn]
В июне 2024 года
[в Google Chrome планируется отключить расширения на Manifest V2](https://developer.chrome.com/blog/resuming-the-transition-to-mv3). Вместе с этим uBlock Origin
больше нельзя будет пользоваться. Вы можете использовать менее эффективный
uBlock Origin Lite, основанный на Manifest V3 или перейти на другой браузер,
например, Firefox (не Chromium) или Brave (форк Chromium).
[Подробнее](https://t.me/KoolTechTricks/116)

### uBlock Origin Lite

Это расширение основано на Manifest V3, более новому стандарту, который
сейчас Google внедряет в свой браузер. Оно менее эффективно из-за ограничений
Manifest V3, как следствие, использует меньше разрешений.

- [Firefox](https://addons.mozilla.org/addon/ublock-origin-lite)
- [Chromium](https://chrome.google.com/webstore/detail/ublock-origin-lite/ddkjiahejlhfcafbddmgiahcphecmpfh)
- [Edge](https://microsoftedge.microsoft.com/addons/detail/ublock-origin-lite/cimighlppcgcoapaliogpjjdehbnofhn)

## Использование

> [info] См. также:
[официальная документация](https://github.com/gorhill/uBlock/wiki) (англ.)

### Меню

Меню расширения содержит информацию и быстрые инструменты. Его можно раскрыть,
чтобы показать больше элементов управления. Здесь же можно перейти в настройки.

**Большая кнопка "питания"** позволяет отключить uBO для текущего сайта. Это
состояние будет запомнено и добавлено в список доверенных сайтов. Если нажать
с зажатым `Ctrl` (или `Cmd`), то будет отключена текущая страница.

**Переключатели для каждого сайта** позволяют настроить поведение uBO для
каждого сайта: **блокировать всплывающие окна**,
**блокировать большие медиа**, **отключить косметическую фильтрацию**,
**блокировать сторонние шрифты**, **отключить JavaScript**. Эти изменения будут
временными до тех пор, пока вы не нажмёте на кнопку с замком.
[Подробнее](https://github.com/gorhill/uBlock/wiki/Per-site-switches)

**Мгновенное скрытие (молния)** позволяет быстро скрыть указанный элемент на
странице. После перезагрузки будет возвращён.

**Войти в режим выбора (пипетка)** позволяет создать фильтр из выбранного
элемента на странице. Элементы будут добавлены в **Мои фильтры**.

**Сообщить о проблеме (чат)** позволяет быстро создать отчёт на
[GitHub](https://github.com/uBlockOrigin/uAssets/issues?q=is%3Aissue) (требуется
аккаунт) в случае некорректной работы фильтров uBlock Origin. Волонтёры
постараются решить проблему как можно быстрее, после чего обновления появятся в
списке фильтров.

**Логгер** позволяет отслеживать блокируемые запросы в режиме реального времени
(требуется перезагрузка страницы).
[Подробнее](https://github.com/gorhill/uBlock/wiki/The-logger)

![Логгер uBlock Origin](/media/ublock_origin_logger.jpg)

**Список подключённых доменов** показывает как много было
разрешено/заблокировано (зависит от количества "+" и "-", а также цветов).

### Списки фильтров

По умолчанию должно быть включено достаточно фильтров для блокировки
большинства рекламы и трекеров. Их можно настроить в разделе списков фильтров.
Вы можете отключить блокировку рекламы, но оставить блокировку трекеров.

Фильтры должны обновляться автоматически.

![Списки фильтров uBlock Origin, включённые по умолчанию](/media/ublock_origin_filter_lists.jpg)

### Свои фильтры

Вы можете заблокировать любой элемент на сайте, для этого либо нажмите ПКМ
по нему и выберите "Блокировать элемент", либо выберите его через меню
расширения. Он будет добавлен в список ваших правил.

## Исправление проблем

Если сайт отображается некорректно или не работает вовсе, то необходимо сообщить
об этом. Используйте функцию **Сообщить о проблеме** в меню расширения (иконка
чата). Для создания отчёта потребуется аккаунт на GitHub и немного времени,
чтобы убедиться в том, что нет дубликатов, и вы делаете правильные действия.

- [Баг-трекер фильтров](https://github.com/uBlockOrigin/uAssets/issues?q=is%3Aissue)

## См. также

- [uBlock Origin — Википедия](https://ru.wikipedia.org/wiki/UBlock_Origin)