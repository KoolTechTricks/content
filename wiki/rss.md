# RSS
> compilations, internet

RSS — это веб-лента, которая позволяет получать информацию об обновлениях и
новых статьях на различных сайтах в общем виде при помощи специальных
приложений-агрегаторов. Это избавляет от необходимости либо проверять каждый
сайт вручную, либо пользоваться социальными сетями, в которых много лишнего
контента и алгоритмов.

## Применение

Вы хотите следить за обновлениями на каком-либо сайте или блоге. Постоянно
заходить на этот сайт вручную не очень удобно. В таком случае, помогают
социальные сети, куда авторы сообщают об обновлениях. Они могут быть довольно
хорошим источником, однако, зачастую, имеют много шума: реклама, алгоритмы.
Можно легко пропустить какие-либо обновления.

RSS позволяет получать обновления автоматически при помощи специальных
приложений и сервисов. Вы подписываетесь на RSS-ленту, а дальше приложение само
получает данные и показывает их в читаемом для человека формате. Здесь нет
никаких алгоритмов, так что вы будете видеть только то, что вам необходимо.
RSS-ленты находятся на том же сайте, откуда вы хотите получать обновления.

## Устройство

RSS-лента является файлом в формате XML, который содержит статьи по
определённому формату. При чтении этого файла агрегаторами, они представляют
его в удобном виде.

На самом деле, RSS — это лишь один из форматов. Также есть Atom, который
является наиболее современным и рекомендуемым для использования на сайтах.
Читателям, обычно, не важен формат ленты, так как приложения-агрегаторы могут
уметь обрабатывать сразу несколько форматов.

## Использование

Для начала необходимо установить приложение-агрегатор. Их существует огромное
множество. [Ниже](#Агрегаторы) будет представлен список некоторых приложений.
Если вам нужно синхронизировать данные между устройствами, то необходимо
воспользоваться [сервисами](#Сервисы).

Далее, нужно найти ссылку на RSS-ленту. Она может быть расположена где угодно
и иногда хорошо спрятана. Некоторые приложения-агрегаторы умеют находить эту
ленту по ссылке. Вы можете установить расширения для
[Firefox](https://addons.mozilla.org/en-US/firefox/addon/awesome-rss),
[Chrome](https://chrome.google.com/webstore/detail/rss-subscription-extensio/nlbjncdgjeocebhnmkbbbdekmmmcbfjd)
и [Safari](https://apps.apple.com/us/app/rss-button-for-safari/id1437501942?mt=12),
которые добавляют кнопку в адресную строку, ведущую на RSS-ленту конкретного
сайта.

Наконец, остаётся подписаться на RSS-ленту, скопировав ссылку на неё в ваше
приложение-агрегатор. В зависимости от возможностей и настроек агрегатора,
обновления будут приходить автоматически, подписки можно организовывать по
папкам, отмечать тегами, фильтровать содержимое. Список лент можно будет
экспортировать в OPML, если нужно перенести их на другое устройство.

### Агрегаторы

В этом разделе будут представлены различные приложения-агрегаторы. Вы можете
установить понравившиеся, либо найти какое-нибудь другое самостоятельно.

Если вы знаете какое-либо хорошее приложение, которые бы подошло для этой
страницы, то можете [предложить добавить
его](https://github.com/KoolTechTricks/website).

#### RSS Guard

- **Платформа:** ПК (Windows, Linux, macOS)
- **Технологии:** [Открытый исходный
код](https://github.com/martinrotter/rssguard), Qt, C++, JavaScript
- **Скачать:** [GitHub](https://github.com/martinrotter/rssguard/releases)

Очень мощный RSS-агрегатор, позволяющий читать ленты как локально, так и в
онлайн-сервисах. Статьи можно фильтровать при помощи JavaScript. Есть версия
как со встроенным браузером, так и без.

![Скриншот RSS Guard](/media/rss_guard.jpg)

#### Thunderbird

- **Платформа:** ПК (Windows, Linux, macOS)
- **Технологии:** Открытый исходный код, на основе Firefox
- **Скачать:** [Официальный сайт](https://www.thunderbird.net)

Thunderbird может быть не только почтовым клиентом, но ещё и агрегатором RSS.
Сообщения можно фильтровать по ключевым словам. Поддерживаются
[расширения](https://addons.thunderbird.net).

![Скриншот Thunderbird](/media/rss_thunderbird.jpg)

#### Newsboat

- **Платформа:** Linux, macOS, Android (через Termux)
- **Технологии:** Открытый исходный код, консольный интерфейс, C++
- **Скачать:** [Официальный сайт](https://newsboat.org)

Это приложение с консольным интерфейсом. Несмотря на это, оно имеет ряд
полезных функций, таких как рендер HTML, фильтр статей, макросы,
интеграция с сервисами.

![Скриншот Newsboat](/media/rss_newsboat.jpg)

#### Feeder

- **Платформа:** Android
- **Технологии:** [Открытый исходный код](https://github.com/spacecowboy/Feeder/releases),
Kotlin
- **Скачать:** [Google Play](https://play.google.com/store/apps/details?id=com.nononsenseapps.feeder.play),
[GitHub](https://github.com/spacecowboy/Feeder/releases),
[F-Droid](https://f-droid.org/repository/browse/?fdid=com.nononsenseapps.feeder)

Полностью свободное мобильное приложение без рекламы и скрытых слежок. Имеет
простой функционал, дизайн Material, синхронизацию через свой сервис.
Присутствует функция чтения полной версии статьи с сайта.

![Скриншот Feeder](/media/rss_feeder.jpg)

### Сервисы

Сервисы позволят вам синхронизировать прочтённые статьи и ваши подписки.

#### Feedly

[Feedly](https://feedly.com) — самый популярный сервис для чтения RSS. Он
предлагает веб-интерфейс и мобильные приложения. Имеет минималистичный
интерфейс и внутренний каталог сайтов.

![Скриншот Feedly](/media/rss_feedly.jpg)

#### Inoreader

[Inoreader](https://www.inoreader.com) — ещё один сервис для чтения RSS. Имеет
веб-интерфейс и мобильные приложения. Есть внутренний каталог сайтов.

![Скриншот Inoreader](/media/rss_inoreader.jpg)

#### NextCloud

[NextCloud](https://nextcloud.com) — это облачное хранилище, которое необходимо
хостить самостоятельно. Помимо хранения файлов, существует множество приложений.
Одно из них — [News](https://apps.nextcloud.com/apps/news). Вы сможете
читать RSS-ленты и синхронизировать их между устройствами. Так как сервис вы
должны хостить самостоятельно, а программа с открытым исходным кодом, то
обеспечивается наибольшая приватность и свобода.

![Скриншот NextCloud News](/media/rss_nextcloud.jpg)

## Добавление ленты на свой сайт

Добавление RSS-ленты на свой сайт обеспечит читателям удобную возможность
постоянно получать обновления.

Для начала, стоит понимать [как устроен RSS](#Устройство). Это всего лишь
XML-файл, который необходимо пополнять при добавлении новых статей на сайт.
Этот процесс можно реализовать по-разному, зависит от устройства сайта.
Рекомендуется использовать современный формат Atom.

Рекомендуется прочитать [эту
статью](https://kevincox.ca/2022/05/06/rss-feed-best-practices) (англ.) про
создание своей RSS-ленты.