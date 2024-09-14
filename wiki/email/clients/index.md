+++
title = 'Почтовые клиенты'
categories = ['internet', 'privacy', 'productivity', 'software-collections']
publishDate = 2024-09-14T17:29:00Z
lastmod = 2024-09-14T17:36:00Z
description = """Специальные программы, которые позволяют получать и \
отправлять электронные письма. Они более удобные, функциональные и \
конфиденциальные, чем веб-почта."""
cover = 'thunderbird.webp'
featured = true
+++

# Почтовые клиенты
{{< categories >}}

Почтовые клиенты — это специальные программы, которые позволяют получать и
отправлять электронные письма. Они более функциональные и конфиденциальные, чем
веб-почта.

**Преимущества почтовых клиентов над веб-почтой:**
- Использование нескольких аккаунтов одновременно без необходимости
переключаться между ними.
- Дополнительные функции и возможности для управления письмами.
- Автономная работа.
- Отсутствие рекламы и прочих отвлекающих элементов.
- Защита от отслеживания в письмах по умолчанию.

Подробнее: [Почему стоит использовать почтовый клиент, а не веб-почту].

[Почему стоит использовать почтовый клиент, а не веб-почту]: https://telegra.ph/Pochemu-stoit-ispolzovat-pochtovyj-klient-a-ne-veb-pochtu-09-14

Для авторизации в почтовом клиенте может потребоваться выполнение настройки.

|Почтовый сервис|Инструкция|
|---------------|----------|
|**Gmail**|Введите свой логин и пароль, разрешите доступ к своей учётной записи.
|**Яндекс Почта**|Разрешите использование почтовых программ в [настройках Почты], создайте [пароль приложения](https://id.yandex.ru/security/app-passwords) и используйте его для авторизации в почтовом клиенте.
|**Mail.ru**|Разрешите использование почтовых программ в настройках Почты, создайте [пароль приложения](https://help.mail.ru/mail/security/protection/external) и используйте его для авторизации в почтовом клиенте.
|**Proton Mail**|Оплатите [подписку](https://proton.me/mail/pricing), настройте [Proton Mail Bridge]
|**Tuta**|Сторонние почтовые клиенты [не поддерживаются](https://tuta.com/de/support/howto#imap)

[настройках Почты]: https://mail.yandex.ru/?dpda=yes#setup/client
[Proton Mail Bridge]: https://proton.me/mail/bridge

У каждого почтового сервиса должно быть руководство в справочной системе о том,
как настроить сторонние почтовые клиенты для вашей учётной записи.

## Thunderbird

![Thunderbird](thunderbird.webp)

|||
|-|-|
|**Платформы**|Windows, Linux, macOS
|**Технологии**|Основано на Firefox, Открытый исходный код
|**Сайт**|https://www.thunderbird.net
|**Поддержать**|https://www.thunderbird.net/?form=support
|**Документация**|https://support.mozilla.org/products/thunderbird
|**Информация актуальна для версии**|128.2.0

- Windows [winget](/wiki/winget): `Mozilla.Thunderbird`
- Linux: [Flathub](https://flathub.org/apps/org.mozilla.Thunderbird)

Почтовый клиент, управляемый Mozilla Foundation и поддерживаемый сообществом.
Полностью свободный, ставит безопасность и конфиденциальность на первое место.
Существует с 2003 года и обладает широким набором возможностей.

Поддерживаются [дополнения](https://addons.thunderbird.net) как в браузерах
Firefox и Chrome.

|||
|-|-|
|**Фоновая работа**|❌ Нет
|**Фильтры**|✅ Есть
|**Загрузка содержимого из Интернета**|✅ Отключена по умолчанию
|**Поддержка шифрования (PGP)**|✅ Есть
|**Экспорт/Импорт настроек**|✅ Есть (папка профиля)
|**Дополнительные функции**|Календарь, контакты, список задач, чат (IRC, XMPP, Matrix), чтение [лент RSS](/wiki/rss)

### Betterbird

Модификация Thunderbird с исправлением некоторых ошибок и добавлением
дополнительных функций, например, иконка в трее на Linux.
[Полностью совместим с Thunderbird], можно использовать тот же профиль, не
перенося аккаунты и настройки.

[Полностью совместим с Thunderbird]: https://betterbird.eu/support/index.html#switch-tb-bb

- [Скачать с официального сайта](https://betterbird.eu/downloads/index.php)
- Windows [winget](/wiki/winget): `Betterbird.Betterbird`
- Linux: [Flathub](https://flathub.org/apps/eu.betterbird.Betterbird)

## FairEmail

![FairEmail](fairemail.webp)

|||
|-|-|
|**Платформа**|Android
|**Технологии**|Java, C++, Открытый исходный код
|**Сайт**|https://email.faircode.eu
|**Поддержать**|https://email.faircode.eu/donate
|**Документация**|https://m66b.github.io/FairEmail
|**Исходный код**|https://github.com/M66B/FairEmail
|**Информация актуальна для версии**|1.2230

- [Google Play](https://play.google.com/store/apps/details?id=eu.faircode.email)
- [GitHub](https://github.com/M66B/FairEmail/releases/latest)
- [F-Droid](https://f-droid.org/packages/eu.faircode.email)

Почтовый клиент, разработанный специально для обеспечения конфиденциальности
пользователя. По умолчанию не загружает сторонние элементы в письмах и
анализирует внешние ссылки перед переходом.

Некоторые функции требуют приобретения версии Pro. Это необходимо для
поддержания разработки проекта.

|||
|-|-|
|**Фильтры**|✅ Есть
|**Загрузка содержимого из Интернета**|✅ Отключена по умолчанию
|**Поддержка шифрования (PGP)**|✅ Есть
|**Экспорт/Импорт настроек**|💰 В версии Pro

## K-9 Mail

![K-9 Mail](k9mail.webp)

|||
|-|-|
|**Платформа**|Android
|**Технологии**|Kotlin, Java, Открытый исходный код
|**Сайт**|https://k9mail.app
|**Поддержать**|https://www.thunderbird.net/?form=support
|**Документация**|(Устарела) https://docs.k9mail.app
|**Исходный код**|https://github.com/thunderbird/thunderbird-android
|**Информация актуальна для версии**|6.804

- [Google Play](https://play.google.com/store/apps/details?id=com.fsck.k9)
- [GitHub](https://github.com/thunderbird/thunderbird-android/releases/latest)
- [F-Droid](https://f-droid.org/packages/com.fsck.k9)

Простой почтовый клиент с открытым исходным кодом для Android, который
разрабатывается под руководством Thunderbird. В будущем будет преобразован в
Thunderbird для Android.

|||
|-|-|
|**Фильтры**|❌ Нет
|**Загрузка содержимого из Интернета**|✅ Отключена по умолчанию
|**Поддержка шифрования (PGP)**|✅ Есть
|**Экспорт/Импорт настроек**|✅ Есть
