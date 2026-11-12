# SWTC (rel. 1.0) for IX-Ray Platform

## Overview

## Remarks

> [!WARNING]
>
> Supported only on __IX-Ray Platform__!
>
> Not compatible with other weather mods! Before installing, delete user.ltx

## Requirements

Installation:

1. Install Shadow of Chernobyl, Clear Sky, or Call of Pripyat
2. Install a matching IX-Ray build with platform-aware addons and CoP-format weather support
3. Extract the archive into the game folder, preserving all four modules in `ixr_addons/ixray-swtc/`
4. Start the game and play

Link to the current __IX-Ray__ [release](https://github.com/ixray-team/ixray-1.6-stcop/releases/latest)

## Modules

| Directory | Platform | Contents |
| --- | --- | --- |
| `swtc-common` | `soc`, `cs`, `cop` | Shared textures, sounds, 17 weather cycles, sun settings, regional graphs, renderer defaults |
| `swtc-soc` | `soc` | Dynamic weather manager, graphs for 12 outdoor locations, native SoC ambient and thunderbolt adapters |
| `swtc-cs` | `cs` | Regional graph assignments, introductory weather conditions, level ambients and textures |
| `swtc-cop` | `cop` | Weather periods, map weather assignments and level textures |

All platform modules use `depends: swtc-common`. The common module's folder and `name` are both `swtc-common`. Keep the common module with the matching platform module; the engine selects the platform automatically.

SoC and CS select weighted weather cycles from regional SWTC graphs every game hour. SoC persists its current graph, cycle and timer in actor pstor without changing the native weather-manager packet. Its underground weather and scripted weather effects remain native. CoP uses four weather-period groups (clear, cloudy, rain, storm), with all 17 SWTC cycles available and a transition between groups.

Map weather is applied through DLTX; map geometry, music and underground settings remain owned by the game. Level textures are loaded only on their matching CS/CoP platform. Disable other weather addons, including CGIM2, before using SWTC.

## Contributors

- Drombeys
- St4lker0k765

## License

Сontents of this repository are licensed under terms of the __CC BY-NC-SA 4.0__ license unless otherwise specified. See [this](./LICENSE.txt) file for details

## Обзор

## Примечаниe

> [!WARNING]
>
> Поддерживается только на __IX-Ray Platform__!
>
> Не совместимо с другими погодными модами! Перед установкой удалите user.ltx

## Рекомендации

Установка:

1. Установить «Тень Чернобыля», «Чистое небо» или «Зов Припяти»
2. Установить сборку IX-Ray для выбранной игры с поддержкой платформ в аддонах и погоды формата ЗП
3. Распаковать архив в папку с игрой, сохранив все четыре модуля в `ixr_addons/ixray-swtc/`
4. Запустите игру и играйте

Ссылка на текущую версию __IX-Ray__ [релиз](https://github.com/ixray-team/ixray-1.6-stcop/releases/latest)

## Структура модулей

| Папка | Платформа | Содержимое |
| --- | --- | --- |
| `swtc-common` | `soc`, `cs`, `cop` | Единые текстуры, звуки, 17 погодных циклов, солнца, региональные графы и настройки рендера |
| `swtc-soc` | `soc` | Динамический менеджер, графы для 12 наземных локаций, адаптеры родных звуков и молний ТЧ |
| `swtc-cs` | `cs` | Региональная погода, условия вступления, эмбиенты и текстуры уровней ЧН |
| `swtc-cop` | `cop` | Периоды погоды, привязки графов и текстуры уровней ЗП |

Все платформенные модули используют `depends: swtc-common`. Имя папки и поле `name` общего модуля совпадают: `swtc-common`. Общий модуль обязателен; движок автоматически выбирает модуль нужной платформы.

В ТЧ и ЧН циклы выбираются каждый игровой час из региональных графов SWTC с учётом весов. В ТЧ текущий граф, цикл и таймер сохраняются в штатном хранилище актёра без изменения формата блока погодного менеджера. Подземелья и сюжетные погодные эффекты ТЧ остаются штатными. В ЗП используются четыре группы периодов (ясно, облачно, дождь, шторм), охватывающие все 17 циклов SWTC, и переходная погода между группами.

Привязки погоды задаются через DLTX без полной замены конфига карты. Текстуры уровней загружаются только для соответствующей платформы ЧН/ЗП. Перед использованием отключите другие погодные аддоны, включая CGIM2.

## Контрибьюторы

- Drombeys
- St4lker0k765

## Лицензия

Содержимое этого репозитория лицензировано в соответствии с условиями лицензии __CC BY-NC-SA 4.0__, если не указано иное. Подробности см. в файле [здесь](./LICENSE.txt)
