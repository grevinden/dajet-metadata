[![Build Release (Self-Contained .NET 10.0)](https://github.com/grevinden/dajet-metadata/actions/workflows/build.yml/badge.svg)](https://github.com/grevinden/dajet-metadata/actions/workflows/build.yml)

# DaJet Metadata

Библиотека для чтения, анализа и восстановления метаданных информационных баз **1С:Предприятие 8** напрямую из таблиц **Microsoft SQL Server** и **PostgreSQL**.

## Возможности

- Чтение свойств основной конфигурации и расширений
- Извлечение структуры объектов метаданных:
  - Планы обмена, константы, перечисления
  - Справочники, документы, задачи, бизнес-процессы
  - Регистры сведений, накопления, бухгалтерии
  - Планы счетов, планы видов характеристик
  - Определяемые типы, общие реквизиты
  - Таблицы регистрации изменений
- Поддержка расширений конфигурации (начиная с 1С:Предприятие 8.3.12)
- Работа с базами данных напрямую, без использования COM-соединения и сервера 1С

## Кроссплатформенная сборка

| Платформа | Архитектура |
|-----------|-------------|
| Windows   | x64, ARM64  |
| Linux     | x64, ARM64  |
| macOS     | x64, ARM64 (Apple Silicon) |

## Структура сборки

```
win-x64/
├── DaJet.Metadata.dll
├── DaJet.Data.dll
├── DaJet.TypeSystem.dll
├── hostfxr.dll
├── coreclr.dll
└── shared/
    └── Microsoft.NETCore.App/
        └── 10.0.x/
            └── (runtime files)
```

## Использование с Python

Библиотека совместима с **pythonnet** и включает полный .NET Runtime в `shared/`.
См. [pydajet-metadata](https://github.com/grevinden/pydajet-metadata) для Python-обёртки.

## Технологии

- **.NET 10.0** (self-contained — не требует установки .NET)
- **Microsoft SQL Server** (Microsoft.Data.SqlClient)
- **PostgreSQL** (Npgsql, сборка для 1С)
