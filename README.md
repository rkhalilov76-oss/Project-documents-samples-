# Библиотека шаблонов и практических инструментов проектного управления
## ИТ-проекты, корпоративная автоматизация и организационные изменения

![status](https://img.shields.io/badge/материалов_готово-56%2F56-success) ![method](https://img.shields.io/badge/подход-PMBOK_%2B_практика-blue) ![gost](https://img.shields.io/badge/ГОСТ-34.602%2F34.603-blue) ![lang](https://img.shields.io/badge/язык-RU-lightgrey)

Открытая библиотека прикладных шаблонов, реестров, матриц и диагностических инструментов для **ИТ-проектов, корпоративной автоматизации, цифровой трансформации и организационных изменений**.

В основе библиотеки – практический опыт управления крупными корпоративными инициативами со стороны заказчика и интегратора, гибридные подходы к управлению проектами, PMBOK и российские стандарты оформления и приёмки автоматизированных систем.

Большая часть исходного комплекта разработана на примере внедрения **1С:ERP** и **1С:Управление холдингом**, однако большинство материалов платформенно независимы и могут адаптироваться для ERP, MDM, ECM, CRM, BI, интеграционных, инфраструктурных и организационных проектов.

> **Назначение.** Это шаблоны и рабочие инструменты, а не готовая нормативная система. Их необходимо адаптировать под масштаб, риски, методологию, договорную модель и внутренние регламенты конкретной организации.

---

## Содержание

- [Что входит в библиотеку](#что-входит-в-библиотеку)
- [Инструменты до запуска проекта](#инструменты-до-запуска-проекта)
- [Особенности основного комплекта](#особенности-основного-комплекта)
- [Сквозная система трассировки](#сквозная-система-трассировки)
- [Состав по фазам](#состав-по-фазам)
- [Форматы файлов](#форматы-файлов)
- [Как пользоваться](#как-пользоваться)
- [Публикации и методический контекст](#публикации-и-методический-контекст)
- [Лицензия и авторство](#лицензия-и-авторство)

---

## Что входит в библиотеку

Материалы разделяются на два слоя:

1. **Предпроектные инструменты** – помогают определить проблему, владельца результата, исходные ограничения и достаточность оснований для запуска проекта.
2. **Проектная документация** – поддерживает управление инициативой от инициации и обследования до внедрения, опытной эксплуатации и закрытия.

Библиотека рассчитана прежде всего на:

- руководителей проектов и программ;
- заказчиков корпоративных ИТ-систем;
- бизнес-аналитиков и архитекторов;
- проектные офисы;
- интеграторов и внутренние ИТ-команды;
- владельцев процессов и бизнес-результатов.

---

## Инструменты до запуска проекта

| Инструмент | Формат | Для чего нужен | Файл |
|---|:---:|---|---|
| Диагностический паспорт бизнес-инициативы | .xlsx | Проверить, определена ли реальная проблема, подтверждены ли симптомы и факты, назначен ли владелец результата и можно ли переходить к проектным обязательствам | [`Diagnosticheskiy_pasport_biznes-iniciativy_shablon.xlsx`](00-predproektnaya-diagnostika/Diagnosticheskiy_pasport_biznes-iniciativy_shablon.xlsx) |

Диагностический паспорт содержит четыре листа:

- **Паспорт** – рабочая форма описания инициативы;
- **Как заполнять** – инструкция и пояснения по разделам;
- **Пример** – образец заполнения;
- **Проверка и решение** – контроль полноты и фиксация решения о дальнейших действиях.

Это не облегчённый устав проекта. Паспорт применяется раньше – когда организация ещё проверяет, существует ли достаточно устойчивая постановка проблемы для формирования проекта.

---

## Особенности основного комплекта

- **Полный жизненный цикл** – от инициации до закрытия и передачи результатов в эксплуатацию.
- **Единая методологическая основа** – гибридное управление: предиктивное планирование верхнего уровня и итеративная детализация.
- **Связь управления и инженерной документации** – проектные артефакты увязаны с требованиями, архитектурой, разработкой, тестированием, миграцией и приёмкой.
- **ГОСТ как каркас формальной приёмки** – ГОСТ 34.602 и 34.603 используются там, где необходимы ТЗ, программы и протоколы испытаний.
- **Сквозные канонические наименования** – единые названия артефактов и идентификаторов.
- **Автопроверки в Excel** – контроль ответственности, сроков, статусов, покрытия и трассировки.
- **Тейлоринг** – состав документов масштабируется под размер и специфику проекта.

---

## Сквозная система трассировки

Документы образуют связанную систему. Идентификаторы протягиваются сквозь весь комплект:

```
Цель проекта (G-ID, Устав р.4)
        │
        ▼
Бизнес-требование (BR, BRD)
        │
        ▼
Функциональное требование (FR, FRD) ──► Детальное требование (REQ, Реестр требований)
        │                                        │
        │                                        ▼
        │                                Матрица трассировки (RTM)
        ▼                                        │
Разрыв (GAP, Gap-анализ)                         │
        │                                        ▼
        ▼                                Тест-кейс (TC, Реестр тест-кейсов)
ЧТЗ на доработку ──► Доработка (DEV, Реестр доработок) ──► Дефект (BUG, Журнал дефектов)
        │                                        │
        ▼                                        ▼
Версия конфигурации                      Критерий приёмки (ПМИ)

Риск (R-ID, Реестр рисков) ◄──► Проблема (ISS, Issue Log)
Запрос на изменение (CR) ──► влияет на требования, базовые линии, доработки
```

---

## Состав по фазам

Основной комплект структурирован по восьми фазам жизненного цикла проекта.

### 1. Инициация и управление
<sub>папка `01-iniciaciya-i-upravlenie/` – готово 14 из 14</sub>

| Документ | Формат | Статус | Файл |
|---|:---:|:---:|---|
| Системный промт проекта | .md | ✅ | [`sistemnyy_promt_proekta.md`](01-iniciaciya-i-upravlenie/sistemnyy_promt_proekta.md) |
| Устав проекта | .docx | ✅ | [`Ustav_proekta_shablon.docx`](01-iniciaciya-i-upravlenie/Ustav_proekta_shablon.docx) |
| Паспорт проекта | .docx | ✅ | [`Pasport_proekta_shablon.docx`](01-iniciaciya-i-upravlenie/Pasport_proekta_shablon.docx) |
| План управления проектом | .docx | ✅ | [`Plan_upravleniya_proektom_shablon.docx`](01-iniciaciya-i-upravlenie/Plan_upravleniya_proektom_shablon.docx) |
| Реестр стейкхолдеров и матрица влияния/интересов | .xlsx | ✅ | [`Reestr_steykholderov_shablon.xlsx`](01-iniciaciya-i-upravlenie/Reestr_steykholderov_shablon.xlsx) |
| Организационная структура проекта | .docx | ✅ | [`Organizacionnaya_struktura_proekta_shablon.docx`](01-iniciaciya-i-upravlenie/Organizacionnaya_struktura_proekta_shablon.docx) |
| Матрица ответственности RACI | .xlsx | ✅ | [`Matrica_RACI_artefakty.xlsx`](01-iniciaciya-i-upravlenie/Matrica_RACI_artefakty.xlsx) |
| Реестр рисков | .xlsx | ✅ | [`Reestr_riskov_shablon.xlsx`](01-iniciaciya-i-upravlenie/Reestr_riskov_shablon.xlsx) |
| Реестр проблем (Issue Log) | .xlsx | ✅ | [`Reestr_problem_Issue_Log.xlsx`](01-iniciaciya-i-upravlenie/Reestr_problem_Issue_Log.xlsx) |
| Матрица коммуникаций | .xlsx | ✅ | [`Matrica_kommunikaciy.xlsx`](01-iniciaciya-i-upravlenie/Matrica_kommunikaciy.xlsx) |
| План управления изменениями | .docx | ✅ | [`Plan_upravleniya_izmeneniyami_shablon.docx`](01-iniciaciya-i-upravlenie/Plan_upravleniya_izmeneniyami_shablon.docx) |
| Реестр запросов на изменение | .xlsx | ✅ | [`Reestr_zaprosov_na_izmenenie.xlsx`](01-iniciaciya-i-upravlenie/Reestr_zaprosov_na_izmenenie.xlsx) |
| Календарный план (MS Project XML) | .xml | ✅ | [`Kalendarnyy_plan_1C_MSProject.xml`](01-iniciaciya-i-upravlenie/Kalendarnyy_plan_1C_MSProject.xml) |
| План управления качеством | .docx | ✅ | [`Plan_upravleniya_kachestvom_shablon.docx`](01-iniciaciya-i-upravlenie/Plan_upravleniya_kachestvom_shablon.docx) |

### 2. Обследование и анализ
<sub>папка `02-obsledovanie-i-analiz/` – готово 7 из 7</sub>

| Документ | Формат | Статус | Файл |
|---|:---:|:---:|---|
| Отчёт о предпроектном обследовании | .docx | ✅ | [`Otchet_o_predproektnom_obsledovanii_shablon.docx`](02-obsledovanie-i-analiz/Otchet_o_predproektnom_obsledovanii_shablon.docx) |
| Описание бизнес-процессов As-Is | .docx | ✅ | [`Opisanie_processov_As-Is_shablon.docx`](02-obsledovanie-i-analiz/Opisanie_processov_As-Is_shablon.docx) |
| Описание бизнес-процессов To-Be | .docx | ✅ | [`Opisanie_processov_To-Be_shablon.docx`](02-obsledovanie-i-analiz/Opisanie_processov_To-Be_shablon.docx) |
| Каталог бизнес-требований (BRD) | .docx | ✅ | [`Katalog_biznes-trebovaniy_BRD_shablon.docx`](02-obsledovanie-i-analiz/Katalog_biznes-trebovaniy_BRD_shablon.docx) |
| Реестр требований | .xlsx | ✅ | [`Reestr_trebovaniy.xlsx`](02-obsledovanie-i-analiz/Reestr_trebovaniy.xlsx) |
| Матрица трассировки требований (RTM) | .xlsx | ✅ | [`RTM_matrica_trassirovki_shablon.xlsx`](02-obsledovanie-i-analiz/RTM_matrica_trassirovki_shablon.xlsx) |
| Реестр разрывов (Gap-анализ) | .xlsx | ✅ | [`Reestr_razryvov_Gap_analiz.xlsx`](02-obsledovanie-i-analiz/Reestr_razryvov_Gap_analiz.xlsx) |

### 3. Проектирование
<sub>папка `03-proektirovanie/` – готово 11 из 11</sub>

| Документ | Формат | Статус | Файл |
|---|:---:|:---:|---|
| Техническое задание (головное) | .docx | ✅ | [`TZ_golovnoe_shablon.docx`](03-proektirovanie/TZ_golovnoe_shablon.docx) |
| ЧТЗ на интеграцию | .docx | ✅ | [`CHTZ_integraciya_shablon.docx`](03-proektirovanie/CHTZ_integraciya_shablon.docx) |
| ЧТЗ на доработку | .docx | ✅ | [`CHTZ_dorabotka_shablon.docx`](03-proektirovanie/CHTZ_dorabotka_shablon.docx) |
| Функциональные спецификации (FRD) | .docx | ✅ | [`FRD_funkcionalnye_trebovaniya_shablon.docx`](03-proektirovanie/FRD_funkcionalnye_trebovaniya_shablon.docx) |
| Концепция архитектуры решения | .docx | ✅ | [`Koncepciya_arhitektury_resheniya_shablon.docx`](03-proektirovanie/Koncepciya_arhitektury_resheniya_shablon.docx) |
| Концепция НСИ | .docx | ✅ | [`Koncepciya_NSI_shablon.docx`](03-proektirovanie/Koncepciya_NSI_shablon.docx) |
| Концепция миграции данных | .docx | ✅ | [`Koncepciya_migracii_shablon.docx`](03-proektirovanie/Koncepciya_migracii_shablon.docx) |
| Концепция интеграции | .docx | ✅ | [`Koncepciya_integracii_shablon.docx`](03-proektirovanie/Koncepciya_integracii_shablon.docx) |
| Модель данных / описание НСИ | .docx | ✅ | [`Model_dannyh_opisanie_NSI_shablon.docx`](03-proektirovanie/Model_dannyh_opisanie_NSI_shablon.docx) |
| Ролевая модель и матрица прав доступа | .docx | ✅ | [`Rolevaya_model_matrica_prav_shablon.docx`](03-proektirovanie/Rolevaya_model_matrica_prav_shablon.docx) |
| Дизайн UI / печатных форм / отчётов | .docx | ✅ | [`Dizayn_UI_pechatnyh_form_otchetov_shablon.docx`](03-proektirovanie/Dizayn_UI_pechatnyh_form_otchetov_shablon.docx) |

### 4. Разработка и настройка
<sub>папка `04-razrabotka-i-nastroyka/` – готово 4 из 4</sub>

| Документ | Формат | Статус | Файл |
|---|:---:|:---:|---|
| Реестр доработок (Backlog) | .xlsx | ✅ | [`Reestr_dorabotok.xlsx`](04-razrabotka-i-nastroyka/Reestr_dorabotok.xlsx) |
| Журнал версий конфигурации | .xlsx | ✅ | [`Zhurnal_versiy_konfiguracii.xlsx`](04-razrabotka-i-nastroyka/Zhurnal_versiy_konfiguracii.xlsx) |
| Стандарты разработки и code style | .docx | ✅ | [`Standarty_razrabotki_code_style_shablon.docx`](04-razrabotka-i-nastroyka/Standarty_razrabotki_code_style_shablon.docx) |
| Протоколы код-ревью | .docx | ✅ | [`Protokol_kod-revyu_shablon.docx`](04-razrabotka-i-nastroyka/Protokol_kod-revyu_shablon.docx) |

### 5. Тестирование
<sub>папка `05-testirovanie/` – готово 5 из 5</sub>

| Документ | Формат | Статус | Файл |
|---|:---:|:---:|---|
| План тестирования и ПМИ | .docx | ✅ | [`Plan_testirovaniya_PMI_shablon.docx`](05-testirovanie/Plan_testirovaniya_PMI_shablon.docx) |
| Реестр тест-кейсов | .xlsx | ✅ | [`Reestr_test_keysov.xlsx`](05-testirovanie/Reestr_test_keysov.xlsx) |
| Протоколы тестирования | .docx | ✅ | [`Protokol_testirovaniya_shablon.docx`](05-testirovanie/Protokol_testirovaniya_shablon.docx) |
| Журнал дефектов (Bug tracking) | .xlsx | ✅ | [`Zhurnal_defektov.xlsx`](05-testirovanie/Zhurnal_defektov.xlsx) |
| Протоколы приёмочных испытаний | .docx | ✅ | [`Protokol_priyomochnyh_ispytaniy_shablon.docx`](05-testirovanie/Protokol_priyomochnyh_ispytaniy_shablon.docx) |

### 6. Внедрение и ОПЭ
<sub>папка `06-vnedrenie-i-ope/` – готово 6 из 6</sub>

| Документ | Формат | Статус | Файл |
|---|:---:|:---:|---|
| План развёртывания / перехода (Cutover) | .docx | ✅ | [`Plan_razvyortyvaniya_Cutover_shablon.docx`](06-vnedrenie-i-ope/Plan_razvyortyvaniya_Cutover_shablon.docx) |
| Детальный план миграции данных | .docx | ✅ | [`Detalnyy_plan_migracii_shablon.docx`](06-vnedrenie-i-ope/Detalnyy_plan_migracii_shablon.docx) |
| План обучения и учебные материалы | .docx | ✅ | [`Plan_obucheniya_shablon.docx`](06-vnedrenie-i-ope/Plan_obucheniya_shablon.docx) |
| Регламент опытной эксплуатации (ОПЭ) | .docx | ✅ | [`Reglament_OPE_shablon.docx`](06-vnedrenie-i-ope/Reglament_OPE_shablon.docx) |
| Журнал замечаний периода ОПЭ | .xlsx | ✅ | [`Zhurnal_zamechaniy_OPE.xlsx`](06-vnedrenie-i-ope/Zhurnal_zamechaniy_OPE.xlsx) |
| План поддержки (Hypercare) | .docx | ✅ | [`Plan_podderzhki_Hypercare_shablon.docx`](06-vnedrenie-i-ope/Plan_podderzhki_Hypercare_shablon.docx) |

### 7. Эксплуатационная документация
<sub>папка `07-ekspluatacionnaya-dokumentaciya/` – готово 4 из 4</sub>

| Документ | Формат | Статус | Файл |
|---|:---:|:---:|---|
| Руководство пользователя | .docx | ✅ | [`Rukovodstvo_polzovatelya_shablon.docx`](07-ekspluatacionnaya-dokumentaciya/Rukovodstvo_polzovatelya_shablon.docx) |
| Руководство администратора | .docx | ✅ | [`Rukovodstvo_administratora_shablon.docx`](07-ekspluatacionnaya-dokumentaciya/Rukovodstvo_administratora_shablon.docx) |
| Регламенты эксплуатации и сопровождения (SLA) | .docx | ✅ | [`Reglamenty_ekspluatacii_SLA_shablon.docx`](07-ekspluatacionnaya-dokumentaciya/Reglamenty_ekspluatacii_SLA_shablon.docx) |
| Инструкции по типовым операциям | .docx | ✅ | [`Instrukcii_po_tipovym_operaciyam_shablon.docx`](07-ekspluatacionnaya-dokumentaciya/Instrukcii_po_tipovym_operaciyam_shablon.docx) |

### 8. Закрытие
<sub>папка `08-zakrytie/` – готово 4 из 4</sub>

| Документ | Формат | Статус | Файл |
|---|:---:|:---:|---|
| Акты сдачи-приёмки | .docx | ✅ | [`Akt_sdachi-priyomki_shablon.docx`](08-zakrytie/Akt_sdachi-priyomki_shablon.docx) |
| Протокол завершения проекта | .docx | ✅ | [`Protokol_zaversheniya_proekta_shablon.docx`](08-zakrytie/Protokol_zaversheniya_proekta_shablon.docx) |
| Отчёт об извлечённых уроках | .docx | ✅ | [`Otchet_ob_izvlechyonnyh_urokah_shablon.docx`](08-zakrytie/Otchet_ob_izvlechyonnyh_urokah_shablon.docx) |
| Реестр переданных активов | .xlsx | ✅ | [`Reestr_peredannyh_aktivov.xlsx`](08-zakrytie/Reestr_peredannyh_aktivov.xlsx) |

---

## Форматы файлов

| Формат | Чем открыть | Назначение |
|---|---|---|
| `.docx` | MS Word, LibreOffice Writer, Google Docs | Согласуемые документы, регламенты и шаблоны |
| `.xlsx` | MS Excel, LibreOffice Calc, Google Sheets | Паспорта, реестры, матрицы, проверки и примеры |
| `.xml` | MS Project | Календарный план в формате MSPDI |
| `.md` | любой текстовый редактор | Инструкции и системные материалы |

> Для корректной работы формул, условного форматирования и проверок в `.xlsx` рекомендуется Microsoft Excel. При первом открытии может потребоваться пересчёт книги.

---

## Как пользоваться

1. **Определите стадию инициативы.** До появления устойчивой постановки проблемы начните с диагностического паспорта, а не с устава проекта.
2. **Выберите только необходимые артефакты.** Не копируйте весь комплект автоматически.
3. **Скопируйте шаблон** и адаптируйте его под проект.
4. **Заполните плейсхолдеры** и удалите инструктивные ремарки из итоговой версии.
5. **Сохраняйте трассировку** между целями, требованиями, решениями, тестами, рисками и изменениями.
6. **Проверьте внутренние нормы.** Шаблоны не заменяют юридическую, договорную, техническую и нормативную экспертизу.

Файл [`Reestr_proektnyh_dokumentov.xlsx`](Reestr_proektnyh_dokumentov.xlsx) остаётся источником истины для исходного комплекта проектной документации. Предпроектные и методические инструменты могут публиковаться отдельно и включаться в реестр при очередной комплексной ревизии библиотеки.

---

## Публикации и методический контекст

Подход к предпроектной диагностике и разграничению ответственности бизнеса и ИТ раскрыт в статьях:

- [«Автоматизировать бардак нельзя навести порядок: где у ИТ должно быть право вето»](https://habr.com/p/1062468/)
- [«Проект уже запущен, а проблему ещё не нашли. Лекарство уже купили – теперь ищем болезнь»](https://habr.com/ru/articles/1063074/)

Статьи объясняют, почему сам факт появления бюджета, срока, решения или проектной команды ещё не доказывает готовность инициативы к реализации.

---

## Лицензия и авторство

**Автор:** Халилов Руслан Энверович – руководитель ИТ-проектов и программ, PMP.

Оригинальные материалы репозитория распространяются на условиях **Creative Commons Attribution 4.0 International (CC BY 4.0)** – см. файл [`LICENSE`](LICENSE).

Разрешены копирование, адаптация, внутреннее и коммерческое использование при указании авторства, ссылки на лицензию и обозначении внесённых изменений.

Шаблоны и примеры обезличены. Перед публикацией или применением материалов проверяйте их на наличие сведений, позволяющих идентифицировать конкретную организацию, проект или участников.

---

<sub>PMBOK®, PMP® и связанные обозначения являются товарными знаками Project Management Institute, Inc. 1С:ERP и 1С:Управление холдингом являются продуктами фирмы «1С». Репозиторий не аффилирован с PMI, фирмой «1С» или иными правообладателями и не является их официальным изданием.</sub>
