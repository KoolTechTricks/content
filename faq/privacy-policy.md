+++
title = 'Политика конфиденциальности'
publishDate = 2024-10-01T11:40:00Z
lastmod = 2024-10-01T11:40:00Z
description = """Как мы используем ваши данные"""
+++

# Политика конфиденциальности

## Просмотр страниц сайта

Сайт размещён на [Codeberg Pages], поэтому просмотр страниц осуществляется
согласно [политике конфиденциальности Codeberg].

При посещении страниц нашего сайта на серверы [Codeberg] отправляются ваши
IP-адреса и строки [User-Agent]. Эти данные хранятся в журналах и уничтожаются
автоматически не более чем за 7 дней. У нас нет доступа к журналам серверов
Codeberg.

[Codeberg Pages]: https://codeberg.page
[политике конфиденциальности Codeberg]: https://codeberg.org/Codeberg/org/src/branch/main/PrivacyPolicy.md
[Codeberg]: https://codeberg.org
[User-Agent]: https://en.wikipedia.org/wiki/User-Agent_header

## Аналитика

На сайте используется аналитика [Plausible]. Эта аналитика создаётся с учётом
конфиденциальности пользователей, и поэтому не собирает персональные данные,
не использует cookie и не создаёт уникальные идентификаторы.

> **Смотрите также:** [Аналитика на сайте](/faq/analytics) — FAQ

[Plausible]: https://plausible.io

### Открытый исходный код

Plausible с [открытым исходным кодом](https://github.com/plausible/analytics).
Любой может посмотреть, проанализировать и проверить, как работает Plausible.

### Запущено на нашем сервере

Мы запускаем экземпляр Plausible из открытого исходного кода на нашем сервере.
Никакие данные не передаются между третьим лицами: всё находится под нашим
контролем.

### Политика данных

> **Основная статья:** https://plausible.io/data-policy

Мы не отслеживаем людей на всех устройствах, на всех сайтах и в приложениях,
которые они посещают. Все данные относятся только к одному дню, одному сайту и
одному устройству. Невозможно узнать, посещает ли один и тот же человек сайт с
нескольких устройств или заходит на другой сайт.

Целью является отслеживание общих тенденций посещаемости нашего сайта, но не
отслеживание отдельных посетителей. Мы не используем файлы cookie, не генерируем
никаких постоянных идентификаторов, не собираем и не храним никаких личных или
идентифицируемых данных. Все данные являются только обобщёнными и не содержат
никакой личной информации.

Все измерения на сайте проводятся абсолютно анонимно. Мы измеряем только самые
необходимые данные и ничего больше. Все метрики, которые мы собираем, умещаются
на одной странице. Вот полный список того, что мы собираем и храним:

#### URL страницы

Пример: _`https://kooltechtricks.org/faq/privacy-policy`_

Мы отслеживаем URL-адрес каждой просмотренной страницы на нашем сайте. Мы
используем его, чтобы понять, сколько раз была просмотрена та или иная страница.

Параметры запроса отбрасываются, за исключением следующих специальных
параметров: `ref=`, `source=`, `utm_source=`, `utm_medium=`, `utm_campaign=`,
`utm_content=` и `utm_term=`. Мы не используем эти параметры на практике и
рекомендуем [очищать их](/wiki/clearurls).

#### HTTP Referer

Примеры: _google.com_, _yandex.ru_

Мы используем строку [Referer] в заголовке HTTP-запроса, чтобы понять количество
посетителей, перешедших на наш сайт по ссылкам с других сайтов.

[Referer]: https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Referer

#### Браузер

Примеры: _Chrome 86.0_, _Firefox 115.0_, _Safari 17.5_

Мы используем эти данные, чтобы понять, какие браузеры и их версии используют
люди при посещении нашего сайта.

Этот показатель определяется из HTTP-заголовка User-Agent. Полный User-Agent
отбрасывается.

#### Операционная система

Примеры: _macOS 10.15_, _Windows 10_, _Android 10_, _GNU/Linux_, _Ubuntu 16.04_

Мы используем эти данные, чтобы понять, какие операционные системы используют
люди при посещении нашего сайта. Мы видим название операционной системы и номер
версии.

Этот показатель определяется из HTTP-заголовка User-Agent. Полный User-Agent
отбрасывается.

#### Тип устройства

Примеры: _Desktop_, _Mobile_, _Laptop_, _Tablet_

Мы используем это, чтобы понять, какие устройства используют люди при посещении
нашего сайта. Устройства делятся на настольные, мобильные и планшетные.

Этот показатель определяется из HTTP-заголовка User-Agent. Полный User-Agent
отбрасывается.

#### Страна

Пример: _Великобритания_

Мы определяем страны посетителей по IP-адресу. Мы не отслеживаем ничего более
детального. IP-адрес посетителя отбрасывается и не хранится в базе данных или
журналах.

#### Уникальность пользователей

Plausible пытается найти разумный баланс между дублированием просмотров страниц
и соблюдением конфиденциальности посетителей.

Мы не генерируем постоянные идентификаторы устройства, поскольку в соответствии
с GDPR они считаются персональными данными. Мы не используем файлы cookie, кэш
браузера или локальное хранилище. Мы не храним, не получаем и не извлекаем
ничего с устройств посетителей.

Каждый HTTP-запрос отправляет на сервер IP-адрес и User-Agent, поэтому мы
используем именно эти данные. Мы генерируем ежедневно меняющийся идентификатор,
используя IP-адрес и User-Agent посетителя. Чтобы анонимизировать эти данные и
сделать их невозможными для обратной связи с пользователем, мы пропускаем их
через хэш-функцию с вращающимся значением соли.

    hash(daily_salt + website_domain + ip_address + user_agent)

Это генерирует случайную строку букв и цифр, которая используется для подсчёта
уникальных посетителей за день. Необработанные данные IP-адреса и User-Agent
никогда не хранятся в наших журналах, базах данных или вообще где-либо на диске.

Старые значения соли удаляются каждые 24 часа, чтобы исключить возможность
связывания информации о посетителях одного дня с другим. Забвение использованных
значений соли также устраняет возможность раскрытия исходных IP-адресов при
атаке методом перебора. Необработанные IP-адреса и User-Agent становятся
полностью недоступными для всех, включая нас самих.

Такой подход делает невозможным проведение хорошего анализа удержания
пользователей. Мы не можем увидеть статистику типа "Новые посетители против
вернувшихся", потому что она зависит от наличия постоянного идентификатора
пользователя.

Если вы зайдёте на наш сайт пять раз за один день, то мы увидим вас как одного
уникального посетителя. Но если вы зайдёте на наш сайт в пять разных дней в
течение месяца, то мы увидим вас как пять уникальных посетителей.

### Отказ от аналитики

{{< opt_out_analytics >}}

Эта настройка сохранится в локальном хранилище текущего браузера. Она не
сохраняется в режиме «Инкогнито» и после сброса данных.

Вы также можете отключить JavaScript в браузере, чтобы скрипт аналитики не
загружался.

## Внесение вклада

Вы можете по собственному желанию внести свой вклад в улучшение содержимого
сайта.

Внесение вклада происходит на платформе [GitHub]. На ней действует
[политика конфиденциальности GitHub].

При внесении вклада используется ваше отображаемое имя пользователя и ссылка
на аккаунт. Мы можем использовать эти данные в качестве благодарности за ваш
труд. Поэтому посетители сайта могут увидеть ваше имя пользователя и перейти на
ваш профиль.

[GitHub]: https://github.com/KoolTechTricks/content
[Политика конфиденциальности GitHub]: https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement

## Вопросы по конфиденциальности

[Свяжитесь с нами](/faq/contact), если у вас есть вопросы, комментарии или
опасения по поводу этой политики конфиденциальности, ваших данных или ваших прав
в отношении вашей информации.