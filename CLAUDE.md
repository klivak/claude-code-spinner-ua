# claude-code-spinner-ua

Кастомні українські спіннери для Claude Code. Чотири паки.

## Паки
- `spinners.json` / `packs/doomer.json` — думерський пак (дефолт)
- `packs/fine.json` — пак "все нормально"
- `packs/filosof.json` — філософський пак
- `packs/memes.json` — мемний пак (реальні українські меми)

## Slash-команди
- `/install-spinner-doomer` — встановити думерський пак
- `/install-spinner-fine` — встановити пак "все нормально"
- `/install-spinner-filosof` — встановити філософський пак
- `/install-spinner-memes` — встановити мемний пак

## Як працює
Slash-команди читають відповідний json і мерджать `spinnerVerbs` в `~/.claude/settings.json`, зберігаючи інші налаштування.

## Структура
- `packs/` — json-файли паків
- `.claude/commands/` — slash-команди для встановлення
- `spinners.json` — дефолтний пак (копія doomer)

## Свій пак
Формат json: `{ "spinnerVerbs": { "mode": "replace", "verbs": ["...", "..."] } }`
Додай файл у `packs/` і slash-команду в `.claude/commands/`.
