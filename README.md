# claude-code-spinner-ua 🇺🇦

> Кастомні українські спіннери для Claude Code — заміна стандартних Thinking, Analyzing, Pondering на щось людське.

Обирай пак під настрій — від думерського тліну до реальних українських мемів.

![Claude Code Spinner UA](assets/into.png)

## 👀 Як це виглядає

Замість нудного `Thinking...` бачиш:

```
⠋ мерж конфлікт душі...
⠙ все одно не задеплоїться...
⠸ кава скінчилась і сенс теж...
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
│   └── install-spinner-cat.md
├── packs/
│   ├── doomer.json        ← 90 фраз
│   ├── fine.json           ← 90 фраз
│   ├── filosof.json        ← 90 фраз
│   ├── memes.json          ← 100 фраз
│   ├── coder.json          ← 60 фраз
│   ├── stazher.json        ← 32 фрази
│   └── cat.json            ← 33 фрази
├── spinners.json          ← дефолт (кодер)
├── CLAUDE.md
└── README.md
```

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

## 📜 Ліцензія

MIT — форкай, перекладай, додавай свої паки. Якщо зламаєш — то не баг, то характер, база, грунт, фундамент і гранітний камінь опенсорсу.

---

**Claude Code spinner** · **Claude Code custom spinner** · **Claude Code українською** · **spinner verbs** · **Claude Code customization** · **Claude Code UI** · **developer tools Ukraine**
