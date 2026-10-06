---
name: framework-principles
description: Принципы SDD Cookbook: unified vs specific agent, четыре раздела, ссылка на согласованную модель OpenSpec
metadata:
  type: project
---

## Принципы SDD Cookbook

### Что это
Фреймворк описания Software Design Documents (SDD) для **agent-based development** IT-продуктов. Стандартизирует проектирование, процессы команды и кейсы реализации.

### Unified и Specific agent

- **Unified agent**: общие практики, применимые к разным командам (общие разделы `roles/`, `store/`, `gates/`).
- **Specific agent**: конкретный кейс реализации с особенностями команды, стека и инструментов (`cases/`).

Перед написанием определить, общий это уровень или командный.

### Четыре раздела

1. **Roles** (`OpenSpec/roles/`): кто что делает. Сейчас описаны аналитик и разработчик.
2. **Store** (`OpenSpec/store/`): общие механизмы Store: принципы, структура, теги, подключение, архивация.
3. **Gates** (`OpenSpec/gates/`): граничные случаи и контрольные точки.
4. **Cases** (`OpenSpec/cases/`): реализации. Эталон: `cases/Sber/`.

### Модель OpenSpec

Описана в [openspec_architecture.md](openspec_architecture.md). Коротко: Store хранит ФТ (чёрный ящик, файлы по областям), кодовые репозитории подключают его как submodule на тег, теги бывают двух видов (фичи и релиза Store), архивация на feature freeze, проверки основные в репозитории, в сборке только codegen.

### Важное

- Содержание на русском, Markdown, Obsidian (файлы должны быть видимы: без скрытых папок; yaml Obsidian не показывает без настройки).
- При расхождении общих документов и кейса Sber правильным считается кейс Sber.
