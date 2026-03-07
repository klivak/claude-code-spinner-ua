# claude-code-spinner-ua 🇺🇦

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub stars](https://img.shields.io/github/stars/klivak/claude-code-spinner-ua)](https://github.com/klivak/claude-code-spinner-ua/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/klivak/claude-code-spinner-ua)](https://github.com/klivak/claude-code-spinner-ua/network)
[![Made in Ukraine](https://img.shields.io/badge/Made_in-Ukraine-ffd700.svg?labelColor=0057b7)](https://stand-with-ukraine.pp.ua)

<a href="https://ko-fi.com/klivak" target="_blank"><img src="https://ko-fi.com/img/githubbutton_sm.svg" alt="ko-fi"></a>

> Кастомні українські спіннери для Claude Code — заміна стандартних Thinking, Analyzing, Pondering на щось людське.

Обирай пак під настрій — від кодерського дзену до екзистенційного тліну.

![Claude Code Spinner UA](assets/into.png)

## 👀 Як це виглядає

Замість нудного `Thinking...` бачиш:

```
⠋ хм, а чому воно працює...
⠙ дай подумати...
⠸ копаю глибше...
```

## 📦 Паки

| Пак | Настрій | Файл |
|-----|---------|------|
| 💀 **Думер** | Екзистенційна втома і легкий тлін | `packs/doomer.json` |
| 🧠 **Філософ** | Сковорода б схвалив | `packs/filosof.json` |
| 😂 **Меми** | Реальні українські меми | `packs/memes.json` |
| 💻 **Кодер** | Повсякденне життя розробника | `packs/coder.json` |
| 🐣 **Стажер** | Перший день — вже продакшн | `packs/stazher.json` |
| 🐱 **Кіт** | Мурчу і працюю | `packs/cat.json` |
| 📋 **PM** | Дедлайн був вчора | `packs/pm.json` |
| 😌 **Все нормально** | Спокійна стоїчність | `packs/fine.json` |

### 💀 Думер

> Коли код — це біль, а деплой — це міф.

```
нащо взагалі...
все одно не задеплоїться...
мерж конфлікт душі...
кава скінчилась і сенс теж...
todo: все...
```

### 🧠 Філософ

> Сковорода б схвалив. Код як дзеркало буття.

```
що є код як не думка в синтаксисі...
рекурсія — це коли ти знову тут...
null — це не порожнеча а можливість...
ми пишемо код а код пише нас...
void — найчесніший тип повернення...
```

### 😂 Меми

> Реальні українські меми — від Кернеса до паляниці.

```
давай по новой, Міша, всьо х**ня...
пропало всьо...
щоб вода стала гарячою — її треба підігріти...
HIMARS o'clock...
бусік незламності виїжджає...
```

### 💻 Кодер

> Без зайвого пафосу. Просто кодиш.

```
хм, а чому воно працює...
дай подумати...
копаю глибше...
є ідея...
складаю пазл...
```

### 🐣 Стажер

> Перший день — вже продакшн.

```
а де тут кнопка run...
я все зламав...
у всіх працює а в мене ні...
копіюю зі Stack Overflow...
ой а це продакшн був?...
```

### 🐱 Кіт

> Мурчу і працюю. Або ні.

```
не чіпай мене я думаю...
лапкою по ентеру...
з'їв баг...
полюю на курсор...
спить але контролює ситуацію...
```

### 📋 PM

> Дедлайн був вчора. А що по статусу?

```
а що по статусу?...
дедлайн був вчора...
перенесемо на наступний спринт...
ще один мітинг...
в джирі не бачу...
```

### 😌 Все нормально

> І не таке бачили. Тримаємось.

```
горить, але терпимо...
бачили і гірше...
нічого, до весілля заживе...
тримаємось...
ще й не вечір...
```

## 🚀 Встановлення

### Через Claude Code (рекомендовано)

```bash
git clone https://github.com/klivak/claude-code-spinner-ua.git
cd claude-code-spinner-ua
```

Запусти Claude Code і виконай одну з команд:

```
/install-spinner-doomer     — думерський пак
/install-spinner-fine       — пак "все нормально"
/install-spinner-filosof    — філософський пак
/install-spinner-memes      — мемний пак
/install-spinner-coder      — кодерський пак (дефолт)
/install-spinner-stazher    — стажерський пак
/install-spinner-cat        — котячий пак
/install-spinner-pm         — PM пак
```

Все. Спіннер зміниться одразу.

### Вручну

Скопіюй вміст потрібного json-файлу в `~/.claude/settings.json`:

```json
{
  "spinnerVerbs": {
    "mode": "replace",
    "verbs": ["нащо взагалі...", "все одно не задеплоїться", "..."]
  }
}
```

Якщо `settings.json` вже існує — додай ключ `spinnerVerbs`, не видаляючи інші налаштування.

## 🗑️ Видалення

Щоб повернути стандартний спіннер, видали ключ `spinnerVerbs` з `~/.claude/settings.json`:

```json
{
  "spinnerVerbs": { ... }  ← видали цей блок
}
```

Або відкрий Claude Code і скажи: «видали spinnerVerbs з settings.json».

## 🔄 Перемикання паків

Просто запусти іншу slash-команду — вона замінить поточний спіннер:

```
/install-spinner-doomer     — назад до тліну
/install-spinner-fine       — назад до спокою
/install-spinner-filosof    — назад до рефлексії
/install-spinner-memes      — назад до мемів
/install-spinner-coder      — назад до коду
/install-spinner-stazher    — назад до навчання
/install-spinner-cat        — назад до муркотіння
/install-spinner-pm         — назад до мітингів
```

## 📁 Структура

```
claude-code-spinner-ua/
├── .claude/commands/
│   ├── install-spinner-doomer.md
│   ├── install-spinner-fine.md
│   ├── install-spinner-filosof.md
│   ├── install-spinner-memes.md
│   ├── install-spinner-coder.md
│   ├── install-spinner-stazher.md
│   ├── install-spinner-cat.md
│   └── install-spinner-pm.md
├── packs/
│   ├── doomer.json         ← 90 фраз
│   ├── fine.json           ← 90 фраз
│   ├── filosof.json        ← 90 фраз
│   ├── memes.json          ← 100 фраз
│   ├── coder.json          ← 60 фраз
│   ├── stazher.json        ← 32 фрази
│   ├── cat.json            ← 33 фрази
│   └── pm.json             ← 35 фраз
├── spinners.json           ← дефолт (кодер)
├── CLAUDE.md
└── README.md
```

## 🔧 Troubleshooting

**Спіннер не змінився після встановлення**
- Перезапусти Claude Code — зміни підхоплюються при старті

**Slash-команда не знайдена**
- Переконайся, що ти запустив Claude Code з директорії `claude-code-spinner-ua`
- Перевір, що папка `.claude/commands/` існує і містить `.md` файли

**settings.json зламався**
- Відкрий `~/.claude/settings.json` і перевір валідність JSON (зайві коми, незакриті дужки)
- Якщо все погано — видали ключ `spinnerVerbs` вручну, спіннер повернеться до дефолтного

**Хочу повернути англійський спіннер**
- Видали блок `spinnerVerbs` з `~/.claude/settings.json`

## ✏️ Свій пак

Створи json у форматі:

```json
{
  "spinnerVerbs": {
    "mode": "replace",
    "verbs": ["твоя фраза 1", "твоя фраза 2", "..."]
  }
}
```

Кинь у `packs/`, додай slash-команду в `.claude/commands/` — і готово.

## 🤝 Contributing

Хочеш додати свій пак або покращити існуючий? Читай [CONTRIBUTING.md](CONTRIBUTING.md).

## 📜 Ліцензія

MIT — форкай, перекладай, додавай свої паки. Якщо зламаєш — то не баг, то характер, база, грунт, фундамент і гранітний камінь опенсорсу.

---

☕ [Buy me a coffee](https://ko-fi.com/klivak) if this project helped you

---

**Claude Code spinner** · **Claude Code custom spinner** · **Claude Code українською** · **spinner verbs** · **Claude Code customization** · **Claude Code UI** · **developer tools Ukraine**
