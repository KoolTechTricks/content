+++
title = 'KeePassXC'
categories = ['security']
publishDate = 2024-06-30T13:59:34Z
lastmod = 2024-11-06T11:46:00Z
description = """Кроссплатформенный менеджер паролей с открытым исходным \
кодом. Хранит все данные локально в зашифрованном виде. В программе нет \
излишних функций, рекламы и платных подписок."""
cover = 'keepassxc.webp'
featured = true
+++

# KeePassXC
{{< categories >}}

[KeePassXC] — кроссплатформенный менеджер паролей с [открытым исходным кодом].
Хранит все данные локально в зашифрованном виде. В программе нет излишних
функций, рекламы и платных подписок.

![KeePassXC](keepassxc.webp)

[KeePassXC]: https://keepassxc.org
[открытым исходным кодом]: https://github.com/keepassxreboot/keepassxc

**Базовые функции:**
- [Создание](#создание-базы-данных), [открытие](#открытие-базы-данных) и
[хранение](#хранение-базы-данных) баз данных на локальном компьютере в формате
KDBX (совместим с KeePass и другими программами);
- Хранение конфиденциальной информации в [записях](#записи),
[организованных по группам](#организация-записей);
- [Генератор безопасных паролей](#генератор-паролей);
- Автоматический ввод паролей в приложениях;
- [Интеграция с браузерами](#расширение-для-браузера) Google Chrome, Mozilla
Firefox, Microsoft Edge, Chromium, Vivaldi, Brave;
- Импорт баз данных из форматов CSV, 1Password и KeePass1.

**Продвинутые функции:**
- [Отчёты по базе данных](#отчёты-по-базе-данных): состояние паролей,
[Have I Been Pwned?], статистика;
- Экспорт базы данных в форматы CSV и HTML;
- [Хранение и генерация TOTP](#двухфакторная-аутентификация) (одноразовые
пароли для двухфакторной аутентификации);
- [Ссылки на поля между записями];
- Вложения файлов и пользовательские атрибуты;
- История записей и откат к предыдущим версиям;
- Поддержка аппаратных ключей YubiKey/OnlyKey;
- Интерфейс командной строки `keepassxc-cli`;
- Автоматическое открытие баз данных;
- Общие базы данных [KeeShare] (импорт, экспорт и синхронизация);
- Агент SSH;
- FreeDesktop.org Secret Service (замена связки ключей Gnome и т.д.).

[Have I Been Pwned?]: https://haveibeenpwned.com
[Ссылки на поля между записями]: https://keepass.info/help/base/fieldrefs.html
[KeeShare]: https://keepassxc.org/docs/KeePassXC_UserGuide#_database_sharing_with_keeshare

## Ключевые особенности

KeePassXC хранит всю информацию на вашем компьютере, а не на сервере, в отличие
от многих других менеджеров паролей. Это гарантирует, что ваши конфиденциальные
данные находятся у вас и ни у кого больше. Однако вам придётся самостоятельно
заботиться о сохранности информации и периодически делать резервные копии. Тем
не менее вы можете синхронизировать базу данных с облаком или между устройствами
с помощью [Syncthing]. Это полностью безопасно, так как никакие данные не
сохраняются в незашифрованном виде на диске, следовательно, недоступны для
прочтения сторонним лицам.

[Syncthing]: /wiki/syncthing

KeePassXC является нативной программой с [открытым исходным кодом], написанной
на языке C++ с использованием графической библиотеки Qt, для Windows, macOS и
Linux. При этом интерфейс на разных операционных системах выглядит одинаково
хорошо, что гарантирует вам беспроблемный опыт использования на любом
устройстве. Также доступен интерфейс командной строки `keepassxc-cli`.

Файл с паролями хранится в зашифрованном виде в формате KDBX. Его можно открыть
и в других программах, которые поддерживают этот формат. Например, существуют
сторонние мобильные приложения, которые полностью поддерживают формат
KeePassXC: [KeePassDX](#android) для Android и [KeePassium](#ios) для iOS.

## Различия между KeePassXC и KeePass

KeePass и KeePassXC с открытым исходным кодом и активно поддерживаются
разработчиками.

[KeePass] — это первоначальная программа, которая вышла в 2003 году. Она
изначально была разработана только для Windows, но потом стала доступна и на
других операционных системах. До этого поддержка для Linux и macOS была в форке
под названием [KeePassX]. Со временем, KeePassX перестал активно
разрабатываться, из-за чего появился другой форк — KeePassXC.

[KeePass]: https://keepass.info
[KeePassX]: https://www.keepassx.org

[Из официального сайта](https://keepassxc.org/docs#faq-keepass)
(переведено с помощью DeepL):

> **Почему KeePassXC вместо KeePass?**
>
> KeePass — очень проверенный и многофункциональный менеджер паролей, и в нем
нет ничего принципиально плохого. Однако он написан на C# и поэтому требует
платформы Microsoft .NET. На системах, отличных от Windows, вы можете запустить
KeePass с помощью библиотек Mono, но при этом вы не получите привычного внешнего
вида и функциональности. KeePassXC, с другой стороны, разработан на C++ и
работает на всех платформах, обеспечивая наилучшую интеграцию платформ.

[Подробнее](https://superuser.com/a/879013) (англ.)

В KeePassXC также встроены дополнительные функции: интеграция с браузером,
агент SSH, системная служба секретов, поддержка аппаратных ключей (YubiKey),
сканер отпечатков пальцев и KeeShare.

## Установка

Официально KeePassXC поддерживается только для компьютера (Windows, macOS и
Linux). Для мобильных платформ существуют сторонние приложения, полностью
совместимые с форматом KeePassXC.

### Компьютер

Официальная программа KeePassXC доступна для Windows, macOS и Linux. Инструкции
по установке можно найти на [официальном сайте](https://keepassxc.org/download).

### Android

[KeePassDX] — менеджер паролей для Android, который совместим с базой данных
KeePassXC (KDBX).

![KeePassDX](keepassdx.webp)

[KeePassDX]: https://www.keepassdx.com

**Функции:**
- Разблокировка биометрией (отпечаток пальца, скан лица);
- Интеграция с клавиатурой (автозаполнение);
- Приложению запрещён доступ в интернет;
- [Открытый исходный код](https://github.com/Kunzisoft/KeePassDX).

Доступны версии Free и Libre. Версия Free подписана разработчиками приложения и
предназначена для повседневного использования. Версия Libre не содержит
проприетарного кода.
[Подробнее](https://github.com/Kunzisoft/KeePassDX/wiki/FAQ#why-a-libre-and-free-version)

- [Google Play](https://play.google.com/store/apps/details?id=com.kunzisoft.keepass.free)
(Free);
- [GitHub](https://github.com/Kunzisoft/KeePassDX/releases) (Free и Libre);
- [F-Droid](https://f-droid.org/packages/com.kunzisoft.keepass.libre) (Libre).

В приложении нет возможности скачать иконки сайтов, в отличие от настольной
версии KeePassXC. Если вы создаёте запись в KeePassDX, вам придётся скачивать
иконку вручную с [сайта](https://www.keepassdx.com/#icons).

### iOS

[KeePassium] — менеджер паролей для iOS, который совместим с базой данных
KeePassXC (KDBX).

[Скриншоты KeePassium](https://github.com/keepassium/KeePassium#screenshots)

[KeePassium]: https://keepassium.com

**Функции:**
- Разблокировка биометрией (отпечаток пальца, скан лица);
- Автозаполнение;
- Возможность автоматической синхронизации базы данных с облаком;
- [Открытый исходный код](https://github.com/keepassium/KeePassium).

**Премиум функции:**
- Множественные базы данных;
- Поддержка YubiKey;
- Ссылки на поля.

Скачать из [AppStore](https://apps.apple.com/app/id1435127111).

## Использование

В этом разделе представлено краткое руководство по базовому использованию
официальной программы KeePassXC для компьютера.

Полное руководство на английском языке поставляется вместе с программой: Меню
*Справка* → *[Начало работы]* / *[Руководство пользователя]*.

[Начало работы]: https://keepassxc.org/docs/KeePassXC_GettingStarted
[Руководство пользователя]: https://keepassxc.org/docs/KeePassXC_UserGuide

### База данных

В базе данных KeePassXC хранится вся ваша конфиденциальная информация в
зашифрованном виде. Чтобы начать использовать KeePassXC, нужно создать базу
данных. При первом запуске программа предложит создать базу данных, открыть
существующую или импортировать из другого формата.

#### Создание базы данных

При создании базы данных будет предложено дать ей название и описание, но можно
пропустить этот этап и оставить поля пустыми. Название и описание доступны
только при расшифровке базы данных.

Далее можно настроить шифрование, но рекомендуется оставить все параметры по
умолчанию. Однако вы можете изменить время расшифровки. Чем больше это значение,
тем сильнее защита, но дольше открывается база данных. Настройки шифрования
можно изменить после создания базы данных.

Теперь требуется ввести главный пароль для базы данных. Пароль должен быть
длинным и состоять из разных символов, чтобы нельзя было легко его перебрать.
Для генерации безопасного пароля можно использовать [встроенный генератор].
Храните этот пароль в надежном месте — либо запомните его, либо запишите
где-нибудь. Потеря пароля может привести к постоянной блокировке базы данных,
и вы не сможете получить информацию, хранящуюся в ней.

[встроенный генератор]: #генератор-паролей

Далее вам будет предложено выбрать место для сохранения файла базы данных. Этот
файл сохраняется на вашем компьютере с расширением `.kdbx` по умолчанию. Вы
можете хранить свою базу данных где угодно, она всегда полностью зашифрована и
предотвращает несанкционированный доступ.

#### Открытие базы данных

Для открытия базы данных, выберите её файл в соответствующем меню, затем
введите пароль. Если вы добавляли дополнительные методы защиты, то вам нужно
также их пройти. Дополнительно поддерживаются варианты разблокировки биометрией
(отпечаток пальца, скан лица). Открытие базы данных может занять несколько
секунд, если вы выбрали большое время расшифровки при создании.

Можно открыть сразу несколько баз данных и даже перемещать записи между ними.
Открытые базы данных отображаются в виде вкладок.

#### Хранение базы данных

Файл базы данных может содержать конфиденциальные данные и должен храниться
очень надежно. База данных должна быть защищена сложным и длинным паролем. Он
обеспечит надёжное шифрование файла.

Следите за тем, чтобы файл базы данных не был случайно удалён кем-либо или
чем-либо. Удаление файла базы данных приведёт к полной потере всей вашей
информации (включая все пароли). Не сообщайте никому учётные данные для доступа
к файлу базы данных, если только вы не доверяете им.

В настройках программы можно включить автоматическое создание резервной копии
перед сохранением. В меню *База данных* можно создать резервную копию вручную.

> [!tip]
> Вы можете безопасно хранить файл базы данных в облаке (OneDrive, Google Drive,
Яндекс Диск, Nextcloud, [Syncthing] и т.д.). Файл базы данных всегда полностью
зашифрован; незашифрованные данные никогда не записываются на диск и не доступны
поставщику облачного хранилища. Мы рекомендуем использовать сервис хранения
данных, который автоматически сохраняет резервные копии (историю версий) файла
базы данных на случай повреждения или случайного удаления.

#### Управление базой данных

Выберите в меню *База данных*, затем *Параметры базы данных*.

Здесь можно изменить пароль, добавить дополнительную защиту или изменить
параметры шифрования. Также можно удалить неиспользуемые значки.

#### Отчёты по базе данных

Выберите в меню *База данных*, затем *Отчёты по базе данных*.

Здесь можно посмотреть подробную статистику о записях. Также доступны
результаты проверки безопасности, которые показывают слабые и просроченные
пароли.

Можно пройти проверку в сервисе [Have I Been Pwned?] (HIBP). Туда передаются
первые пять символов от хеша пароля. Другие сведения, за исключением количества
паролей и IP-адреса, не передаются. Этот сервис показывает, не были ли раскрыты
ваши пароли в ходе различных утечек.
[Подробнее](https://en.wikipedia.org/wiki/Have_I_Been_Pwned)

### Записи

Записи — это ячейки, в которых хранится информация о каком-то одном объекте:
имя пользователя, пароль, URL, вложения, заметки и так далее.

#### Создание записей

Добавить запись можно нажатием на кнопку «+» в панели инструментов или через
меню «Записи». Затем введите нужные данные (все поля опциональные).

- **Название.** Отображаемое имя записи (обычно, это название сервиса, на
котором находится ваш аккаунт).
- **Имя пользователя.** Логин, почта или номер телефона, по которым можно войти
в аккаунт. Часто используемые имена пользователя будут предложены в выпадающем
списке.
- **Пароль.** Можно сгенерировать при помощи [встроенного генератора].
- **URL.** Ссылка на сайт, на котором находится ваш аккаунт. Иконку сайта можно
скачать, для этого используется служба DuckDuckGo. По URL
[расширение для браузера] определяет наличие аккаунта и предлагает заполнить
данные.
- **Теги.** Нужны для быстрого поиска.
- **Истекает.** Время, после которого пароль будет предложено заменить.

[встроенного генератора]: #генератор-паролей
[расширение для браузера]: #расширение-для-браузера

Можно добавить дополнительные атрибуты. Например, если вы привязывали к аккаунту
почту или телефон, то следует добавить и эти данные, чтобы иметь возможность
отслеживать их использование. Атрибуты можно быстро копировать при
необходимости.

Можно прикрепить вложения, добавить свой значок, настроить автоматический ввод.

#### Редактирование записей

Выберите запись и нажмите иконку с карандашом в панели инструментов. Внесите
изменения и нажмите «ОК», чтобы сохранить их.

История изменений сохраняется, при необходимости возможно откатить или удалить.

#### Список записей

Главное окно KeePassXC представлено в виде списка записей. Это таблица, столбцы
которой можно настраивать обычными действиями мыши (перемещение, изменение
размера, видимость (правая кнопка мыши)).

При выделении записи, внизу отобразится подробная информация. Нажмите
`Ctrl`+`C`, чтобы скопировать пароль, `Ctrl`+`B` — скопировать имя пользователя.
`Ctrl`+`U` — скопировать URL. Скопированные данные не сохраняются в буфере
обмена и будут очищены через 10 секунд.

#### Организация записей

Вы можете создать группы, они работают как папки. Для этого нажмите правой
кнопкой мыши по корневой группе, а затем создайте новую. Для группы можно
задать параметры, которые будут наследоваться дочерними записями. Записи можно
вкладывать во сколько угодно уровней групп.

Переместить запись можно удержанием левой кнопкой мыши (можно выделить сразу
несколько). Доступно перемещение как в другие группы, так и в другие базы
данных.

По умолчанию удалённые записи перемещаются в корзину.

Записи можно искать по ключевым словам (поддерживается расширенный поиск с
использованием модификаторов), а также фильтровать по тегам.

### Генератор паролей

В KeePassXC всегда доступен генератор паролей при нажатии на значок игральной
кости в панели инструментов или в поле ввода пароля.

В поле ввода можно ввести пароль, затем отобразится его качество. Качество
пароля оценивается энтропией (количество битов). Чем уникальнее комбинация
символов, тем выше энтропия.

Можно сгенерировать пароль: выберите длину и группы символов (можно задать
свои). Или же можно сгенерировать парольную фразу: выберите список слов,
количество и дополнительные параметры.

### Расширение для браузера

Расширение KeePassXC-Browser устанавливается в ваш браузер, чтобы вы могли
автоматически извлекать имена пользователей и пароли из KeePassXC и вводить их
непосредственно в поля сайта. Это очень полезное и безопасное расширение,
которое повышает вашу производительность при использовании KeePassXC. С этим
расширением вам не нужно вручную копировать данные из базы данных KeePassXC и
вставлять их в поля сайта.

> **Смотрите также:**
[Исправление проблем](https://github.com/keepassxreboot/keepassxc-browser/wiki/Troubleshooting-guide)
(англ.)

Расширение доступно для [Chromium] (Chrome, Brave, Vivaldi, Edge) и [Firefox].

[Chromium]: https://chromewebstore.google.com/detail/oboonakemofpalcgghocfoadofidjkkk
[Firefox]: https://addons.mozilla.org/firefox/addon/keepassxc-browser

> [!important]
> Расширение может не работать, если браузер находится в песочнице (например,
[Snap на Ubuntu]). При таких условиях у браузера нет доступа ко всей системе,
из-за чего не получается связаться с другими программами (в данном случае
с KeePassXC).

[Snap на Ubuntu]: https://www.bentasker.co.uk/posts/blog/general/enabling-nativemessaging-for-keepassxc-on-ubuntus-snap-firefox.html

В настройках KeePassXC (параметры программы, а не базы данных) нужно включить
интеграцию с браузером. Выберите здесь браузеры, в которых установлено
расширение.

Убедитесь, что база данных разблокирована, затем откройте (или перезапустите)
браузер. Нажмите на значок расширения KeePassXC-Browser, затем
*Подключиться (Connect)*. Откроется окно в KeePassXC, вас попросят назвать
подключение уникальным именем (например, *firefox-laptop*). Если вы повторно
используете название подключения к базе данных, предыдущее подключение
браузера будет перезаписано и не позволит получить доступ.

После успешного подключения в полях ввода данных аккаунта на сайтах начнут
появляться иконки KeePassXC. Если KeePassXC открыт, база данных разблокирована
и в ней есть данные для текущего сайта, то нажатие на иконку заполнит поля
логина и пароля. Если в базе данных несколько записей на один и тот же сайт, то
будет предложено выбрать подходящее.

При первой попытке заполнения данных появится запрос на использование записи.
Вы можете запомнить, чтобы окно не появлялось каждый раз.

### Двухфакторная аутентификация

Двухфакторная аутентификация посредством одноразовых паролей (TOTP) является
наиболее популярной для дополнительной защиты аккаунта. Для входа требуется
ввести код (обычно шестизначный), который меняется каждые 30 секунд. Он
определяется на основе общего секретного значения и текущего времени. Для этого
существуют специальные приложения, например, Google Authenticator, но можно
использовать и KeePassXC.

> [!caution]
> Хранение кодов TOTP в той же базе данных, что и паролей, лишает вас
преимуществ двухфакторной аутентификации. Если вы хотите обеспечить максимальную
безопасность, мы рекомендуем хранить коды TOTP в отдельной базе данных, которую
вы разблокируете только при необходимости.
>
> Лучше всего генерировать TOTP другим приложением на мобильном устройстве,
например, [Aegis].

[Aegis]: https://getaegis.app

> [!important]
> Время вашего компьютера должно быть синхронизировано с интернет-источником
времени, чтобы генерировать действительные коды TOTP.
[Подробнее](https://www.nist.gov/pml/time-and-frequency-division/time-distribution/internet-time-service-its).
(англ.)

Чтобы добавить TOTP к записи в базе данных, необходимо сначала получить
секретную строку с сайта или приложения, на котором вы проходите аутентификацию.
Часто она сопровождается QR-кодом.

Получив секретный код, щёлкните правой кнопкой мыши на нужной записи, выберите
*TOTP* → *Настроить TOTP...*, после чего появится окно настройки. В этом окне
вставьте секретный код с сайта, при необходимости установите пользовательские
настройки, затем нажмите ОК, чтобы сохранить настройки.

После того как запись настроена на TOTP, в строке записи появится значок часов,
а в панели предварительного просмотра можно будет показать текущий код. Кроме
того, вы можете перейти в меню TOTP записи, чтобы показать код в отдельном окне.
Вы также можете просмотреть секретную строку и конфигурацию в виде QR-кода для
экспорта на мобильное устройство. Коды TOTP можно вводить в формы с помощью
расширения для браузера или функции автоматического ввода.

## Ссылки

- [Документация](https://keepassxc.org/docs) (англ.)
- [Fediverse (Mastodon)](https://fosstodon.org/@keepassxc) (англ.)
- [Поддержать](https://keepassxc.org/donate)

## Альтернативы

- [Bitwarden] — менеджер паролей, который хранит все данные надёжно в облаке.
Это удобно, если вы не готовы заботиться о резервных копиях и синхронизации
локальной базы данных KeePassXC. Код сервера и клиентов
[открыт](https://github.com/bitwarden).

[Bitwarden]: https://bitwarden.com

## Смотрите также

- [Введение в пароли](https://www.privacyguides.org/ru/basics/passwords-overview)
— Privacy Guides
- [Пароли](https://wiki.archlinux.org/title/Security_(Русский)#Пароли)
— ArchWiki