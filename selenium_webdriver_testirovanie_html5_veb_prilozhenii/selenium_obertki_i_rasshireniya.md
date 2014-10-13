# Selenium "обертки" и расширения
Selenium Webdriver создавался максимально простым и незамысловатым с тем, чтобы поддерживать кроссфплатформенность и кроссбраузерность на эффективном уровне. Это должно означать, что большая часть функционала, которая востребована пользователями, не доступна "из коробки". Такова цена гибкости и простоты использования инструмента.

Взамен Selenium Webdriver предлагает легкость и множество способов расширения инструмента или агрегации в другие инструменты. Конечно это стало доступено прежде всего благодаря открытому исходному коду проекта, а также грамотной ООП архитектуре, построенной на интерфейсах и абстрактных классах.

Расширение инструмента подразумевает добавление в него нового, изначально не доступного функционала в зависимости от целей использования этого инструмента. Часто расширениею подвергаются основные компоненты: Webdriver, WebElement или By.

Отличным примером расширения Selenium Webdriver является HTML Elements framework от yandex, который предложил сразу несколько идей для расширения Page Object паттерна:* 
* Идея разбиения страницы на блоки - аннотация <code>@Block</code>
* Выделение разных типов элемементов (<code>button</code>, <code>checkbox</code>)
* Возможность аннотировать методы как степы - аннотация <code>@Step</code> для работы в стиле step-based

Официальный сайт инструмента http://htmlelements.qatools.ru/

Примеры можно найти на https://github.com/yandex-qatools/htmlelements-examples

Термин "обертка" (wrapper) означает то, что над Webdriver сделана надстройка и доступ к Webdriver API опосредован поллностью либо частично. В качестве "оберток" для Selenium Webdriver на Java наиболее популярные:
* Thucydides
* Geb
* Selenide

Первый инструмент ориентирован прежде всего на автоматизацию приемочного тестирования, а также на красивые отчеты. Thucydides - это report-based фреймворк, позволяющий строить очень подробные html отчеты со скриншотами, степами и другой информацией о тестах.

Geb использует скриптовый язык Groovy(JVM-based) и ориентирован на быстрое и лаконичное написание тестов.

Selenide похож на Geb, но написан на Java. Этот инструмент, кроме легких и гаконичных тестов, оринетирован также на эффективную работу с AJAX элементами.