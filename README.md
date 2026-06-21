# Библиотека шаблонов проектной документации
## Внедрение 1С:ERP + 1С:Управление холдингом

![status](https://img.shields.io/badge/шаблонов_готово-47%2F55-success) ![method](https://img.shields.io/badge/метод-PMBOK_8th_ed.-blue) ![gost](https://img.shields.io/badge/ГОСТ-34.602%2F34.603-blue) ![lang](https://img.shields.io/badge/язык-RU-lightgrey)

Готовый к работе комплект шаблонов проектной документации для **крупного внедрения корпоративной ИС** на базе 1С:ERP Управление предприятием и 1С:Управление холдингом. Шаблоны разработаны на основе **PMBOK Guide (8-е издание)** в гибридном подходе, с использованием **ГОСТ 34.602 / 34.603** в качестве каркаса для документов формальной приёмки.

Комплект рассчитан на масштаб: бюджет от 100 млн руб., 100–500 стейкхолдеров, холдинговая производственная структура, множество интеграций, полный цикл производственного и финансового учёта, консолидация.

> **Назначение.** Это **шаблоны** (а не готовые документы): структура, разделы, таблицы, плейсхолдеры `[в квадратных скобках]` и встроенные инструкции по заполнению. Заполняются под конкретный проект. Не все артефакты обязательны для каждого проекта — состав адаптируется (тейлоринг).

---

## Содержание

- [Особенности комплекта](#особенности-комплекта)
- [Сквозная система трассировки](#сквозная-система-трассировки)
- [Состав по фазам](#состав-по-фазам)
- [Форматы файлов](#форматы-файлов)
- [Как пользоваться](#как-пользоваться)
- [Источник истины — реестр документов](#источник-истины--реестр-документов)
- [Условные обозначения](#условные-обозначения)
- [Лицензия и авторство](#лицензия-и-авторство)

---

## Особенности комплекта

- **Единая методология** — PMBOK 8th ed. (гибридный подход: предиктивное планирование верхнего уровня + итеративная проработка волнами), отраслевые практики внедрения 1С, ГОСТ 34.602/34.603 для ТЗ/ЧТЗ и испытаний.
- **Единый визуальный стиль** — шрифт Arial, тёмно-синий акцент, единая структура (титул, лист регистрации изменений, лист согласования, содержание, назначение, глоссарий). Реестры в .xlsx имеют листы: Инструкция, основной, Сводка, Справочники, Журнал изменений.
- **Сквозные канонические наименования** — единые названия артефактов во всех документах, без синонимов.
- **Встроенные автопроверки** в .xlsx-реестрах — контроль распределения ответственности (RACI), покрытия требований тестами (RTM), сроков и статусов, трассировки.
- **Сквозная трассировка** между документами (см. ниже).

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

Комплект структурирован по 8 фазам жизненного цикла проекта. Файлы разложены по папкам соответственно.

### 1. Инициация и управление
<sub>папка `01-iniciaciya-i-upravlenie/` — готово 14 из 14</sub>

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
<sub>папка `02-obsledovanie-i-analiz/` — готово 7 из 7</sub>

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
<sub>папка `03-proektirovanie/` — готово 11 из 11</sub>

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
<sub>папка `04-razrabotka-i-nastroyka/` — готово 4 из 4</sub>

| Документ | Формат | Статус | Файл |
|---|:---:|:---:|---|
| Реестр доработок (Backlog) | .xlsx | ✅ | [`Reestr_dorabotok.xlsx`](04-razrabotka-i-nastroyka/Reestr_dorabotok.xlsx) |
| Журнал версий конфигурации | .xlsx | ✅ | [`Zhurnal_versiy_konfiguracii.xlsx`](04-razrabotka-i-nastroyka/Zhurnal_versiy_konfiguracii.xlsx) |
| Стандарты разработки и code style | .docx | ✅ | [`Standarty_razrabotki_code_style_shablon.docx`](04-razrabotka-i-nastroyka/Standarty_razrabotki_code_style_shablon.docx) |
| Протоколы код-ревью | .docx | ✅ | [`Protokol_kod-revyu_shablon.docx`](04-razrabotka-i-nastroyka/Protokol_kod-revyu_shablon.docx) |

### 5. Тестирование
<sub>папка `05-testirovanie/` — готово 5 из 5</sub>

| Документ | Формат | Статус | Файл |
|---|:---:|:---:|---|
| План тестирования и ПМИ | .docx | ✅ | [`Plan_testirovaniya_PMI_shablon.docx`](05-testirovanie/Plan_testirovaniya_PMI_shablon.docx) |
| Реестр тест-кейсов | .xlsx | ✅ | [`Reestr_test_keysov.xlsx`](05-testirovanie/Reestr_test_keysov.xlsx) |
| Протоколы тестирования | .docx | ✅ | [`Protokol_testirovaniya_shablon.docx`](05-testirovanie/Protokol_testirovaniya_shablon.docx) |
| Журнал дефектов (Bug tracking) | .xlsx | ✅ | [`Zhurnal_defektov.xlsx`](05-testirovanie/Zhurnal_defektov.xlsx) |
| Протоколы приёмочных испытаний | .docx | ✅ | [`Protokol_priyomochnyh_ispytaniy_shablon.docx`](05-testirovanie/Protokol_priyomochnyh_ispytaniy_shablon.docx) |

### 6. Внедрение и ОПЭ
<sub>папка `06-vnedrenie-i-ope/` — готово 6 из 6</sub>

| Документ | Формат | Статус | Файл |
|---|:---:|:---:|---|
| План развёртывания / перехода (Cutover) | .docx | ✅ | [`Plan_razvyortyvaniya_Cutover_shablon.docx`](06-vnedrenie-i-ope/Plan_razvyortyvaniya_Cutover_shablon.docx) |
| Детальный план миграции данных | .docx | ✅ | [`Detalnyy_plan_migracii_shablon.docx`](06-vnedrenie-i-ope/Detalnyy_plan_migracii_shablon.docx) |
| План обучения и учебные материалы | .docx | ✅ | [`Plan_obucheniya_shablon.docx`](06-vnedrenie-i-ope/Plan_obucheniya_shablon.docx) |
| Регламент опытной эксплуатации (ОПЭ) | .docx | ✅ | [`Reglament_OPE_shablon.docx`](06-vnedrenie-i-ope/Reglament_OPE_shablon.docx) |
| Журнал замечаний периода ОПЭ | .xlsx | ✅ | [`Zhurnal_zamechaniy_OPE.xlsx`](06-vnedrenie-i-ope/Zhurnal_zamechaniy_OPE.xlsx) |
| План поддержки (Hypercare) | .docx | ✅ | [`Plan_podderzhki_Hypercare_shablon.docx`](06-vnedrenie-i-ope/Plan_podderzhki_Hypercare_shablon.docx) |

### 7. Эксплуатационная документация
<sub>папка `07-ekspluatacionnaya-dokumentaciya/` — готово 0 из 4</sub>

| Документ | Формат | Статус | Файл |
|---|:---:|:---:|---|
| Руководство пользователя | .docx | ⬜ | — |
| Руководство администратора | .docx | ⬜ | — |
| Регламенты эксплуатации и сопровождения (SLA) | .docx | ⬜ | — |
| Инструкции по типовым операциям | .docx | ⬜ | — |

### 8. Закрытие
<sub>папка `08-zakrytie/` — готово 0 из 4</sub>

| Документ | Формат | Статус | Файл |
|---|:---:|:---:|---|
| Акты сдачи-приёмки | .docx | ⬜ | — |
| Протокол завершения проекта | .docx | ⬜ | — |
| Отчёт об извлечённых уроках | .docx | ⬜ | — |
| Реестр переданных активов | .xlsx | ⬜ | — |

---

## Форматы файлов

| Формат | Чем открыть | Назначение |
|---|---|---|
| `.docx` | MS Word, LibreOffice Writer, Google Docs | Согласуемые деловые документы |
| `.xlsx` | MS Excel, LibreOffice Calc, Google Sheets | Реестры и матрицы (с формулами и автопроверками) |
| `.xml` | MS Project (Файл → Открыть → импорт) | Календарный план (формат MS Project XML / MSPDI) |
| `.md` | любой текстовый редактор | Системный промт проекта |

> **Календарный план** поставляется в формате **MS Project XML**, а не `.mpp`: это официальный обменный формат Microsoft. Откройте его в MS Project через «Файл → Открыть» и при необходимости сохраните как `.mpp`. Все данные — задачи, фазы, вехи, связи, ресурсы (роли), назначения — импортируются корректно.

> **Реестры .xlsx** содержат формулы и условное форматирование (контроль сроков, светофоры статусов, автопроверки RACI/RTM). Для корректной работы открывайте в приложении, поддерживающем формулы; при первом открытии может потребоваться пересчёт (F9).

---

## Как пользоваться

1. **Начните с реестра** — `Reestr_proektnyh_dokumentov.xlsx` в корне: единый перечень всех документов с каноническими наименованиями, фазами, статусами и связями.
2. **Скопируйте шаблон** нужного документа из папки фазы.
3. **Заполните плейсхолдеры** `[в квадратных скобках]` своими данными.
4. **Удалите инструктивные ремарки** (серый курсив) в финальной версии.
5. **Сохраняйте трассировку** — используйте сквозные ID (G-ID, BR, FR, REQ, GAP, DEV, TC, BUG, R-ID, CR) единообразно во всех документах.
6. **Соблюдайте канонические наименования** из реестра — без синонимов.

> Документы — это шаблоны под адаптацию. Применяйте тейлоринг: не каждый артефакт обязателен для каждого проекта; масштабируйте состав под размер и специфику.

---

## Источник истины — реестр документов

Файл **`Reestr_proektnyh_dokumentov.xlsx`** (в корне репозитория) — единый перечень всех документов комплекта. Это источник истины по составу и наименованиям. При работе с комплектом сверяйтесь с ним; при добавлении нового документа сначала вносится строка в реестр, затем создаётся файл.

---

## Условные обозначения

| Знак | Значение |
|:---:|---|
| ✅ | Шаблон готов и доступен в репозитории |
| ⬜ | Артефакт предусмотрен методологией, шаблон в планах |
| `[текст]` | Плейсхолдер — заполняется под конкретный проект |

---

## Лицензия и авторство

**Автор:** Халилов Руслан Энверович, руководитель проектов, PMP (PMI)

Комплект распространяется на условиях лицензии **Creative Commons Attribution 4.0 International (CC BY 4.0)** — см. файл [`LICENSE`](LICENSE). Вы можете свободно использовать, адаптировать и распространять шаблоны, в том числе в коммерческих проектах, при условии указания авторства.

Шаблоны обезличены и не содержат данных конкретных организаций. Идентификаторы юрлиц, наименования и числовые значения в примерах — условные плейсхолдеры.

---

<sub>Методологическая основа: PMBOK® Guide — Eighth Edition (PMI). PMBOK и PMP — зарегистрированные товарные знаки Project Management Institute, Inc. Настоящий комплект не аффилирован с PMI и не является официальным изданием PMI. 1С:ERP и 1С:Управление холдингом — продукты фирмы «1С».</sub>