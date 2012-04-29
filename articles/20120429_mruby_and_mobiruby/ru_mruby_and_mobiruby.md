Эмруби и МобиРуби
=================

| Проект:        | [Энту́ру](https://www.github.com/kyrylo/entooru/)
|:---------------|:-----------------------------------------------------------------
| Автор:         | Мэтт Аймонетти [@merbist][a]
| Дата:          | 20 апреля 2012 года
| URI:           | [http://matt.aimonetti.net/posts/2012/04/20/mruby-and-mobiruby/][0]
| Перевел:       | Кирилл Силин <kyrylosilin@gmail.com>
| Дата перевода: | 29 апреля 2012 года


Сегодня, прямо из Японии, пришли две большие новости о Руби:

* Открытие исходных кодов Эмруби (англ. mruby) и их [релиз на Гитхабе][5]
* Анонс [МобиРуби][6] (англ. MobiRuby): подающее надежды решение для разработки
  приложений для АйОС и Андроида на Руби

Вероятно, из-за моей причастности к [МакРуби][7], люди спрашивали меня, что я думаю
по поводу этих новостей.

Эмруби
------

Эмруби — это далеко не новый проект. Он основан на РайтВМ (англ. RiteVM),
которая спонсируется [Министерством экономики, торговли и промышленности Японии][8]
и возглавляется создателем Руби — [Юкихиро «Matz» Матсумото][4], который пояснил
детали во время своего [лейтмотива на РубиКонфе 2010][9].

Еще в ноябре 2011 Мац говорил об Эмруби. Был записан его доклад, где он довольно
доходчиво объяснял текущую экосистему Руби и почему в Эмруби есть смысл.

Видео доклада на английском языке: «Эмруби — Минималистический Руби и его
перспектива» ([часть первая][01] | [часть вторая][1])

Как сказано, основная цель Эмруби — иметь в наличии версию Руби, которая может
быть внедрена и скомпилирована, а также слинкована внутри другого приложения.

У Хироши Накамуры есть отличное определение Эмруби длиной в одну строчку:

![Hiroshi Nakamura][2]

Эмруби ориентируется на разработчиков игр (для использования вместо Луа
(англ. Lua)), разработчиков встраиваемых систем (устройства, телевизоры,
телефоны…) и приложения с небольшими объемами памяти (вместо Джаваскрипта, к
примеру). Лично я рад Эмруби: он еще не применяется, да и всё еще нужно
проделать большой объем работы, чтобы он доказал свою ценность, но это
определенно большой шаг в верном направлении. Что ещё здорово, так это то, что
проект выпущен под свободной лицензией, позволяющей всем нам вносить свой вклад,
а компаниям — улучшать реализацию для своих конкретных нужд.

_Выводы_: Эмруби — это многообещающий проект, не смотря на то, что он находится
в ранней стадии развития. Помимо того, что это еще одна реализация Руби, факт
того целевая аудитория и ниша проекта хорошо определены и то, что проектом
управляет создатель Руби, а также спонсируется Министерством экономики, торговли
и промышленности Японии, заставляет меня верить в то, что он может оказаться
успешным проектом. Тем не менее, Луа проще и он уже неплохо крутится на целевом
рынке, так что надеюсь, Мац, его команда и Японское правительство имеют план,
который отстоит и защитит эту новую технологию. Им удачи, ну, а я буду
внимательно следить за проектом.

МобиРуби
--------

[МобиРуби][6] разрабатывается [Юитиро Масуи][10], который работает в [Апселераторе][11]
(англ. Appcelerator), компании известной по платформе для написания приложений
на Джаваскрипте для АйОС, Андроида под названием [Титаниум][12] (англ. Titanium).
МобиРуби — это надстройка над Эмруби, которая является первой демострацией того,
что мотивированные разработчики могут сделать с новой реализацией Маца. Подобно
Эмруби, МобиРуби будет выпущен под свободной лицензией. Однако в отличие от
Эмруби, была выбрана [лицензия Апача][13]. Пока что МобиРуби — это всего лишь анонс с
примером кода и скриншотом. Этого достаточно, чтобы попасть на главную страницу
[ХакерНьюс][14]. Очевидно, автор планирует выпустить первую версию через несколько
месяцев.

![МобиРуби][3]

Может это кого и удивит, но я вполне доволен видеть проекты такого типа, даже
если они в некоторой степени и конкурируют с МакРуби. Это доказывает две вещи:

* Существует сильный интерес к Руби на мобильных устройствах
* Это осуществимо с технической точки зрения

Не открою Америки, если скажу, что разработчики на Луа имели возможность
какое-то время писать приложения для АйОС. Но пока еще большинство разработчиков
для АйОС все равно пользуются Обжектив-Си. С какими камнями преткновения можно
столкнуться, пытаясь заменить Обжектив-Си?

Язык для замены может не подойти под архитектуру Кокоа
------------------------------------------------------

Разработка приложения для АйОС/ОС Х означает, что вы тратите свое время на
использование предоставленных библиотек (названных фреймворками на жаргоне
Эпла). Эти фреймворки имеют заданные шаблоны, четко обозначенный синтаксис
и, обычно, они работают в очень последовательном/стесняющем ключе. Либо ваш язык
более или менее похож (как Руби) и переход легок, либо вам нужно начинать писать
и поддерживать обертки (Титаниум).

Перемыкающиеся рантаймы
-----------------------

Иметь одновременно два рантайма — это довольно сомнительно и неэффективно. Это
одна из причин, почему Эпл подтолкнула МакРуби к отклонению от курса [РубиКокоа][15],
который является мостом и создать реализацию Руби, работающую в самом рантайме
Обжектив-Си. Это открывает новый горизонт: в МакРуби все объекты, на самом деле,
являются объектами Обжектив-Си, что означает, что вам ничего не нужно
конвертировать, а АПИ (англ. API) Кокоа могут быть расширены из кода Руби,
просто путем переоткрывания их.

Поддержка
---------

Этот пункт является переломным для многих. Часто бывает так, что вы не желаете,
чтобы ваш следующий большой проект полагался на технологию, которая никем не
опекается. Что происходит, когда вы строите свое приложение с помощью
альтернативной реализации и вдруг разработчикам надоедает проект и они его
покидают (или занимаются другими вещами)? Что насчет нужных обновлений согласно
обновлениям платформ Эпла/Гугла? Возможно, это не лучшая причина для отказа от
альтернативы, однако это разумная причина, особенно для компаний, которые хотят
быть в «безопасности».

Кокоа
-----

АПИ Кокоа представляют, наверное, 90% проблем при написании приложений для
АйОС/ОС Х. Хоть АПИ и мощны, и производительны, они часто причиняют страдания
во время привыкания и изучения. Вы испытываете проблему документации, когда все
примеры написаны только на Обжектив-Си, требуя, чтобы кто-то [написал книгу][16] и/или
перевел огромное количество документации. Также, у вас есть все инструменты
Эпла, которые вы часто не можете использовать на полную катушку, потому что вы
не используете их инструментарий. По правде говоря, после многих лет
использования МакРуби, я думаю, что настоящая ценность подобного проекта не в
более легком синтаксисе, а в том, что вы легко можете строить обертки и
интерфейсы более высокого уровня вокруг повторяющихся задач. Иметь комплекс
хорошо спроектированных ДСЛ (англ. DSL) и при этом иметь доступ к родному
объекту — это нечто в высшей степени могучее.

Обжектив-Си развивается
----------------------

Обжектив-Си развивается: с появлением [АРС][17] (англ. ARC) управление памятью стало
намного легче. Последняя версия Клэнга (Clang) одарила Обжектив-Си более
приятным синтаксисом благодаря новым литералам и объектным указателям ([узнать
больше][18]). По сути, синтаксис Обжектив-Си становится все ближе и ближе похожим на
синтаксис Руби. Решение о выборе необходимости использования альтернативы
становится все более трудным.

``` objective-c
// Символьные литералы.
NSNumber *theLetterZ = @'Z';          // аналог [NSNumber numberWithChar:'Z']

// Интегральные литералы.
NSNumber *fortyTwo = @42;             // аналог [NSNumber numberWithInt:42]

// Литералы чисел с плавающей точкой.
NSNumber *piDouble = @3.1415926535;   // аналог [NSNumber numberWithDouble:3.1415926535]

// Булевы литералы.
NSNumber *yesNumber = @YES;           // аналог [NSNumber numberWithBool:YES]

// Контейнерные литералы
NSArray *array = @[ @"Hello", NSApp, [NSNumber numberWithInt:42] ];
id value = array[idx];

NSDictionary *dictionary = @{
  @"name" : NSUserName(),
  @"date" : [NSDate date],
  @"processInfo" : [NSProcessInfo processInfo]
};
id oldObject = dictionary[key];
dictionary[key] = newObject; // замените oldObject на newObject
```

Производительность
------------------

Хотя устройства и становятся всё более мощными, производительность часто
критична, и Эпл оптимизировал производительность их решения для их языка. Если
вы когда-либо разрабатывали Титаниумовское приложение, вы знаете, что это может
быть проблемой и может быть вам нужно искать обходные пути, чтобы добиться
приличной производительности.

_Выводы_: Опираясь на всё это, когда МобиРуби будет выпущен, я буду иметь
возможность судить более хорошо. Однако опираясь на то, что я пока что видел,
я весьма обеспокоен синтаксисом и производительностью, которую мы получим из
коробки. Но время покажет и есть куда расти. Руби на АйОС/Андроиде — это что-то
захватывающее, и я уже вижу себя в будущем, тестирующего первые беты.

[a]: http://twitter.com/merbist
[0]: http://matt.aimonetti.net/posts/2012/04/20/mruby-and-mobiruby/
[01]: http://youtu.be/n7XRYWclYDY "Часть 1"
[1]: http://youtu.be/sB-IifjyeLI "Часть 2"
[2]: http://img-fotki.yandex.ru/get/6209/98991937.9/0_7646a_3cae4786_orig
[3]: http://img-fotki.yandex.ru/get/9/98991937.9/0_7640d_d0bd2d30_orig
[4]: http://ru.wikipedia.org/wiki/%D0%9C%D0%B0%D1%86%D1%83%D0%BC%D0%BE%D1%82%D0%BE,_%D0%AE%D0%BA%D0%B8%D1%85%D0%B8%D1%80%D0%BE
[5]: https://github.com/mruby/mruby
[6]: http://mobiruby.org/
[7]: http://macruby.org/
[8]: http://www.meti.go.jp/english/
[9]: http://www.slideshare.net/yukihiro_matz/rubyconf-2010-keynote-by-matz
[10]: https://github.com/masuidrive
[11]: http://www.appcelerator.com/
[12]: http://www.appcelerator.com/platform/titanium-sdk
[13]: http://www.dataved.ru/2011/03/apache-license-2.html
[14]: http://news.ycombinator.com/item?id=3866418
[15]: http://en.wikipedia.org/wiki/RubyCocoa
[16]: http://www.amazon.com/gp/product/1449380379/ref=as_li_ss_tl?ie=UTF8&tag=merbist-20&linkCode=as2&camp=1789&creative=390957&creativeASIN=1449380379
[17]: http://developer.apple.com/library/ios/#releasenotes/ObjectiveC/RN-TransitioningToARC/Introduction/Introduction.html
[18]: http://clang.llvm.org/docs/ObjectiveCLiterals.html