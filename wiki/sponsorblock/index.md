+++
title = 'SponsorBlock'
categories = ['browser-extensions']
publishDate = 2023-08-23T15:57:00Z
lastmod = 2024-08-18T14:14:00Z
description = """Расширение и API для пропуска раздражающих сегментов в видео \
на YouTube. Пользователи отмечают напоминания о подписке, заставки, рекламу, \
тем самым создавая базу данных, которой может пользоваться любой желающий."""
cover = 'image.webp'
featured = true
+++

# SponsorBlock
{{< categories >}}

[SponsorBlock] — расширение и API для пропуска раздражающих сегментов в видео на
[YouTube]. Пользователи отмечают напоминания о подписке, заставки, рекламу, тем
самым создавая базу данных, которой может пользоваться любой желающий.

[SponsorBlock]: https://sponsor.ajay.app
[YouTube]: /wiki/youtube

![Плеер YouTube с установленным расширением SponsorBlock. Сегменты с рекламой
выделены цветом и пропускаются автоматически.](image.webp)

## Этичность

По умолчанию рекламные интеграции пропускаются автоматически. Такого рода
блокировщик рекламы в теории может вредить авторам, так как отсутствие времени
просмотра сегмента снижает статистику для рекламодателя, из-за чего автор
получает меньшую прибыль. Но, *предположительно*, рекламодатели платят за
количество просмотров и переходы по реферальным ссылкам, ведь большинство
людей пропускают рекламу вручную. Тем не менее возможно добавить каналы в белый
список, чтобы расширение не активировалось при просмотре видео с этих каналов.

Разработчики приложения FreeTube добавили функциональность SponsorBlock, но
отключили пропуск рекламы по умолчанию. Цитата из
[документации](https://docs.freetubeapp.io/usage/sponsorblock/#disclaimer)
(переведено через DeepL):

> Мы, команда FreeTube, считаем конфиденциальность пользователей нашим главным
приоритетом. В то время как большинство рекламных методик имеют тенденцию
вторгаться в частную жизнь пользователей, спонсорство (или спонсорские сегменты)
внутри видео - один из немногих методов, который не ущемляет пользователей в
этом отношении. По этой причине (а также в связи с недавней и заслуженной
популярностью) мы призываем создателей контента использовать этот метод рекламы,
а пользователей - разрешить спонсорство в своих привычках использования сервиса,
чтобы дружественные к частной жизни методы рекламы могли продолжать процветать в
этом сообществе. Если авторы решат, что такой способ рекламы не является
оптимальным, то это, помимо прочего, будет способствовать появлению еще большего
количества рекламы, нарушающей приватность.

В любом случае, вы вольны решать, стоит ли вам пропускать рекламу. Расширение
позволяет отключить автоматический пропуск сегментов определённых категорий.

## Установка

### Браузер

Официальное расширение:

- [Firefox](https://addons.mozilla.org/addon/sponsorblock)
- [Chromium](https://chromewebstore.google.com/detail/mnjggcdmjocbbbhaepdhchncahnbgone)
- [Microsoft Edge](https://microsoftedge.microsoft.com/addons/detail/mbmgnelfcpoecdepckhlhegpcehmpmji)
- [Safari](https://github.com/ajayyy/SponsorBlock/wiki/Safari)

Это расширение работает для официального сайта YouTube. В настройках можно
включить сторонние сайты Invidious, CloudTube, Piped, YouTube Kids (потребуется
выдать разрешение на доступ к ним).

### Android

Вы можете установить
[расширение](https://addons.mozilla.org/android/addon/sponsorblock) в Firefox
для Android.

Сторонние приложения:
- [ReVanced](https://revanced.app) позволяет модифицировать оригинальное
приложение YouTube для добавления поддержки SponsorBlock.
- [LibreTube](https://github.com/libre-tube/LibreTube) — клиент Piped.
- [Tubular](https://github.com/polymorphicshade/Tubular) — форк NewPipe, который
поддерживает SponsorBlock. Включите его в настройках.
- [SkyTube](https://github.com/SkyTubeTeam/SkyTube) поддерживает SponsorBlock.
- [Clipious](https://github.com/lamarios/clipious) поддерживает SponsorBlock.

### iOS

> **Основная статья:**
[SponsorBlock для iOS](https://github.com/ajayyy/SponsorBlock/wiki/iOS)

- [Расширение в Safari](https://github.com/ajayyy/SponsorBlock/wiki/Safari) для
мобильной версии YouTube ([m.youtube.com](https://m.youtube.com)).
- Стороннее приложение [Yatee](https://apps.apple.com/app/yattee/id1595136629)
- Jailbreak: [iSponsorBlock](https://github.com/Galactic-Dev/iSponsorBlock) в
официальном приложении.

### Телевизор

- [SmartTube](https://github.com/yuliskov/SmartTube) (Android TV и Chromecast);
- [iSponsorBlockTV](https://github.com/dmunozv04/iSponsorBlockTV).

### Сторонние реализации

Благодаря открытому API разработчики могут создавать [сторонние приложения и
реализации], и вы можете пользоваться SponsorBlock практически где угодно.

[сторонние приложения и реализации]: https://github.com/ajayyy/SponsorBlock/wiki/3rd-Party-Ports

## Использование

### Сегменты

SponsorBlock предназначен для автоматического или ручного пропуска и заглушения
раздражающих сегментов в видео. Вы можете настроить поведение как вам удобно.

Доступные категории:

- Напоминание о взаимодействии (подписка, лайк и т.п.);
- Пауза/начальная заставка (интро);
- Конечная заставка/титры;
- Показ отрывков из видео в начале;
- Спонсор;
- Самореклама;
- Шутки, отвлечённые темы;
- Тишина в музыкальных видео.

Благодаря SponsorBlock можно быстро пропускать эти сегменты и сохранять время и
нервы.

Также пользователи могут отметить важный момент из видео: пропуск вступления,
переход к сути видео, ответ на вопрос, куплет песни. Вы можете сразу перейти к
этой отметке, чтобы сэкономить время.

### Метки

Метки означают, что видео целиком посвящено какой-либо категории. Такие
категории нельзя разделить на сегменты, не отметив ею большую часть ролика. Это
может помочь при просмотре обзоров.

- Спонсор — автору заплатили деньги за рекламу объекта во всём видео.
- Эксклюзивный доступ — автору предоставили объект бесплатно за создание видео
про него.
- Самореклама.

> [!warning]
> Эти метки устанавливают такие же пользователи, как и вы, поэтому информация
может быть недостоверной. Проверяйте перед отправкой, и не отправляйте, если не
уверены.

![Все виды меток на видео](labels.png)

### Эпизоды

SponsorBlock позволяет указывать эпизоды — собственные тайм-коды в случае, если
они не указаны автором. Помогает при просмотре больших видео и записей
трансляций. Внутри больших эпизодов могут быть маленькие.

Для отправки эпизодов требуется набрать некоторое количество репутации, из-за
этого они встречаются редко.

![Эпизоды на видео от SponsorBlock](chapters.png)

## Краудсорсинг

Чтобы расширение знало, где находятся сегменты, необходимо их кому-то заранее
отправить. Это очень популярное расширение, на всех видео (за исключением самых
новых и от маленьких каналов) скорее всего уже проставлены необходимые сегменты
в правильном порядке. Согласно статистике сервера, более 13 млн пользователей
отправили более 17 млн сегментов.

### Внести вклад

Внести свой вклад можно в официальном расширении или в любом поддерживаемом
приложении. Помощь является почти анонимной и не требует регистрации. Есть
[список лидеров](https://sponsor.ajay.app/stats), кто больше внёс вклад. Своё
отображаемое имя можно сменить в меню расширения.

Иконка с щитом и треугольником в плеере начинает запись сегмента, после чего
можно выбрать категорию и отправить. Здесь же можно посмотреть результат и
ознакомиться с краткими инструкциями.

![Основной интерфейс отправки сегментов](creating_segments.webp)

Постарайтесь отмечать границы сегментов с точностью до миллисекунды, чтобы
пропуск был максимально плавным для глаз и ушей. Используйте кнопки `,` и `.`
для перемещения видео по кадрам, и кнопку «Предпросмотр», чтобы посмотреть
результат.

> [!tip]
> Если вы не уверены в правильности сегмента, то лучше не отправлять его. Вы
можете спросить знающих людей в чате [Matrix] или [Discord].

> **Смотрите также:**
> - [Создание сегментов](https://wiki.sponsor.ajay.app/w/Creating_Segments)
> - [Принципы и методика](https://wiki.sponsor.ajay.app/w/Guidelines)
> - [Советы и рекомендации](https://wiki.sponsor.ajay.app/w/Advice_for_submitting)

### Злоупотребление

Пользователи могут отправлять некорректные сегменты намеренно или случайно. На
самом деле, это происходит очень редко. При возможности, вы можете проголосовать
против и исправить несоответствия. В тяжёлых случаях можно пожаловаться в чат
[Matrix] или [Discord]. В качестве мер защиты также присутствует автоматическая
блокировка.

[VIP](https://wiki.sponsor.ajay.app/w/VIP) имеют возможность модерировать
сегменты и других пользователей. В их полномочия входят:

- Повышенный вес голосов;
- Мгновенная доступность исправлений;
- Блокировка отправки изменений для видео с уже правильно обозначенными
сегментами;
- Выдача предупреждений и блокировок пользователям, отправляющим заведомо
некорректные сегменты.

На данный момент выдача VIP приостановлена на неопределённый срок.

## Открытость

Расширение и [API] с [открытым исходным кодом]. Это позволяет интегрировать
возможности SponsorBlock в [другие приложения].

[База данных] открыта и доступна всем для скачивания. Можно запустить
[собственный сервер] в случае отказа работы официального.

[API]: https://wiki.sponsor.ajay.app/w/API_Docs
[открытым исходным кодом]: https://github.com/ajayyy/SponsorBlock
[другие приложения]: https://github.com/ajayyy/SponsorBlock/wiki/3rd-Party-Ports
[База данных]: https://sponsor.ajay.app/database
[собственный сервер]: https://github.com/mchangrh/sb-mirror

## Исправление проблем

- [Статус сервера](https://status.sponsor.ajay.app);
- [Отчёты об ошибках](https://github.com/ajayyy/SponsorBlock/issues);
- Чат и поддержка в [Matrix] и [Discord];
- Обновления и новости в [Fediverse (Mastodon)] и [X].

[Matrix]: https://go.kde.org/matrix/#/#sponsor:ajay.app
[Discord]: https://discord.gg/SponsorBlock
[Fediverse (Mastodon)]: https://fosstodon.org/@sponsorblock
[X]: https://x.com/SponsorBlock