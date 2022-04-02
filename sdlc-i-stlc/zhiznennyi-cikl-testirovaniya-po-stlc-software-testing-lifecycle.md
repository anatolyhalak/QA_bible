# Жизненный цикл тестирования ПО (STLC - Software Testing Lifecycle)

**STLC** - это процесс тестирования, который включает в себя определенную последовательность шагов, чтобы гарантировать достижение целей в области качества. В процессе STLC каждое действие выполняется планомерно и систематически. Каждый этап имеет разные цели и результаты. У разных организаций разные этапы STLC, однако основа остается прежней.

**Каждая фаза STLC имеет критерии начала и окончания**:

* _**Критерии входа (entry criteria): Набор общих и специфичных условий для продолжения процесса с определенной задачей, например, фаза тестирования. Цель критериев входа - предотвращение начала задачи, которое может потребовать больше (бесполезных) усилий, чем на устранение не пройденных критериев входа. (Gilb and Graham)**_
* _**Критерии выхода (exit criteria): Набор общих и специфичных условий, согласованных заранее с заинтересованными сторонами, для того, чтобы процесс мог официально считаться завершенным. Цель критериев выхода - предотвращение возможности, когда задание считается завершенным, однако еще существуют отдельные незавершенные части задания. Критерии выхода используются для отчетности, а также планирования того, когда остановить тестирование. (Gilb and Graham)**_

**Фазы STLC**

![https://bambooagile.eu/insights/wp-content/uploads/2021/01/In-article-STLC-copy.png](https://bambooagile.eu/insights/wp-content/uploads/2021/01/In-article-STLC-copy.png)

STLC имеет несколько взаимосвязанных фаз и в целом очень похож на SDLC. Эти фазы являются последовательными и называются:

* **Анализ требований** (Requirement Analysis): один из важнейших этапов, потому что именно на нем можно почти бесплатно исправить недостатки проекта. Этап анализа требований также определяет потенциальную потребность в автоматизированном тестировании и позволяет производить экономические расчеты затрат на рабочую силу на основе оценки проекта. На этом же этапе обсуждаются и документируются критерии начала и окончания тестирования.
  * Entry Criteria: BRS (Business Requirement Specification)
  * Deliverables: список всех проверяемых требований, технико-экономическое обоснование автоматизации (если применимо);
* **Планирование тестирования** (Test Planning): на этом этапе формируется план тестирования, т.е. мы определяем действия и ресурсы, которые помогут достичь целей тестирования (участники и их роли, инструменты, окружение). Во время планирования мы также пытаемся определить метрики, метод сбора и отслеживания этих метрик. План составляют исходя из требований, тестовой стратегии и анализа рисков.
  * Entry Criteria: Requirements Documents;
  * Deliverables: Test Strategy, Test Plan, and Test Effort estimation document.
* **Разработка тест-кейсов** (Test Case Development): подразумевает использование ручного и автоматизированного тестирования для достижения полного охвата функциональности программного обеспечения, при этом процесс основан на заранее установленных требованиях. Чаще всего тест-кейсы для автоматического тестирования пишутся отдельно, так как кейсы для ручного тестирования описаны в виде шпаргалок (cheat sheets).
  * Entry Criteria: Requirements Documents (Updated version);
  * Deliverables: Test cases, Test Scripts (if automation), Test data.
* **Настройка тестовой среды** (Test Environment Setup): в плане тестирования четко указано, какую тестовую среду следует использовать. На этом этапе STLC настраиваются операционные системы и виртуальные машины, развертываются инструменты тестирования, такие как Selenium, Katalon Studio, а также тестовая среда и базы данных проекта. Мы также обращаемся с запросами к DevOps и администраторам, если требуется поддержка.
  * Entry Criteria: Test Plan, Smoke Test cases, Test Data;
  * Deliverables: Test Environment. Smoke Test Results.
* **Выполнение тестов** (Test Execution): тесты выполняются на основе готовой тестовой документации и правильно настроенной тестовой среды. Все результаты тестирования регистрируются в Системе управления тестированием. Отрицательно пройденные тесты, в которых фактический результат отличается от ожидаемого, регистрируются как ошибки и передаются команде разработчиков на доработку с последующей перепроверкой после исправления.
  * Entry Criteria: Test Plan document, Test cases, Test data, Test Environment;
  * Deliverables: Test case execution report, Defect report, RTM.
* **Завершение цикла испытаний** (Test Cycle Closure): окончательная генерация отчетов о тестировании для клиента. Они должны включать затраченное время, процент обнаруженных ошибок и положительных результатов тестирования, общее количество обнаруженных и исправленных ошибок. Что касается отдела тестирования, то это момент для анализа его работы, подведения итогов, анализа его продуктивности и возможности внести предложения по улучшению качества тестирования.
  * Entry Criteria: Test Case Execution report (убедитесь, что нет открытых high severity defects), Defect report;
  * Deliverables: Test Closure report, Test metrics.

**Разница STLC и SDLC**

STLC и SDLC тесно связаны друг с другом, но они одновременно преследуют разные задачи с одной и той же целью, а именно:

* сбор требований в желаемой форме и разработка заявленной функциональности (SDLC);
* анализ требований, помощь клиенту и команде разработчиков и подтверждение качества реализованной функциональности (STLC).

Общая цель - удовлетворение клиента и получение максимально возможного балла на этапах верификации и валидации.

**Почему тестирование разбито на отдельные этапы?**

Ответ из ISTQB Foundation Level Exam: У каждого этапа своя цель.

В большинстве случаев тестирование разбивается на несколько этапов в зависимости от развития самого кода и стремления к эффективному использованию ресурсов. Давайте рассмотрим пример приложения, которое включает в себя как службы REST, так и веб-интерфейс, в agile команде, которая предоставляет набор user stories, которые в конечном итоге будут развернуты как производственный выпуск.

Если команда следует Acceptance Test Driven Development (ATDD), то члены команды будут совместно работать над дизайном тестов историй. Это происходит до начала разработки (одна из характеристик ATDD). Допустим, Мэри - разработчик, который напишет код для служб REST, и допустим, что она практикует разработку через тестирование (TDD). Она строит модульные тесты, по одному, сначала позволяя тесту не пройти, а затем пишет достаточно кода для прохождения теста. Когда имеется достаточное количество тестов для удовлетворения всех требований к истории и эти тесты проходят, тогда разработка и модульное тестирование завершаются. Затем Мэри может написать автоматизированные тесты, которые включают базу данных и, возможно, другие зависимости вне ее кода. Это интеграционные тесты. Поскольку команда использует ATDD, у нее уже есть набор приемочных тестов, поэтому она основывает свои автоматизированные тесты на них. Когда код Мэри проверяется и объединяется в общую ветвь разработки, в процессе сборки выполняются автоматические регрессионные тесты, чтобы убедиться, что существующие функциональные возможности не были нарушены работой Мэри. Эти тесты часто представляют собой просто набор автоматических приемочных испытаний, проводимых в течение месяцев или лет.

Если Сэм является разработчиком пользовательского интерфейса, возможно, он также пишет модульные тесты для некоторых частей своего кода. Когда его работа будет завершена, он может также написать автоматизированные интеграционные тесты, хотя в его тестах могут отсутствовать некоторые сценарии данных, поскольку они охватываются тестами Мэри, и он больше сосредоточится на использовании самого пользовательского интерфейса. Это все еще автоматизированные приемочные тесты, но цель состоит в том, чтобы избежать излишней избыточности существующих тестовых примеров. Как и в случае с кодом Мэри, когда код Сэма проверяется и объединяется в общую ветвь, автоматически выполняется набор регрессии пользовательского интерфейса.

После того, как Сэм и Мэри закончат, Джо, QA-инженер, может провести некоторое ручное приемочное тестирование всей истории, а также некоторое исследовательское тестирование, чтобы убедиться, что сумасшедшее поведение пользователя не приводит к сумасшедшему поведению приложения. Эта комбинация автоматических и ручных тестов составляет приемочное тестирование истории. По завершении ряда историй набор изменений внедряется в интегрированную тестовую среду для окончательного тестирования. Это может представлять собой приемочное тестирование более высокого уровня, а также дополнительное регрессионное тестирование. Дополнительное приемочное тестирование может выполняться инженерами по обеспечению качества, которые следят за тем, чтобы набор историй обеспечивал согласованный рабочий процесс для пользователей и, в конечном итоге, ценность некоторых требований более высокого уровня, которые ранее были разбиты на истории.

Заключительное регрессионное тестирование проводится поверх ранее запущенного пакета автоматизированной регрессии. Возможно, это приложение имеет некоторые функции, которые просто требуют человеческого вмешательства, или, возможно, это окончательная оценка другой группы тестировщиков, которые следят за соблюдением стиля и стандартов поведения.

Как видно из этого рабочего процесса, многие из этих шагов было бы неэффективно выполнить раньше, чем когда они описаны выше. Автоматические тесты являются исключением, так как они могут и часто выполняются многократно на протяжении всего процесса. Однако большинство других «этапов» тестирования - это просто естественное развитие, основанное на развитии выпуска.

Источники:

* [What is Software Testing Life Cycle (STLC)](https://bambooagile.eu/insights/what-is-stlc/)
* [What Is Software Testing Life Cycle (STLC)?](https://www.softwaretestinghelp.com/what-is-software-testing-life-cycle-stlc/)
* [What is Software Testing Life Cycle (STLC) & STLC Phases](https://www.softwaretestingmaterial.com/stlc-software-testing-life-cycle/)
* [Why is testing split into distinct stages?](https://www.quora.com/Why-is-testing-split-into-distinct-stages)

Доп. материал:

* [A Quick Guide to Software Testing Life Cycle](https://hackernoon.com/a-quick-guide-to-software-testing-life-cycle)
* [Как встроить качество в процессы производства ПО? (Часть 2)](https://habr.com/ru/post/591993/)